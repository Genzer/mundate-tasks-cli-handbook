# Mundane Tasks CLI Handbook

Handbook for doing mundane tasks with CLI tools.

## What is this?

As a software developer, I find myself often need to do some of these tasks: convert an EPOCH timestamp to a formatted date, inspect a JSON Web Token, convert back-and-forth Base64 encoded string, encoding URLs, etc.

Usually, I would reach out to some of the online services for these tasks, but I realized that it would be better if I could do them from the terminal via CLI tools. By doing this, it saves me time and it is more secure (pasting some JWT onto an online service emposes a security risk).

This is just a personal handbook (reads "cheatsheet") as a reference for all those tasks.

## Dates and Times

NOTE: Most of the time, I use GNU `date`.

### Convert an EPOCH timestamp to a formatted date

Suppose you just got an EPOCH, `1671704790.281809` and you want to know the exact date time.

```bash
$> date -d '@1671704790.281809'
Thu Dec 22 17:26:30 +07 2022

$> date -d '@1671704790.281809' --rfc-3339=seconds
2022-12-22 17:26:30+07:00

$> date -d '@1671704790.281809' --rfc-3339=seconds --utc
2022-12-22 10:26:30+00:00

$> TZ=Pacific/Auckland date -d '@1671704790.281809' --rfc-3339=seconds
2022-12-22 23:26:30+13:00
```

Alternative: https://www.epochconverter.com/.

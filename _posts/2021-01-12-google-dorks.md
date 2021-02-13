---
title:  Google Dorks
date:   2021-01-12 20:00:00 -0700
tags: [Search Engines]
---

Dorking is using a search engine, in this case Google, to find very specific information via advanced search operators.

## Operators

(These can be combined)

* `"phrase"`: exact match
* `"-phrase"`: exclusion
* `phrase AND phrase`: must include both
* `phrase OR phrase`: must include either or both
* `*`: wildcard
* `...`: range (numbers, years anything sequential)

## Text Searches

* `intitle:`
* `inurl:`
* `related:`
* `site:`
* `intext:`
* `inposttitle`

## Email Searches

* `name @gmail.com`


## File Searches

* `filetype:pdf`
* spreadsheets: `filetype:csv OR filetype:xlsx OR filetype:xls OR filetype:xltx OR filetype:xlt OR inurl:airtable.com/universe/`
* google docs: `site:docs.google.com "gumroad"`


## Misc
* `inurl:ftp -inurl:(http|https)`: FTP Search

## So Many More

(Google Hacking Database)[https://www.exploit-db.com/google-hacking-database]
---
title: Poison Null Byte Attack
date: 2021-04-18 23:00:00 -0700
tags: [Application Security]
---

Also known as Null Byte Injection, the term poison null byte was originally coined by Olaf Kirch. 

A null byte (or NULL terminator) is used in many languages to detect the end of a string. Systems that do not handle null bytes properly can be exploited by injecting a null byte to get around sanity checks in file names.

Common attacks using this technique are [LFI/RFI Injection]({% post_url 2021-04-19-local-remote-file-inclusion %}) or bypassing file extension checks.

```
CODE:
$whatever = addslashes($_REQUEST['whatever']);
include("/path/to/program/" . $whatever . "/header.htm");

MALICIOUS URL:
http://vuln.example.com/phpscript.php?whatever=../../../etc/passwd%00
```

## URL Escaping

The null byte `%00` must be url encoded to `%2500` for use in a web application.

[source](https://www.whitehatsec.com/glossary/content/null-byte-injection)
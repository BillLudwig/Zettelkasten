---
title:  SMTP Enumeration
date:   2021-02-14 10:50:00 -0700
tags: [Pentesting]
---

## [SMTP]({% post_url 2021-02-14-smtp-pop-imap %}) Enumeration with MetaSploit

Using the `smtp_version` and `smtp_enum` modules Metaspoit will return the version number of any SMTP servers found within a given IP range. Then using the `VRFY`, `EXPN`, and `RCPT TO` SMTP commands we can get a list of valid users.
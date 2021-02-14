---
title:  SMTP Enumeration
date:   2021-02-14 10:50:00 -0700
tags: [Pentesting, MetaSploit]
---

## [SMTP]({% post_url 2021-02-14-smtp-pop-imap %}) Username Enumeration with [MetaSploit]({% post_url 2021-02-14-metasploit %})

Using the `smtp_version` and `smtp_enum` modules Metaspoit will return the version number of any SMTP servers found within a given IP range. Then using the `VRFY`, `EXPN`, and `RCPT TO` SMTP commands we can get a list of valid users.

1. (*If SMTP Port Unknown*) Scan with [Nmap]({% post_url 2021-01-21-nmap %}) to get port #.
2. Use `smtp_version` with `RHOSTS` IP and `RPORT` port # to learn about the service and OS.
3. Use `smtp_enum` with username list (Use [SecLists](https://github.com/danielmiessler/SecLists)) to get list of valid usernames.
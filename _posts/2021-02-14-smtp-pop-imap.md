---
title:  SMTP POP/IMAP
date:   2021-02-14 10:50:00 -0700
tags: [Networking]
---

SMTP (*Simple Mail Transfer Protocol*) paired with POP/IMAP is used for sending email. The SMTP server validates mail sender, sends mail, and returns undeliverable mail. SMTP typically works over port 25.

POP (*Post Office Protocol*) and IMAP (*Internet Message Access Protocol*) both handle the transfer of email between server and client. The main difference between the two as far as email delivery is concerned is that IMAP will synchronize between different clients.

## SMTP Handshake

Heres a technical(ish) explanation of [how SMTP works](https://www.afternerd.com/blog/smtp/) and the SMTP handshake process.

{% include image-linked.html url="/assets/img/SMTP-sequence-diagram.png" description="Source: https://www.afternerd.com/blog/smtp/" source="https://www.afternerd.com/blog/smtp/" %}
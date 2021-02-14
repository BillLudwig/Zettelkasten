---
title:  SMB Protocol
date:   2021-01-25 18:28:30 -0700
tags: [Networking]
---

SMB (*Server Message Block Protocol*) is a network protocol for sharing files/printers/serial ports etc between a client and server. The client connection is done with NetBIOS over [TCP/IP]({% post_url 2021-01-06-tcp-ip %}). Windows provides client and server support natively since Windows 95. Unix systems can use Samba.
## SMBClient

`smbclient //<IP>/<SHARE PATH> -U <user> -p <port>`

[Documentation](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)
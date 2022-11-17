tags:: #CompSci, #Networking

- NFS (_Network File System_) is a protocol for file & directory sharing across a network. Files or folders “mounted” via NFS can be accessed pretty much the same as local files. [Technical Docs](https://docs.oracle.com/cd/E19683-01/816-4882/6mb2ipq7l/index.html)
- ## Mounting on Linux
	- 1. (_If missing nfs-common package_) Install [nfs-common](https://packages.ubuntu.com/xenial/nfs-common) via `sudo apt install nfs-common.
	  2.  (_If port unknown_) Enumerate with [Nmap](https://billludwig.me/posts/nmap/). I used `sudo nmap <IP> -p- -vv -sS -sC`
	  3.  Find available shares via `showmount -e <IP>`.
	  4.  Create folder to mount into `mkdir /local/path`
	  5.  Mount with `sudo mount -t nfs <IP>:share /local/path -nolock`
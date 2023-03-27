tags:: #CompSci, #CompSci/Networking

- SMB (_Server Message Block Protocol_) is a network protocol for sharing files/printers/serial ports etc between a client and server. The client connection is done with NetBIOS over [[TCP/IP]]. Windows provides client and server support natively since Windows 95. Unix systems can use Samba.
- [Documentation](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)
- ## SMBClient
	- `smbclient //<IP>/<SHARE PATH> -U <user> -p <port>`
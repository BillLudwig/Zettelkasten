tags:: #Networking

- DNS is a [[TCP/IP]] protocol that converts IP addresses to a domain name and vice versa.
- ## When a request for a domain name made this happens.
	- 1. The computer checks it’s local DNS cache. 
	  You can see this cache in Windows with `ipconfig /displaydns`.
	  2.  If unsuccessful the computer sends a request to a _recursive_ DNS server. This information is stored in the router and there are many of these maintained by ISPs, Google, and other providers.
	  3.  If the domain is not in the recursive DNS Server’s cache a request is sent to one of the 13 root name DNS servers.
	  4.  The root name DNS server will forward the request on to one of the Top-Level Domain (TLD) Servers based on the url extension (.com/.org/etc).
	  5.  The Top-Level Domain Server then forwards the request to the appropriate Authoritative name server which responds with the relevant information.
- Public DNS Servers
	- There are many public domain services. Google has two at `8.8.8.8` and `8.8.4.4`. You can search google for additional free DNS servers.
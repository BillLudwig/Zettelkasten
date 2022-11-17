tags:: compsci, networking

- The TCP/IP model is similar to the [[OSI Model]] but is actually used in real life. Since it is less rigid it is harder to conceptualize which is why the OSI model is still relevant. [[Encapsulation]] works the same in both models.
## The 4 TCP/IP Layers
	- Application
	- Transport
	- Internet
	- Network Interface
- ## The Three Way Handshake
	- TCP is a connection-based protocol so the process of creating a connection between two parties uses a process often referred to as the three-way handshake.
	- 1.  `SYN`: The initializing computer sends a request to the remote computer containing a **SYN**(synchronise) packet. This begins the process.
	  2. `SYN/ACK`: The recieving computer responds with a packet that contains both the **SYN** packet and an **ACK**(acknoledgmement) bit.
	  3. `ACK`: The initializing computer then sends a final packet containing the **ACK** bit which confirms that the connection is set up correctly.
	  4. `RST`: Sent to reset the connection. According to [RFC 793](https://tools.ietf.org/html/rfc793) “If the connection does not exist (CLOSED) then a reset is sent in response to any incoming segment except another reset. In particular, SYNs addressed to a non-existent connection are rejected by this means.”
- ## TCP/IP Layers vs OSI Layers
	- | OSI | TCP/IP |
	  |---------------|
	  | Application | Application |
	  | Presentation | Application |
	  | Session | Application |
	  | Transport | Transport |
	  | Network | Internet |
	  | Data Link | Network Interface |
	  | Physical | Network Interface |
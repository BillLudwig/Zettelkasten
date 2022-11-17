tags:: #CompSci

- The OSI (_Open Systems Interconnection Model_) model abstractly describes the flow of data in computer systems through seven heirarchal layers. Each layer is served by the layer before, and in turn serving the next layer through well-defined communication protocols.
- The OSI Model is defined in [ISO/IEC 7498](https://www.iso.org/standard/20269.html).
- The value of the OSI Model is primarily as an abstract mental model that is easy to understand. Real-world networking uses  [[TCP/IP]].
## The 7 Layers
	- _Please do not throw sausage pizza away (PDNTSPA)_
	- Layer 1: Physical - hardware. Transmits/Recieves. Converts to/from binary.
	- Layer 2: Data Link - locates physical address (MAC), formats outgoing data for transmission, and checks recieved packets for corruption
	- Layer 3: Network - locates logical address (IP) and routing.
	- Layer 4: Transport - Chooses protocol (TCP/UPD/..) and splits data into bite sized segments(TCP)/datagrams(UDP)
	- Layer 5: Session - creates/manages connection(session) with remote computer
	- Layer 6: Presentation - translates data into standardized format (also encrypts, compresses, etc)
	- Layer 7: Application - accepts communication requests from applications
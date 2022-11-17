tags:: #CompSci, #Networking

- SMTP (_Simple Mail Transfer Protocol_) paired with POP/IMAP is used for sending email. The SMTP server validates mail sender, sends mail, and returns undeliverable mail. SMTP typically works over port 25.
- POP (_Post Office Protocol_) and IMAP (_Internet Message Access Protocol_) both handle the transfer of email between server and client. The main difference between the two as far as email delivery is concerned is that IMAP will synchronize between different clients.
- ## SMTP Handshake
	- Heres a technical(ish) explanation of [how SMTP works](https://www.afternerd.com/blog/smtp/) and the SMTP handshake process. Source: https://www.afternerd.com/blog/smtp/
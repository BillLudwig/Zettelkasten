tags:: Networking

- [CORS – Cross-Origin Resource Sharing – What, how, and why?](https://www.secjuice.com/cross-origin-resource-sharing-what-is-it-cors/)
	- CORS stands for Cross-Origin Resource Sharing, a system or software framework that allows limited resources on a web page from other domains to be requested as if they were on the same domain server.
	- CORS allows limited resources on a web page from other domains to be requested as if they were on the same domain. CORS is used for Cross-origin requests, that is, if you want to request a resource from a different origin than the one your page is running on.
	- ## CORS Headers
	  collapsed:: true
		- Access-Control-Allow-Origin (ACAO) header. This header is obligated to the implementation of CORS on the data host.
		- Access-Control-Allow-Header header. This one is responsible for restricting servers, domains, or browsers seeking requests; it is sent by hosts restricted to specific domains or URL credentials
	- ## Vulnerabilities
	  collapsed:: true
		- CORS Denial of Service (DoS): Once a malicious user can gain access to your CORS server, then that single access can be manipulated as they can manipulate your server and gain access with a different "origin header," making passage for their [DoS](https://medium.com/@michealtremendous/what-is-a-dos-attack-9b530c9a4927) botnet
		- CORS Referrer Leak: If your CORS-protected server is not properly set up against a referrer leak, then a malicious user can send you their information, which includes their referrer data.
		- CORS Improper Authenticity Protection - If a malicious user sends a request to your server with a valid Origin but an invalid "Host" and "Port" header, then they can request your server.
		- CORS HTTP Response Splitting: If your CORS security is open to HTTP response splitting, then a malicious user who can request your server with a valid "Origin" header can send you a request with a "Content-Type" header that is different from the one you sent them.
- [Cache your CORS, for performance & profit](https://httptoolkit.com/blog/cache-your-cors/)
  id:: 64211362-67b9-4998-8af0-a629bdf9f63c
- [Exploiting CORS Misconfigurations](https://attackshipsonfi.re/p/exploiting-cors-misconfigurations) #CORS
  id:: 64178a57-1c5c-4a27-8200-51bc3eb2e4f6
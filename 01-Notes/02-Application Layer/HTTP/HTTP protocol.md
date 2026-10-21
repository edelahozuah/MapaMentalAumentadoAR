#flashcards/http 
#review2

- Protocol for transferring [[Web resource|web resources]].
- Specified in several versions: 
	- HTTPv1.0, specified in RFC 1945
	- HTTPv1.1, specified in RFC 2616.
	- HTTP/2 (HTTPv2.0), specified in RFC 7540
	- HTTP/3, specified in RFC 9114 (does not use TCP as its transport protocol)
- Operates according to the Client-Server model
	- The client requests resources from a server.
	- On receiving the client's requests, the server returns the resources.
- **Stateless** and **connectionless** protocol
	- In its basic operation, the server does not keep information about clients or transactions.
- Unreliable and insecure protocol.
	- If reliability and/or security are required, the services of other protocols must be used (TCP for reliability and TLS for security, for example).
- Types of TCP connections for HTTP sessions
	- Non-persistent. Solutions used in HTTPv1.0.
	- [[Persistent TCP connections]]. Solutions used in HTTPv1.1 and later.
- There are two types of [[HTTP messages]]
	- Requests, sent by clients to servers.
	- Responses, returned by servers to clients.

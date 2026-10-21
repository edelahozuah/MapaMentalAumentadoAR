#flashcards/http 
#review2 

- It is logically located {{between the web clients to be served and the servers connected to the Internet}}. The proxy's IP address must be configured in the web clients.
	- To web clients, the HTTP proxy acts as a normal web server, while to HTTP servers the proxy is just another client.
- When a client wants to access an HTTP server, it sends the request to its configured HTTP proxy, which in turn sends the request to the HTTP server in question. On receiving the response, the proxy stores the information in its local cache and forwards the response to the web client.
	- If the proxy has the [[Web resource]] requested by the client in its cache, it will carry out the steps described in [[Web cache]]. In this way, the web proxy works as a shared cache for all the web clients using it.

![[Ejemplo_HTTP_Proxy.png]]

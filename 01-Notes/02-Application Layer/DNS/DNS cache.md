#flashcards/dns 
#review2 

- It consists of {{storing temporary copies of DNS resolutions that are NOT the responsibility of the system in question (DNS entity)}}.
	- Possibly as a result of having performed a recursive query.
	- The DNS client (resolver) of a host can also do it.
	- It is stored on hard disk or in RAM for a certain time (the storage time is set by the host's [[Authoritative DNS server|authoritative DNS server]] through its TTL field (see [[DNS resource records (RR)]])).
- It reduces response times.
	- If a DNS client has made a query in the recent past, it will possibly still have that information, and therefore it will not need to contact the [[Local DNS server|local DNS server]]
	- If a client contacts a [[Local DNS server|local DNS server]] that has the requested information in its cache, the server can return it without contacting other DNS servers.

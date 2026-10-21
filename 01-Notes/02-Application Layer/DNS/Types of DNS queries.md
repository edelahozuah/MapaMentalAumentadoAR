#flashcards/dns 
#review2 

- Local
	- Used for queries to the local [[DNS cache]].
- Recursive [^1]
	- Service by which a DNS server contacts other DNS servers if it does not have the information requested in a query.
- Iterative [^1]
	- Service by which a DNS server replies with the record of another, more appropriate DNS server. This is done when the contacted server does not have the exact answer to the query received.
- Inverse
	- A query that requests a hostname given an IP address.

[^1]: **Usually**, [[Local DNS server|local DNS servers]] provide a recursive service, while the rest of the servers ([[Root DNS server]], [[TLD DNS server]] and [[Authoritative DNS server]]) provide an iterative service.

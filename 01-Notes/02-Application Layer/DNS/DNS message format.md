#flashcards/dns 
#review2 

- DNS query and reply messages have the same format, which can be seen below:
- The header section is the first 12 bytes, and contains the following fields:
	- Identification (2 bytes), assigned by the client and returned unchanged in the reply, to match queries with their replies.
	- Flags (2 bytes), which contain several subfields or flags:
		- Query (0) or Reply (1) flag
		- Authoritative flag: indicates whether the responding DNS server is authoritative (1) or not.
		- "Recursion Desired" flag: indicates, in a *query*, that the DNS server should perform recursion (1) if it does not have the RR.
		- "Recursion Available" flag: indicates, in a *reply*, whether the DNS server supports (1) or does not support (0) recursion.
	- The "Number of ..." fields each indicate the number of fields of that type that follow the header.
	- The Questions field contains information about the query.
	- The Answers field contains the records of the requested resource, of which there may be several.
	- The Authority field contains records of other [[Authoritative DNS server|authoritative DNS servers]].

![[Mensaje_DNS.png]]

#flashcards/dns 
#review2 

- Information stored in DNS servers. It consists of four fields: *Type*, *Name*, *Value*, *TTL*. The *Name* and *Value* depend on the *Type* field:
	- If *Type = A*, then *Name* is a hostname and *Value* is the IP address corresponding to that name.
	- If *Type = NS*, then *Name* is a domain and *Value* is the hostname of an [[Authoritative DNS server|authoritative DNS server]] for that domain.
	- If *Type = CNAME*, then *Value* is a canonical/full name corresponding to the alias specified by *Name*.
- In DNS replies ([[DNS queries]]) the DNS servers contacted return zero or more RRs (in a format different from the stored one, but the information is the same).

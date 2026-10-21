#flashcards/tcp
#review2

- TCP header
	- Mandatory part
		- Total length: 20 bytes
		- Fields
			- Source port
			- Destination port
			- [[TCP sequence number]] (SN)
			- [[TCP acknowledgment number]] (AN)
			- [[TCP header length]]
			- Flags (1 bit each)
				- [[URG (TCP flag)]]
				- [[ACK (TCP flag)]]
				- [[PSH (TCP flag)]]
				- RST
				- [[SYN (TCP flag)]]
				- [[FIN (TCP flag)]]
			- [[TCP receive window]] (W)
			- [[TCP checksum]]
			- Urgent Pointer
	- Optional part
		- Length: variable, but 40 bytes at most
		- MSS is an optional field
			- It is included only in the first two segments of the connection (SYN and SYN+ACK)
- Data
	- Contains the application-layer message (or part of the message).
	- Its length must be less than or equal to the connection MSS [[MSS - Maximum Segment Size]]

![[Cabecera_TCP.png]]


#flashcards/tcp
#review2 

- The TCP header has a {{variable}} length, but it is always a multiple of {{32 bits}}.
	- There is a mandatory part and an optional part.
- The *Data Offset* field of the TCP header indicates the number of 32-bit words contained in the header of a given segment.
- The *Data Offset* field is 4 bits long, so the maximum number of 32-bit words in the header is 15. Since the mandatory part of the TCP header takes up 5 32-bit words, 10 remain for the optional part.



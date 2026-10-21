#flashcards/http 
#review2 

The HTTP message format is similar for *requests* and *responses*
- Headers, made up of:
	- *Request line* (in the case of [[HTTP requests]]) or *status line* in the case of [[HTTP responses]].
	- *Header lines* provide extra information. One per line. They have the format:
		- header field name: \<sp\> value \<cr\>\<lf\>
		- The *header field name* is the specific name of the header used and *value* contains the value of that header.
- *Body*:
	- Optional in request messages. When included, it contains parameters related to the requested resource.
	- In response messages it contains:
		- The requested resource, if successful.
		- Text describing an error, if there is a problem.

![[Formato_solicitudes.png]]
![[Formato_respuestas.png]]

#flashcards/http 
#review2 

- HTTP mechanism that {{allows the client to ask the server whether the copy it has stored (downloaded earlier) is still valid}}.
	- In [[HTTP responses]], besides the web resource, the server includes the object's last-modification date (_header line_ _Last-Modified_), so the client, in addition to storing the object in its cache, also stores this date.
	- Before sending an [[HTTP requests|HTTP request]], the browser checks whether it already has the content in its cache. If so, it adds the **If-Modified-Since** _header line_ together with the last-modification date stored with the resource.
- When it receives a request that includes the **If-Modified-Since** header, a server compares the local modification date with the value carried in the header:
	- If the dates match (object not modified), the server replies with a response {{with code _304 (Not modified)_ and an **empty message body**}}
	- If the dates do not match (object modified), the server replies with a message {{with code _200 (OK)_ and the message body will contain the requested [[Web resource]].}}
		- In addition, the **Last-modified** header will contain the date and time of the object's last update.
		- On receiving this message, the web client updates its cache.

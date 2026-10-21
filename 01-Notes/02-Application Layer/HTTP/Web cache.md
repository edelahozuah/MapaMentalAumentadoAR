#flashcards/http 
#review2

- It is {{the temporary storage of [[Web pages|pages]] and [[Web resource|web resources]] at the client, after receiving the server's response}}.
- It makes it possible to {{reduce browsers' access time to recently accessed resources}}.
- Problem: the content may be modified on the server side, so the copy in the client's memory would be out of date.
	- Solution: create a new _header line_ for requests, called _If-Modified-Since_ (known as **conditional GET**)

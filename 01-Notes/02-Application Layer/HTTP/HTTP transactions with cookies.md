#flashcards/http 
#review2 

There are three possible scenarios:
1. When a user visits a website that uses cookies for the first time, the server performs the following actions on receiving a request:
	1. It generates a unique identifier for the user.
	2. It creates an indexed entry in its database associated with that identifier.
	3. It sends a response containing the "Set-Cookie" header with the identifier, for example: `Set-Cookie: 4342` in the responses.
2. When the browser receives a response that includes a cookie, it performs the following steps:
	1. It adds a line to the cookie file it manages, mainly including the "Server name" and the "Identifier" (the cookie).
	2. Subsequently, in every request the user makes to browse the website:
	    a. The browser checks the cookie file.
	    b. If there is a cookie for the site, it extracts the identifier and includes it in the "Cookie" header of the requests, for example: `Cookie: 4342`.
3. Then, every time the user wants to browse the website:
	1. The browser checks the cookie file.
    2. If there is a cookie for the site, it extracts the identification number and includes it in the "Cookie" header of the request messages, for example: `Cookie: 4342`.

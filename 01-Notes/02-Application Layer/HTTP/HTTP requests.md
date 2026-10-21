#flashcards/http 
#review2 

- Messages sent by HTTP clients to HTTP servers to start a transaction.
- The first line of request messages is called the _request line_, and it consists of three fields separated by spaces:
	- _Method_: see below for the different methods that exist.
	- _URL_ of the requested resource.
	- _Version_ of the HTTP protocol.
- The most commonly used methods (requests) are:
	- GET: to download a page/object (obtain information)*.
		- The most widely used request message.
		- Where applicable, parameters are sent together with the URL.
	- POST: to send information to the server (e.g. form data).*
		- Parameters/information are sent in the message body. E.g., to fill in a form.
		- What the server returns depends on the content sent.
	- HEAD: similar to GET, but to download only the header of the page/object.
		- For monitoring and debugging. E.g., last modification of an object, checking links, etc.
	- PUT: to upload a new page/object.
	- DELETE: to delete a page/object.
	- OPTIONS: to query options.
		- E.g., properties of the server or of a resource.

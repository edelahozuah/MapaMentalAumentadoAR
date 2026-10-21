#flashcards/http 
#review2

- “Specific” mechanism for identifying users upon request from the server.
	- Status code “401 Unauthorized”.
	- With the “WWW-Authenticate” header.
- The request message must contain “credentials”.
	- In the “Authorization” header.
		- Credentials: “username” and “password”.
	- Transparently to the user.
		- They are typed once and remain in the device's cache
	- Stateless.
		- Credentials in every request.
	- Stateful.
		- The server associates a “cookie”.

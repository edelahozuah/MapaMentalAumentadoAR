#flashcards/http 
#review2 


- Some _header lines_ common to both *request* and *response* messages: 

| **Header** | **Content** |
| --- | --- |
| Date | Date and time at which the message is sent |
| Connection | Indicates, regarding the TCP connection, whether to close it or keep it open |

- Some _header lines_ of _request_ messages:
 
| **Header**| **Content** |
| --- | --- |
|Accept|Content types the Client can accept|
|Accept-Charset|Character sets the Client can accept|
|Accept-Encoding|Encodings the Client can accept|
|Accept-Language|Languages the Client can handle|
|Host|Domain name of the Server|
|Authorization|Client credentials (username and password)|
|Cookie|Notification of a “cookie” previously set by a Server|

- Some _header lines_ of _response_ messages:
  
|**Header**|**Content**|
| --- | --- | 
|Server|Information about the Server|
|Content-Encoding*|Content encoding type|
|Content-Language|Language of the intended audience of the content|
|Content-Length*|Number of bytes of the content|
|Content-Type*|MIME type of the content|
|Last-Modified|Date and time of the resource's last modification|
|Location|Tells the Client where to send the request for the requested resource|
|Set-Cookie|Cookie that the Server sends to the Client|
|WWW-Authenticate|Indication to the Client that authentication is required|

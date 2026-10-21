#flashcards/http 
#review2


- This is a simple example of an [[HTML]] file
>\<!DOCTYPE html\>
>
>\<html\>
>
>\<head\>
>  \<title\>Basic HTML Example\</title\>
>\</head\>
>
>\<body\>
>  \<h1\>Level 1 heading\</h1\>
>  \<p\>This is a paragraph of text.\</p\>
>  \<h2\>Level 2 heading\</h2\>
>  \<p\>Another paragraph of text. \</p\>
>  \<a href="https://www.ejemplo.com/hola.html"\>Welcome page!\</a\>
>  \<img src=”https://www.ejemplo.com/imagen.jpg" alt=”Image"\>
>\</body\>
>
>\</html\>

- If a browser processes this file, the output would be the following:
	- **IMPORTANT**: after processing the HTML file shown at the beginning, the browser's user agent detects that it must download the [[Web resource]] with [[Addressing in HTTP|URL]] https://www.ejemplo.com/imagen.jpg. Once that image has been downloaded, the user agent can display the web page completely.
	- If the user clicks on the link, the user agent must ask the browser's HTTP client to download the object with the associated URL.

![[Ejemplo_basico_HTML.png]]

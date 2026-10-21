#flashcards/http 
#review2 

- If two or more [[Web resource|web resources]] must be downloaded from the same server, the client must wait for one to be downloaded before requesting the next.
- If $N$ resources must be downloaded from a server, all of the same size and with transmission time $X_p$, the total download time [^1] is [^2]:
	- $T_{PSC} = RTT + N\times (RTT+X_p)$

![[Ejemplo_HTML_sin_canalizacion.png]]

[^1]: the transmission time of the GET is assumed to be negligible.
[^2]: the $RTT=2\times T_{prop}$

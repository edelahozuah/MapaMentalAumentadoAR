#flashcards/http 
#review2 

- If two or more [[Web resource|web resources]] must be downloaded from the same server, all the requests can be sent {{back to back without waiting for their responses}}.
- If $N$ resources must be downloaded from a server, all of the same size and with transmission time $X_p$, the total download time[^1] is [^2]
	- $T_{PCC} = 2\times T_{prop} + N\times X_p$

![[Ejemplo_HTML_con_canalizacion.png]]

[^1]: the transmission time of the GET is assumed to be negligible.
[^2]: one of the $T_{prop}$ is due to the propagation of the GET and the other to the propagation of the object (the figure clearly shows how the last bit of the last resource needs one $T_{prop}$ to reach the client.)

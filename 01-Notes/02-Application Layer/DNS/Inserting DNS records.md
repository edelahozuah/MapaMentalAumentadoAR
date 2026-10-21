#flashcards/dns 
#review2 

- Let's look at an example of how records are added to a DNS server.
- To do so, we buy a domain, for example *jaimegarciareinoso.es*, from any accredited registrar (there are several).
- Each DNS provider has its own configuration system, usually web-based. The following figure shows the control panel of the provider we bought ours from:
![DNS Control Panel](03-Figures/Panel-control-DNS.png)
- The figure shows several entries stored in **the authoritative server of the domain**, each of a different type ([[DNS resource records (RR)|RR]]):
	- Type A RRs map the hostnames in the *Entrada DNS* (DNS entry) field to the [[IP address|IP addresses]] in the *Valor* (Value) field. For example, the host named *www.jaimegarciareinoso.es* has the IP address *217.76.142.216*. Since we sometimes forget to type the host name in the browser, in this case *www*, an A RR is usually also added for the name without that part, in this case *jaimegarciareinoso.es*, associating it with the same IP address. The following capture shows part of the content of the *response* message that the local DNS server sends to the client that requested the IP address of the web server [^1] (note that the IP address matches the *Valor* field of the authoritative DNS server):
![Wireshark DNS A capture](03-Figures/Wireshark-DNS-A.png)
	- CNAME RRs *point* to a different domain name. This means that when a name in the left-hand column is to be resolved, the reply will contain the name in the *Valor* field. In addition, the *response* message will return another type A RR, with the mapping between the name in the value field and its corresponding IP address, as can be seen in the following capture:
![Wireshark DNS CNAME capture](03-Figures/Wireshark-DNS-CNAME.png)

[^1]: recall that a *response* message includes the *Queries* field sent in the query.

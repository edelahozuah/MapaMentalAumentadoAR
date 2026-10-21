#flashcards/intro 
#review2 

- In the vertical communication of a transmitting [[Host]], an upper layer (at level *i+1*) sends a [[Protocol data unit (PDU)|PDU]] to the adjacent lower layer (at level *i*), together with control information ([[Interface control information (ICI)|ICI]]). The lower layer adds a {{[[Header|header]]}} to the received PDU (which at this level we will call {{[[Service data unit (SDU)|SDU]]}}) and generates its own level *i* PDU. This layer *i* is said to *encapsulate* [^1] the received PDU.
- In the vertical communication of a receiving [[Host]], a lower layer at level *i* receives its PDU from the level below. This layer *i* extracts and processes the header of its level contained in the received PDU. If everything is correct, it removes that header (which is known as {{decapsulation}}) and sends the rest of the content to the upper layer *i+1*, which will receive the level *i+1* PDU.

![[Modelo-de-capas.png]]

[^1]: we can use the analogy of a coffee capsule, where the capsule wraps or protects the coffee inside it. In our case, the level *i* header "protects" the level *i+1* PDU.
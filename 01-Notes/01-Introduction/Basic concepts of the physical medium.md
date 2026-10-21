#flashcards/intro 
#review2
- Bit: {{basic unit of information representation in the binary system}}
- Signal: {{the way a bit or set of bits is transmitted over a transmission medium}}
- Link: {{transmission medium used to transmit signals between network devices}}
- Guided medium: {{propagates signals over a solid medium: copper (twisted pairs, coaxial), glass fiber (optical fiber)}}
- Unguided medium: {{propagates signals over a non-solid medium, without the need for a conductor: radio, for example}}
- Propagation time ($T_{prop}$): {{the time elapsed from when the signal is generated at a transmitter until it reaches the receiver
	- Propagation time$=T_{prop} = \frac{distance}{Propagation\ speed} = \frac{d (m)}{s (m/s)}$}}
- Transmission rate ($R$): {{the number of bits that a network card can generate as a signal in a given time interval. It is normally expressed in bits/second [bps] or in multiples of it, such as kilobits/second [kbps] (1000 bps), megabits/second [Mbps]  ($1\times 10^6$ bps) or gigabits/second [Gbps] ($1\times 10^9$ bps).}}
- Transmission time ($T_{tx}$): {{the time a device's network card needs to generate the signal corresponding to the information to be transmitted.
	- Transmission time$=T_{tx}= \frac{n (bits)}{R (bits/s)}$}} 
- End-to-end delay ($T_{ee}$): {{the time needed from when transmission starts until the information has completely reached the destination. On a direct link:
	- $T_{ee} = T_{tx} + T_{prop}$ }}
- Packet error probability ($P_{eb}$): {{the probability that at least one of the transmitted bits has reached the receiver with an error:
	- $P_{eb} = 1 - (1-BER)^n$
		- $BER$=Bit Error Rate
		- $n$ is the number of bits transmitted in a packet.}}
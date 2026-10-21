#review2 

- The checksum is computed over the [[IP pseudo-header]], the [[The UDP header|UDP header]] (with the checksum field set to two zero bytes for the calculation) and the data of the UDP segment. Zero bytes are appended at the end so that the total length of the resulting string is a multiple of two bytes.
- To compute the checksum, the 16-bit one's complement of the one's complement sum of that string is taken.

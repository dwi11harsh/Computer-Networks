- Detecting errors is only one part of the problem. The other part is correcting errors once detected
- There are two basic approaches that can be taken when the recipient of a message detects an error.
	- One is to notify the sender that the message was corrupted so that the sender can retransmit a copy of the message.
	- Alternatively, there are some types of error detection algorithms that allow the recipient to reconstruct the correct message even after it has been corrupted; such algorithms rely on ***error correcting codes***

- The basic idea behind any error detection scheme is to add redundant information to a frame that can be used to determine if errors have been introduced.
- In general, these redundant bits are referred to as error-detecting codes.
- In specific cases, when the algorithm to create the code is based on addition, they may be called a checksum.
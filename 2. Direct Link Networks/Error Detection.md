- Detecting errors is only one part of the problem. The other part is correcting errors once detected
- There are two basic approaches that can be taken when the recipient of a message detects an error.
	- One is to notify the sender that the message was corrupted so that the sender can retransmit a copy of the message.
	- Alternatively, there are some types of error detection algorithms that allow the recipient to reconstruct the correct message even after it has been corrupted; such algorithms rely on ***error correcting codes***

- The basic idea behind any error detection scheme is to add redundant information to a frame that can be used to determine if errors have been introduced.
- In general, these redundant bits are referred to as error-detecting codes.
- In specific cases, when the algorithm to create the code is based on addition, they may be called a *checksum*.

# Two-Dimensional Parity
For example, odd parity sets the eighth bit to 1 if needed to give an odd number of 1s in the byte, and even parity sets the eighth bit to 1 if needed to give an even number of 1s in the byte.

![[Screenshot 2024-10-30 at 1.17.33 PM.png]]

# Internet Checksum Algorithm
The idea behind the Internet checksum is very simple—you add up all the words that are transmitted and then transmit the result of that sum. The result is called the checksum. The receiver performs the same calculation on the received data and compares the result with the received checksum. If any transmitted data, including the checksum itself, is corrupted, then the results will not match, so the receiver knows that an error occurred.

a pair of single-bit errors, one of which increments a word and one of which decrements another word by the same amount, will go undetected.

# Cyclic Redundancy Check
a 32-bit CRC gives strong protection against common bit errors in messages that are thousands of bytes long

- The theoretical foundation of the cyclic redundancy check is rooted in a branch of mathematics called finite fields.
The theoretical foundation of the cyclic redundancy check is rooted in a branch of mathematics called ==finite fields==.


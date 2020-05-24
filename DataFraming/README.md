# Data Framing

## Problem Statement
when data is transfered in stream of bytes, receiving end need a 
method to divide a long stream of bytes into discrete messages. called- FRAMING

Framing (the method of dividing a long stream of bytes into discrete messages) isn't immediately obvious with protobuf. What you get from a protobuf serialization is a binary buffer of data. You almost certainly want to send more than one such buffer over time, so how does your peer know when one message ends and another starts?

## Solution
There are two approaches commonly used for message framing: length prefixing and delimiters.

### Length Prefixing
- Length prefixing prepends each message with the length of that message. The format (and length) of the length prefix must be explicitly stated; “4-byte signed little-endian” (i.e., “int” in C#) is a common choice. To send a message, the sending side first converts the message to a byte array and then sends the length of the byte array followed by the byte array itself.

- Receiving a length-prefixed message is harder, because of the possibility of partial receives. First, one must read the length of the message into a buffer until the buffer is full (e.g., if using “4-byte signed little-endian”, this buffer is 4 bytes). Then one allocates a second buffer and reads the data into that buffer. When the second buffer is full, then a single message has arrived, and one goes back to reading the length of the next message.

### Delimeters
- Delimiters are more complex to get right. When sending, any delimiter characters in the data must be replaced, usually with an escaping function. The receiving code cannot predict the incoming message size, so it must append all received data onto the end of a receiving buffer, growing the buffer as necessary. When a delimiter is found, the receiving side can apply an unescaping function to the receiving buffer to get the message. If the messages will never contain delimiters, then one may skip the escaping/unescaping functions.


## Examples
- https://eli.thegreenplace.net/2011/08/02/length-prefix-framing-for-protocol-buffers
- https://blog.stephencleary.com/2009/04/message-framing.html
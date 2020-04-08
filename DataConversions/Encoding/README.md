# What is Encoding and Decoding?
Most people like to work with text.
However, computer storage can only work with bytes.
`Encoding is the process of converting text to bytes.`

Over the past few decades, many different encoding schemes have been developed for different purposes, such as brevity, compatibility, or internationalization.
Today, everything should simply use UTF8. (sadly, not everything does yet)

## Definition
Encoding is the process of putting a sequence of characters such as letters, numbers and other special characters into a specialized format for efficient transmission.

Decoding is the process of converting an encoded format back into the original sequence of characters. It is completely different from Encryption which we usually misinterpret.

Encoding and decoding are used in data communications and storage. Encoding should NOT be used for transporting sensitive information.

In simpler terms, encoding refers to the way any character is understood “within” the computer for storage or transmission from one machine to another.

Since, a computer can only understand two values 0 and 1, each character that you want to store or send across has to be converted into a sequence of 0’s and 1’s.

- http://kunststube.net/encoding/
- https://www.tutorialspoint.com/security_testing/encoding_and_decoding.htm

- https://www.quora.com/Who-does-encoding-and-decoding-in-a-computer

# When to encode and decode?
- Used for communicating the data. 
- Encode at the very last moment before you send the data to the external system.  

- https://www.jardinesoftware.net/2011/09/25/when-should-i-encode/


# Different Types of encoding
- Base64 Encoding
- URL Encoding
- ASCII Encoding
- Unicode Encoding
- Hex Encoding
- RLP Encoding
- Amino Encoding

- https://skorks.com/2009/08/different-types-of-encoding-schemes-a-primer/


# Why are there different encoding types?
- 

- https://stackoverflow.com/questions/10088473/why-are-there-different-encoding-types

## References

- http://kunststube.net/encoding/
- https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/


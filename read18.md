# Crptography

## Encrypting a message

Imagine Caesar wants to send this message:

SECRET MEETING AT THE PALACE

Here's what that might look like encrypted:

YKIXKZ SKKZOTM GZ ZNK VGRGIK

That looks an awfully lot like gobbledygook at first, but this encrypted message is actually very related to the original text.

The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.

To make the encrypted message above, I shifted the alphabet by 6 and used this substitution table:

A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C	D	E	F

S shifts 6 letters over to Y, E shifts 6 letters over to K, etc. Here's the first word and its shifts:

S	E	C	R	E	T
Y	K	I	X	K	Z

## Decrypting a message

According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift amount, it was trivial for them to decode the message.

Imagine Caesar sends this message to a comrade:

EHZDUH EUXWXV

The comrade uses this substitution table, where the alphabet is shifted by 3:

A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z
D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C

They can then decode the message with certainty. The first letter "E" was shifted by 3 from "B", the second letter "H" was shifted by 3 from "E", etc. The result is this ominous message:

BEWARE BRUTUS

## Cracking the cipher

Imagine that a very literate and savvy enemy intercepts one of Caesar's messages.

RZ VMZ WMDIBDIB VGG AJMXZN OJ EJDI RDOC XGZJKVOMV OJ YZAZVO OCZ ZIZHT LPZZI VO OCZ IDGZ YZGOV

That enemy does not know that Caesar always uses a shift of 3, so he must attempt to "crack" the cipher without knowing the shift.

There are three main techniques he could use: frequency analysis, known plaintext, and brute force.

## Encryption, decryption, and cracking

Thanks to this exploration of the Caesar Cipher, we now understand the three key aspects of data encryption:

Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).

Decryption: recovering the original data from scrambled data by using the secret key.

Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

Whenever we consider a possible encryption technique, we need to think about all those aspects: how easy is it to encrypt? how easy is it to decrypt? And most importantly, how easy is it for a nefarious individual to crack the code?

We can no longer use the Caesar Cipher to secure our data, as it is far too easy to crack, but understanding the Cipher prepares us for understanding modern encryption techniques.

[source](https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:online-data-security/xcae6f4a7ff015e7d:data-encryption-techniques/a/encryption-decryption-and-code-cracking)

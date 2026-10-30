In Asymmetric Encryption, we use 2 different mathematically related keys for encryption and decryption. These are the ==🟠Private key==, which is obviously kept private, and the ==🟠Public key==, which is public information that anyone may find.

A way to picture this is an open padlock. I can hand out as many open padlocks (public keys) as I want, and anyone can snap one shut on a box to lock it, but only I have the key (private key) that can open it.

In cases of information transfer over the internet, when we send a message we use the public key of the recipient to encrypt the information being sent out. We also send a ==🟠digital signature==, which is a hash of the message encrypted with our own private key, to the recipient.

The data encrypted by the public key can only be decrypted by the private key of the recipient, say John. So John will receive our message and use his private key to decrypt the contents and read the message. He can then use our public key to check the digital signature, which proves the message came from us ([[Proof of Origin]]) and was not modified on the way ([[Proof of Integrity]]).

In case of a reply, John will use our public key to encrypt the message and send it to us with a digital signature made using his private key. Upon receiving the message, we will use our private key to decrypt the message and read it, thus successfully completing communication between two parties over the internet securely.

The downside is that this is much slower than [[Symmetric Encryption]], so in practice it is used for small jobs such as exchanging keys and signing, which we look at in [[Cryptographic Keys]].

# Previous Topic
[[Symmetric Encryption]]
# Previous Section
[[Public Key Infrastructure]]
# Next Topic
[[Key Escrow]]

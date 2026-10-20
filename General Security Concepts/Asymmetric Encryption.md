In Asymmetric Encryption, we use 2 different mathematically related keys for encryption and decryption. These are the Private key which is obviously kept private and the Public key which is public information that anyone may find. 

In cases of information transfer over the internet, when we send a message we use the public key of the recipient to encrypt the information that is being sent out and we also send a hash of the message calculated from our private key to the recipient. 

The data encrypted by the public key can only be decrypted by the private key of the recipient say John. So John will receive our message and use his private key to decrypt the contents and read the message. 

In case of a reply, John will use our public key to encrypt the message and send it to us with a hash calculated from his private key. Upon receiving the message, we will use our private key to decrypt the message and read it, thus successfully completing communication between two parties over the internet securely.

# Previous Section
[[Public Key Infrastructure]]
# Previous Topic
[[Symmetric Encryption]]
# Next Topic
[[Key Escrow]]

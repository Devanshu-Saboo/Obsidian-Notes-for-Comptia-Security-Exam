Encryption is a process which is used to ensure confidentiality. In simple terms, if I talk to my friend and I want to ensure our conversation is not understood by anyone else even if they overhear us, I would use encryption.

Symmetric encryption is a type of encryption that uses keys to encrypt and decrypt data. In symmetric encryption, the same key is used for both encryption and decryption, so both me and my friend would use a key, say "21", to encrypt and decrypt our conversation. ==🟢ex. AES, which we look at in [[Encryption Algorithms]]==

This process is very fast to implement, which is why it is used for encrypting large amounts of data. However, as more people get involved the number of keys required grows very quickly, since every pair of people needs their own key. ==🟡With n people the number of keys is n(n-1)/2, so 4 people need 6 keys but 10 people already need 45.==

That makes it difficult to keep and maintain keys, and there is also the problem of how to safely get the key to the other person in the first place (see [[Cryptographic Keys]]). This is why we also have [[Asymmetric Encryption]].

# Previous Section
[[Public Key Infrastructure]]
# Next Topic
[[Asymmetric Encryption]]

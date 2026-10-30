An encryption algorithm is simply the set of steps (the math) that takes your plain text and turns it into unreadable cipher text, and then back again. Going back to my example with my friend in [[Symmetric Encryption]], the algorithm is *how* we scramble the conversation and the key "21" is what we scramble it with.

There are a lot of different algorithms out there and not all of them are equally good. They differ in how they do the encryption, how fast they are and how big the key they use is. ==🟢ex. DES is an old symmetric algorithm that is now considered weak, whereas AES is the one most commonly used today==

An important thing to remember is that the algorithm itself is usually public and well studied, the thing that keeps the data safe is the key and not hiding how the algorithm works. That is why it is a bad idea for an organization to invent its own algorithm, since a public one has already been tested by thousands of people trying to break it.

# Previous Topic
[[Transport Encryption]]
# Previous Section
[[Encrypting Data]]
# Next Topic
[[Cryptographic Keys]]

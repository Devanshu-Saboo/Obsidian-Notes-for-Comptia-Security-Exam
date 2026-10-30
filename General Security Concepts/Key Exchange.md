Key exchange is simply the process of getting both sides to end up with the same symmetric key, without anyone else being able to get hold of it. This is important for real-time encryption such as a web session or a VPN, since we need the speed of [[Symmetric Encryption]] but cannot meet the other person beforehand to agree on a key.

There are two main ways to do this:
1. ==🟠Out-of-band key exchange==: The key is shared outside of the network. ==🟢ex. Telling someone the key over the phone, handing it over in person or sending it with a courier==. It is safe from anyone listening on the network, but it is slow and does not scale. Imagine doing this for every website you visit.
2. ==🟠In-band key exchange==: The key is exchanged over the network itself, but protected so that an eavesdropper still cannot use it. This is what is used for real-time encryption.

### How In-band Works
The problem is that [[Asymmetric Encryption]] is much too slow to encrypt all the data of a session, and symmetric encryption needs a shared key to work. The solution is to use the asymmetric keys only for the exchange and then switch to symmetric for the actual data.

Lets say Alice and Bob want to talk securely. Each of them has their own public and private key pair, and they swap their *public* keys with each other, which is fine since anyone may see these.
1. Alice combines her own private key with Bob's public key
2. Bob combines his own private key with Alice's public key
3. Mathematically, both of them end up with the exact same result, which becomes their ==🟠symmetric key==

The key part is that the symmetric key was never sent over the network. Both sides worked it out on their own, so an attacker who captured everything that was sent only ever saw the public keys, which are not enough to work out the symmetric key. The idea behind this is known as Diffie-Hellman, which you may see named.

A good way to picture this is mixing paint. Alice and Bob agree on a common paint colour in public, then each of them secretly picks their own colour, mixes it with the common one and sends the mixture across. Mixing is easy but separating a mixture back into its colours is basically impossible, so an eavesdropper cannot find out their secret colours. When each of them then adds their own secret colour to the mixture they received, they both end up with the identical final colour. That final colour is the shared key.

Once both sides have the symmetric key, it is used to encrypt everything for the rest of the conversation. This temporary key is called a ==🟠session key== and is thrown away when the session ends, so the next session uses a brand new one.

This is exactly what is happening behind the scenes in [[Transport Encryption]], whether it is HTTPS or a VPN. The [[Public Key Infrastructure]] certificates are what let us confirm that the public key we received really belongs to who we think it does.

> [!joke] Asymmetric encryption does the introductions and then symmetric encryption does all the actual talking.

# Previous Topic
[[Cryptographic Keys]]
# Previous Section
[[Encrypting Data]]
# Next Topic
[[Encryption Technologies]]

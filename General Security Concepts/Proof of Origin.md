This is verifying the origin point of data to ensure that the communication originated from who we think it originated from and not anyone else. This can be done with digital signatures that rely on private key and public key cryptography, as seen in [[Asymmetric Encryption]].

The idea is that the sender signs the data using their *private key*, which only they have. Anyone can then use the sender's *public key* to check the signature. If it checks out, it could only have come from the owner of that private key. ==🟢ex. A digitally signed email or a code signed software installer==

This is just like a handwritten signature, but much harder to forge. A digital signature actually gives us both proofs at once, as it is made from a hash of the data (so [[Proof of Integrity]]) signed with the private key (so proof of origin). That is how we get full [[Non-Repudiation]].

To trust that a public key really belongs to the person who says so, we rely on certificates, see [[Public Key Infrastructure]].

# Previous Topic
[[Proof of Integrity]]
# Previous Section
[[CIA Triad]]
# Next Section
[[AAA Framework]]

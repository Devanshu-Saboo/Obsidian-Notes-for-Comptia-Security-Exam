A cryptographic hash is used to represent data as a short string of text. You may also hear this called a ==🟠message digest== or a ==🟠fingerprint==. Hashing is *not* encryption, it works one way only, so you cannot take a hash and turn it back into the original data.

The same input will always give the same hash, but if even one single character of the input changes, the hash is completely different. ==🟡SHA-256 produces 256 bits, which is shown as 64 hexadecimal characters==. ==🟢ex. "My name is Professor Messer." gives 19da9a2e26f3bff67f0522f962851c42542b8659333ac53397c8d65aa7a3f871, but changing the full stop to an exclamation mark gives 54381cae1eea10892d81c8688d06d1928b4ee8495061a792864f83092b033aea==

This is what we use for [[Proof of Integrity]]. Hashes are also used for storing passwords, verifying that a file was not changed, creating digital signatures and in [[Blockchain Technology]].

### Password Storage
Databases do not store the actual passwords, they only store the hash of each password. When you log in, the system hashes whatever you typed and compares it to the stored hash. If a hacker steals the database, they get the hashes but not the passwords themselves.

### Rainbow Tables and Salting
A ==🟠rainbow table== is a pre-compiled set of every possible input and the hash that goes with it. Instead of working out each hash, the attacker just looks the hash up, so it can reverse an unsalted hash in seconds.

The fix is ==🟠salting==. A salt is random data that is added to the password *before* it is hashed, and each user gets a different one. This means that two users with the same password, say "dragon", will have completely different hashes, and a precomputed rainbow table is of no use because it was never built with these salts. The attacker is then left with brute force, which takes much longer. This is the salt column I mentioned in [[Database Encryption]].

### Key Stretching
Key stretching slows down brute force attacks by making the hashing process do much more work. For example, you hash the password, then hash that hash, then hash that again, and keep going many times. It makes no difference to a real user who logs in once, but it makes it painfully slow for an attacker who has to try millions of guesses. ==🟢ex. PBKDF2 and bcrypt==

An easy way for me to remember it is that salting beats *precomputed* attacks, key stretching beats *fast guessing*.

### Digital Signatures
A digital signature is the digital version of a handwritten signature. It gives us three things: ==🟠integrity==, ==🟠authentication== and ==🟠non-repudiation==, so the sender cannot later deny sending it ([[Non-Repudiation]]).

It works almost the opposite way to encryption. In [[Asymmetric Encryption]] we encrypt using the recipient's *public* key, but to sign we use *our own private key*. Lets say Alice sends Bob "You're hired, Bob":
1. Alice's email program hashes the message
2. It then encrypts that hash with Alice's *private key*, and this encrypted hash is the digital signature
3. The message is sent along with the signature. Note that the message itself is still plain text, the signature does not encrypt it.
4. Bob's email program decrypts the signature using Alice's *public key*, which gives him the hash Alice made
5. It then hashes the message it received and compares the two hashes

If the two hashes match, the message was not changed ([[Proof of Integrity]]) and it must have come from Alice, as only she has her private key ([[Proof of Origin]]). If they do not match, either the message was changed or it was not signed by Alice. In most email programs this is as simple as ticking a checkbox.

# Previous Topic
[[Obfuscation]]
# Previous Section
[[Encrypting Data]]
# Next Topic
[[Blockchain Technology]]

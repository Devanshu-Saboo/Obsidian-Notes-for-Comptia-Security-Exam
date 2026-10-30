As you must know by now, databases hold data such as usernames, password hashes and, in some more advanced databases, a separate column called a ==🟠salt==, which further increases the complexity of the password hash. A salt is a random value that is added to the password before hashing, so even if two users have the same password their hashes will be different.

In database encryption, we have two major types of encryption, namely:
1. ==🟠Transparent encryption==
2. ==🟠Record level encryption==

Transparent encryption simply encrypts all the database information with a symmetric key, in which both the encryption process and decryption process use the same key. It is called "transparent" because the applications using the database do not need to be changed or even know about it. This protects the data at rest, for example if someone steals the database files.

Whereas in Record level encryption, individual columns of the database are encrypted with symmetric keys. Thus each column of the database would have a unique key for encrypting and decrypting that particular column. ==🟢ex. The credit card column could be encrypted with its own key that only the payments team can use, whilst the name column is encrypted with a different key.==

The benefit of record level encryption is that access can be controlled much more finely, but it is also more work to manage since there are many more keys. These are [[Symmetric Encryption]] keys, so everything we said about key handling applies here as well.

# Previous Section
[[Encrypting Data]]
# Next Topic
[[Transport Encryption]]

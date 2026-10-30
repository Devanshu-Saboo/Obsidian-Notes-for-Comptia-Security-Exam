Blockchain technology is the foundation of cryptocurrency, but it can also be used for many other things. In simple terms it is a ==🟠distributed ledger==, which is a ledger that is available for anyone to see and whose job is to keep track of individual transactions. Everyone who takes part in the blockchain can keep a copy of the ledger, and once a change is recorded it is sent out to everyone else who has a copy. This is also called an ==🟠open public ledger==.

Anything that needs to track transactions can use it. ==🟢ex. Payment processing, Digital identification, Supply chain monitoring, Digital voting, Transferring a house title==

This is how it works:
1. A transaction happens, say sending some Bitcoin from one person to another
2. The transaction is sent to *everyone* taking part in the blockchain, not just the two people involved, and each device keeping a copy of the ledger receives it
3. The transaction is added to a larger ==🟠block== of transactions
4. A [[Hashing and Digital Signatures]] hash is added to the block, which gives integrity to all of the transactions in it
5. A copy of the finished block is sent to everyone who has a copy of the ledger

The hash is the important security part. If somebody goes back and modifies one of the existing transactions, the hash of that block will no longer be valid. The other devices that are keeping the ledger will notice that the block has an invalid hash, throw it out, and know that it has been tampered with.

Each block also contains the hash of the block before it, which links them together into a chain. That is why it is called a blockchain, and it means that changing an old block would break every block that comes after it.

This is basically [[Integrity]] from the CIA triad, but with the proof being kept by lots of people instead of just one central authority.

# Previous Topic
[[Hashing and Digital Signatures]]
# Previous Section
[[Encrypting Data]]
# Next Topic
[[Certificates]]

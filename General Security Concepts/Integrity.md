Integrity is simply ensuring that data is unmodified by any unauthorized user. This may include ensuring that communication between 2 parties is unmodified and that the original text sent between the two is untampered with.

Think of a bank transfer. If someone were able to change the amount from $100 to $10,000 while it was on its way, nobody would have read anything secret but the integrity of the transaction would be gone. ==🟢ex. A tampered bank transaction, A software download that has been modified to include malware==

There are a couple of ways to check this:
1. ==🟠Hashing==: A hash is calculated from the data and compared before and after. If even a tiny part of the data changes the hash will be completely different, see [[Proof of Integrity]]
2. ==🟠Digital Signatures==: Using asymmetric encryption on the hash, this proves the data has not changed and also who it came from, see [[Asymmetric Encryption]]

The reason I put this right before Non-Repudiation is that they are very closely related, integrity is about the data being unchanged and [[Non-Repudiation]] builds on this by also proving where it came from.

# Previous Topic
[[Confidentiality]]
# Previous Section
[[CIA Triad]]
# Next Topic
[[Availability]]

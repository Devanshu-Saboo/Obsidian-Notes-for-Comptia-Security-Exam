This is simply verifying that the data received is accurate and consistent with the data that was sent. This is commonly done by using a hash such as a message digest hash.

A hash takes any amount of data and produces a fixed length string, and it works one way only, you cannot take the hash and get the original data back. If even one character of the data changes, the hash that comes out is completely different. ==🟢ex. Downloading a file and comparing its hash with the one published by the vendor, if they match the file was not changed==

Common hashing algorithms are ==🟡SHA-256 (widely used today) and MD5 (older and no longer considered secure)==.

One limitation to keep in mind is that a hash only proves the data was not changed. It does not tell us *who* sent it, since anyone can calculate a hash. For that we need [[Proof of Origin]].

# Previous Topic
[[Non-Repudiation]]
# Previous Section
[[CIA Triad]]
# Next Topic
[[Proof of Origin]]

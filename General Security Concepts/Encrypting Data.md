Data stored in plain text is inherently considered insecure because anyone with a certain level of access, or anyone eavesdropping on the network, would be able to read the plain text and the data. This is why there is an inherent need to encrypt data.

There are three situations in which you want to encrypt data, namely:
1. ==🟠Data at rest==
2. ==🟠Data in transit==
3. ==🟠Data in use==

As the name implies, data at rest is data that is stored, such as on your computer or in a database. In case of an attack this data should not be readable by an attacker, or else it may leak sensitive information to the wrong people, and this is why we need to encrypt it. ==🟢ex. Full disk encryption on a laptop, so that if it is stolen the data cannot be read. We look at databases in [[Database Encryption]].==

Similarly, data in transit is data that is being transferred over a medium such as the internet, or a local network transfer using FTP (File Transfer Protocol) etc. This is covered in [[Transport Encryption]].

Finally, we have data in use. This is data that is pulled into your RAM (Random Access Memory) and is being utilized by your Operating System and the different applications running on it. Data in use may contain a lot of sensitive information since all data has to pass through this stage to be displayed. An even bigger concern is the chance of a buffer overflow attack on the RAM, which can grant an attacker elevated or administrator privileges.

This is the hardest of the 3 to protect, as the data usually has to be in a readable form for the system to be able to work with it.

# Previous Section
[[Public Key Infrastructure]]
# Next Topic
[[Database Encryption]]

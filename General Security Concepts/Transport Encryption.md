Transport encryption is simply encrypting data while it is in transit, which is the second state we looked at in [[Encrypting Data]]. Anything travelling across a network can be eavesdropped on by someone sitting in the middle, so we encrypt it before it leaves the device and only the intended recipient can read it.

There are a few common ways this is done:
1. ==🟠VPN (Virtual Private Network)==: Creates an encrypted tunnel between a device and the organization network, so everything inside the tunnel is unreadable to anyone listening in between. This is the same VPN we mentioned in [[Threat Scope Reduction]]. ==🟢ex. An employee working from a coffee shop connecting back to the company network==
2. ==🟠SSL/TLS (Transport Layer Security)==: Encrypts the communication between your browser and a web server, which is what HTTPS is. ==🟢ex. The padlock next to the URL when you log in to your bank==
3. ==🟠WPA3==: Encrypts the traffic between your device and the wireless access point, so people sitting nearby cannot just sniff your Wi-Fi traffic.

Most of these use a combination of the [[Symmetric Encryption]] and [[Asymmetric Encryption]] we have already seen, I will break down how in [[Cryptographic Keys]].

> [!joke] Using public Wi-Fi without a VPN is basically shouting your password across a crowded room.

# Previous Topic
[[Database Encryption]]
# Previous Section
[[Encrypting Data]]
# Next Topic
[[Encryption Algorithms]]

The cryptographic key is the secret piece of information that is fed into the [[Encryption Algorithms]] to encrypt and decrypt the data. Without the key, the algorithm alone cannot get the data back.

In general, the ==🟠longer the key== the harder it is to crack, because there are far more possible combinations an attacker would have to try. ==🟡Symmetric keys are typically 128 bits or larger, while asymmetric keys have to be much larger, 3072 bits or more==. A longer key also means more work for the system though, so it is a trade-off between security and speed.

### Key Exchange
Symmetric encryption is very fast but has one problem, how do both sides get the same key without anyone else seeing it? If we send the key over the internet, an attacker could just grab it. There are a few ways to solve this:
1. ==🟠Out-of-band==: Share the key outside of the network entirely. ==🟢ex. Telling someone over the phone or handing it over in person== This works but is slow and does not scale.
2. ==🟠In-band==: Share the key over the network but protect it by encrypting it first, typically using [[Asymmetric Encryption]].

In reality, this is exactly how [[Transport Encryption]] works. Asymmetric encryption is used at the start to safely agree on a temporary symmetric key (a session key) and then that symmetric key is used to encrypt the rest of the data, giving us the security of asymmetric with the speed of symmetric.

If an organization needs someone else to hold on to private keys for them, we also have [[Key Escrow]].

# Previous Topic
[[Encryption Algorithms]]
# Previous Section
[[Encrypting Data]]
# Next Section
[[Key Exchange]]
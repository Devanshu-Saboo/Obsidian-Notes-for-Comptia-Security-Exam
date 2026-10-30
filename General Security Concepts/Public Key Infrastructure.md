This is a very broad term, but the focus this time is on creating, storing, distributing and revoking certificates that can help establish trust and verify identity to a certain degree. It also refers to the binding of public keys to people or devices, thus helping with identity, but it cannot be solely relied upon.

A way to understand this is with a passport. A government office checks who you are and then issues you a passport, and other countries trust it because they trust the office that issued it. In PKI, the office is the ==🟠Certificate Authority (CA)==, which checks the identity of a person or device and then issues a ==🟠digital certificate== that ties their public key to them. Anyone who trusts the CA can then trust the certificate.

The certificate can also be revoked if it is no longer trustworthy, for example if the private key was stolen, so the whole life of the certificate (creating, storing, distributing and revoking) is what PKI manages.

This is the base for the encryption topics that come next, starting with [[Symmetric Encryption]].

# Previous Section
[[Technical Change Management]]
# Next Topic
[[Symmetric Encryption]]
# Next Section
[[Encrypting Data]]

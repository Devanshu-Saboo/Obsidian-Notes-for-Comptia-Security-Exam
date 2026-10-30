This is the same as the [[Asymmetric Encryption]] mentioned earlier, only in this case your private keys are instead managed and owned by a 3rd party organization. This would be helpful in organizations where, even if a person were to leave the company, their encrypted data would still be accessible to the organization.

Without this, if the only copy of a private key is lost or an employee leaves, then all the data encrypted for them is gone forever. The 3rd party basically holds a spare copy of the key for emergencies.

This may also be used when 2 different organizations are working on a common task, where each organization would have a copy of the private key to be able to easily access the data that is required.

The downside is that now there is another place where the keys are kept, so it becomes a very attractive target for an attacker, and access to the escrowed keys has to be very tightly controlled. We have to also trust the 3rd party to look after them.

# Previous Topic
[[Asymmetric Encryption]]
# Previous Section
[[Public Key Infrastructure]]
# Next Section
[[Encrypting Data]]

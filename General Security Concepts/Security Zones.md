In Security Zones, security will be more than a one-to-one relationship between the user and the organization network. Instead of treating the whole network as one big space, we split it up into areas and decide which ones are allowed to talk to which.

For example, an organization can set up multiple zones inside the organization network, with some zones being ==🟠untrusted== such as trying to connect from the internet and certain zones being ==🟠trusted== such as when trying to connect from the internal company network while the physical location of the device is inside the organization premises.

Policies would be set up such that devices in an untrusted security zone would not be able to access data that is in a trusted security zone, and only trusted security zone devices may access internal zone traffic. ==🟢ex. Someone on the internet cannot reach the internal HR database directly, but an employee at their desk on the company network can.==

Trusted security zones can also be further split into smaller security zones via the addition of trunk switches and different VPN connections. This way, even if an attacker does get into one zone, they cannot freely move into the rest.

# Previous Topic
[[Policy Driven Access Control]]
# Previous Section
[[Zero Trust Framework]]
# Next Topic
[[Policy Enforcement Point (PEP)]]

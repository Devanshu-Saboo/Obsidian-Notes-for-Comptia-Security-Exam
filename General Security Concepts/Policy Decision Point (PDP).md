This is the software that will examine the data previously provided by the [[Policy Enforcement Point (PEP)]] and then finally take a decision on whether to grant, deny or revoke access for the device to the requested resources, relaying this decision back to the PEP.

Continuing the club example from the PEP, this is the manager who looks at what the bouncer found and makes the final call.

PDP is further split into 2 separate sections:
1. ==🟠Policy Engine==: This is responsible for the decision making inside the PDP based on the data collected by the PEP. It checks the data against the organization's policies.
2. ==🟠Policy Administrator==: This is responsible for relaying the decision made by the Policy Engine back to the PEP. This will also forward data, such as any credentials that were created for the device, through the PEP to the device.

So the full flow is: the device tries to connect, the PEP collects the data, the Policy Engine decides, the Policy Administrator passes the decision along and the PEP enforces it.

![[Zero Trust Diagram.png]]

# Previous Topic
[[Policy Enforcement Point (PEP)]]
# Previous Section
[[Zero Trust Framework]]
# Next Section
[[Physical Security]]

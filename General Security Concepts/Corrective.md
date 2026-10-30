Corrective control types are implemented when you wish to apply a control after an event has been detected, sometimes to keep the business running after a particular downtime.

This is commonly used in real production systems. When an attack has taken place but you cannot shut down the entire system to focus on the attack, a corrective control helps keep business operational while the attacker is isolated on the system and removed. ==🟢ex. Restoring data from a backup, Applying a patch to the vulnerability that was exploited, Isolating and removing malware from an infected machine, Reissuing credentials after an account was compromised==

The order I always think of is: [[Detective]] controls find the problem and Corrective controls then clean it up. The goal is to reduce the damage and get the organization back to normal as fast as possible.

It might get confusing with the next type, [[Compensating]]. A corrective control *fixes* the problem, whereas a compensating control only covers for it until a proper fix is ready.

![[Control Type Examples.png]]

# Previous Topic
[[Detective]]
# Previous Section
[[Security Control Types]]
# Next Topic
[[Compensating]]

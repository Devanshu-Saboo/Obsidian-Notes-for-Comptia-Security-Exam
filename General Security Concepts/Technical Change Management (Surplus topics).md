I am including the rest of the topics mentioned in the exam in this one page as none of them individually contain a lot of information.

### Restarts
After implementing a patch, it is common to restart the system to fully implement the patch. This could include things like the Operating System, particular services or even just signing every user out of the application and restarting it. ==🟢ex. A Windows update that is not complete until the computer reboots==

### Legacy Applications
There may be some applications that have been running since a long time ago which may no longer receive security patches from their developers, making it very risky to continue running them on the system as any attacker can gain access to the internal network using legacy systems. It is always advisable to replace such software as soon as possible and find proper workarounds for each of them. Until then, a [[Compensating]] control such as isolating the system can be used.

### Dependencies
If an application A cannot execute without application B first being installed, we call this a dependency. In IT we need to be very careful about such software, as whilst making changes to software B we must also ensure not to break software A. An example of this may be a firewall and a switch which operate on different devices, but you would still need to ensure any new firewall rules do not break the current switches routing packets through the network.

### Documentation
Required with each new update made to the system to transfer accurate knowledge ahead. This may also require updating diagrams mentioned in the documentation, policies, procedures, versions etc. If the documentation is out of date, the next person who has to fix the system will be working with the wrong information.

### Version Control
Simply tracking the versions of the software in which the business can proceed as intended. This not only includes software but also Operating System versions, router or switch configurations, firewall rules etc.

It is also a good idea to take a snapshot of the system in its optimal working state, to ensure that if anything breaks it is easy to revert to the old system when it was still at full capacity. This ties directly back to the backout plan from [[Change Approval Process Steps (detailed)]].

# Previous Topic
[[Technical Change Management Downtime]]
# Previous Section
[[Technical Change Management]]
# Next Section
[[Public Key Infrastructure]]

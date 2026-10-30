In the previous section we talked about changes from the client side, lets take a look at it from the IT department side, who actually have to implement these changes.

Firstly, on the technical side we have ==🟠allow lists== and ==🟠deny lists==. These are simply lists of applications that you may or may not install. These decisions are taken based on various factors such as the version of the software, as some versions are vulnerable and can be easily attacked by a threat actor.

There are two ways to use them, the allow list direction or the deny list direction. In the allow list direction, only software that has been approved by the IT team may be installed, whereas in the deny list direction, every piece of software can be installed and used other than the software that the IT team has blacklisted by adding it to the deny list.

Each direction has a trade-off:
1. ==🟠Allow list==: Much more secure, since anything unknown is blocked by default, but it takes more effort for IT to maintain and can slow people down when they need new software
2. ==🟠Deny list==: Much easier to run and more flexible, but an attacker's new or unknown program will be allowed to run since it is not on the list yet

In the rest of this section we look at how the actual change is carried out, starting with its [[Technical Change Management Scope]].

# Previous Section
[[Change Management]]
# Next Topic
[[Technical Change Management Scope]]
# Next Section
[[Public Key Infrastructure]]

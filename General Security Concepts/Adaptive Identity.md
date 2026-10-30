This is an addition on the earlier mentioned [[Zero Trust Framework]]. In zero trust we authenticate the device at every step, even after it passes through the firewall connecting the internet and the organization network.

In Adaptive Identity, we collect and consider even more information such as ==🟢physical location of the device, IP address of the device, the type of connection etc.== The idea is that the same person might be trusted a lot in one situation and much less in another.

For example, if an employee normally logs in from their office laptop and suddenly there is a login with their credentials from a different country on a public Wi-Fi network, the system will see this as unusual.

Depending on the data collected from the above mentioned sources, if the system still flags the user as a risk it may attempt to authenticate the user with even more tests, such as an OTP (One Time Password) using an authenticator app such as Microsoft or Google Authenticator.

# Previous Topic
[[Control Plane]]
# Previous Section
[[Zero Trust Framework]]
# Next Topic
[[Threat Scope Reduction]]

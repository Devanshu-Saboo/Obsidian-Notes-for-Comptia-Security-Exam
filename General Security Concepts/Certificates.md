We use certificates to provide trust when we are accessing other devices or services. This builds on the [[Public Key Infrastructure]] note, where I mentioned that PKI is about creating, storing, distributing and revoking certificates.

A ==🟠digital certificate== is simply a file that contains a public key and a digital signature (see [[Hashing and Digital Signatures]]), along with information about who the certificate belongs to. They follow the X.509 standard, which is why they all have the same format.

### Certificate Authority (CA)
Imagine I connect to a random website. I have no way to know if it can be trusted. So instead of trusting every website individually, I trust a ==🟠Certificate Authority== and the CA signs the certificate of the website. If I trust the CA, I trust the site. Browsers and operating systems already come with a list of CAs that they trust.

The process to get a certificate looks like this:
1. The server creates a public and private key pair
2. It then makes a ==🟠CSR (Certificate Signing Request)==, which contains the public key and the identifying information that needs to be bound to it
3. The CSR is sent to the CA, which validates who is asking
4. The CA signs the certificate with its own private key and sends it back
5. The server now presents this certificate to anyone who connects, who can verify it using the CA's public key

### Types of Certificates
1. ==🟠Third-party certificates==: Signed by a public CA that everyone already trusts. We have to pay for these, in a way we are buying trust.
2. ==🟠Self-signed certificates==: Signed by the same entity that it certifies. Companies use these internally, since the only ones who need to trust the certificate are their own devices and so there is no need to buy trust from a public CA. They are not trusted by the outside world, and browsers will show a warning for them. A company can also run its own internal CA and set up its devices to trust it.
3. ==🟠Wildcard certificates==: One certificate that covers all of the subdomains of a domain. ==🟢ex. *.professormesser.com covers every server name under professormesser.com==. These make use of the ==🟠SAN (Subject Alternative Name)==, which is a field in the certificate that lists additional names that the certificate is valid for.

Certificates are usually signed by an intermediate CA rather than the root CA, so there is a chain of trust going from the website's certificate, up through the intermediate CA, to the root CA that our device already trusts. The ==🟠root of trust== is that top level which everything else depends on.

### Key Revocation
Sometimes a certificate has to be cancelled before it expires, for example if the private key was stolen. There are 3 ways for a device to check this:
1. ==🟠CRL (Certificate Revocation List)==: A list from the CA of all the certificates that have been revoked. The device has to download and check the list.
2. ==🟠OCSP (Online Certificate Status Protocol)==: Instead of downloading a whole list, the device asks the CA about one certificate (using its serial number) and gets a response back right away. The problem is that the CA has to answer every client's request, which may not scale well.
3. ==🟠OCSP stapling==: The server asks the CA for its own status and then "staples" the signed response to its certificate when a client connects. The CA no longer has to answer every client and the client gets the answer immediately.

> [!joke] A self-signed certificate is like writing yourself a reference letter. It might be perfectly true, but don't expect strangers to accept it.

# Previous Topic
[[Blockchain Technology]]
# Previous Section
[[Encrypting Data]]
# Next Section
%% Add the next video's note here %%

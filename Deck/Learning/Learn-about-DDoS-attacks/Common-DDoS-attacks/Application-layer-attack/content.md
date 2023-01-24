##

What is an Application Layer DDoS attack?
Application layer attacks or layer 7 (L7) DDoS attacks refer to a type of malicious behavior designed to target the “top” layer in the OSI model where common internet requests such as HTTP GET and HTTP POST occur. These layer 7 attacks, in contrast to network layer attacks such as DNS Amplification, are particularly effective due to their consumption of server resources in addition to network resources.

How do application layer attacks work?
The underlying effectiveness of most DDoS attacks comes from the disparity between the amount of resources it takes to launch an attack relative to the amount of resources it takes to absorb or mitigate one. While this is still the case with L7 attacks, the efficiency of affecting both the targeted server and the network requires less total bandwidth to achieve the same disruptive effect; an application layer attack creates more damage with less total bandwidth.

To explore why this is the case, let's take a look at the difference in relative resource consumption between a client making a request and a server responding to the request. When a user sends a request logging into an online account such as a Gmail account, the amount of data and resources the user’s computer must utilize are minimal and disproportionate to the amount of resources consumed in the process of checking login credentials, loading the relevant user data from a database, and then sending back a response containing the requested webpage.

Even in the absence of a login, many times a server receiving a request from a client must make database queries or other API calls in order to produce a webpage. When this disparity is magnified as a result of many devices targeting a single web property like during a botnet attack, the effect can overwhelm the targeted server, resulting in denial-of-service to legitimate traffic. In many cases simply targeting an API with a L7 attack is enough to take the service offline.

Why is it difficult to stop application layer DDoS attacks?
Distinguishing between attack traffic and normal traffic is difficult, especially in the case of an application layer attack such as a botnet performing an HTTP Flood attack against a victim’s server. Because each bot in a botnet makes seemingly legitimate network requests the traffic is not spoofed and may appear “normal” in origin.

Application layer attacks require an adaptive strategy including the ability to limit traffic based on particular sets of rules, which may fluctuate regularly. Tools such as a properly configured WAF can mitigate the amount of bogus traffic that is passed on to an origin server, greatly diminishing the impact of the DDoS attempt.

With other attacks such as SYN floods or reflection attacks such as NTP amplification, strategies can be used to drop the traffic fairly efficiently provided the network itself has the bandwidth to receive them. Unfortunately, most networks cannot receive a 300Gbps amplification attack, and even fewer networks can properly route and serve the volume of application layer requests an L7 attack can generate.

What tactics help mitigate application layer attacks?
One method is to implement a challenge to the device making the network request in order to test whether or not it is a bot. This is done through a test much like the CAPTCHA test commonly found when creating an account online. By giving a requirement such as a JavaScript computational challenge, many attacks can be mitigated.

Other avenues for stopping HTTP floods include the use of a web application firewall, managing and filtering traffic through an IP reputation database, and through on-the-fly network analysis by engineers.

Having the advantage of scale with millions of users on our network, Cloudflare has the ability to analyze traffic from a variety of sources, mitigating potential attacks with constantly updated WAF rules and other mitigation strategies, often before they occur or have a chance to retarget others. Explore Cloudflare's DDoS advanced protection services.
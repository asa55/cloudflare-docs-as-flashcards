##

What are DoS and DDoS attacks?
Denial-of-service (DoS) and distributed denial-of-service (DDoS) attacks are malicious attempts to disrupt the normal operations of a targeted server, service, or network by overwhelming it with a flood of Internet traffic.

DoS attacks accomplish this disruption by sending malicious traffic from a single machine — typically a computer. They can be very simple; a basic ping flood attack can be accomplished by sending more ICMP (ping) requests to a targeted server than it is able to process and respond to efficiently.

DDoS attacks, meanwhile, use more than one machine to send malicious traffic to their target. Often, these machines are part of a botnet — a collection of computers or other devices that have been infected with malware and can thus be controlled remotely by an individual attacker. In other circumstances, multiple individual attackers launch DDoS attacks by working together to send traffic from their individual computers.

DDoS attacks are more prevalent and damaging in the modern Internet for two reasons. First, modern security tools have evolved to stop some ordinary DoS attacks. Second, DDoS attack tools have become relatively cheap and easy to operate.

How are DoS/DDoS attack tools categorized?
A number of tools exist that can be adapted to launch DoS/DDoS attacks, or are explicitly designed for that purpose. The former category are often ““stressors”” — tools with the stated purpose of helping security researchers and network engineers perform stress tests against their own networks, but which can also be used to perform genuine attacks.

Some are specialized and only focus on a particular layer of the OSI model, while others are designed to allow for multiple attack vectors. Categories of attack tools include:

Low and slow attack tools
As the name implies, these types of attack tools use a low volume of data and operate very slowly. Designed to send small amounts of data across multiple connections in order to keep ports on a targeted server open as long as possible, these tools continue to take up the server's resources until it is unable to maintain additional connections. Uniquely, low and slow attacks may at times be effective even when not using a distributed system such as a botnet and are commonly used by a single machine.

Application layer (L7) attack tools
These tools target layer 7 of the OSI model, where Internet-based requests such as HTTP occur. Using an HTTP flood attack to overwhelm a target with HTTP GET and POST requests, a malicious actor can launch attack traffic that is difficult to distinguish from normal requests made by actual visitors.

Protocol and transport layer (L3/L4) attack tools
Going further down the protocol stack, these tools utilize protocols like UDP to send large volumes of traffic to a targeted server, such as during a UDP flood. While often ineffective individually, these attacks are typically found in the form of DDoS attacks where the benefit of additional attacking machines increases the effect.

What are commonly used DoS/DDoS attack tools?
Some commonly used tools include:

Low Orbit Ion Cannon (LOIC)
The LOIC is an open-source stress testing application. It allows for both TCP and UDP protocol layer attacks to be carried out using a user-friendly WYSIWYG interface. Due to the popularity of the original tool, derivatives have been created that allow attacks to be launched using a web browser.

High Orbit Ion Cannon (HOIC)
This attack tool was created to replace the LOIC by expanding its capabilities and adding customizations. Using the HTTP protocol, the HOIC is able to launch targeted attacks that are difficult to mitigate. The software is designed to have a minimum of 50 people working together in a coordinated attack effort.

Slowloris
Slowloris is an application designed to instigate a low and slow attack on a targeted server. It needs a relatively limited amount of resources in order to create a damaging effect.

R.U.D.Y (R-U-Dead-Yet)
R.U.D.Y. is another low and slow attack tool designed to allow the user to easily launch attacks using a simple point-and-click interface. By opening multiple HTTP POST requests and then keeping those connections open as long as possible, the attack aims to slowly overwhelm the targeted server.

How can I defend against DoS/DDoS tools?
Since DoS and DDoS attacks take a variety of forms, mitigating them requires a variety of tactics. Common tactics for stopping DDoS attacks include:

Rate limiting: Limiting the number of requests a server will accept over a certain time window
Web application firewalls: Tools that filter web traffic based on a series of rules
Anycast network diffusion: Placing a large, distributed cloud network between a server and incoming traffic, providing additional computing resources with which to respond to requests.
Cloudflare applies all of these strategies and more to defend against the largest, most complex DoS and DDoS attacks. Learn more about Cloudflare's DDoS protection and how it works.
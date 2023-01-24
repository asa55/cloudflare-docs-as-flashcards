##

What are layer 3 DDoS attacks?
A distributed denial-of-service (DDoS) attack attempts to overwhelm its target with large amounts of data. A DDoS attack is like a traffic jam clogging up a freeway, preventing regular traffic from reaching its destination.

Layer 3 DDoS attacks target layer 3 (L3) in the OSI model. Like all DDoS attacks, the goal of a layer 3 attack is to slow down or crash a program, service, computer, or network, or to fill up capacity so that no one else can receive service. L3 DDoS attacks typically accomplish this by targeting network equipment and infrastructure.

There are a few important differences between layer 3 DDoS attacks and attacks at the higher layers:

Layer 3 attacks target the network layer, not transport layer or application layer processes (as layer 4 and layer 7 DDoS attacks do)
Layer 3 attacks do not have to open a TCP connection with the target first
Layer 3 attacks do not target a specific port
What is the OSI model?
The OSI model is a conceptual model of how the Internet works. The main goals of the OSI model are to help people talk about networking equipment and protocols, determine which protocols are used by which software and hardware, and show how the Internet can function regardless of the underlying hardware.

The OSI model divides the different technologies that make the Internet work into layers. There are seven layers in total:

OSI Model
What is layer 3 in the OSI model?
OSI layer 3 is called the network layer. Layer 3 comprises the protocols and technologies that make interconnected networks – in other words, the Internet – possible. This layer is where routing across networks takes place. Data that traverses networks is divided into packets, and these packets are addressed and sent to their destinations at layer 3. The most important protocol for this process is the Internet Protocol (IP).

Protocols at layer 3 do not open connections, ensure reliable data delivery, or indicate which service on the targeted device should use the data; those are layer 4 processes. Layer 4 involves the use of transport protocols like TCP and UDP. Sending packets across networks without a layer 4 transport protocol is like mailing a letter to an address without making sure that the address is correct, including the name of a specific person at that address who should open the letter, or using a reputable postal delivery service. The data may arrive, or it may not. This is why many layer 3 protocols are always used in conjunction with a layer 4 transport protocol that ensures the data goes to the right place.

However, it is still possible to send data packets to a network destination over IP without the use of a transport protocol.

As layer 3 is connectionless, layer 3 DDoS attacks do not need to open a connection via TCP or indicate port assignments. Layer 3 DDoS attacks target the network software a computer is running instead of a specific port.

What are the protocols used for layer 3?
These are the most widely used layer 3 protocols, and the ones most likely to be used in a DDoS attack:

IP: The Internet Protocol (IP) routes and addresses packets of data so that they arrive at the correct destination. Every device that connects to the Internet has an IP address, and the IP protocol attaches the correct IP address to each data packet – like addressing a letter to someone.

IPsec: IPsec is actually a suite of several protocols, not a single protocol. IPsec is the encrypted version of IP used by VPNs, similar to the difference between HTTPS and HTTP.

ICMP: The Internet Control Message Protocol (ICMP) handles error reports and testing. A connectionless protocol, ICMP does not use a transport protocol like TCP or UDP. Rather, ICMP packets are sent over IP alone. Developers and networking engineers use ICMP for its ping and traceroute functions. Typically only one ICMP packet needs to be sent at a time.

Other layer 3 protocols include:

IGMP: The Internet Group Message Protocol manages IP multicast groups, enabling multiple devices within a network to receive the same IP traffic.
ARP: The Address Resolution Protocol is for use within a single network only. Computers use this protocol to map IP addresses to MAC addresses within the network (a MAC address is a unique identifier hardwired into every Internet-capable device, like a fingerprint).
Attacks are theoretically possible using any of these protocols. ICMP is commonly used to flood a server with too many pings to respond to, or with one large ping packet that crashes the receiving device (this is known as the "ping of death"). Attackers can use IPsec to flood the target with junk data or overly large security certificates.

However, not all of these protocols are practical for DDoS attacks, and some types of attacks are made impossible by hardware updates. For example, ARP only operates within a local network, so an attacker would first need to connect to the local network before carrying out the DDoS attack. And ICMP ping of death attacks are not possible with modern hardware, which ignores IP packets that are too large.

How do L3 DDoS attacks work?
As with other types of DDoS attacks, the attacker sends a large volume of junk network traffic via these protocols. There are various methods for doing this, depending on the protocol. The junk traffic gets in the way of legitimate user requests, slowing down responses to them or blocking them altogether. Sometimes there is so much junk data that it overwhelms the target's resources, and the target crashes.

What are some well-known types of layer 3 DDoS attacks?
While other attacks are possible, including attacks over IP alone, ICMP-based attacks are the most common. Well-known ICMP attacks include:

Ping flood: In a ping flood DDoS attack, the attacker sends thousands or even millions of ping requests to a server at once.
Smurf attack: ICMP has no security or verification measures in place, making it possible for an attacker to spoof an IP address in an ICMP request. In a Smurf DDoS attack, the attacker sends out ping requests to thousands of servers, spoofing the target's IP address in the ping requests so that the responses go to the target, not the attacker. Most modern networking hardware is no longer vulnerable to this attack.
Ping of death: In an ICMP ping of death attack, an attacker sends a ping request that is larger than the maximum allowable size to the target. Routers along the way to the target will fragment the ping into smaller packets, so that the target accepts them, but when it tries to reassemble the large packet from the smaller fragments, the packet size exceeds the maximum and crashes the target. Modern devices are not vulnerable to this attack.
How does Cloudflare protect against layer 3 DDoS attacks?
In addition to blocking DDoS attacks at layers 4 and 7, Cloudflare mitigates layer 3 DDoS attacks. Cloudflare Magic Transit is designed specifically to stop attacks on internal network infrastructure, including DDoS attacks at any layer. The Cloudflare WAF and CDN also stop layer 3 DDoS attacks by only accepting traffic to HTTP and HTTPS ports – these are layer 7 only.

What is layer 3 in the TCP/IP model?
The TCP/IP model is an alternative model of how networking works. Instead of seven layers, the TCP/IP model has four:

Application Layer (corresponds to layers 5-7 in the OSI model)
Transport Layer (corresponds to layer 4 in the OSI model)
Internet Layer (corresponds to layer 3 in the OSI model)
Network Access/Link Layer (corresponds to layers 1-2 in the OSI model)
Referencing the TCP/IP model instead of the OSI model, layer 3 DDoS attacks would be called layer 2 DDoS attacks.
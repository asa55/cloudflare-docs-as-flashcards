##

What is a ping of death attack?
A Ping of death (PoD) attack is a denial-of-service (DoS) attack, in which the attacker aims to disrupt a targeted machine by sending a packet larger than the maximum allowable size, causing the target machine to freeze or crash. The original ping of death attack is less common today. A related attack known as an ICMP flood attack is more prevalent.

How does a ping of death attack work?
An Internet Control Message Protocol (ICMP) echo-reply message or “ping”, is a network utility used to test a network connection, and it works much like sonar – a “pulse” is sent out and the “echo” from that pulse tells the operator information about the environment. If the connection is working, the source machine receives a reply from the targeted machine.

While some ping packets are very small, IP4 ping packets are much larger, and can be as large as the maximum allowable packet size of 65,535 bytes. Some TCP/IP systems were never designed to handle packets larger than the maximum, making them vulnerable to packets above that size.

Ping of Death DDoS Attack
When a maliciously large packet is transmitted from the attacker to the target, the packet becomes fragmented into segments, each of which is below the maximum size limit. When the target machine attempts to put the pieces back together, the total exceeds the size limit and a buffer overflow can occur, causing the target machine to freeze, crash or reboot.

While ICMP echo can be used for this attack, anything that sends an IP datagram can be used for this exploit. That includes TCP, UDP and IPX transmissions.

How is a ping of death DDoS attack mitigated?
One solution to stop an attack is to add checks to the reassembly process to make sure the maximum packet size constraint will not be exceeded after packet recombination. Another solution is to create a memory buffer with enough space to handle packets which exceed the guideline maximum.

The original Ping of Death attack has mostly gone the way of the dinosaurs; devices created after 1998 are generally protected against this type of attack. Some legacy equipment may still be vulnerable. A new Ping of Death attack for IPv6 packets for Microsoft Windows was discovered more recently, and it was patched in mid 2013. Cloudflare DDoS Protection mitigates Ping of Death attacks by dropping malformed packets before they reach the targeted host computer.
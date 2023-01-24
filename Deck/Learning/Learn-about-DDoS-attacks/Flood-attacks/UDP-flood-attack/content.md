##

What is a UDP flood attack?
A UDP flood is a type of denial-of-service attack in which a large number of User Datagram Protocol (UDP) packets are sent to a targeted server with the aim of overwhelming that device’s ability to process and respond. The firewall protecting the targeted server can also become exhausted as a result of UDP flooding, resulting in a denial-of-service to legitimate traffic.

How does a UDP flood attack work?
A UDP flood works primarily by exploiting the steps that a server takes when it responds to a UDP packet sent to one of it’s ports. Under normal conditions, when a server receives a UDP packet at a particular port, it goes through two steps in response:

The server first checks to see if any programs are running which are presently listening for requests at the specified port.
If no programs are receiving packets at that port, the server responds with a ICMP (ping) packet to inform the sender that the destination was unreachable.
A UDP flood can be thought of in the context of a hotel receptionist routing calls. First, the receptionist receives a phone call where the caller asks to be connected to a specific room. The receptionist then needs to look through the list of all rooms to make sure that the guest is available in the room and willing to take the call. Once the receptionist realizes that the guest is not taking any calls, they have to pick the phone back up and tell the caller that the guest will not be taking the call. If suddenly all the phone lines light up simultaneously with similar requests then they will quickly become overwhelmed.

DDoS bot traffic metaphor
As each new UDP packet is received by the server, it goes through steps in order to process the request, utilizing server resources in the process. When UDP packets are transmitted, each packet will include the IP address of the source device. During this type of DDoS attack, an attacker will generally not use their own real IP address, but will instead spoof the source IP address of the UDP packets, impeding the attacker’s true location from being exposed and potentially saturated with the response packets from the targeted server.

As a result of the targeted server utilizing resources to check and then respond to each received UDP packet, the target’s resources can become quickly exhausted when a large flood of UDP packets are received, resulting in denial-of-service to normal traffic.

UDP flood DDoS attack animation
How is a UDP flood attack mitigated?
Most operating systems limit the response rate of ICMP packets in part to disrupt DDoS attacks that require ICMP response. One drawback of this type of mitigation is that during an attack legitimate packets may also be filtered in the process. If the UDP flood has a volume high enough to saturate the state table of the targeted server’s firewall, any mitigation that occurs at the server level will be insufficient as the bottleneck will occur upstream from the targeted device.

How does Cloudflare mitigate UDP Flood attacks?
In order to mitigate UDP attack traffic before it reaches its target, Cloudflare drops all UDP traffic not related to DNS at the network edge. Because Cloudflare’s Anycast network scatters web traffic across many Data Centers, we have sufficient capacity to handle UDP flood attacks of any size. Learn more about Cloudflare DDoS Protection.
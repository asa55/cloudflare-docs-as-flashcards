##

What is a SSDP DDoS Attack?
A Simple Service Discovery Protocol (SSDP) attack is a reflection-based distributed denial-of-service (DDoS) attack that exploits Universal Plug and Play (UPnP) networking protocols in order to send an amplified amount of traffic to a targeted victim, overwhelming the target’s infrastructure and taking their web resource offline.

Here is a free tool to check to see if your public IP has any exposed SSDP devices: check SSDP DDoS vulnerability.

How does a SSDP Attack work?
SSDP DDoS Attack
Under normal circumstances, the SSDP protocol is used to allow UPnP devices to broadcast their existence to other devices on the network. For example, when a UPnP printer is connected to a typical network, after it receives an IP address, the printer is able to advertise its services to computers on the network by sending a message to a special IP address called a multicast address. The multicast address then tells all the computers on the network about the new printer. Once a computer hears the discovery message about the printer, it makes a request to the printer for a complete description of its services. The printer then responds directly to that computer with a complete list of everything it has to offer. An SSDP attack exploits that final request for services by asking the device to respond to the targeted victim.

Here are the 6 steps of a typical SSDP DDoS attack:
First the attacker conducts a scan looking for plug-and-play devices that can be utilized as amplification factors.
As the attacker discovers networked devices, they create a list of all the devices that respond.
The attacker creates a UDP packet with the spoofed IP address of the targeted victim.
The attacker then uses a botnet to send a spoofed discovery packet to each plug-and-play device with a request for as much data as possible by setting certain flags, specifically ssdp:rootdevice or ssdp:all.
As a result, each device will send a reply to the targeted victim with an amount of data up to about 30 times larger than the attacker’s request.
The target then receives a large volume of traffic from all the devices and becomes overwhelmed, potentially resulting in denial-of-service to legitimate traffic.
How is a SSDP Attack mitigated?
For network administrators, a key mitigation is to block incoming UDP traffic on port 1900 at the firewall. Provided the volume of traffic isn’t enough to overwhelm the network infrastructure, filtering traffic from this port will likely be able to mitigate such an attack. For a deeper dive on SSDP attacks and more mitigation strategies, explore technical details about an SSDP attack.

Do you want to know if you have a vulnerable SSDP service that can be used in a DDoS attack? As mentioned before, we’ve created a free tool to check to see if your public IP has any exposed SSDP devices. To check for a SSDP DDoS vulnerability, you can use this free tool.

How does Cloudflare mitigate SSDP attacks?
Cloudflare eliminates SSDP attacks by stopping all the attack traffic before it reaches it’s target; UDP packets targeting Port 1900 are not be proxied to the origin server, and the load for receiving the initial traffic falls on Cloudflare’s network. We offer full protection from SSDP and other layer 3 amplification attacks.

Although the attack will target a single IP address, our Anycast network will scatter all attack traffic to the point where it is no longer disruptive. Cloudflare is able to use our advantage of scale to distribute the weight of the attack across many Data Centers, balancing the load so that service is never interrupted and the attack never overwhelms the targeted server’s infrastructure. During a recent six-month window, our DDoS mitigation system "Gatebot" detected 6,329 simple reflection attacks (that's one every 40 minutes), and the network successfully mitigated all of them. Learn more about Cloudflare's DDoS Protection.
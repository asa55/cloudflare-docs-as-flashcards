##

What is a Smurf attack?
A Smurf attack is a distributed denial-of-service (DDoS) attack in which an attacker attempts to flood a targeted server with Internet Control Message Protocol (ICMP) packets. By making requests with the spoofed IP address of the targeted device to one or more computer networks, the computer networks then respond to the targeted server, amplifying the initial attack traffic and potentially overwhelming the target, rendering it inaccessible. This attack vector is generally considered a solved vulnerability and is no longer prevalent.

How does a Smurf attack work?
While ICMP packets can be utilized in a DDoS attack, normally they serve valuable functions in network administration. The ping application, which utilizes ICMP packets, is used by network administrators to test networked hardware devices such as computers, printers or routers. A ping is commonly used to see if a device is operational, and to track the amount of time it takes for the message to go round trip from the source device to the target and back to the source. Unfortunately, because the ICMP protocol does not include a handshake, hardware devices receiving requests are unable to verify if the request is legitimate.

This type of DDoS attack can be thought of metaphorically as a prankster calling an office manager and pretending to be the company’s CEO. The prankster asks the manager to tell each employee to call the executive back on his private number and give him an update on how they’re doing. The prankster gives the callback number of a targeted victim, who then receives as many unwanted phone calls as there are people in the office.

Here's how a Smurf attack works:
First the Smurf malware builds a spoofed packet that has its source address set to the real IP address of the targeted victim.
The packet is then sent to an IP broadcast address of a router or firewall, which in turn sends requests to every host device address inside the broadcasting network, increasing the number of requests by the number of networked devices on the network.
Each device inside the network receives the request from the broadcaster and then responds to the spoofed address of the target with an ICMP Echo Reply packet.
The target victim then receives a deluge of ICMP Echo Reply packets, potentially becoming overwhelmed and resulting in denial-of-service to legitimate traffic.
How can a Smurf attack be mitigated?
Several mitigation strategies for this attack vector have been developed and implemented over the years, and the exploit is largely considered solved. On a limited number of legacy systems, mitigation techniques may still need to be applied. A simple solution is to disable IP broadcasting addresses at each network router and firewall. Older routers are likely to enable broadcasting by default, while newer routers will likely already have it disabled. In the event that a Smurf attack occurs, Cloudflare eliminates the attack traffic by preventing the ICMP packets from reaching the targeted origin server. Learn more about how Cloudflare's DDoS Protection works.
##

What is an IP stresser?
An IP stresser is a tool designed to test a network or server for robustness. The administrator may run a stress test in order to determine whether the existing resources (bandwidth, CPU, etc.) are sufficient to handle additional load.

Testing one’s own network or server is a legitimate use of a stresser. Running it against someone else’s network or server, resulting in denial-of-service to their legitimate users, is illegal in most countries.

What are booter services?
Booters, also known as booter services, are on-demand DDoS (Distributed-Denial-of-Service) attack services offered by enterprising criminals in order to bring down websites and networks. In other words, booters are the illegitimate use of IP stressers.

Illegal IP stressers often obscure the identity of the attacking server by use of proxy servers. The proxy reroutes the attacker’s connection while masking the IP address of the attacker.

Booters are slickly packaged as SaaS (Software-as-a-Service), often with email support and YouTube tutorials. Packages may offer a one-time service, multiple attacks within a defined period, or even “lifetime” access. A basic, one-month package can cost as little as $19.99. Payment options may include credit cards, Skrill, PayPal or Bitcoin (though PayPal will cancel accounts if malicious intent can be proved).

How are IP booters different from botnets?
A botnet is a network of computers whose owners are unaware that their computers have been infected with malware and are being used in Internet attacks. Booters are DDoS-for-hire services.

Booters traditionally used botnets to launch attacks, but as they get more sophisticated, they are boasting of more powerful servers to, as some booter services put it, “help you launch your attack”.

What are the motivations behind denial-of-service attacks?
The motivations behind denial-of-service attacks are many: skiddies* fleshing out their hacking skills, business rivalries, ideological conflicts, government-sponsored terrorism, or extortion. PayPal and credit cards are the preferred methods of payment for extortion attacks. Bitcoin is also in use is because it offers the ability to disguise identity. One disadvantage of Bitcoin, from the attackers’ point of view, is that fewer people use bitcoins compared to other forms of payment.

*Script kiddie, or skiddie, is a derogatory term for relatively low-skilled Internet vandals who employ scripts or programs written by others in order to launch attacks on networks or websites. They go after relatively well-known and easy-to-exploit security vulnerabilities, often without considering the consequences.

What are amplification and reflection attacks?
Reflection and amplification attacks make use of legitimate traffic in order to overwhelm the network or server being targeted.

When an attacker forges the IP address of the victim and sends a message to a third party while pretending to be the victim, it is known as IP address spoofing. The third party has no way of distinguishing the victim’s IP address from that of the attacker. It replies directly to the victim. The attacker’s IP address is hidden from both the victim and the third-party server. This process is called reflection.

This is akin to the attacker ordering pizzas to the victim’s house while pretending to be the victim. Now the victim ends up owing money to the pizza place for a pizza they didn’t order.

Traffic amplification happens when the attacker forces the third-party server to send back responses to the victim with as much data as possible. The ratio between the sizes of response and request is known as the amplification factor. The greater this amplification, the greater the potential disruption to the victim. The third-party server is also disrupted because of the volume of spoofed requests it has to process. NTP Amplification is one example of such an attack.

The most effective types of booter attacks use both amplification and reflection. First, the attacker fakes the target’s address and sends a message to a third party. When the third party replies, the message goes to the faked address of target. The reply is much bigger than the original message, thereby amplifying the size of the attack.

The role of a single bot in such an attack is akin to that of a malicious teenager calling a restaurant and ordering the entire menu, then requesting a callback confirming every item on the menu. Except, the callback number is that of the victim’s. This results in the targeted victim receiving a call from the restaurant with a flood of information they didn’t request.

What are the categories of denial-of-service attacks?
Application Layer Attacks go after web applications, and often use the most sophistication. These attacks exploit a weakness in the Layer 7 protocol stack by first establishing a connection with the target, then exhausting server resources by monopolizing processes and transactions. These are hard to identify and mitigate. A common example is a HTTP Flood attack.

Protocol Based Attacks focus on exploiting a weakness in Layers 3 or 4 of the protocol stack. Such attacks consume all the processing capacity of the victim or other critical resources (a firewall, for example), resulting in service disruption. Syn Flood and Ping of Death are some examples.

Volumetric Attacks send high volumes of traffic in an effort to saturate a victim’s bandwidth. Volumetric attacks are easy to generate by employing simple amplification techniques, so these are the most common forms of attack. UDP Flood, TCP Flood, NTP Amplification and DNS Amplification are some examples.

What are common denial-of-service attacks?
The goal of DoS or DDoS attacks is to consume enough server or network resources so that the system becomes unresponsive to legitimate requests:

SYN Flood: A succession of SYN requests is directed to the target's system in an attempt to overwhelm it. This attack exploits weaknesses in the TCP connection sequence, known as a three-way handshake.
HTTP Flood: A type of attack in which HTTP GET or POST requests are used to attack the web server.
UDP Flood: A type of attack in which random ports on the target are overwhelmed by IP packets containing UDP datagrams.
Ping of Death: Attacks involve the deliberate sending of IP packets larger than those allowed by the IP protocol. TCP/IP fragmentation deals with large packets by breaking them down into smaller IP packets. If the packets, when put together, are larger than the allowable 65,536 bytes, legacy servers often crash. This has largely been fixed in newer systems. Ping flood is the present-day incarnation of this attack.
ICMP Protocol Attacks: Attacks on the ICMP protocol take advantage of the fact that each request requires processing by the server before a response is sent back. Smurf attack, ICMP flood, and ping flood take advantage of this by inundating the server with ICMP requests without waiting for the response.
Slowloris: Invented by Robert 'RSnake' Hansen, this attack tries to keep multiple connections to the target web server open, and for as long as possible. Eventually, additional connection attempts from clients will be denied.
DNS Flood: The attacker floods a particular domain’s DNS servers in an attempt to disrupt DNS resolution for that domain
Teardrop Attack: The attack that involves sending fragmented packets to the targeted device. A bug in the TCP/IP protocol prevents the server from reassembling such packets, causing the packets to overlap. The targeted device crashes.
DNS Amplification: This reflection-based attack turns legitimate requests to DNS (domain name system) servers into much larger ones, in the process consuming server resources.
NTP Amplification: A reflection-based volumetric DDoS attack in which an attacker exploits a Network Time Protocol (NTP) server functionality in order to overwhelm a targeted network or server with an amplified amount of UDP traffic.
SNMP Reflection: The attacker forges the victim’s IP address and blasts multiple Simple Network Management Protocol (SNMP) requests to devices. The volume of replies can overwhelm the victim.
SSDP: An SSDP (Simple Service Discovery Protocol) attack is a reflection-based DDoS attack that exploits Universal Plug and Play (UPnP) networking protocols in order to send an amplified amount of traffic to a targeted victim.
Smurf Attack: This attack uses a malware program called smurf. Large numbers of Internet Control Message Protocol (ICMP) packets with the victim's spoofed IP address are broadcast to a computer network using an IP broadcast address.
Fraggle Attack: An attack similar to smurf, except it uses UDP rather than ICMP.
What should be done in case of a DDoS extortion attack?
The data center and ISP should be immediately informed
Ransom payment should never be an option - a payment often leads to escalating ransom demands
Law enforcement agencies should be notified
Network traffic should be monitored
Reach out to DDoS protection plans, such as Cloudflare’s free-of-charge plan
How can botnet attacks be mitigated?
Firewalls should be installed on the server
Security patches must be up to date
Antivirus software must be run on schedule
System logs should be regularly monitored
Unknown email servers should not be allowed to distribute SMTP traffic
Why are booter services hard to trace?
The person buying these criminal services uses a frontend website for payment, and instructions relating to the attack. Very often there is no identifiable connection to the backend initiating the actual attack. Therefore, criminal intent can be hard to prove. Following the payment trail is one way to track down criminal entities.
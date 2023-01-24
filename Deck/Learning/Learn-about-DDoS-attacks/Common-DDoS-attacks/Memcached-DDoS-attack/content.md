##

What is a memcached DDoS attack?
A memcached distributed denial-of-service (DDoS) attack is a type of cyber attack in which an attacker attempts to overload a targeted victim with internet traffic. The attacker spoofs requests to a vulnerable UDP memcached* server, which then floods a targeted victim with internet traffic, potentially overwhelming the victim’s resources. While the target’s internet infrastructure is overloaded, new requests cannot be processed and regular traffic is unable to access the internet resource, resulting in denial-of-service.

*Memcached is a database caching system for speeding up websites and networks.

Cloudflare Memcached Traffic Map
Here are data centers in Cloudflare’s global network and the relative amount of memcached attack traffic they received during a recent attack.

How does a memcached attack work?
A Memcached attacks operates similarly to all DDoS amplification attacks such as NTP amplification and DNS amplification. The attack works by sending spoofed requests to a vulnerable server, which then responds with a larger amount of data than the initial request, magnifying the volume of traffic.

Memcached amplification can be thought of in the context of a malicious teenager calling a restaurant and saying "I'll have one of everything, please call me back and tell me my whole order." When the restaurant asks for a callback number, the number given is the targeted victim’s phone number. The target then receives a call from the restaurant with a lot of information that they didn’t request.

This method of amplification attack is possible because memcached servers have the option to operate using the UDP protocol. UDP is a network protocol that allows for the sending of data without first getting what’s known as a handshake, which is a network process where both sides agree to the communication. UDP is utilized because the targeted host is never consulted on whether or not they’re willing to receive the data, allowing for a massive amount of data to be sent to the target without their prior consent.

A memcached attack occurs in 4 steps:

An attacker implants a large payload* of data on an exposed memcached server.
Next the attacker spoofs an HTTP GET request with the IP address of the targeted victim.
The vulnerable memcached server that receives the request, which is trying to be helpful by responding, sends a large response to the target.
The targeted server or its surrounding infrastructure is unable to process the large amount of data sent from the memcached server, resulting in overload and denial-of-service to legitimate requests.
Memcached
This is a 260 GB per second memcached attack against Cloudflare’s network being mitigated

How big can a memcached amplification attack be?
The magnification factor of this type of attack is truly staggering; in practice we have witnessed amplification factors of up to a whopping 51,200x! That means that for a 15 byte request, a 750 kB response can be sent. This represents a massive amplification factor and security risk to web properties that are unable to shoulder the weight of this volume of attack traffic. Having such a large amplification factor coupled with vulnerable servers makes memcached a prime use case for attackers looking to launch DDoS against various targets.

How can a memcached attack be mitigated?
Disable UDP - For memcached servers, make sure to disable UDP support if you do not need it. By default, memcached has UDP support enabled, potentially leaving a server vulnerable.
Firewall memcached servers - by firewalling memcached servers from the Internet, system administrators are able to use UDP for memcached if necessary without exposure.
Prevent IP spoofing - as long as IP addresses can be spoofed, DDoS attacks can make use of the vulnerability to direct traffic to a victim's network. Preventing IP spoofing is a larger solution that cannot be implemented by any particular system administrator, and it requires transit providers to not allow any packets to leave their network that have a source IP address originating outside the network. In other words, companies such as internet service providers (ISPs) must filter traffic such that the packets that leave their network are not allowed to pretend to be from a different network somewhere else. If all major transit providers implemented this type of filtration, spoofing-based attacks would disappear overnight.
Develop software with reduced UDP responses - another way to eliminate amplification attacks is to remove the amplification factor to any incoming request; If the response data sent as a result of a UDP request is smaller than or equal to the initial request, amplification is no longer possible.
Cloudflare filters UDP traffic at our network edge, eliminating the risk posed by amplification attacks such as this one. Explore Cloudflare’s advanced DDoS protection.

For a more in-depth look at Cloudflare encountering memcached attacks and specific commands and processes for mitigation, explore the blog post Memcrashed - Major amplification attacks from UDP port 11211.
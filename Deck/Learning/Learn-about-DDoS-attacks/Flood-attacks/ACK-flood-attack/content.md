##

What is an ACK flood DDoS attack?
An ACK flood attack is when an attacker attempts to overload a server with TCP ACK packets. Like other DDoS attacks, the goal of an ACK flood is to deny service to other users by slowing down or crashing the target using junk data. The targeted server has to process each ACK packet received, which uses so much computing power that it is unable to serve legitimate users.

Imagine a prank caller filling up someone's voicemail box with fake messages so that voicemails from real callers cannot get through. Now imagine that every one of those fake messages says, "Hi, I'm calling to say I received your message." This is somewhat like what happens in an ACK flood DDoS attack.

What is a packet?
All data that is sent over the Internet is broken up into smaller segments called packets. Think of when someone wants to make an in-depth point or tell a long story on Twitter, and they have to break their text up into 280-character segments and post it in a series of tweets instead of all at once. For those who don't use Twitter, think of how cell phones without dedicated texting apps used to break up long SMS text messages into smaller sections.

The Transmission Control Protocol (TCP) is an essential part of Internet communication. Packets that are sent using the TCP protocol have information attached to them in the packet header. The TCP protocol uses the packet header to tell the recipient how many packets there are and in what order they should arrive. The header may also indicate the length of the packet, what type of packet it is, and so on.

This is somewhat like naming a file folder so that people know what is inside it. Returning to the Twitter example, people posting a long series of tweets will often indicate how many total tweets are in the series and number each tweet to help readers follow along.

What is an ACK packet?
ACK is short for "acknowledgement." An ACK packet is any TCP packet that acknowledges receiving a message or series of packets. The technical definition of an ACK packet is a TCP packet with the "ACK" flag set in the header.

TCP Handshake
ACK packets are part of the TCP handshake, a series of three steps that start a conversation between any two connected devices on the Internet (just as people may greet each other with a handshake in real life before initiating conversation). The three steps of the TCP handshake are:

SYN
SYN ACK
ACK
The device that opens the connection – say, a user's laptop – starts the three-way handshake by sending a SYN (short for "synchronize") packet. The device at the other end of the connection – suppose it's a server that hosts an online shopping website – replies with a SYN ACK packet. Finally, the user's laptop sends an ACK packet, and the three-way handshake is complete. This process ensures that both devices are online and ready to receive additional packets that, in this example, would allow the user to load the website.

However, this is not the only time ACK packets are used. The TCP protocol requires that connected devices acknowledge they have received all packets in order. Suppose a user visits a webpage that hosts an image. The image is broken up into data packets and sent to the user's browser. Once the entire image arrives, the user's device sends an ACK packet to the host server to confirm that not one pixel is missing. Without this ACK packet, the host server has to send the image again.

Since an ACK packet is any TCP packet with the ACK flag set in the header, the ACK can be part of a different message the laptop sends to the server. If the user fills out a form and submits data to the server, the laptop can make one of those packets the ACK packet for the image. It doesn't need to be a separate packet.

How does an ACK flood attack work?
ACK flood attacks target devices that need to process every packet that they receive. Firewalls and servers are the most likely targets for an ACK flood. Load balancers, routers, and switches are not susceptible to these attacks.

Legitimate and illegitimate ACK packets look essentially the same, making ACK floods difficult to stop without using a content delivery network (CDN) to filter out unnecessary ACK packets. Although they look similar, packets used in an ACK DDoS attack do not contain the main part of a data packet, also known as a payload. In order to appear legitimate, they only have to include the ACK flag in the TCP header.

ACK floods are layer 4 (transport layer) DDoS attacks. Learn about layer 4 and the OSI model.

How does a SYN ACK flood attack work?
A SYN ACK flood DDoS attack is slightly different from an ACK attack, although the basic idea is still the same: to overwhelm the target with too many packets.

Remember how a TCP three-way handshake works: The second step in the handshake is the SYN ACK packet. Usually a server sends this SYN ACK packet in response to a SYN packet from a client device. In a SYN ACK DDoS attack, the attacker floods the target with SYN ACK packets. These packets are not part of a three-way handshake at all; their only purpose is to disrupt the target's normal operations.

It is also possible for an attacker to use SYN packets in a SYN flood DDoS attack.

How does Cloudflare stop ACK flood DDoS attacks?
The Cloudflare CDN proxies all traffic to and from a Cloudflare customer's origin server. The CDN does not pass along any ACK packets that are not associated with an open TCP connection. This ensures that the malicious ACK traffic does not reach the origin server. The Cloudflare network of data centers is large enough to absorb DDoS attacks of almost any size, so ACK floods have little to no effect on Cloudflare as well.

Cloudflare Magic Transit and Cloudflare Spectrum also stop these kinds of DDoS attacks. Magic Transit proxies layer 3 traffic and Spectrum proxies layer 4 traffic, instead of layer 7 traffic like the CDN. Both products block ACK floods by automatically detecting attack patterns and blocking attack traffic.
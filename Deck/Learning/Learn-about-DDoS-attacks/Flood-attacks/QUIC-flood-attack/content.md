##

What is the QUIC protocol?
The QUIC protocol is a new way to send data over the Internet that is faster, more efficient, and more secure than earlier protocols. QUIC is a transport protocol, which means it affects the way data travels over the Internet. Like almost any Internet protocol, QUIC can be used maliciously to carry out DDoS attacks.

In more technical terms, the QUIC protocol is a transport layer protocol that can theoretically replace both TCP (a transport protocol) and TLS (an encryption protocol). In July 2019, about 3% of all websites were using QUIC, and proponents of the protocol, including Cloudflare, hope that adoption rates continue to rise over time. The latest version of the HTTP protocol, HTTP/3, runs over QUIC.

How does the QUIC protocol work?
The QUIC protocol aims to be both faster and more secure than traditional Internet connections. For increased speed it uses the UDP transport protocol, which is faster than TCP but less reliable. It sends several streams of data at once to make up for any data that gets lost along the way, a technique known as multiplexing.

For better security, everything sent over QUIC is automatically encrypted. Ordinarily, data has to be sent over HTTPS to be encrypted. But QUIC builds TLS encryption into the normal communication process.

This built-in encryption speeds up the protocol still further. In typical HTTPS, a three-way TCP handshake has to be completed at the transport layer before the multi-step TLS handshake can begin. This all has to happen before any actual data can be sent between client and server. QUIC combines these two handshakes so that they happen all at once: the client and server acknowledge the connection is open and jointly generate TLS encryption keys at the same time.

What is a QUIC flood?
A QUIC flood DDoS attack is when an attacker attempts to deny service by overwhelming a targeted server with data sent over QUIC. The victimized server has to process all the QUIC data it receives, slowing service to legitimate users and, in some cases, crashing the server altogether. DDoS attacks over QUIC are hard to block because:

QUIC uses UDP, which provides very little information to the packet recipient that they can use to block the packets
QUIC encrypts packet data so that the recipient of the data cannot easily tell if it is legitimate or not
A QUIC flood attack can be carried out using a number of methods, but the QUIC protocol is particularly vulnerable to reflection-based DDoS attacks.

What is a QUIC reflection attack?
In a reflection DDoS attack, the attacker spoofs the victim's IP address and requests information from several servers. When the servers respond, all the information goes to the victim instead of the attacker. Imagine someone maliciously sending out letters with someone else's return address so that the second person gets deluged with unwanted mail.

With the QUIC protocol, it is possible to carry out reflection attacks using the initial "hello" message that starts a QUIC connection. Unlike in a TCP connection, a QUIC connection does not open with the server sending a simple "ACK" message. Because QUIC combines the UDP transport protocol with TLS encryption, the server includes its TLS certificate in its first reply to the client. This means that the server's first message is much larger than the client's first message. By spoofing the victim's IP address and sending a "hello" message to a server, the attacker tricks the server into sending large amounts of unwanted data to the victim.

To partially mitigate this type of attack, the architects of the QUIC protocol set a minimum size for the initial client hello message so that it costs the attacker considerable bandwidth to send a large amount of fake client hello messages. However, the server hello is still larger than the client hello, so an attack of this nature remains a possibility.

Are QUIC floods similar to UDP floods?
A UDP flood is a type of DDoS attack that overwhelms a targeted server with unwanted UDP packets. QUIC uses UDP, but a QUIC flood is not necessarily the same as a UDP flood.

One way a UDP flood can take down a targeted server is by sending spoofed UDP packets to a specific port on a server that is not actually in use. The server has to reply to all the packets with an ICMP error message, which takes up processing power and slows the server down. This attack would be possible using QUIC, but it is usually cheaper for the attacker to carry it out over UDP alone, without the added overhead of generating QUIC packets.

Does Cloudflare block QUIC flood DDoS attacks?
Cloudflare mitigates a wide variety of DDoS attacks, including QUIC floods. The Cloudflare global network, which spans 275 cities in more than 100 countries, is large enough to absorb and mitigate even the biggest DDoS attacks on record. Learn more about DDoS attacks.
##

What is layer 7 of the Internet?
Layer 7 refers to the top layer in the 7-layer OSI Model of the Internet. It is also known as the "application layer." It is the top layer of the data processing that occurs just below the surface or behind the scenes of the software applications that users interact with. The HTTP requests and responses used to load webpages, for example, are layer 7 events.

DDoS attacks that take place at this level are known as layer 7 attacks or application layer attacks. DDoS attacks can also take place at layers 3 or 4 of the OSI Model.

What is the OSI Model?
The OSI (open systems interconnection) Model divides the functions of a networking system into 7 layers, each layer abstracted from the one below it. Within the model, each layer interacts only with the layers above and below itself.

It is worth keeping in mind that the OSI Model is purely theoretical, and it is designed to help describe what takes place in networking communications, not to describe the actual technology involved. Just because the OSI Model is only a conceptual framework does not mean it is not useful; referencing the model helps engineers, developers, and IT professionals pinpoint what a product or protocol does and where it belongs in the process of network communication.

The OSI Model
At the bottom of the model is the physical layer (layer 1), or the pulses of electricity that communicate bits of information across the cables, routers, switches, and WiFi networks making up Internet infrastructure. At the top, in layer 7, are the protocols and services applications use in order to function. In between are various functionalities and protocols that data passes through over the course of network communications.

For a more thorough breakdown of what each layer does, see "What is the OSI model?"

What does layer 7 do?
Although layer 7 is known as the application layer, it is not the user interface of the applications themselves. Rather, layer 7 provides functionalities and services that user-facing software applications use to present data. If an application is like a house, then layer 7 is the foundation, not the house itself.

API calls and responses belong to this layer, and some of the main protocols used are HTTP and SMTP (Simple Mail Transfer Protocol, which email applications use).

How does layer 7 interact with the other OSI layers?
Data from layer 7 gets passed down the stack, although layer 7 only interacts with layer 6. As data goes down through the stack, it is broken up into packets, and certain layers add headers and footers to each packet – for example, at layer 3, an IP header containing the destination and source IP addresses is added to each packet. At the bottom of the stack, data is converted into bits and transmitted across the physical Internet.

Upon reaching its destination, data goes back up the stack, starting at layer 1. At each layer, header and footer data is interpreted and stripped, and data is put into a form that is usable for the next layer up. Once data reaches layer 7 on the other side, it is made available to applications. (Despite all these steps, the whole process takes only milliseconds.)

Crucial to understanding how the OSI Model works is the fact that each layer only communicates with that same layer on the other end of the interaction. Layer 7 data is only interpreted by layer 7 on the receiving end of the communication; the other layers on the receiving end merely pass the data up to layer 7. Similarly, the IP header data that is appended to data packets in layer 3 on one side is only read and interpreted by layer 3 on the other side.

How do layer 7 DDoS attacks work?
Layer 7 or application layer DDoS attacks attempt to overwhelm network or server resources with a flood of traffic (typically HTTP traffic). An example would be sending thousands of requests for a certain webpage per second until the server is overwhelmed and cannot respond to all of the requests. Another example would be calling an API over and over until the service crashes.

To learn more, see "Application layer DDoS attacks."

How is the OSI Model different from the TCP/IP model?
The TCP/IP networking conceptual model is an alternative to the OSI Model. It divides the networking stack into four layers instead of seven, and although it is similar to the OSI Model, it does not match up exactly. In the TCP/IP model, there is no "layer 7," but this is a purely semantic distinction and does not mean that networking functions differently in the two models.

The four layers in the TCP/IP model are:

The application layer (for protocols such as HTTP and SMTP)
The transport layer (for transport protocols such as TCP and UDP)
The Internet layer (the Internet protocol and ICMP)
The network access layer
How does Cloudflare protect against layer 7 attacks?
Cloudflare DDoS protection is built to protect against DDoS attacks no matter which OSI layer they target. By intelligently filtering and distributing network traffic across 275 data centers worldwide, the Cloudflare network is able to absorb massive amounts of layer 7 traffic. The Cloudflare network is shielded by these attacks when following Cloudflare best practices.
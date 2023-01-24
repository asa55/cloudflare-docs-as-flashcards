##

What is a R.U.D.Y. attack?
‘R U Dead Yet?’ or R.U.D.Y. is a denial-of-service attack tool that aims to keep a web server tied up by submitting form data at an absurdly slow pace. A R.U.D.Y. exploit is categorized as a low-and-slow attack, since it focuses on creating a few drawn-out requests rather than overwhelming a server with a high volume of quick requests. A successful R.U.D.Y. attack will result in the victim’s origin server becoming unavailable to legitimate traffic.

The R.U.D.Y. software includes a user-friendly point-and-click interface, so all an attacker needs to do is point the tool at a vulnerable target. Any web service that accepts form input is vulnerable to a R.U.D.Y. attack, since the tool works by sniffing out form fields and exploiting the form submission process.

How does a R.U.D.Y. attack work?
A R.U.D.Y. attack can be broken down into the following steps:

The R.U.D.Y. tool crawls the victim’s application looking for a form field.
Once a form is found, the tool creates an HTTP POST request to mimic a legitimate form submission. This POST request contains a header* which alerts the server that a very lengthy piece of content is about to be submitted.
The tool then drags out the process of submitting the form data by breaking it down into packets as small as 1 byte each, sending these packets to the server at randomized intervals of around 10 seconds each.
The tool continues submitting data indefinitely. The web server will keep the connection open to accept the packets, since the behavior of the attack is similar to that of a user with a slow connection speed submitting form data. Meanwhile the web server’s capacity to handle legitimate traffic is impaired.
The R.U.D.Y. tool can simultaneously create several of these slow requests all targeting one web server. Since web servers can only handle so many connections at once, it’s possible for the R.U.D.Y. attack to tie up all available connections, meaning any legitimate users trying to access the web server will be denied service. Even a robust web server with a high number of connections available can be taken down by R.U.D.Y. via a network of computers conducting attacks simultaneously, this is known as a Distributed Denial-of-Service (DDoS) attack.

*HTTP headers are key/value pairs that are sent with any HTTP request or response, and they provide vital information such as the HTTP version being used, what language the content is in, how much content is being delivered, etc.

How to stop R.U.D.Y. attacks
Because slow and low attacks are carried out much more subtly than traditional denial-of-service attacks, they can be hard to detect, but protections can be put in place to prevent them. One such prevention measure is to set stricter connection timeout intervals on a web server, meaning that the slowest connections will be severed. This solution comes with a side effect: legitimate users with slow Internet connections could be denied service by the server. Alternately a reverse-proxy solution, such as Cloudflare’s DDoS protection, can filter out low-and-slow attack traffic like R.U.D.Y. attacks, without disconnecting legitimate users.
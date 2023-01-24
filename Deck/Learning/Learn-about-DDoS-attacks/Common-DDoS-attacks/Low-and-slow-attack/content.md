##

What is a low and slow attack?
A low and slow attack is a type of DoS or DDoS attack that relies on a small stream of very slow traffic targeting application or server resources. Unlike more traditional brute-force attacks, low and slow attacks require very little bandwidth and can be hard to mitigate, as they generate traffic that is very difficult to distinguish from normal traffic. While large-scale DDoS attacks are likely to be noticed quickly, low and slow attacks can go on undetected for long periods of time, all while denying or slowing service to real users.

Because they do not require a lot of resources to pull off, low and slow attacks can be successfully launched using a single computer, as opposed to more distributed attacks that may require a botnet. Two of the most popular tools for launching a low and slow attack are called Slowloris and R.U.D.Y.

How does a low and slow attack work?
Low and slow attacks target thread-based web servers with the aim of tying up every thread with slow requests, thereby preventing genuine users from accessing the service. This is accomplished by transmitting data very slowly, but just fast enough to prevent the server from timing out.

Think of a 4-lane bridge with a tollbooth for each lane. Drivers pull up to the tollbooth, hand over a bill or a handful of coins, and then drive across the bridge, opening up the lane for the next driver. Now imagine four drivers showing up at once and occupying every open lane while they each slowly hand pennies over to the tollbooth operator, one coin at a time, clogging up all available lanes for hours and preventing other drivers from getting through. This incredibly frustrating scenario is very similar to how a low and slow attack works.

Attackers can use HTTP headers, HTTP POST requests, or TCP traffic to carry out low and slow attacks. Here are 3 common attack examples:

The Slowloris tool connects to a server and then slowly sends partial HTTP headers. This causes the server to keep the connection open so that it can receive the rest of the headers, tying up the thread.
Another tool called R.U.D.Y. (R-U-DEAD-YET?) generates HTTP POST requests to fill out form fields. It tells the servers how much data to expect, but then sends that data in very slowly. The server keeps the connection open because it is anticipating more data.
Yet another type of low and slow attack is the Sockstress attack, which exploits a vulnerability in the TCP/IP 3-way handshake, creating an indefinite connection.
How can web services detect a low and slow attack?
The rate detection techniques used to identify and stop traditional DDoS attacks will not pick up on a low and slow attack, since they look like normal traffic. The best shot at detecting them is careful monitoring and logging of server resource usage combined with behavioral analysis. Compare traffic and user behavior during normal times to traffic and user behavior during the potential attack period.

If servers are performing slowly or crashing and a low and slow attack is suspected, one sign of such an attack is that normal user processes take much longer. If a user action (such as filling out a form) typically takes a few seconds but is instead taking minutes or hours, occupying far more server resources than normal, a low and slow attack may be the cause.

Once a low and slow attack is detected, mitigation is another issue.

How to stop a low and slow attack
One way to mitigate a low and slow attack is to upgrade your server availability; the more connections your server can simultaneously maintain, the more difficult it will be for an attack to clog your server. The problem with this approach is that an attacker can attempt to scale their attack to meet your server’s availability.

Another solution is reverse proxy-based protection, which will mitigate low and slow attacks before they ever reach your origin server. Learn about how Cloudflare’s cloud-based DDoS protection can mitigate low and slow attacks.
##

What is the Low Orbit Ion Cannon (LOIC)?
The Low Orbit Ion Cannon is a tool commonly used to launch DoS and DDoS attacks. It was originally developed by Praetox Technology as a network stress-testing application, but it has since become open-source and is now mostly used with malicious intent. It is known for being a very user-friendly and accessible tool, and it gained notoriety for its use by members of hacktivist group Anonymous as well as users of the 4Chan forums.

This tool puts the ability to launch DDoS attacks in the hands of users with very little technical knowledge. It is widely available for download and has a simple point-and-click interface, additionally users can even launch attacks from a web browser using a JavaScript version called JS LOIC and a web version known as the Low Orbit Web Cannon.

How does the LOIC work?
It works by flooding a target server with TCP, UDP, or HTTP packets with the goal of disrupting service. One attacker using the LOIC can’t generate enough junk traffic to make a serious impact on a target; serious attacks require thousands of users to coordinate a simultaneous attack on the same target. In order to make these coordinated attacks easier, users can use IRC chat channels to run a ‘Hivemind’ version of the LOIC which lets one primary user control several networked secondary computers, creating a voluntary botnet. This is a popular approach because owners of the secondary devices can claim they were innocent victims of an involuntary botnet.

LOIC hiveminds were used by Anonymous in 2008 to attack Church of Scientology websites in response to the Church’s legal efforts to take down YouTube videos. The LOIC was also notably used in 2010, when WikiLeaks supporters went after the Visa and MasterCard sites in response to the credit card companies freezing payments to WikiLeaks.

How do you stop an LOIC attack?
Small LOIC HTTP attacks can be mitigated with a local firewall by having a server administrator look at the logs and identify the IPs of the attackers and dropping their requests. However this strategy won’t stand up to a large-scale attack where hundreds or even thousands of different attackers are working in tandem. Local firewalls also can’t protect against TCP or UDP floods, the latter of which can even target and disrupt a firewall. A Web Application Firewall (WAF) can provide strong protection against HTTP floods, and dedicated DDoS protection can stop TCP and UDP attacks.

Fortunately, attackers using the LOIC are fairly easy to detect; it can’t be used through a proxy, so attackers’ IP addresses are visible to the target. Numerous countries have taken legal action against attackers using the LOIC including the U.S., U.K., Spain, and Turkey.
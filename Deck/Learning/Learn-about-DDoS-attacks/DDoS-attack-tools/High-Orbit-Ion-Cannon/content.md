##

What is the High Orbit Ion Cannon (HOIC)?
The High Orbit Ion Cannon is a popular tool used to launch DoS and DDoS attacks, which aims to flood a victim’s network with web traffic and shut down a web site or service. It is an easily available piece of open-source software developed by hacktivist group Anonymous, and it’s a successor to an older DDoS tool called the Low Orbit Ion Cannon (both named after sci-fi video game weapons). While most malicious software tools require a high level of technical skill, the HOIC provides a simple and user-friendly interface and can be turned on with the click of a button.

Although it is used in many malicious and illegal attacks, the HOIC is still legally available because it has applications as a legitimate testing tool for users who want to implement a “stress test” on their own networks.

How does the HOIC work?
The HOIC works via an application layer HTTP Flood DDoS attack, flooding a victim’s server with HTTP ‘GET’ and ‘POST’ requests with the goal of overloading the server’s request capacity. For advanced attacks, custom scripts can be used to target multiple sub-domains of the victim’s site at once. The HOIC can also target as many as 256 sites simultaneously, making it possible for users to coordinate concurrent attacks. This ‘shotgun approach’ of having several attackers targeting many different pages and domains at once can make mitigation and detection efforts much more challenging.

Built-in booster scripts also help attackers avoid detection. In addition to the booster scripts, many HOIC users also use Swedish proxies to obfuscate their location (it is believed that they choose Sweden because of the strict internet privacy laws in that country).

Launching a serious attack with the HOIC requires some coordination, as it requires around 50 different users to launch the attack on the same target simultaneously. Anonymous demonstrated the HOIC’s effectiveness in 2012 when it successfully launched attacks against several major record companies, the RIAA, and even the FBI. It was one of the biggest DDoS attacks in history and required an estimated 27,000 computers simultaneously using the HOIC.

What can stop an HOIC attack?
Several strategies exist to mitigate HTTP flood attacks from the HOIC. IP Reputation Filtering (IPRF) is a preventative measure that checks incoming IP addresses against databases of known malicious IP addresses and keeps their traffic off the network. A Web Application Firewall (WAF) can set rate-limiting rules which will drop traffic from IP addresses that are making suspicious amounts of requests. There are also methods to test if a web client is legitimate, such as captcha verification and a more sophisticated method that asks web browsers to solve a simple math problem without interrupting the user experience.

Protection from HOIC attacks should be included in most DDoS protection products and services. A comprehensive DDoS protection plan which includes a WAF like the one offered by Cloudflare, offers a strong defense against layer 7 attacks, such as those launched by the HOIC.
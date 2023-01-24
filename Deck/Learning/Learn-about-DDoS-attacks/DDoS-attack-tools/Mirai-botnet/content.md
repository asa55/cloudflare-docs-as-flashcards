##

What is Mirai?
Mirai is malware that infects smart devices that run on ARC processors, turning them into a network of remotely controlled bots or "zombies". This network of bots, called a botnet, is often used to launch DDoS attacks.

Botnet - networked malicious bots
Malware, short for malicious software, is an umbrella term that includes computer worms, viruses, Trojan horses, rootkits and spyware.

In September 2016, the authors of the Mirai malware launched a DDoS attack on the website of a well-known security expert. A week later they released the source code into the world, possibly in an attempt to hide the origins of that attack. This code was quickly replicated by other cybercriminals, and is believed to be behind the massive attack that brought down the domain registration services provider, Dyn, in October 2016.

How does Mirai work?
Mirai scans the Internet for IoT devices that run on the ARC processor. This processor runs a stripped-down version of the Linux operating system. If the default username-and-password combo is not changed, Mirai is able to log into the device and infect it.

IoT, short for Internet of Things, is just a fancy term for smart devices that can connect to the Internet. These devices can be baby monitors, vehicles, network routers, agricultural devices, medical devices, environmental monitoring devices, home appliances, DVRs, CC cameras, headset, or smoke detectors.

The Mirai botnet employed a hundred thousand hijacked IoT devices to bring down Dyn.

Who were the creators of the Mirai botnet?
Twenty-one-year-old Paras Jha and twenty-year-old Josiah White co-founded Protraf Solutions, a company offering mitigation services for DDoS attacks. Theirs was a classic case of racketeering: Their business offered DDoS mitigation services to the very organizations their malware attacked.

Why does the Mirai malware remain dangerous?
The Mirai is mutating.

Though its original creators have been caught, their source code lives on. It has given birth to variants such as the Okiru, the Satori, the Masuta and the PureMasuta. The PureMasuta, for example, is able to weaponize the HNAP bug in D-Link devices. The OMG strain, on the other hand, transforms IoT devices into proxies that allow cybercriminals to remain anonymous.

There is also the recently discovered - and powerful - botnet, variously nicknamed IoTrooper and Reaper, which is able to compromise IoT devices at a much faster rate than Mirai. The Reaper is able to target a larger number of device makers, and has far greater control over its bots.

What are the various botnet models?
Centralized botnets
If you think of a botnet as a theatrical play, the C&C (Command and Control Server, also known as the C2) server is its director. The actors in this play are the various bots that have been compromised by malware infection, and made part of the botnet.

When the malware infects a device, the bot send out timed signals to inform the C&C that it now exists. This connection session is kept open till the C&C is ready to command the bot to do its bidding, which can include sending out spam, password cracking, DDoS attacks, etc.

In a centralized botnet, the C&C is able to convey commands directly to the bots. However, the C&C is also a single point of failure: If taken down, the botnet becomes ineffective.

Tiered C&Cs
Botnet control may be organized in multiple tiers, with multiple C&Cs. Groups of dedicated servers may be designated for a specific purpose, for example, to organize the bots into subgroups, to deliver designated content, and so on. This makes the botnet harder to take down.

Decentralized botnets
Peer-to-peer (P2P) botnets are the next generation of botnets. Rather than communicate with a centralized server, P2P bots act as both a command server, and a client which receives commands. This avoids the single point of failure problem inherent to centralized botnets. Because P2P botnets operate without a C&C, they are harder to shut down. Trojan.Peacomm and Stormnet are examples of malware behind P2P botnets.

How does malware turn IoT devices into bots or zombies?
In general, email phishing is a demonstrably effective way of infecting the computer - the victim is tricked into either clicking a link that points to a malicious website, or downloading infected attachment. Many times the malicious code is written in such a way that common antivirus software is not able to detect it.

In the case of Mirai, the user doesn’t need to do much beyond leaving the default username and password on a newly installed device unchanged.

What is the connection between Mirai and click fraud?
Pay-per-click (PPC), also known as cost-per-click (CPC), is a form of online advertising in which a company pays a website to host their advertisement. Payment depends on how many of that site’s visitors clicked on that ad.

When CPC data is fraudulently manipulated, it is known as click fraud. This can be done by having people manually click on the ad, by use of automated software, or with bots. Through this process, fraudulent profits can be generated for the website at the expense of the company placing those ads.

The original authors of Mirai were convicted for leasing their botnet out for DDoS attacks and click fraud.

Why are botnets dangerous?
Botnets have the potential to impact virtually every aspect of a person’s life, whether or not they use IoT devices, or even the Internet. Botnets can:

Attack ISPs, sometimes resulting in denial-of-service to legitimate traffic
Send spam email
Launch DDoS attacks and bring down websites and APIs
Perform click fraud
Solve weak CAPTCHA challenges on websites in order to imitate human behavior during logins
Steal credit card information
Hold companies to ransom with threats of DDoS attacks
Why is botnet proliferation so hard to contain?
There are many reasons why it is so difficult to stop the proliferation of botnets:

IoT device owners
There is no cost or interruption in service, so there is no incentive to secure the smart device.

Infected systems may be cleaned out with a reboot, but since scanning for potential bots happens at a constant rate, it’s possible for them to be reinfected within minutes of the reboot. This means users have to change the default password immediately after reboot. Or they must prevent the device from accessing the Internet until they can reset the firmware, and change the password offline. Most device owners have neither the know-how, nor the motivation to do so.

ISPs
The increased traffic on their network from the infected device typically does not compare to the traffic that media streaming generates, so there is not much incentive to care.

Device manufacturers
There is little incentive for device manufacturers to invest in the security of low-cost devices. Holding them liable for attacks might be one way of forcing change, though this might not work in regions with lax enforcement.

Ignoring device security comes at great peril: Mirai, for example, is able to disable anti-virus software, which makes detection a challenge.

Magnitude
With over a billion-and-a-half ARC-processor-based devices flooding the market each year, the sheer number of devices that can be conscripted into powerful botnets means that these malware variants have grown in possible impact.

Simplicity
Ready-to-go botnet kits obviate the need for tech savvy. For $14.99-$19.99, a botnet may be leased for an entire month. Refer to What is a DDoS Booter/Stresser? for more details.

Global IoT Security Standards
There is no global entity, or consensus, to define and enforce IoT security standards.

While security patches are available for some devices, users might not have the skill, or the incentive, to update. Many manufacturers of low-end devices don’t offer any kind of maintenance at all. For ones that do, it is often not long term. There is also no way to decommission devices once the updates are no longer maintained, making them indefinitely unsecure.

Global Law Enforcement
The difficulty in tracking down and prosecuting botnet creators makes the containment of botnet proliferation difficult; There is no global Interpol-equivalent (International Criminal Police Organization) for cybercrime, with corresponding investigative skills. Law enforcement across the globe is commonly not been able to keep up with cybercriminals when it comes to latest technology.

Many botnets now employ a DNS technique called Fast Flux in order to hide the domains they use to download malware, or to host phishing sites. This makes them extremely hard to track, and take down.

Does botnet infection degrade performance for IoT devices?
It might. Every once in a while, infected devices might perform sluggishly, but they mostly work as intended. Owners have no great motivation to find ways to clear out the infection.

Addendum
A legislation on the desk of California governor, Jerry Brown, requires that IoT devices have reasonable security feature(s) “appropriate to the nature and function of the device.” This would come into effect in January 2020.

Why this legislation is so important? The lucrative California market makes it impossible for companies to ignore. If they want to sell in California, they will need to improve security in their devices. This will benefit all states.
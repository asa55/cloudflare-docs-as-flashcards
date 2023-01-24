##

What was the largest DDoS attack of all time?
The biggest DDoS attack to date took place in September of 2017. The attack targeted Google services and reached a size of 2.54 Tbps. Google Cloud disclosed the attack in October 2020.

The attackers sent spoofed packets to 180,000 web servers, which in turn sent responses to Google. The attack was not an isolated incident: the attackers had directed multiple DDoS attacks at Google's infrastructure over the previous six months.

What are some other famous DDoS attacks?
The February 2020 attack reported by AWS
AWS reported mitigating a massive DDoS attack in February of 2020. At its peak, this attack saw incoming traffic at a rate of 2.3 terabits per second (Tbps). AWS did not disclose which customer was targeted by the attack.

The attackers responsible used hijacked Connection-less Lightweight Directory Access Protocol (CLDAP) web servers. CLDAP is a protocol for user directories. It is an alternative to LDAP, an older version of the protocol. CLDAP has been used in multiple DDoS attacks in recent years.

The February 2018 GitHub DDoS attack
One of the largest verifiable DDoS attacks on record targeted GitHub, a popular online code management service used by millions of developers. This attack reached 1.3 Tbps, sending packets at a rate of 126.9 million per second.

The GitHub attack was a memcached DDoS attack, so there were no botnets involved. Instead the attackers leveraged the amplification effect of a popular database caching system known as memcached. By flooding memcached servers with spoofed requests, the attackers were able to amplify their attack by a magnitude of about 50,000x.

Luckily, GitHub was using a DDoS protection service, which was automatically alerted within 10 minutes of the start of the attack. This alert triggered the process of mitigation and GitHub was able to stop the attack quickly. The massive DDoS attack only ended up lasting about 20 minutes.

The 2016 Dyn attack
Another massive DDoS attack was directed at Dyn, a major DNS provider, in October of 2016. This attack was devastating and created disruption for many major sites, including Airbnb, Netflix, PayPal, Visa, Amazon, The New York Times, Reddit, and GitHub. This was done using malware called Mirai. Mirai creates a botnet out of compromised Internet of Things (IoT) devices such as cameras, smart TVs, radios, printers, and even baby monitors. To create the attack traffic, these compromised devices are all programmed to send requests to a single victim.

Fortunately Dyn was able to resolve the attack within one day, but the motive for the attack was never discovered. Hacktivist groups claimed responsibility for the attack as a response to WikiLeaks founder Julian Assange being denied Internet access in Ecuador, but there was no proof to back up this claim. There are also suspicions that the attack was carried out by a disgruntled gamer.

The 2015 GitHub attack
The largest DDoS attack ever at the time, this one also happened to target GitHub. This politically motivated attack lasted several days and adapted itself around implemented DDoS mitigation strategies. The DDoS traffic originated in China and specifically targeted the URLs of two GitHub projects aimed at circumventing Chinese state censorship. It is speculated that the intent of the attack was to try and pressure GitHub into eliminating those projects.

The attack traffic was created by injecting JavaScript code into the browsers of everyone who visited Baidu, China’s most popular search engine. Other sites who were using Baidu’s analytics services were also injecting the malicious code; this code was causing the infected browsers to send HTTP requests to the targeted GitHub pages. In the aftermath of the attack it was determined that the malicious code was not originating from Baidu, but rather being added by an intermediary service.

The 2013 Spamhaus attack
Another largest-ever-at-the-time attack was the 2013 attack directed at Spamhaus, an organization that helps combat spam emails and spam-related activity. Spamhaus is responsible for filtering as much as 80% of all spam, which makes them a popular target for people who would like to see spam emails reach their intended recipients.

The attack drove traffic to Spamhaus at a rate of 300 Gbps. Once the attack began, Spamhaus signed up for Cloudflare. Cloudflare’s DDoS protection mitigated the attack. The attackers responded to this by going after certain Internet exchanges and bandwidth providers in an attempt to bring down Cloudflare. This attack did not achieve its goal, but it did cause major issues for LINX, the London Internet exchange. The main culprit of the attack turned out to be a teenage hacker-for-hire in Britain who was paid to launch this DDoS attack.

Read more about this attack and how it was mitigated on the Cloudflare blog.

The 2000 Mafiaboy attack
In 2000, a 15-year-old hacker known as ‘Mafiaboy’ took down several major websites including CNN, Dell, E-Trade, eBay, and Yahoo!, the last of which at the time was the most popular search engine in the world. This attack had devastating consequences, including creating chaos in the stock market.

Mafiaboy, who was later revealed to be a high schooler named Michael Calce, coordinated the attack by compromising the networks of several universities and using their servers to conduct the DDoS attack. The aftermath of this attack directly led to the creation of many of today’s cybercrime laws.

The 2007 Estonia attack
In April 2007 the nation of Estonia was hit with a massive DDoS attack targeting government services, financial institutions, and media outlets. This had a crushing effect since Estonia’s government was an early adopter of online government and was practically paperless at the time; even national elections were conducted online.

The attack, considered by many to be the first act of cyber warfare, came in response to a political conflict with Russia over the relocation of the ‘Bronze Soldier of Tallinn’, a World War II monument. The Russian government was suspected of involvement and an Estonian national from Russia was arrested as the result, but the Russian government has not let Estonian law enforcement do any further investigation in Russia. This ordeal led to the creation of international laws for cyber warfare.

Are DDoS protection vendors able to mitigate attacks of this size?
It depends on their network capacity: whether or not they can absorb the amount of traffic that the DDoS attack in question is generating, while still providing service. Many DDoS protection and mitigation vendors today have enough network capacity to do so.

Although the largest DDoS attack Cloudflare has mitigated in terms of volume was 1.2 Tbps, Cloudflare features 172 Tbps of network capacity, which is much larger than the largest DDoS attacks ever recorded. Cloudflare has also mitigated DDoS attacks that featured extremely high packet rates and HTTP request rates. In June 2020, Cloudflare mitigated a 754 million packet-per-second DDoS attack. And in August 2021, Cloudflare mitigated a 17.2 million request-per-second attack.

It is important to keep in mind that the vast majority of DDoS attacks are not as big as the attacks chronicled in this article. Cloudflare's research shows that most DDoS attacks do not exceed 10 Gbps. However, even these smaller DDoS attacks can knock websites or applications offline for long periods of time if they do not have DDoS mitigation in place.
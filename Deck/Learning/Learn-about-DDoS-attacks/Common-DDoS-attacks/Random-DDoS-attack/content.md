##

What is a ransom DDoS attack?
Ransom DDoS attack diagram: Attacker sends junk network traffic and ransom note to victim
A ransom DDoS (RDDoS) attack is when malicious parties attempt to extort money from an individual or organization by threatening them with a distributed denial-of-service (DDoS) attack. The malicious party in question may carry out a DDoS attack and then follow up with a ransom note demanding payment to stop the attack, or they may send the ransom note threatening a DDoS attack first. In the second case, the attacker may not actually be capable of carrying out the attack, although it is not wise to assume that they are making an empty threat.

The best protection against DDoS ransom attacks is a strong DDoS mitigation service. It is never a good idea to pay the ransom to the person or group making the threats.

What is a DDoS attack?
A DDoS attack is an attempt to exhaust the resources of an application, website, or network so legitimate users cannot receive service. DDoS attacks send a flood of junk network traffic to their targets, much like a traffic jam clogging up a freeway. DDoS attacks are "distributed," meaning they send traffic from a variety of sources (often spoofed sources), making them more difficult to block than a denial-of-service (DoS) attack from a single source.

DDoS attackers use a number of different networking protocols. Read about different types of DDoS attacks here.

DDoS attacks can have a major impact on an organization's operations. For many businesses, any downtime means a loss of revenue. Organizations may also lose credibility if they are offline for an extended period of time.

How does a ransom DDoS attack work?
Most DDoS ransom attacks start with a ransom note sent to the target in which the attacker threatens the business or organization. In some cases, an attacker may carry out a small demonstration attack to illustrate their seriousness before sending a ransom note. If the threat is genuine and the attacker decides to follow through with it, the attack is carried out as follows:

1. The attacker begins sending attack traffic to the target. They could be using their own botnet or a DDoS service they have hired in order to carry out the attack. Several people working together can also generate attack traffic using DDoS tools. Attack traffic can target layers 3, 4, or 7 in the OSI model.

2. The targeted application or service becomes overwhelmed by the attack traffic, and it either slows to a crawl or crashes altogether.

3. The attack continues until the attacker's resources are exhausted, they shut off the attack for some other reason, or the target is able to mitigate the attack. Mitigation methods include rate limiting, IP blocking, blackhole routing, or a DDoS protection service; the first three are difficult to implement against highly distributed attacks.

4. The attacker may renew their demands for payment, carry out subsequent attacks, or both.

Learn more about the specifics of how DDoS attacks are carried out.

What goes into a typical DDoS ransom note?
A DDoS ransom note is a message sent from a malicious party to a business demanding money, or else the malicious party will carry out a DDoS attack. Often these are sent via email. Sometimes the attacker will send multiple messages, with each message revealing more details about their specific threats or demands.

The threat
The threat contained in a DDoS ransom note can take a few different forms:

The malicious party may take credit for a previous DDoS attack and threaten another one
They may take credit for a DDoS attack that is currently in progress against the target
They may threaten a future DDoS attack, either at a certain time or at an undefined time
Details of the threatened attack
To make the threat sound more dangerous, the attacker may claim to be capable of carrying out a DDoS attack of a certain size and duration. These claims are not necessarily true: just because someone claims to be capable of a 3 Tbps attack that lasts 24 hours does not mean they actually have the resources to follow through with it.

Group affiliation
To add credibility to their threats, the attacker may claim affiliation with well-known "hacker" groups such as Fancy Bear, Cozy Bear, the Lazarus Group, the Armada Collective, or others. These claims might be true but are difficult to verify. It may be a bluff or a copy-cat attempt on the part of the attacker.

Demand for payment and instructions for delivering the payment
The ransom note will demand payment in some form. Payment in Bitcoin is a common request, but the attacker may ask for the ransom in another cryptocurrency as well, or in a state-sanctioned currency (dollars, euros, etc.). At a certain point, they will usually ask for a specific amount of money and provide instructions for delivering the money.

Time limit or deadline
Finally, to give their demand urgency and increase the likelihood that the targeted party will comply, the ransom note may include a hard deadline for delivering the ransom before the threatened attack will commence, or in order for the current attack to end. Some attackers will add that the required payment amount increases every hour or day past the given deadline.

Is it a good idea to pay the ransom?
No. Aside from the fact that paying the ransom involves giving money to criminals, payment does not guarantee that the attackers will stop their activities. On the contrary, an organization that pays a ransom is an even more desirable target: it has shown it is willing to meet the attackers' demands, and thus is more likely to meet future demands too.

In addition, the more money an attacker obtains, the better they will be able to fund their extortion operation, expanding their capabilities for future attacks.

Finally, there is always the possibility that the threat is not credible, and the business has paid a ransom for nothing.

Businesses that receive DDoS ransom demands should report them to the appropriate law enforcement authorities and put safeguards in place to defend themselves against potential attacks, in case the attackers carry out their threats. Cloudflare DDoS Protection is one example of a service that can safeguard against DDoS attacks of any size.

Are most DDoS ransom threats likely to be credible?
All security threats should be taken seriously. However, not all DDoS ransom threats are genuine. It is fairly easy to type and send a short email. It requires far more resources to maintain, manage, and activate a large network of compromised devices (known as a botnet) in order to carry out large DDoS attacks.

That being said, many DDoS-for-hire services are available on the dark web, and an attacker may contract with one of these services in order to carry out the attack. Naturally this costs the attacker money — which they can obtain via DDoS ransom threats.

Usually, ransom DDoS attacks are a numbers game. Whether or not the party demanding the ransom is actually capable of carrying out their threats, they count on some small percentage of their targets to pay the ransom.

Rather than attempting to assess the credibility of the threat, the safest course is to use a DDoS protection service that can keep a web property or network online no matter what.

How does Cloudflare protect against RDDoS attacks?
All Cloudflare customers, including free customers, have access to DDoS protection that mitigates even very large DDoS attacks. Additionally, Cloudflare Magic Transit protects enterprise customers' network infrastructure from layer 3 DDoS attacks. The Cloudflare network has 172 Tbps of capacity, which is many times larger than the largest DDoS attacks ever recorded. While all security threats should be recorded and monitored, this level of protection means Cloudflare customers do not have to worry about DDoS ransom notes and other DDoS-related threats.

If your organization received a ransom note, you can contact Cloudflare here.

What is the difference between a ransom DDoS attack and ransomware?
Ransomware attacks are another common form of online extortion. Ransomware is malicious software that encrypts an organization's systems and databases, rendering them unusable. Once the encryption is complete, the attacker will demand money in exchange for decrypting the organization's systems. Ransomware has to be brought inside a business's internal systems or network somehow; malicious email attachments combined with phishing attacks are a common threat vector.

Unlike a ransomware attack, a DDoS ransom attack does not encrypt a company's systems; it merely aims to knock them offline. It also does not require the attacker to gain access to a business's internal systems before it can be carried out. However, with strong enough DDoS protection in place, a DDoS ransom attack has little to no effect on a business's functioning.
##

Data from the latest DDoS report
Cloudflare has observed and mitigated massive numbers of DDoS attacks against network infrastructure. While some of these attacks were quite large, the majority were both small and short. This trend has remained consistent—even as overall numbers of attacks rose and fell, and different network-layer protocols gained and lost popularity amongst attack perpetrators.

While the prospect of small, short DDoS attacks may sound encouraging, such attacks can harm unprotected or underprotected networks. They can also allow attackers to pressure-test an organization’s defenses and can distract security teams from separate, more serious threats.

What trends and tactics are behind the popularity of smaller DDoS attacks? And what should organizations do to respond?

Smaller DDoS attacks are surging
DDoS attacks are designed to exploit bottlenecks within an organization’s IT infrastructure and the applications receiving the traffic. While many types of DDoS attacks exist, most use one of two techniques:

Large packet volumes: Any server or application has a limited number of concurrent requests that it can process. By exceeding these limits, it is possible to degrade or destroy the applications’ ability to process legitimate requests.

Large data volumes: Network links, servers, and applications also have limits on the amount of data that they can transmit or process. Exceeding these bandwidth limitations can also bring a system down.

The image below, which draws on Cloudflare network data from Q4 2021, shows that the vast majority of attacks did not attempt to use the first technique. During these three months, over 98% of DDoS attacks had rates of 1 million packets per second (pps) or lower — a trend consistent with findings from previous quarters.

Network-Layer DDoS Attacks - Distribution by packet rate - Image
For reference, a large-scale DDoS attack against GitHub in 2018 reached rates of 129.6 million packets per second. In Q4 2021, only 2% of DDoS attacks reached a tenth of this size, indicating that most attackers are performing DDoS attacks with smaller packet volumes.

The graph below demonstrates that most Layer 3/4 DDoS attacks from Q4 were also not attempting to overwhelm their targets with massive volumes of data. In fact, 97% of all attacks carried less than half a gigabyte of data per second.

Network-Layer DDoS Attacks - Distribution by bit rate - Image
DDoS attackers are no longer using the same tactics that were common in the past. The reason for this is that shorter, smaller attacks can provide them with several different benefits.

Why are these shorter, smaller attacks so common?
The prevalence of smaller attacks may seem unusual because it indicates DDoS attackers are not using their full capabilities. However, there are many reasons why shorter, smaller DDoS attacks have become more common.

Reason 1: The rise of DDoS-for-hire
In recent years, DDoS-for-hire platforms have become increasingly popular. On these platforms - also known as stressors - it is possible to rent an existing DDoS botnet to perform an attack against a target organization of the customer’s choosing.

On a DDoS-for-hire site, performing a short, relatively small attack is rather cheap, with prices ranging from $5 for 5 minutes to $400 for a full day. As these smaller attacks become easier to launch, we expect them to continue growing in popularity.

Reason 2: More network infrastructure is becoming vulnerable
Cybercriminals tend to focus their efforts where they can have the greatest impact. One way they do so is by attacking network infrastructure that is already struggling to manage a large amount of traffic.

Remote access solutions like VPNs and RDP are an example. The COVID-19 pandemic has forced many organizations to drastically increase their usage of these services as a large percentage of the workforce telecommutes. Such increases can quickly overburden the service, as seen from examples of large, established organizations having to ration VPN usage to prevent broader network outages.

Sure enough, remote access solutions have been the target of DDoS attacks since the beginning of the pandemic. In such an attack, the perpetrator may be able to launch comparatively smaller attack traffic and still disrupt the target organization’s ability to handle that traffic.

Reason 3: Preparation for a ransom demand
If a company has a DDoS mitigation solution in place, a small attack may have little or no impact on the availability of services to legitimate users. However, these small attacks may not be the attacker’s final objective.

In recent years, Ransom DDoS attacks have emerged where an attacker threatens to perform a DDoS attack if a ransom demand is not met. In many cases, the groups demanding the ransom will pretend to be well-known threat actors like Fancy Bear, Cozy Bear, or the Lazarus Group to induce the victim to pay up.

A small-scale DDoS attack can be used as a lead-up to a Ransom DDoS demand. By demonstrating the ability to perform even a small DDoS attack, the attacker increases the probability that a target organization will pay to avoid the risk of a large-scale DDoS attack.

Reason 4: Evasion of legacy DDoS mitigation systems
Early DDoS mitigation solutions were designed to identify and block large volumes of traffic. These systems may only turn on if traffic volumes exceed a set threshold.

Smaller-scale DDoS attacks can evade the protections provided by legacy DDoS mitigation solutions that rely on these thresholds to identify a potential attack. By remaining just below the threshold at which the defense would trigger, these attacks can disrupt the target networks’ operations without needing to overwhelm the defenses the organization may have in place.

Reason 5: Network defense exploration
Large-scale DDoS attacks can be expensive and require significant resources to perform. An attacker’s use of a small DDoS attack may be intended as reconnaissance for a later attack.

If an organization has a DDoS mitigation solution in place, a small DDoS attack will have no impact on the performance of the application under attack. In contrast, an unprotected application may experience measurable latency from even a small DDoS attack. By using a smaller-scale attack, it is possible to identify which organizations have defenses and which do not, providing useful information for planning later attacks.

Reason 6: Concealment of other attacks
Many DDoS attacks are designed to be noticeable. If successful, a DDoS attack takes down the network application under attack, providing an organization’s security team with a clear problem that it needs to solve. The importance of network infrastructure for communicating with and providing services to customers makes addressing the attack a priority.

For these reasons, DDoS attacks can be used as a “smokescreen” for other types of attacks that might be detected and blocked by an alert security team. If an organization is focused on remediating the DDoS attack, they may not be paying sufficient attention to notice an attempted data breach or infiltration of malware into the network. A small-scale DDoS attack may not be enough to take down an organization’s systems, but it can be enough to distract from the real threat.

What risks do these smaller attacks pose?
While smaller DDoS attacks may feel like less of an immediate threat than larger ones, they still present organizations with a number of risks. In some cases, a small attack can still take infrastructure down, or at least hurt its performance. Additionally, smaller DDoS attacks can help attackers look for security gaps or distract their targets from other attacks using different methods altogether.

Risk 1: Vulnerable infrastructure takedown
Organizations that have implemented a robust DDoS mitigation solution will be shielded from even the largest DDoS attacks. The same cannot be said of unprotected or underprotected networks — especially if those networks are already overburdened.

A small DDoS attack involves up to half a gigabyte of malicious data reaching an organization’s network infrastructure each second. An organization’s network may have potential bottlenecks including:

Network bandwidth

Open TCP connections

CPU utilization

If the capacity of any of these resources is exceeded by the attack, the network will be unable to process legitimate requests.

Risk 2: Reduced network performance
Any request - legitimate or otherwise - to an organization’s network consumes resources. Under normal circumstances, most requests are legitimate, and any malicious requests have a small or negligible impact.

During a DDoS attack, on the other hand, malicious requests can outnumber legitimate traffic - often by orders of magnitude. Even if an attack does not take down the target service, increasing the operating costs of the site by orders of magnitude can have a significant impact on an organization's bottom line. The cost of processing spam requests uses up computational resources, and, if a company has a metered DDoS mitigation service, the cost of protection can be high.

Risk 3: Post-attack consequences
The impact of a DDoS attack can also last long after the attack is completed. In some cases, a DDoS attack may only cause an application to be unable to respond to legitimate requests while the attack is occurring but returns to normal after it is complete. In others, an attack may cause applications or servers to crash, forcing IT teams to restart the machines or software and restore any lost data (if possible). In the second scenario, a short, small attack may have an extended impact despite a relatively small price tag.

What should organizations do to prepare for these risks?
The best way that an organization can prepare for a DDoS attack is by deploying a DDoS mitigation solution. However, not all DDoS mitigation solutions are created equal. Some key qualities to look for include:

Always-on protection: Some DDoS mitigation solutions don’t turn on until malicious traffic reaches a certain threshold. Unfortunately, small-scale DDoS attacks can slip past these solutions. An always-on DDoS mitigation solution provides continuous protection against attack.

Security integration: DDoS attacks may be designed to act as a smokescreen for another attack. A DDoS solution integrated with other security tools can help with identifying the attack that a small DDoS attack is trying to conceal.

Edge-based scrubbing: Sending all network traffic to a central system for inspection and scrubbing increases network latency. Scrubbers should be distributed at the network edge to minimize performance impacts.

Unmetered DDoS mitigation: Some vendors will charge based on the network bandwidth being used at the peak of the attack, which can be crippling in the case of large-scale attacks. Look for a DDoS solution that eschews surge pricing.

DDoS attacks are growing more common, and attack techniques are evolving away from large-scale attacks to focus on smaller, shorter DDoS campaigns. Ensuring high web service availability and performance requires investment in a leading DDoS mitigation solution.
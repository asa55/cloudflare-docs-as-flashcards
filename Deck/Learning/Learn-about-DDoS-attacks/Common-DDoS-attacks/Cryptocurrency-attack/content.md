##

What is a cryptocurrency?
A cryptocurrency is a form of digital currency that has two key differences which distinguish it from traditional money. First of all, cryptocurrency is not tied to or backed by any government, making it a truly international form of currency. Secondly, cryptocurrency is always decentralized.

What is the difference between centralized and decentralized currency?
Traditional money is centralized. If someone who has US Dollars puts their money in a brick-and-mortar bank, that bank will be responsible for keeping track of that currency. The owner of the money will have to go back to that bank to take their currency out. Similarly, if that person wants to put their dollars into an online bank, that online bank will keep a record of the amount of money in that person’s account in a central server. That bank’s central server is the authoritative source of information for that person’s account. In both these cases, the currency is centralized, meaning it’s kept track of in one place.

With cryptocurrencies, the information about the amount of currency each investor owns is stored across many (often thousands) different computers, known as nodes. The information on these nodes are publicly accessible, and there is no single central authority responsible for keeping track of these accounts. This means whenever a transaction happens, every node has to be updated simultaneously to ensure that the ledgers in all the nodes remain in sync.

It is very important that all these nodes remain in sync, because otherwise the currency would be invalidated by the possibility that someone spends the same money twice before all the ledgers have a chance to update; this is known as double-spending. Double-spending of cryptocurrencies is prevented by a process called blockchain.

What is blockchain?
Blockchain is the technological breakthrough that made cryptocurrency a possibility. A full technical explanation of blockchain is beyond the scope of this article, but the important takeaway is that blockchain requires mining.

What is cryptocurrency mining?
Mining of cryptocurrency is a process where a computer spends time solving a highly complex math problem, and once that problem is solved, a set of cryptocurrency transactions gets added to a queue of similar sets of transactions which will be broadcast to all the nodes, updating their ledgers. In order to encourage mining, computers which solve these complex math problems are rewarded for doing so with newly minted coins of the currency they are mining. This is how new cryptocurrency comes into circulation.

Why are cryptocurrencies being DDoSed?
Like most high-visibility business, coin exchanges have been targeted with DDoS attacks. With the surge in interest and the resulting increase of traffic around cryptocurrencies, the door has been opened for bad actors to attempt to disrupt cryptocurrency resources, denying cryptocoin users access.

A distributed denial-of-service (DDoS) attack is one of the primary methods of disruption in the modern Internet. By overloading a target with bogus traffic, a bad actor is able to render a website or service unavailable. The popularity and importance of cryptocurrencies makes them a prime target for attack.

We’ve been analyzing some of the DDoS attacks hitting the many coin exchanges on our network in order to gauge any discernible patterns of interest. The most prominent volume of DDoS traffic originated from SSDP amplification attacks, NTP amplification attacks, and application layer attacks.

One popular coin exchange service has been flagged for 76 application layer DDoS attacks over about a year, though it’s worth noting that the incredible surge in traffic may create false positives where normal traffic may show some signs of being an attack. Regardless, it’s clear that bitcoin exchanges have become prime targets for DDoS.

Here’s a graph showing the number of potential application layer attacks targeting popular cryptocurrency web properties through mid December 2017.

Cryptocurrency DDos Attack Frequency
Of particular interest is the huge spike in attacks around November 11. During this time a number of blockchain currency provider sites appear to have been targeted. Luckily, our DDoS mitigation software and infrastructure were able to prevent service disruption.

Even in the best of circumstances, many of the websites and applications related to bitcoin and other cryptocurrencies do not have the resources to deal with a massive surge in traffic. Such increases can occur during a DDoS attack or during high levels of normal activity, resulting in temporary outages and denial-of-service. Hosting content on a CDN can be essential to keeping a site online, though it may also take a properly load balanced network of servers to be able to handle the number of database requests a surge can produce. Learn more about Cloudflare’s DDoS Protection, which is helping keep many high traffic cryptocurrency services online.
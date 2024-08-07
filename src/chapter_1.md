# Chapter 1

The Dunning-Kruger effect shows that when you start learning a skill, you often have very high confidence in yourself and your skill because of how little you know about what you're doing. As you actually start learning, your confidence drops, and over time, as you begin to master the skill, your confidence increases again, but this confidence is now backed by your actual skill. The same applies to privacy and security. Initially, when you start, you might think that opening an incognito tab makes you safe, and nobody knows what you're doing. But as you learn more, paranoia can creep in because you realize how vulnerable you actually are. However, over time, you will build confidence and actually feel safer, and this time, you are genuinely safer than before.

In the first chapter, the focus will be on uncovering some privacy and security myths that most newbies in the world of privacy believe in, which can actually make your privacy worse by making you more unique while providing no actual benefit.

## I have no enemies

The first myth, and apparently the biggest one in the world of privacy, is what I call the "I have no enemies" phenomenon or what you might know as "I have nothing to hide."

As I mentioned in the introduction, even if we don’t have things to “hide,” we certainly have things we want to protect. Or maybe it’s not about us; perhaps people we know and care about have things to hide, and we could be the weak link in their privacy.

You and I don’t have enemies today; we don’t have things to hide today. But can we say for sure that this will be true in five or ten years? Certainly not. We don’t and can’t know what will happen. Our current privacy can serve as insurance for what may happen later.

Imagine someone managed to gather your personal information and used it for illegal activities. Would it be harder to convince the police or FBI that you didn’t do it than to protect your personal information in the first place? Or maybe, ten years later, if Google turns evil and acts as a “terrorist detection tool” for the government, and while traveling with your wife and kids, they pull up your emails, search histories, and ad suggestions. If, because of your search on explosives last year for your kid’s birthday and the ad suggestions you received, you are flagged as a terrorist, you could end up spending the rest of your life on a watchlist.

But I assume if you are reading this book, you probably understand the importance of privacy, especially in this day and age when it is one of the least respected human rights. However, we all can change that. The blame for this situation falls on governments, doxxers, companies, and those so-called "national security agencies." Nevertheless, the responsibility to make things right is on us. We should protect our privacy.

## I'd just go incognito

If you ask someone who's not familiar with how the internet works what they would do to become totally anonymous online, they might say, "I'd just open incognito mode." This is probably the most common myth in the privacy world among those who aren't tech-savvy—that incognito mode means no one will be able to track them or see their activities online. But that's far from reality. All incognito mode does is prevent the browser from saving your history and logins.

Your ISP still knows what you're doing, the websites you visit know your IP address, and you remain unique and fingerprintable. Incognito mode does have some privacy benefits, particularly if you use someone else's computer; in that case, you wouldn’t want your cookies, search history, or logins to be stored on their device. However, it doesn't contribute much to your overall privacy or security beyond that.

To hide your activities, you would need something that encrypts your requests and reroutes them to the destination you want to go, such as a secure proxy, an SSH tunnel, or a VPN. However, the sites you visit can still fingerprint you and track you across other websites. I’ll cover these in depth in the next chapters.

## VPNs are Anonymous

This is kind of the biggest myth in the privacy and anonymity world: that if you use a VPN, nobody will know what you’re doing, and you’ll become totally anonymous. But that’s completely wrong. See VPNs as shifting the trust from your ISP to your VPN provider. When you connect to your VPN, you are now letting them see what your ISP was seeing before.

Also, they don’t do a good job at hiding your real IP. With most VPN companies, a court order can compel them to hand over all the logs and data they have on you, and usually, they have a lot. There are some exceptions, though; some companies like Mullvad, ProtonVPN, and Windscribe have built their companies based on the privacy of their users. They can be signed up for anonymously, paid with cash or crypto, and they don’t log user traffic and activities. But still, that doesn’t make them an anonymity tool.

Even if your VPN provider doesn’t log anything, the data centers hosting their servers surely will. Another issue is that VPNs are vulnerable to traffic analysis. VPN traffic can be analyzed to find patterns that indicate the source and destination of your traffic, and that is fine; VPNs aren’t meant to be an anonymity tool after all.

Another problem with VPNs is fingerprinting. With Tor, you have the Tor Browser, which is designed to make all Tor users look identical. But with VPNs, you’re the most unique person on this planet, especially if you have a browser that is modified in any way or if you’re using an operating system like Linux or BSD. Smallest changes can make you super unique when it comes to fingerprinting, and that’s what you don’t want for anonymity. For privacy, though, that would be fine. You can safely use a hardened Firefox, for example, for your personal usage, like watching YouTube and paying your bills. That’s actually a good move. In that scenario, you don’t need to look like everybody else; you can be unique. I’ll cover fingerprinting more in the next chapters.

If you want to keep your anonymity, you should use tools specifically built for it, like Tor (and the Tor Browser). What Tor does is what its name stands for: The Onion Router. It works like an onion; it encrypts your data in three layers. As the data passes through each Tor relay, one layer of encryption is removed, revealing the address of the next relay in the chain until the data reaches the final destination. When browsing the clearnet with Tor, your last relay will be a node called the exit node. The exit node can see the data inside your packet, but it won’t know for sure where the origin of the packet is. To trace a packet back to its sender, all relays that your traffic passes through must be controlled by one person, and that’s very unlikely and costly to implement. When you browse websites hosted on the Tor network, your data is end-to-end encrypted with the website’s public key (the website’s address is the public key, and that’s why Tor addresses are so long and hard to memorize). So nobody in the middle can open the traffic; they will just pass it through until it reaches its destination.

There are other anonymity tools as well, such as Lokinet (which is the newest) and I2P. Both are technically more anonymous than the Tor network, but technicality isn’t everything. I2P and Lokinet both have very limited nodes compared to Tor, which makes the network more vulnerable. Additionally, neither provides a browser like the Tor Browser to prevent fingerprinting of users. For now, the best option is Tor, both because of its proven track record over the years and its considerable number of volunteer nodes and relays, and also because the Tor Browser does a great job at making Tor users identical to each other when using the Tor network.

Something to keep in mind when using the Tor Browser is that you shouldn’t modify anything. Leave it as is; don’t install plugins or tweak it. The Tor Browser is meant to have similar fingerprints to other Tor Browsers, and even the smallest changes might make you the most unique person on the Tor network.

## I'm using a strong password
Another myth that I see a lot of normies believing is that they have to have a strong password—something random and hard to memorize. Having strong passwords is a must, but having a strong password for everything not only doesn’t contribute much to your security but also makes you very vulnerable.

Imagine you use your strong, complicated password for every site you’ve ever signed up for. If one of these sites didn’t store your password properly and they got hacked, and their database went public, now anybody can use that same password for any other website or service you’ve signed up for, and they’d log in.

Instead of bothering with memorizing a really hard password, you should use a password manager, either something locally stored like KeePass or something online like Bitwarden.

Those password managers that store passwords locally are obviously more secure than the online ones, simply because if anyone wants to get access to their database, they’d have to gain access to your computer. I’m not saying it’s not possible to gain access to your computer, but Bitwarden’s servers might be far more targeted than your personal device. Other than that, they’re both fully encrypted. Even if something got leaked someday, your data will be securely stored and nearly impossible to access, at least with the tools and computers we have today.

Your password manager can then be accessed using a passphrase (not a password). Passphrases are way more memorable while being a lot more secure. A passphrase can be something like: `Name-Seat-Look-Chair-Plane7-Stree7`—just 6 words, one punctuation character, and 7s instead of the letter T. Compared to a password like `*&(*747983HJGHgdgsutpshlnb`, the passphrase will be more secure while being memorable.

## Big Tech is evil
There is this idea, even among people who are not normies, that big tech companies are evil, and that they have bad security and bad privacy. That might be true for privacy, but not much for security. Companies like Google and Microsoft probably have good security, but we can never be sure.

This is because they’re not open about how they have implemented things. We can’t see what they do to protect our data, and that’s what makes them untrustworthy. A company like Signal has its server, client, and encryption schemes open-sourced for the public. On the other hand, something like Telegram only has its client open-sourced, and that’s it. We don’t know much about the server or even their encryption scheme, which they brag is unbreakable. In this situation, we say Telegram is not good for its purpose, which is messaging people. It is not secure. 

However, in the case of something like Google Drive, which gives you a reasonable amount of free cloud storage, you can use it. If you already have a Google account associated with your identity, you can use Google Drive to upload some encrypted data that you don’t have space for. Just because it’s Google doesn’t mean that it’s pure evil, and there can be uses for it. You can use Google once you are self-conscious of your privacy.

Although every day more and more privacy-friendly alternatives are coming out, so in the near future you might not need to use Google or other companies like it.

## Open-source means private

Yes, open-source software is more transparent than proprietary software and has the potential to be more secure and private, but transparency and potential alone don’t make them more private or more secure. You need to look for independent audits of the software you are about to use. Also, being proprietary doesn’t mean they’re less safe. Look for the reputation of the software and the maintainers of it and whether they are audited or not.

---



These were some of the most common myths about privacy and security online. There are endless myths that people believe in. In these situations, we should be logical rather than biased. We need to plan out what we need to do, what is worth our time and energy, and the next chapter is about that—about threat modeling and common threats that you need to know before you start designing your threat model.
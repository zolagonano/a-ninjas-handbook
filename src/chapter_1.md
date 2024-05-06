# Chapter 1

The Dunning-Kruger effect manifests when you begin learning a skill. Initially, you have high confidence in yourself and your abilities due to your limited understanding of the task. As you delve deeper into learning, your confidence declines as you realize how much you still have to grasp. However, as you continue to master the skill, your confidence gradually rises again. This time, it's supported by your actual proficiency.

The same principle applies to privacy and security. Initially, you might believe that simply opening an incognito tab makes you safe and anonymous. But as you learn more, paranoia sets in as you realize how vulnerable you actually are. Yet, over time, you'll build confidence, and you'll feel safe again. This time, however, your safety is grounded in actual knowledge and skill.

In the first chapter, the focus will be on debunking some privacy and security myths that many newcomers in the world of privacy believe in. These myths can actually worsen your privacy by making you more identifiable while providing no real benefit.

## I have no enemies

The first myth, and perhaps the biggest one in the world of privacy, is what I call the "I have no enemies" phenomenon, or what you might know as "I have nothing to hide." As I mentioned in the introduction, even if we don't have things to "hide," we surely have things we want to protect. Maybe it's not even about us; perhaps people we know and care about have things to hide, and we could be the weak link in their privacy chain.

You and I might not have enemies today, and we might not have things to hide today. But can we say for sure that this will be true in five or ten years? Surely not. We don't and can't know what will happen. Our privacy today can serve as insurance for what might happen later.

Imagine if someone managed to gather your personal information and used it for illegal activity. Would it be harder to convince the police or FBI that you didn't do it than it would be to protect your personal information in the first place? Or maybe ten years later, if Google turned evil and worked as a "terrorist detection tool" for the government. When you're traveling with your wife and kids, they pull up your emails, search histories, and suggestions you've received. Due to your searches on explosives last year for your kid's birthday and the ad suggestions you received because of them, you get flagged as a terrorist. Now you spend the rest of your life on a watchlist.

But I assume that if you're reading this book, you probably understand the importance of privacy, especially in this day and age where it's the least respected human right. But we all can change that. The blame for this situation lies with governments, doxxers, companies, and those so-called "national security agencies." However, the responsibility to make things right lies with us. We should protect our privacy.

## I'd just go incognito

If you ask someone who's not familiar with how the internet works what they would do to become totally anonymous online, they might say, 'I'd just open incognito mode.' And that is probably the most common myth in the privacy world among normies. The belief that incognito mode means no one will be able to track them or see their activities online. But that's far from reality. All incognito mode does is it won't save the history and logins on the browser you're using. 

Still, your ISP knows what you're doing, the website knows your IP address, and you're still unique and fingerprintable. Incognito mode has some privacy benefits though, especially if you're using someone else's computer. In that case, you wouldn't want your cookies, your search history, or your logins to be stored on their device. But it doesn't contribute much more to your privacy or security than that.

To hide your activities, you'd need something that encrypts your requests and redirects them to your desired destination. This could be a secure proxy, an SSH tunnel, or a VPN. However, it's crucial to note that the sites you visit can still fingerprint you and track you across other websites. I'll cover these in depth in the next chapters.

## VPNs are Anonymous

This is kind of the biggest myth in the privacy and anonymity world: the belief that if you use a VPN, nobody will know what you're doing and you'll become totally anonymous. But that's completely wrong. Think of VPNs as shifting the trust from your ISP to your VPN provider. When you connect to your VPN, you're now letting them see what your ISP was seeing before.

Also, they don't do a good job at hiding your real IP. With most VPN companies, a court order will get them to hand over all the logs and data they have on you, and usually, they have a lot. There are some exceptions though. Companies like Mullvad, ProtonVPN, and Windscribe have built their reputations based on the privacy of their users. They can be signed up for anonymously, paid with cash or crypto, and they claim not to log user traffic and activities. But still, that doesn't make them an anonymity tool.

Even if your VPN provider doesn't log anything, the datacenters hosting their servers surely will. Another thing is that VPNs are vulnerable to traffic analysis; the VPN traffic can be analyzed to find patterns that indicate the source and destination of your traffic. And that's okay; VPNs aren't meant to be anonymity tools after all.

Another problem with VPNs is fingerprinting. With Tor, you have the Tor Browser, which is designed to make all Tor users look identical. But with VPNs, you're the most unique person on this planet, especially if you have a browser that is modified in any way or if you're using an operating system like Linux or BSD. Even the smallest changes can make you super unique when it comes to fingerprinting, and that's not what you want for anonymity. For privacy, though, that would be fine. You can safely use a hardened Firefox, for example, for your personal usage, like watching YouTube and paying your bills. That's actually a good move. In that scenario, you don't need to look like everybody else; you can be unique. I'll cover fingerprinting more in the next chapter.

If you want to maintain your anonymity, you should use tools specifically built for it, like Tor (and the Tor Browser). What Tor does is precisely what its name stands for: the onion router. It works like an onion, encrypting your data in three layers. As the data passes through each Tor relay, one layer of encryption will be removed, revealing the address of the next relay in the chain until the data reaches the final destination. When browsing the clearnet with Tor, your last relay will be a node called the exit node. The exit node is able to see the data inside your packet, but it won't know for sure where the packet originated. To trace a packet back to its sender, all relays that your traffic passes through must be controlled by one person, which is very unlikely and costly to implement.

However, when you browse websites hosted on the Tor network, your data is end-to-end encrypted with the website's public key (the website's address is the public key, which is why Tor addresses are so long and hard to memorize). Therefore, nobody in the middle can open the traffic; they will simply pass it through until it reaches its destination.

There are other anonymity tools as well, such as Lokinet, which is the newest, and I2P. Both of these are technically more anonymous than the Tor network, but technicality isn't everything. I2P and Lokinet both have very limited nodes compared to Tor, which makes the network more vulnerable. Additionally, neither of them provides a browser like the Tor Browser to prevent fingerprinting of users.

So for now, the best option is Tor, both because of its proven track record over the years and the considerable number of volunteer nodes and relays it has. Moreover, the Tor Browser does a great job of making Tor users identical to each other when using the Tor network.

Something to keep in mind when using the Tor Browser is that you shouldn't modify anything. Leave it as is; don't install plugins or tweak it. The Tor Browser is meant to have similar fingerprints to other Tor browsers, and even the smallest changes might make you the most unique person on the Tor network.

## I'm using a strong password
Another/ myth that I see a lot of normies believe in is that they have to have a strong password, something random and hard to memorize. Having strong passwords is a must, but having a strong password for everything not only doesn't contribute much to your security but also makes you really vulnerable.

Imagine you've used your password for every site you've ever signed up for. The password is really complicated and strong, though. But if one of these sites didn't store your password properly and they got hacked, and their database went public, now anybody can use that same password for any other website or service that you've signed up for, and they'd log in.

Instead of bothering with memorizing a really hard password, you should be using a password manager, either something locally stored like KeePass or something online like Bitwarden.

Those password managers that store the passwords locally are obviously more secure than the online ones, simply because if anyone wants to gain access to their database, they'd have to gain access to your computer. Not saying that it's impossible to gain access to your computer, but Bitwarden's servers might be far more targeted than you personally. Other than that, they're both fully encrypted. Even if something got leaked someday, your data will be securely stored and near impossible to access, at least with the tools and computers we have today.

Your password manager then can be accessed using a passphrase (not a password). Passphrases are way more memorable while being a lot more secure. A passphrase can be something like: `Name-Seat-Look-Chair-Plane7-Stree7`, just six words, one punctuation character, and 7s instead of the letter T. Compared to a password like: `*&(*747983HJGHgdgsutpshlnb`, the passphrase will be more secure while being memorable.

## Big Tech is evil
There's this idea, even among people who are not normies, that the big tech companies are evil. They're believed to have bad security and bad privacy practices. While this may hold true for privacy concerns, it's not necessarily the case for security. Companies like Google and Microsoft probably have good security measures in place, but we can never be entirely sure.

The reason for this uncertainty is that they're not transparent about how they implement things. We can't see what they do to protect our data, and that's what makes them untrustworthy. A company like Signal has its server, client, and encryption schemes open-sourced for the public. On the other hand, something like Telegram only has its client open-sourced, and that's it. We don't know much about the server or even their encryption scheme that they brag is unbreakable. In this situation, we might say Telegram is not suitable for its purpose, which is messaging people, as it is not secure.

However, in the case of something like Google Drive, which offers a reasonable amount of free cloud storage, you can still use it. If you already have a Google account associated with your identity, you can use that Google Drive to upload some encrypted data that you don't have space for elsewhere. Just because it's Google doesn't mean it's pure evil, and there can still be uses for it. You can use Google once you're self-conscious about your privacy.

Although, every day, more and more privacy-friendly alternatives are emerging. In the near future, you might not need to use Google or other similar companies.
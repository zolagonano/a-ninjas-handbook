# Chapter 2

Imagine you're playing Minecraft. You've respawned somewhere random on the map, and you don't have the geo-location of the house you had built. It would be really annoying and time-consuming, or sometimes even impossible (leading to frustration), to find your home in the game if you don't know where and in which direction to go. You run out of food, out of energy, and there will be nights with all the mobs—zombies trying to attack you, skeletons shooting arrows at you, and creepers blowing themselves up right beside you. But if you had the X, Y, Z coordinates of your house and the direction you needed to go, you could've gotten there before nightfall, before facing all those challenges.

In this book, I've planned to explain more advanced stuff as the chapters progress. So, the first chapter was about debunking some common myths about privacy and security. In this chapter, things get a little more actionable. This chapter will focus on threat modeling because I believe it's the most crucial step to take when you start your privacy journey. Otherwise, you'll spend a lot of time, stress, hard work, and sufferings without achieving your personal needs.

Having a threat model can be the equivalent of having the location of your house in Minecraft written down on a paper. Whenever you go far away from your home, you know where to go to get back. In the case of privacy and security, you'll be understanding what threats are relevant to you personally, what you want to protect, and taking actions based on that. Instead of blindly using Tor on Whonix OS for no actual reason and making your own life harder and even worsening your privacy in the process.

## There's nothing called full security

Nothing can be fully secure, fully private, or fully anonymous. When it comes to threat modeling, you need to make sacrifices. You should prioritize what matters the most and work on those areas, rather than wasting time trying to make everything private and secure, which would be impossible.

A threat model is a list of the threats that are most likely to happen. You can't protect yourself from every threat, never. However, you can work on protecting yourself from those that are most likely to occur.

For example, for a rapper, the most likely threat could be their music getting leaked. When designing your threat model, you should address these questions:

- What do I need to protect the most? In the example of the rapper, the unreleased music would be the answer.
- Who do I need to protect it from? For the rapper, this could include online hackers and those physically with access to the songs.
- What are the chances of it happening? For the rapper, if they're famous enough, it's quite likely.
- What will happen if I fail? For the rapper, this could cost them financially.
- What can I do to protect it? For the rapper's example, they could use encrypted hard drives and restrict access to prevent human errors.

### What do I need to protect the most?

To answer this question for yourself, you first need to list what you value the most. It could be your digital assets, like your cryptocurrencies, the information you have, such as your emails, contacts, messages, or important files. Whatever you value, write them down.

Make your list like this: specify what data it is that you're protecting, how and where you're keeping it, who you want to allow access to it, and what can be done to prevent unauthorized access.

Once you've written your list, prioritize it based on the most valuable to the least valuable data. Then, you can take a step forward.

### Who do I need to protect it from?

It can be anyone or anything, depending on your personal situation. For an activist, for example, it could be governments. For someone protesting against fascism, it could be neo-Nazi hackers and doxxers. For a business, it could be their competitors.

Try making a list of those who might be interested in getting their hands on your assets or data. Your list can include individuals, federal agencies, corporations, doxxing groups, cults—anything you think might be relevant.

This list can help you understand what and who you're up against, what they can do, and what costs they might be willing to pay to get their hands on your data. It helps you see more clearly and realistically.

### What are the chances of it happening?

Not everything that might happen will happen. Write down the threats that you think are likely to occur, as many as you can think of, and then rate them based on their probability. Is it highly probable to happen? Is it unlikely? Is it even possible to protect your data against it?

For example, you might get struck by lightning when it's raining and die, but how probable is that? Would you find an insulating shelter until the rain ends? No, because there's a low chance of it happening. Or you might crash your car every time you get behind the wheel to drive, but do you stop driving? No. Or you might get shot if you go to a gang war zone, and you probably won't, because it's quite likely to happen. The same applies to your threat modeling—you need to rate the threats based on their probability of happening.

### What will happen if I fail?

Next, you need to consider the consequences of failing to protect your data. For example, if an anti-fascist protester's home address and information are put online by doxxers, it could pose physical threats to their safety. If a company fails to protect its data, hackers or competitors might corrupt all the company's data, leading to bankruptcy. Or, in my case, if someone were to read the memes I send to my friends on Telegram, probably nothing horrible would happen to me.

You need to write down what the attackers might want to do when they get their hands on your data. Will the harm they cause be minor enough that you wouldn't bother? Or is it severe enough that it could be life-threatening? You need to address those potential consequences.

### What can I do to protect it?

Then, you can move on to researching what can be done to protect that data, what costs come with those measures, and how much they'll complicate your life, or if you're willing to make the effort.

For example, if you have cryptocurrencies, you can explore how to protect your assets. You might need to implement multisignature wallets, or store your assets offline on a secure and dedicated machine with encryption and no additional software.

### Then you take action

After designing your threat model, you can move on to taking action. For example, with cryptocurrency assets, you can start by backing up your assets on paper, storing them somewhere safe, using an offline and audited wallet, downloading your own blockchain instead of relying on other nodes run by others, or even purchasing a dedicated machine specifically hardened for this need and purpose.

You might create a checklist at this point to ensure you don't forget anything and implement all the actions you believe will keep your data secure.

## Common threats when threat modeling

Different threats require different actions; there would be no action you can take to protect yourself from all of them. And that's fine—you don't need to. That's why you designed a threat model: to take actions on the most probable and most consequential threats based on your own personal situation.

Your threats might not be among this list of common threats; they might require their unique strategies to protect yourself against. Again, you should act on your threat model. These are some concepts that I will refer to in this book, especially in this chapter:

- Anonymity: Separating and protecting your real identity from your online activities, shielding yourself from anyone or anything wanting to unveil your vigilante mask and expose your real face.
- Targeted Attacks: Shielding yourself from hackers, doxxers, government agencies, etc., that are specifically trying to get their hands on your data.
- Passive Attacks: Defending yourself against attacks that target a large group of people, like when a company gets hacked and their data breaches to the public, or malware and scammers targeting thousands of people.
- Supply Chain Attacks: Attacks that occur because of a vulnerability in a dependency of a trusted program, like the Linux distros getting backdoored because of a backdoor in xz utils (CVE-2024-3094) in 2024.
- Service Providers: Protecting your data from service providers, like your ISP, usually through end-to-end encryption of your communications.
- Mass Surveillance: Shielding yourself from surveillance systems that target the mass population, usually done by governments, but the websites that track you across the web are also in this category.
- Big Tech Surveillance: Safeguarding yourself from big tech companies that profit from tracking you on the internet and selling your data for advertisement, like Google, Facebook, etc.
- Public Exposure: Limiting the data available of you publicly on the internet, for example, your personal data indexed by search engines, etc.
- Censorship: Bypassing digital censorship or avoiding being censored when using the internet or putting something out on the internet.

### Anonymity vs Privacy

Anonymity is totally different from privacy, but privacy is required to achieve anonymity. Anonymity is when Daredevil goes out at night to fight the Russians working for Wilson Fisk. They don't know that Daredevil is Matt Murdock, but they know what he does. Matt Murdock has untied his personal identity, which is a blind attorney, from his vigilante identity, which is this badass dude in a black and red suit fighting crime in Hell's Kitchen. Matt Murdock is anonymous when he's Daredevil, and the Wilson Fisk and every other criminal he has fought are the attackers who would love to unveil his identity and find out who's behind this mask.

Here in this example, Matt Murdock has used privacy to achieve that anonymity. He has separated his identity in a way that nobody would be suspicious of him being Daredevil. He pretended all the years that he can't see anything, can't even walk without his cane, and even if he was injured, he would say that he fell down some stairs. And that's the privacy there, protecting his anonymity. He decided for people to see this side of Matt Murdock, not the Daredevil side of him.

The same thing applies in the online world, but here the tools are different. The masks are digital tools using encryption and onion routing, but the concept is the same. If you're some kind of vigilante like Matt Murdock, you probably need to protect and separate your real identity from your vigilante identity.

### Targeted Attacks

Daredevil was targeted too; all of the Hell's Kitchen criminals were after him. So he needed to protect his identity and anonymity while defending himself against targeted attacks from one of the most powerful villains of New York, the Kingpin. But who else might be in a situation like Daredevil's? Whistleblowers, activists, and protesters. However, they need different tools than Matt Murdock. They might need the Tor browser rather than a mask, or end-to-end encryption tools to communicate and store data rather than an indestructible suit made by Melvin Potter.

But if you think the NSA, CIA, and other agencies are after you, you can't run from them forever. You might be able to fake your death and live in a submarine, but they will probably find you. This usually falls into the category of threats that you'd rather not bother about because of how difficult it might make your life. Also, it is quite rare to be that targeted. Usually, those targeted by the NSA have the support of another corrupt government.

### Passive Attacks

This kind of attack affects most people of Hell's Kitchen, from Foggy Nelson to the Frank Castle, even the people of Gotham City. It affects both villains and heroes, from Batman to Harley Quinn. These attacks are usually towards large groups of people, like malware spreading on the internet. When WannaCry spread on the internet, it affected anything that had that vulnerable version of Windows; it didn't choose.

This kind of attack, in my opinion, is the most probable for the majority of people. We all have signed up for many websites in our lifetimes; a data breach in one of them would be really likely and can definitely affect us if we haven't taken any precautions.

### Supply Chain Attacks

Supply chain attacks can target even the most trusted programs by exploiting vulnerabilities in the programs they depend on. Sometimes, these attacks are targeted towards businesses or governments, but they can affect the mass population in the process. Preventing supply chain attacks is challenging; it requires time and energy to audit and test every dependency in the chain to be sure, but even then, there are always flaws. Nothing can be fully secure.

But how are these attacks performed? There are several common methods:

- Someone with enough power and a high enough position in a company or developer team can have the authority to add malicious code to a software.
- In the open-source world, someone can contribute malicious code in a way that it gets added to the codebase unnoticed.
- The author and maintainer of a library or dependency can decide to inject a backdoor into the code.

#### Minimizing the Risk

While the risk can't be fully eliminated, there are ways to reduce it:

- Software and services from big companies like Google generally have a good reputation and better security than software developed by a small team or an individual.
- Checking the commits, changes, and contributors in the case of open-source software.
- Frequently checking for known security flaws in software.
- Using independently audited software.
- Sandboxing and isolation to minimize the impact of possible attacks.

### Service Providers
Your ISP can see all your traffic, much like Joker has put a GPS tracker on Batman's Batmobile. Joker knows where Batman is going, and he can log that information as well. However, thanks to TLS and HTTPS, the data that ISPs can see has become limited. They can know the IP address, the Server Name Indicator (SNI) of your traffic, and the DNS queries. But there are fixes for this. We can encrypt DNS, encrypt the client hello and SNI, and then all your service provider would see is the destination IP and timestamps if TLS is enabled for that website or service.

Here, you can shift the trust from your ISP to a VPN provider that doesn't log your traffic and allows you to sign up anonymously, such as Mullvad and ProtonVPN. However, this is just shifting the trust, not eliminating it. For that, there are other tools made, like TOR, which would ensure that no one in the middle would be able to see where you are going and what you are doing if you use the websites on the TOR network and not the clearnet. Using encrypted DNS is also shifting the trust; still, the DNS server knows you and when and where you wanted to go. Luckily, TOR has its own DNS as well.

### Mass Surveillance

David Liberman, also known as Micro, was an NSA analyst and hacker who, when trying to expose the CIA's drug transshipment in Afghanistan, got "killed" by a corrupt Homeland Security agent. However, he survived and gained access to all CCTV cameras and everything that these government agencies had access to so he could find Frank Castle, aka Punisher, to help him kill all those who were a threat to his family so he could get back home. At least, that's what I remember from the show. The movie is not the point. This kind of act—spying on all people, spying on all internet traffic, logging every packet—is what's called mass surveillance. It affects everyone.

Governments usually justify this by saying that they're fighting terrorism, but in reality, it has little to no effect on crime, and some governments use it for social credit systems.

### Big Tech Surveillance

There is another kind of mass surveillance that isn't done by governments or agencies; it's done by big tech companies like Google and Facebook. Being the largest tech companies with the most internet users, they gather and collect a vast amount of data—sometimes even more than what governments collect in certain countries.

This kind of mass surveillance differs from that of governments. These companies don't deny their activities or claim it's for stopping terrorism or national security. They simply do it to sell the data they gather.

They make tons of money from your data by using it for advertising, tracking you across the internet. However, there are no guarantees that this won't go beyond being about money and advertisements. These companies might work with government agencies in the future as well.

### Public Exposure

When I was 8 years old, I created a personal website that included my name, email, and phone number. It took months of back-and-forth with Google and the blogging website to remove it from search engine results. This is what public exposure is: the data publicly available about you online, often put out there by yourself when you didn't care about privacy. It can be quite hard and sometimes impossible to take this information down. In fact, it's always impossible to truly delete something you've posted on the internet. This is why you should adopt the mindset that anything you say, post, or share online might stay there forever. Even if it's encrypted, you need to assume it will be read one day—maybe not in your lifetime, but eventually.

Prevention is the best treatment. The best way to keep your data private is to not make it public in the first place. Remember, nobody will call the cops on you because you didn't sign up on Instagram with your real identity. It's the internet, not the military or a bank. You don't need to use your real name, phone number, or home address. Keep your real phone number for people you know personally, not for every troll, doxxer, or whoever might use the internet. The same goes for your real name and other personal details.

### Avoiding Censorship

Sometimes you need privacy and security to avoid censorship, whether it's applied by a government, a platform like Twitter, or a Matrix server administrator. Most of us, including myself, hate censorship. Censorship holds society back from growth; it's like shutting off innovation, creativity, and new ideas. It is typically applied by those who need to protect their empires by force because they themselves know how wrong they are.

In this scenario, privacy tools like VPNs, proxies, encrypted DNS, and Tor can help you bypass censorship. Privacy-friendly platforms like Mastodon, which allow you to host them yourself, enable you to freely express your thoughts without someone like Elon Musk getting mad at you.

## The journey begins...

These were some of the common threats and common ways to design your threat model based on. It can vary based on your very unique situation; you need to address your own personal needs when it comes to threat modeling. But it's not something you should skip; otherwise, you would be lost, wasting time and energy on things you don't need. That's how I started my privacy journey—I didn't design a threat model. Instead, I tried to make myself bulletproof from every possible attack and ended up wasting a year of my life. I also gave myself long-lasting anxiety and paranoia for no reason, all because I didn't plan out who I'm protecting my data from.

That's it for this chapter. In the next one, I'll cover operational security, which I find to be not technical yet one of the most important aspects of privacy and anonymity online. Operational security, or OpSec, is about preventing sensitive data from getting into the wrong hands.

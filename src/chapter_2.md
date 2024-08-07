# Chapter 2

Imagine you're playing Minecraft, and you have respawned somewhere random on the map. You don’t have the geolocation of the house you built. It will be really annoying and time-consuming, or even sometimes impossible (you might give up due to frustration), to find your home in the game if you don’t know where and in which direction to go. You run out of food and energy, and there will be nights with all the mobs, zombies trying to attack you, skeletons shooting arrows at you, and creepers blowing themselves up right beside you. But if you had the X, Y, Z coordinates of your house and the direction you needed to go, you could have gotten there before nightfall and avoided all that hard time fighting mobs and getting nowhere.

In this book, I’ve planned to explain more advanced topics as it progresses. So the first chapter debunked some common myths about privacy and security, and in this chapter, things get a little more actionable. This chapter is all about threat modeling, as I believe it is the most important step to take when you start your privacy journey. Otherwise, you’ll spend a lot of time, stress, and hard work, and all the effort will be of no benefit for your personal needs.

Having a threat model can be the equivalent of having the location of your house in Minecraft written down on paper. Whenever you go far away from your home, you know where to go to get back. In the case of privacy and security, you will know what threats you personally face, what you want to protect, and take actions based on that, rather than blindly using Tor on Whonix OS for no actual reason and potentially making your life harder and even your privacy worse in the process.

## There's nothing called full security

Nothing can be fully secure, fully private, or fully anonymous. When it comes to threat modeling, you need to make sacrifices. You should see what matters the most and work on those areas rather than wasting time trying to make everything private and secure, which is impossible.

A threat model is a list of what threats are most likely to happen. You can't protect yourself from every threat, but you can work on protecting yourself from those that are most likely to happen.

For example, for a rapper, the most likely threat could be their music getting leaked. When designing your threat model, you should address these questions:

- What do I need to protect the most? In the example of the rapper, the unreleased music would be the answer.
- Who do I need to protect it from? For the rapper, that could be online hackers and those who are physically with him and have access to the songs.
- What are the chances of it happening? For the rapper, if he's famous enough, it's quite likely.
- What will happen if I fail? For the rapper, that could cost him financially.
- What can I do to protect it? For the rapper's example, he could use encrypted hard drives and restrict access to others to prevent human errors.

### What do I need to protect the most?

To answer this question for yourself, you need to first list what you value the most. It could be your digital assets, like your cryptocurrencies, the information you have, like your emails, your contacts, your messages, or some files that are important to you. Whatever you value, write them down.

Make your list like this: what data it is that you're protecting, how and where you're keeping it, who you want to allow to have access to it, and what can be done to prevent unauthorized access to it.

When you write your list, prioritize it based on the most valuable to the least valuable data. Then you can take a step forward.

### Who do I need to protect it from?

It can be anyone and anything; it's up to your personal situation. For an activist, for example, it could be the government. For someone who protests against fascism, it could be neo-Nazi hackers and doxxers. For a business, it can be their competitors.

Try making a list of those who might be interested in getting their hands on your assets or data. Your list can include individuals, a federal agency, a corporation, a doxxing group, a cult, anything—you know it better.

This list can help you see what and who you're standing against, what they can do, and what costs they might be willing to pay to get their hands on your data. It helps you see more clearly and realistically.

### What are the chances of it happening?

Not everything that might happen will happen. Write down the threats that you think are going to happen, as many as you can think of, and then rate them based on their probability of happening. Is it highly probable to happen? Is it rarely going to happen? Is it even possible to protect your data against it?

For example, you might get struck by lightning when it's raining and die, but how probable is that? Would you find an insulating shelter until the rain ends? No, because there's a low chance of it happening. Or you might crash your car every time you get behind the wheel to drive, but do you stop driving? No. Or you might get shot if you go to a gang war zone, and you probably won't, because it's quite likely to happen. The same goes for your threat modeling; you need to rate the threats based on their probability of happening.

### What will happen if I fail?

Then you need to see what the consequences of failing to protect your data are. For example, for an anti-fascist protester, if doxxers put his home address and all information online, it could pose physical threats to him. Or, if a company fails to protect its data, hackers or competitors might corrupt all the company's data and drive it toward bankruptcy. On the other hand, if I, who sends memes to my friends on Telegram, have my messages read by someone, probably nothing horrible will happen to me.

You need to write down what the attackers might want to do when they get their hands on your data. Will the harm they cause be so little that you wouldn't bother? Or is it so significant that it could be life-threatening? You need to address these questions.

### What can I do to protect it?

Then you can move on to doing your research, seeing what can be done to protect that data, what costs will come with it, and how much it will make your life harder. Are you willing to take the effort?

For example, if you have cryptocurrencies, you can see how you might protect your assets. You might need to implement multi-signature wallets or store your assets offline on a safe and dedicated machine with encryption and no additional software on it.

### Then you take action

After you design your threat model, you can move on to taking action toward it. In the example of cryptocurrency assets, you can start by backing up your assets on paper, putting it somewhere safe, using an offline and audited wallet, downloading your own blockchain instead of relying on nodes run by others, and even buying a dedicated machine specifically hardened for this need and purpose.

You might create a checklist at this point to make sure you don't forget anything and implement all the actions you think would keep your data secure.

## Common threats when threat modeling

Different threats require different actions; there is no action you can take to protect yourself from all of them. And that's fine—you don't need to. That's why you designed a threat model: to take actions on the most probable and most consequential threats based on your own personal situation.

Your threats might not be among this list of common threats. They might require unique strategies to protect yourself against. Again, you should act on your threat model. These are some concepts that I will refer to in this book, especially in this chapter:

- **Anonymity:** Separating and protecting your real identity from your online activities, protecting yourself from anyone/anything wanting to take your vigilante mask and see your real face.
- **Targeted Attacks:** Protecting yourself from hackers, doxxers, government agencies, etc., that are specifically trying to get their hands on your data.
- **Passive Attacks:** Protecting yourself from attacks that target a large group of people, such as when a company gets hacked and their data breaches to the public, or from malware and scammers targeting thousands of people.
- **Supply Chain Attacks:** Attacks that happen because of a vulnerability in a dependency of a trusted program, like the Linux distros getting backdoored because of a backdoor in xz utils (CVE-2024-3094) in 2024.
- **Service Providers:** Protecting your data from service providers, like your ISP, usually through end-to-end encryption of your communications.
- **Mass Surveillance:** Protecting yourself from surveillance systems that target the mass population, usually done by governments, but also includes websites that track you across the web.
- **Big Tech Surveillance:** Protecting yourself from big tech companies that profit from tracking you on the internet and selling your data for advertisement, like Google, Facebook, etc.
- **Public Exposure:** Limiting the data available about you publicly on the internet, for example, your personal data indexed by search engines, etc.
- **Censorship:** Bypassing digital censorship or avoiding being censored when using the internet or putting something out on the internet.

### Anonymity vs Privacy

Anonymity is totally different from privacy, but privacy is required to achieve anonymity. Anonymity is when Daredevil goes out at night to fight the Russians working for Wilson Fisk—they don't know that Daredevil is Matt Murdock, but they know what he does. Matt Murdock has untied his personal identity, which is a blind attorney, from his vigilante identity, which is this badass dude in a black and red suit fighting crime in Hell's Kitchen. Matt Murdock is anonymous when he's Daredevil, and Wilson Fisk and every other criminal he has fought are the attackers who would love to unveil his identity and find out who's behind the mask.

In this example, Matt Murdock has used privacy to achieve that anonymity. He has separated his identity in a way that nobody would be suspicious of him being Daredevil. He pretended all these years that he can't see anything, can't even walk without his cane, and even if he was injured, he would say that he fell down some stairs. That's the privacy there protecting his anonymity. He decided to let people see this side of Matt Murdock, not the Daredevil side of him.

The same thing applies in the online world, but here the tools are different. The masks are digital tools using encryption and onion routing, but the concept is the same. If you're some kind of vigilante like Matt Murdock, you probably need to protect and separate your real identity from your vigilante identity.

### Targeted Attacks

Daredevil was targeted too; all of Hell's Kitchen criminals were after him. So he both needed to protect his identity and anonymity while protecting himself against targeted attacks from one of the most powerful villains of New York, the Kingpin. But who else might be in the situation of Daredevil? The whistleblowers, the activists, and the protesters. But they need different tools than Matt Murdock. They might need the Tor browser rather than a mask; they might need E2EE tools to communicate and store data rather than an indestructible suit made by Melvin Potter.

But if you think the NSA, CIA, and other agencies are after you, you can't run from them forever. You might be able to fake your death and live in a submarine, but they will probably find you. This usually categorizes as those threats that you rather not bother about because of how difficult it might make your life. Also, it is quite rare to be that targeted. Usually, those targeted by the NSA have the support of another corrupt government.

### Passive Attacks

This kind of attack affects most people of Hell's Kitchen, from Foggy Nelson to Frank Castle, even the people of Gotham City. It affects the villains and the heroes, from Batman to Harley Quinn. These attacks are usually toward large groups of people, like malware spreading on the internet. When WannaCry spread on the internet, it affected anything that had that vulnerable version of Windows. It didn't choose. 

This kind of attack, in my opinion, is most probable for the majority of people. We all have signed up for many websites in our lifetimes. A data breach in one of them would be really likely and can definitely affect us if we haven't taken any precautions.

### Supply Chain Attacks

Supply chain attacks can target even the most trusted programs by attacking other programs that our programs are built on. Supply chain attacks are sometimes targeted at businesses or governments, but they can affect the mass population in the process. These attacks are hard to prevent; they require time and energy to audit and test every dependency on the chain to be sure, but we can't be certain. There are always flaws—nothing can be fully secure.

So, how can these attacks be performed? There are a lot of ways; here are some common ones:

- Someone with enough power and a high enough position in a company or developer team can have the authority to add malicious code to a software.
- In the open-source world, someone can contribute malicious code in a way that it gets added to the codebase unnoticed.
- The author and maintainer of a library or dependency can decide to inject a backdoor in the code.

#### Minimizing the Risk

How can we minimize the risk? Well, it can't be fully eliminated, that's for sure. But there are ways:

- Software and services from big companies like Google usually have a good reputation and better security than software developed by a small team or an individual.
- Checking the commits, changes, and contributors in the case of open-source software.
- Frequently checking for known security flaws in software.
- Using independently audited software.
- Sandboxing and isolating to minimize the impact of possible attacks.

### Service Providers
Your ISP can see all your traffic, like the Joker putting a GPS on Batman's Batmobile. The Joker knows where Batman is going and can log those movements as well. However, thanks to TLS and HTTPS, the data that ISPs can see has become limited. They can know the IP address and the Server Name Indicator (SNI) of your traffic and the DNS queries, but there are fixes. We can encrypt DNS, encrypt the Client Hello, and SNI, so all your service provider would see is the destination IP and timestamps if TLS is enabled for that website or service.

You can also shift the trust from your ISP to a VPN provider that doesn't log your traffic and allows you to sign up anonymously, such as Mullvad or Proton VPN. But remember, this is just shifting the trust, not eliminating it. For that, there are other tools, such as Tor, which ensures that no one in the middle can see where you're going and what you're doing (if you use websites on the Tor network and not the clearnet).

Using encrypted DNS is also shifting the trust; the DNS server still knows who you are and when and where you wanted to go. Luckily, Tor has its own DNS as well.

### Mass Surveillance

David Liberman, also known as Micro, was an NSA analyst and hacker who, when he tried to expose the CIA's drug trafficking in Afghanistan, was "killed" by a corrupt Homeland Security agent. However, he survived. He gained access to all CCTV cameras and everything that these government agencies had access to, so he could find Frank Castle, aka the Punisher, to help him kill all those who were a threat to his family so he could get back home. At least, that’s what I remember. The movie is not the point. This kind of act—spying on all people, spying on all internet traffic, logging every packet—is what is called mass surveillance. It affects everyone.

Governments usually justify this by saying that they're fighting terrorism, which is not true in reality. It has little to no effect on crime, and some governments use it for social credit systems.

### Big Tech Surveillance

There is another kind of mass surveillance that is not done by governments or agencies; it is done by big tech companies like Google and Facebook. Being the biggest tech companies with the most internet users, they gather and collect a huge amount of data, sometimes even more than the government would do in some countries.

This kind of mass surveillance is different from that done by governments. The companies don’t deny it or claim it’s for stopping terrorism or national security; they simply do it to sell the data they gather.

They make tons of money from your data by using it for advertising. They track you across the internet. But there is no guarantee that it won't go beyond just money and advertising. They might work with government agencies in the future as well.

### Public Exposure

When I was 8 years old, I created a personal website for myself, which had my name, email, and phone number on it. It took me months, going back and forth with Google and the blogging website, to take it down from the search engine results. This is what public exposure is: the data that is publicly available about you online. It can even be put out there by yourself when you didn't care about privacy. It is quite hard and sometimes impossible to take it down. In fact, it is always impossible to truly delete something you have put out there on the internet. That's why you should set your mindset to assume that if you say something, post something, or share something, it might stay on the internet forever. Even if it's encrypted, you need to assume it will be read one day—maybe not in your lifetime, but eventually.

Prevention is the best treatment. The best way to keep your data private is to not make it public to start with. Keep in mind that nobody will call the cops on you for not signing up on Instagram with your real identity. It's the internet; you're not signing up for the military or opening an account at a bank. You don’t need to use your real name, phone number, and home address on the internet. Nobody needs to know these things about you. Keep your real phone number for those you know personally, not for every troll, doxxer, or anyone who might use the internet. The same goes for your real name and other personal details.

### Avoiding Censorship

Sometimes you just need privacy and security to avoid censorship, whether it is applied by a government, a platform like Twitter, or a Matrix server administrator. Most of us, including myself, hate censorship. Censorship holds society back from growth; it's like shutting off innovation, creativity, and new ideas. It is usually imposed by those who need to protect their empires by force because they themselves know how wrong they are.

In this scenario, privacy tools like VPNs, proxies, encrypted DNS, and Tor can help you bypass censorship. Privacy-friendly platforms like Mastodon, which allow you to host them yourself, enable you to speak freely without someone like Elon Musk getting mad at you.

## The journey begins...

These were some of the common threats and ways to design your threat model. It can vary based on your unique situation; you need to address your own personal needs when it comes to threat modeling. But it's not something you should skip; otherwise, you would be lost and waste time and energy on things you don’t need. That was how I started my privacy journey. I didn’t design a threat model; instead, I tried to make myself bulletproof from every possible attack. Not only did I waste a year of my life, but I also gave myself long-lasting anxiety and paranoia for no reason, all because I didn’t plan out who I was protecting my data from.

---

This concludes this chapter. In the next chapter, I will cover operational security, which, though not technical, is one of the most important aspects of privacy and anonymity online. Operational security, or opsec, involves preventing sensitive data from falling into the wrong hands.

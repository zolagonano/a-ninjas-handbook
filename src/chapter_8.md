# Chapter 8

Maintaining privacy, security, and anonymity requires skills, patience, dedication, and a lot of time. This book is supposed to be a starting point for the privacy journey of those people who need it, rather than being a complete guide, as such a thing never existed and never will. Most of the time, you need to do your own research, program stuff the way you need them, configure systems to make them private for you, and there aren't always resources to learn from. You need to learn by trial and error and playing around with different things. The more you expand your knowledge in different areas, the more you can combine them and find new solutions for a problem, and it can be for anything, not just privacy or security.

Your journey will be different than someone else's. What works for you won't work for others; you might need different skills than someone else. What is effective today might not be tomorrow; what is good today might become evil tomorrow. One thing that remains consistent in the privacy journey is the need to adapt because the world never stops changing, and privacy and security are part of it as well. Someday, most of the things in this book might become obsolete, and that is fine if you adapt to the new situation and try to find new strategies and solutions.

Privacy and security aren't destinations you can reach; they're the road and the journey itself. You might not even want to be 100% secure or private, even if it was possible (which it is not and will not be). The best you can do is to find a middle ground between ignorance and chronic fear and paranoia. The more you learn and expand your knowledge, the easier it might be to get there, as you are more aware of threats and know more about ways to protect yourself against them. The key is to remain cautious, persistent, and keep on learning and adapting to the changes.

In this chapter, which is the final chapter, I will go through some of the skills that I find important, but they're not everything. There are a lot more skills, a lot more tools, a lot more techniques that you might find useful. I tried to keep things more general so that most people can use them, but every unique situation needs unique solutions.

## Adapt the Hacker's Mindset

Hackers are driven by curiosity; they want to understand how things work, no matter what it is—even if it’s not computer-related. This curiosity involves continuous learning and staying updated with the changes in the world.

Hackers are also good at problem-solving and are creative. They enjoy finding unconventional solutions to problems, and their creativity allows them to see possibilities and connections that others might not notice.

Hackers are persistent and patient, willing to spend hours, days, or even months working on a problem until they solve it.

They pay close attention to details, noticing small elements that others overlook, which allows them to identify vulnerabilities and exploit them effectively.

They constantly test the limits of systems, pushing these limits to discover what’s possible.

Most importantly, hackers are collaborative, working in communities to share knowledge, tools, and techniques. Such communities allow them to build on each other’s work and ideas.

Hackers are aware of the risks involved in their activities and try to manage these risks, balancing potential rewards against possible consequences.

They are flexible thinkers who can adjust their strategies in response to new information or situations.

This hacker mindset helps you understand how systems work, identify potential privacy and security flaws, and explore and test systems to discover new vulnerabilities and ways to protect against them.

Thinking outside the box allows for creative solutions to privacy and security challenges. The ability to adapt strategies and develop new techniques helps protect yourself against new threats.

Paying close attention to detail ensures thorough security checks and correct implementation of privacy measures by noticing small, often overlooked vulnerabilities that could compromise privacy or security.

Persistently testing and evaluating systems helps you find hidden vulnerabilities you didn’t know existed. The continuous improvement that comes with persistent testing will enhance your security and privacy measures over time.

Risk assessment helps you understand potential consequences and implement more effective protections.

## Researching Skills

Researching is the biggest part of learning, in my opinion at least. You cannot gather information about a subject if you can't research properly for it. If you are able to research effectively from credible sources, extract relevant information, and synthesize that knowledge to form an understanding, that will not only help with your privacy and security journey but any other field as well.

### Using Search Engines Effectively

Search engines like Google not only can help with your research about privacy and security but research about yourself. If you can use them effectively, you can see what information of yours is indexed on them. This can be done by learning advanced search operators, such as `site:`, `inurl:`, `intitle:`, and Boolean operators (AND, OR, NOT) to filter the search results.

And also nowadays most search engines are basically artificial intelligences, so learning prompt engineering can help you a lot as well.

### Checking Sources

Checking for the credibility of websites and authors of an article or information and looking for reputable sources which have a good track of accuracy and reliability can save you from gathering wrong and inaccurate information about a subject.

To verify information, one thing you can do is to cross-reference it with multiple sources if possible, this will ensure its consistency and accuracy along multiple sources.

### Scholarly Databases

You can also use databases like Google Scholar, JSTOR, and IEEE Xplore to find peer-reviewed articles on privacy and security. And feel free to pirate them if you find it ethical (I find it ethical; knowledge and science shouldn't be behind paywalls, it is what drives societies forward).

### Follow Tech News Websites

Follow reputable tech news websites to see what is happening in the world. Also, following some security blogs with reputable authors can help a lot. You can follow the Hacker News (Y Combinator) feed with keywords related to privacy, security, anonymity, and tools like Tor, PGP, etc., to get new articles on them, usually from reputable authors with accurate and in-detail information. Also, you can follow forums and group chats dedicated to privacy and security, for example, Reddit’s r/privacy or the Matrix group chat of Privacy Guides and PrivSec, or Techlore and Surveillance Report on YouTube.

### Gather and Organize Information

When you research a subject, try gathering the information at first, then go through it, double-check it and organize it. It will be nice of you if you share it with others, making a positive change by sharing your newly earned knowledge.

## Data Management Skills

Having the ability to manage the data and information you share or store is one of the biggest skills required to maintain privacy and anonymity and keep good OPSEC. It includes practices and strategies to protect personal information from getting into the wrong hands, misuse, or breaches. Effective data management is a must in order to maintain data privacy and security. Here are some key skills needed for data management:

1. **Data Minimization**: Only share, collect, process, and store the minimum data necessary for a specific purpose. Avoid giving unnecessary personal information and opt for services that require minimal data. Share only essential information and avoid oversharing.

2. **Encryption**: Encrypt data at rest to protect data stored on devices or servers. Encrypt data in transit to protect data as it moves across networks. Use end-to-end encryption to ensure only the communicating users can read the messages.

3. **Access Control and Authentication**: Use multi-factor authentication systems to prevent unauthorized access to data and use **Role-Based Access Control (RBAC)** to limit access to data based on user roles (great for separating identities and users on a device).

4. **Data Retention Policies**: Define how long data should be kept and when it should be deleted. For example, you might want to delete all cookies on your browser every day and your server logs every week. It depends on your needs. Configure systems to delete data after a certain period and periodically review and delete unnecessary data.

5. **Metadata Management**: Metadata can reveal information about the data itself, like the creation date, author, or location. Always remove metadata from files before sharing them.

6. **Backup and Recovery**: Ensure backups are encrypted to protect data from unauthorized access. Regularly back up and follow a good backup strategy (explained in Chapter 5).

These are some of the skills and practices for data management. There are a lot more, and you can find more or create your own.

## Technical Skills

To obtain and maintain privacy and security requires a lot of technical skills, from programming to understanding networks and operating systems, encryption, and more.

So it should be obvious that you need to learn or level up your technical skills every day. I will point out some starting skills to jump-start your learning journey if you don't know where to start:

### Encryption

Encryption is an inseparable part of privacy, security, and anonymity; it’s the chain that connects these three together. Without encryption, there can be no security on the internet. It is really important to know what you're doing when it comes to encryption, as it can go wrong easily due to the complexities of mathematical attacks on encryption algorithms. You don't have to become a cryptographer or cryptography analyst; just having some basic understanding is enough.

You might want to learn about different algorithms, how they operate differently, what attacks can target encrypted information or the encryption process, what algorithms are not safe to use, which implementations of an algorithm are audited and good to use, and what schemes are best suited for your encryption needs. These are things you need to know.

A good starting course on encryption would be the "[Introduction to Cryptography by Christof Paar](https://www.youtube.com/@introductiontocryptography4223)," which can benefit you greatly in terms of a deep understanding of cryptographic algorithms. The course is freely available on YouTube. If it weren't, you could find it by searching elsewhere.

Having a deep understanding of encryption will also help with understanding other tools such as the Tor network, VPNs, multi-factor authentication devices, and more.

### Networks

All of your data are passing through computer networks every second. Knowing how these networks work and operate is a must to prevent attacks, leaks, and more. You need to know what is happening when you tunnel your network through VPNs or Tor. You should be able to monitor them for potential leaks, set up firewalls, block unauthorized access to your data, and configure your network for better security and privacy by default.

There are many courses from beginner to advanced on computer networks that you can take. As I said before, feel free to pirate them if you can’t afford them. There should also be plenty of good resources and courses for free on YouTube and other websites. What matters is learning and understanding the subjects. Much of it will come from real-life practice and experience as well.

### Programming

To automate tasks like backups, create tools for your specific needs, or read and check source codes of other programs, you need to know some programming. Learning one scripting language like Python or Bash scripting (especially for Linux users) and one system-level language like Rust (which has built-in safety features) would be more than enough.

There are a ton of resources, many of them high-quality and free, for programming that you can use to learn. It will make your journey much easier if you can automate repetitive tasks or build the tools you need that don’t exist. Also, be sure to adopt secure coding practices as you learn.

### Operating Systems

Having a deep understanding of your operating system is essential to obtain privacy and security. Especially learning and understanding Linux, as Linux is free and open-source, well-audited, and less likely to have zero-day vulnerabilities compared to Windows. It can be extremely customizable—you can make it operate exactly as you want, not more, not less. This is a great feature when it comes to operating systems. Also, most tools are available for Linux and other Unix-like operating systems.

There are courses like Linux Essentials for Beginners and LPIC1, LPIC2, LPIC3, and Red Hat courses for more advanced users. Make sure to start one of these courses if you decide to install Linux for your operating system, and follow the order from beginner to advanced as it can get confusing.

### Virtualization and Containerization

Understanding how virtualization and containerization systems and tools work will help you a lot with isolating different identities, separating tasks, and preventing malicious code from running on your actual system.

There are many resources on these two topics as well. I highly recommend learning about them as they are very useful tools for activity isolation, which is a key part of maintaining good security and privacy, in my opinion.

---

And the skills don't end here. Anything you learn comes in handy. As I said at the beginning of this chapter, the more skills and knowledge you have, the more you can combine them and create unique and better solutions to a problem.

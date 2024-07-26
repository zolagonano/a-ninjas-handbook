# Chapter 5

Encryption tools are a non-separable part of security, privacy, and anonymity online. You can't achieve anonymity if you don't have privacy, you can't have privacy if you are not secure, and you can't be secure if there's no encryption.

Encryption is like the house you build in Minecraft; it only allows you inside, not the zombies and the mobs, and keeps your stuff safe when you're not home. The encryption algorithm and scheme would be the material that your house is built with. A weak encryption scheme/algorithm is like a Minecraft house built with dirt or wood; it can be destroyed by a creeper blowing up near it or catch on fire if you accidentally light a flint on it. The more proven and tested the algorithm is, the more secure it becomes. So, the first rule of encryption is to never roll your own encryption, as that can be like building a Minecraft house out of thin air, with no structure and no good quality material, and it will fall apart with the most effortless attacks of a professional.

## Don't Roll Your Own Cryptography

If you're new to the cryptography world, you might think if a cryptographic algorithm is not known to others it will be more secure, but this is not true in any way. A cryptographic algorithm should be secure not because no one knows how the algorithm works but rather due to the security of the algorithm itself. It should go through all sorts of attacks, both the algorithm and the implementation of the algorithm. When it comes back untouched, then it is considered safe to use. For example, algorithms like AES, Twofish, Serpent, and ChaCha20 have all gone through the process of testing by actual mathematicians and cryptographers and have been around long enough for their security to be proven.

When you decide to create your own cryptographic scheme or algorithm, it's like witchcraft compared to a well-known cryptographic algorithm because you're not a mathematician, cryptographer, or cryptography analyst. You can't build your own algorithm nor test and attack your algorithm effectively. When your algorithm faces a real professional who has been working with this type of stuff for decades, your algorithm doesn't stand a chance.

Here is a quote from the book, *Introduction to Cryptography*, by the creator of PGP:

> When I was in college in the early 70s, I devised what I believed was a brilliant encryption scheme. A simple pseudorandom number stream was added to the plaintext stream to create ciphertext. This would seemingly thwart any frequency analysis of the ciphertext, and would be uncrackable even to the most resourceful government intelligence agencies. I felt so smug about my achievement.
>
> Years later, I discovered this same scheme in several introductory cryptography texts and tutorial papers. How nice. Other cryptographers had thought of the same scheme. Unfortunately, the scheme was presented as a simple homework assignment on how to use elementary cryptanalytic techniques to trivially crack it. So much for my brilliant scheme.
>
> From this humbling experience, I learned how easy it is to fall into a false sense of security when devising an encryption algorithm. Most people don’t realize how fiendishly difficult it is to devise an encryption algorithm that can withstand a prolonged and determined attack by a resourceful opponent.
>
> -- Creator of PGP, Phil Zimmermann

## Even the Most Secure Algorithms Can Be Vulnerable

It is not only the cryptographic algorithm that has to be secure; the implementation of it needs to be secure, well-known, and audited as well, both for hardware and software level implementations. Several attacks can be done through the implementation of an algorithm, for example:

- **Timing Attacks**: An attacker measures the time it takes to perform cryptographic operations and uses this information to deduce secret keys.
- **Simple Power Analysis (SPA)**: An attacker analyzes power consumption traces to extract keys or other sensitive information.
- **Differential Power Analysis (DPA)**: An attacker collects power consumption data over many encryption operations and uses statistical methods to deduce the secret key.
- **Electromagnetic (EM) Attacks**: An attacker uses EM emissions to gain information about the internal state of the device and extract secret keys.
- **Fault Injection Attacks**: An attacker uses techniques like voltage glitching, clock glitching, or laser fault injection to induce faults and analyze the erroneous outputs to deduce the secret key.
- **Cache Attacks**: An attacker uses cache timing information to infer which memory accesses are made during cryptographic operations and deduces secret keys.
- **Cold Boot Attacks**: An attacker freezes the RAM to preserve its state and then reads the memory contents after rebooting the system to extract encryption keys.
- **Differential Fault Analysis (DFA)**: An attacker compares faulty and correct outputs to deduce information about the internal state and secret keys.
- **Glitching Attacks**: An attacker uses power or clock glitches to cause incorrect operations in cryptographic algorithms, then analyzes the faulty outputs to extract keys.
- **Buffer Overflow**: An attacker crafts input data that causes buffer overflows and gains control over the execution flow to extract keys or sensitive data.
- **Side-Channel via Shared Resources**: An attacker running code on the same machine as the cryptographic software can use shared resource behavior to infer secret keys.
- **Physical Attacks**: An attacker uses techniques like microprobing to directly read out memory contents or manipulate hardware components.

These attacks can be done on algorithms that are considered unbreakable, only through the implementation side of things. All these attacks can be prevented as well. A well-known software or device that has been audited is probably secure against all or most of these attacks.

Some best practices would be keeping the software updated, looking for independent audits, using proven libraries (if you are developing a tool that needs encryption), and using standard encryption algorithms, modes, and schemes.

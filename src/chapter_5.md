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

## Encrypt Your Data at Rest

Encryption doesn't always have to be for communication channels, messengers, VPNs, etc. Your offline data needs encryption too. Just like when you put your important stuff in a safe box and it is available to you only when the safe box is opened, your data on your phone, computer, NAS, USB sticks should be encrypted as well, so only when they are opened is their data available. At rest, encryption doesn't mean that if malware finds its way to your computer it cannot access your data; it means when you don't use it, when it's locked, it is not accessible.

Imagine someone robs your laptop. If it's not encrypted, they can simply take out the hard drive and steal all the data on it, but if it's encrypted and locked, there should be no way to access any of your data.

For the encryption of your hard drives, you can use software like VeraCrypt if cross-platform compatibility matters to you. On Windows, there's BitLocker, and on Linux, you can use cryptsetup or a file system that allows encryption.

But there are differences between container encryption tools like VeraCrypt and cryptsetup and file system-level encryption like fscrypt. Here are some of the key differences:

| Feature              | File System Encryption                         | Container Encryption                         |
| -------------------- | ---------------------------------------------- | -------------------------------------------- |
| **Encryption Scope** | Individual files/directories                   | Entire volumes/containers                    |
| **Integration**      | Built into file system (e.g., ext4, F2FS)      | Separate from file system                    |
| **Performance**      | Lower overhead, selective encryption           | Higher overhead, encrypts all data           |
| **Key Management**   | User-specific keys, multiple keys per file/dir | Single key or passphrase per container       |
| **Ease of Use**      | Transparent after setup                        | Requires mounting/unmounting containers      |
| **Cross-Platform**   | Limited to supporting file systems             | Broad support (Windows, Linux, macOS)        |
| **Security**         | Encrypts data, but not always metadata         | Encrypts all data and metadata               |
| **Use Cases**        | Selective encryption, performance-sensitive    | Full volume encryption, cross-platform needs |

When it comes to full disk encryption, having modern hardware really helps with the security and performance of encryption, as modern CPUs have built-in AES accelerating features allowing them to encrypt and decrypt AES without affecting the I/O performance as much. Also, most modern devices have TPMs (Trusted Platform Modules) which are hardware microcontrollers designed to enhance security at the hardware level by providing a secure environment for generating, storing, and managing cryptographic keys.

## Keep Your Backups Off-Site and Encrypted

The most important thing about taking backups of your data is that they need to be stored off-site. Otherwise, you just made a copy of your data; it is not a backup. A good backup can be restored even if your whole house gets burnt down, and it should be restored only by you, not anyone else.

You need to always store your backups securely encrypted, especially for things like crypto wallets, backups of GPG keys, and passwords. This should be done strategically and routinely. For data that is really important to restore, like crypto wallets and GPG keys, you might need to store them in several places, including outside your house (it can be a cloud service as well, just in case of physical disasters), and on different devices like DVDs, USB sticks, hard drives, and SD cards.

For that, you should first develop a backup strategy to know what data is most important, how you are going to perform backups, how you are going to encrypt the backups, and where you are going to store them. Do this on a regular basis if the data tends to change. Some data might not need to be backed up weekly, but some do, and some might change daily. It depends on your data and your backup strategy.

A good and well-known backup strategy is the 3-2-1 rule, which means:

- **Three** copies of your data: one primary and two backups.
- **Two** different media types: such as internal/external hard drives, SSDs, and cloud storage.
- **One** copy off-site: store a backup in a remote location or in the cloud to protect against physical disasters.

For cloud storage, it is better to use a reputable cloud storage provider. Even something like Google Drive, though its privacy is not good, will be a more reliable option compared to other services. You can also host your own cloud storage, but it will never be as reliable as a huge company like Google.

You can also invest in a NAS for automatic and centralized backups, and you can configure it for RAID (Redundant Array of Independent Disks) for data redundancy and protection. Be sure to take snapshots and version your backups to be able to restore them easily.

Always regularly test your backups to make sure they're valid and restorable. Otherwise, you might be backing up corrupted data for years, and when you need to restore your data, you can't; all your data is gone.

Lastly, develop a disaster recovery plan and ensure you have clear procedures for data restoration in case of data loss incidents.

## Five Dollar Wrench Attack

No matter how securely a hard drive is encrypted, it is always vulnerable to the 5-dollar wrench attack, meaning someone can always beat you up with a 5-dollar wrench to make you give up your passwords. How can this be prevented? Well, it is complicated, but there are some things you can do.

![XKCD Security Meme](./pictures/xkcd-security-meme.png)

### 1. Have a Kill Switch

Creating a kill switch system in which, if a specific password is entered, the key file is permanently wiped could save your data by making it inaccessible forever for everyone, including yourself. Now even you can't restore your data.

Or you can create a panic button instead. In case of something like kidnapping, it would alert the authorities. It all boils down to your own unique threat model. Based on the threats that might target your data, you might need to change this to suit the situation.

### 2. Have a Decoy System

You can create fake wallets and fake accounts and reveal those instead of the real ones. For example, some activists have created a version of Telegram called Partisan Telegram to help Belarus protesters. The way it works is you can set a lock on your Telegram and have multiple PIN codes on it and program each PIN code to do certain things. For example, if you enter the PIN "1234," it will wipe all data and send a message to everyone to alert them, but if you enter "1349," it will show a decoy account, and if you enter "6782," it will function normally.

These decoy systems can really help with situations like a protest where you might get arrested or have your devices searched. Combining them with kill switches can both fool the attacker and, at the same time, delete all the data.

### 3. Reduce the Value of the Target

Store minimal sensitive data on the devices that are most vulnerable to this kind of physical attack. For example, you don't need so much sensitive data on the phone you take out with you. Frequently back up sensitive data securely to a secure location. It can be a physical location or a remote cloud, so the data is not all in one place and not always with you.

### 4. Use Multi-Factor Authentication for Sensitive Data

Use physical authentication devices like YubiKey that require both possession of the token and a PIN or password, and keep them in a safe place. This way, your data is not accessible without the authentication device. You can hand them the passwords, but they still won't be able to get inside.

Avoid biometric authentication; it is not resistant to physical force. Someone can forcefully use your fingerprint if they need to.

### 5. Be Aware of Social Engineering Tactics

Some might use social engineering tactics instead of force, especially if they are in a position of authority. Always be aware of the tactics and mind games someone might play to get you to hand them sensitive information, passwords, and credentials.

Understand your legal rights regarding self-defense and data protection in your jurisdiction. Have a list of emergency contacts, including legal counsel, who can provide immediate assistance in case of coercion or threats.

---

These were all I had on encrypting and securely storing sensitive information. The next chapter will be about footprints and fingerprints and what actions can be taken to minimize or even erase the trace you left behind when you didn't care much about privacy.

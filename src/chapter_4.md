# Chapter 4

Continuing with the Minecraft analogy from Chapter 2, imagine you're still in the game. You've become quite familiar with it now—you've even got your locations written down, and you've gathered some wood and set up a crafting table. With these resources, you can start crafting essential tools like wooden axes, shovels, swords, a bed, and a shelter to survive the night. You're ready to take on mobs, gather rocks and stones, and explore your surroundings.

As you become more skilled, you'll progress to stone tools, then iron, and maybe even diamond if you're up for the challenge. Just like in the game, reaching the diamond level requires embarking on deep adventures into scary caves, requiring time and dedication.

But this chapter focuses on the essentials—the wooden and stone tools—of the privacy world. These are the basic building blocks of your digital privacy and security. The essentials in the privacy world include encryption tools, anonymity tools, VPNs, emails, secure messengers, password managers, and multi-factor authentication tools. These are the bare minimums for privacy, aligning with the threat models of most individuals.

## Passwords and Password Managers

Passwords are crucial for protecting our accounts, devices, and secrets. It's essential to ensure they are kept safe, secure, and accessible to us. Trying to remember a complex password for each account isn't practical. As I've explained earlier, using the same password for multiple accounts, regardless of its complexity, poses a significant risk. If one account is compromised, all others using the same password become vulnerable. Conversely, trying to remember different passwords for each site is challenging for humans, especially if not used frequently.

This is where password managers come into play. Password managers are software, either online or offline, designed to securely store passwords and other sensitive information using encryption. Access to the contents is typically protected by a master password, which you memorize. With a password manager, you only need to remember this master password to access all other stored passwords securely.

Here are some characteristics of a good password manager, in my opinion:

1. **Encryption:** A reliable password manager should use robust encryption. Never use one where you're uncertain about its encryption methods.
   
2. **Open-source:** While open-source software isn't inherently safer, it allows users to inspect the code and encryption implementation, increasing transparency and trust.

3. **Independent Audits:** Password managers should undergo independent audits to identify any potential flaws in their encryption methods.

4. **Offline or Self-hosted:** While cloud-based password managers can be secure if implemented correctly, opting for a self-hosted or offline option, like Bitwarden or KeePass, reduces the risk of data breaches since you're less likely to be targeted compared to a server hosting thousands of users' passwords.

### Choosing a Secure Master Password

But how do you generate a secure master password? First, it's crucial to understand the difference between passwords and passphrases. Passwords are random strings of letters, numbers, and symbols, challenging for humans to remember but easier for computers to crack. Passphrases, on the other hand, consist of a series of words separated by a character, making them easier for humans to recall but more challenging for computers to crack due to their length and higher entropy.

These passphrases are known as Diceware Passphrases. For example: `Batboy Wielder Defective Squire Facial Reptilian Monologue Avatar`.

![XKCD's password strength meme](./pictures/xkcd-password-strength.png)

Avoid changing your master password frequently unless you suspect it's compromised to minimize the risk of forgetting it. It's also wise to maintain an encrypted backup of your passwords in a secure location, ideally outside your devices, and with a different password in case you forget the main one. This ensures you can restore your passwords and reduce the risk of losing access to your accounts.
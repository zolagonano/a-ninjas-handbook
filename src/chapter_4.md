# Chapter 4

Continuing with the Minecraft analogy from Chapter 2, imagine you're still in the game. You've become quite familiar with it now—you've even got your locations written down, and you've gathered some wood and set up a crafting table. With these resources, you can start crafting essential tools like wooden axes, shovels, swords, a bed, and a shelter to survive the night. You're ready to take on mobs, gather rocks and stones, and explore your surroundings.

As you become more skilled, you'll progress to stone tools, then iron, and maybe even diamond if you're up for the challenge. Just like in the game, reaching the diamond level requires embarking on deep adventures into scary caves, requiring time and dedication.

But this chapter focuses on the essentials—the wooden and stone tools—of the privacy world. These are the basic building blocks of your digital privacy and security. The essentials in the privacy world include encryption tools, anonymity tools, VPNs, emails, secure messengers, password managers, and multi-factor authentication tools. These are the bare minimums for privacy, aligning with the threat models of most individuals.

I'm sorry for misunderstanding your instructions. Let me correct the grammar, spelling, and formatting errors while preserving your original tone and style.

## Passwords and Password Managers

Passwords are what protect our accounts, devices, and our secrets. We need to take all actions to keep them safe, secure, and accessible to ourselves. Trying to remember a hard password is a bad idea, and I've already explained why. If you use a single password for everything, no matter its complexity, and a data breach containing your account happens, then all your other accounts are accessible using that leaked password. And if you try remembering different passwords for every website, you will forget them all. Humans aren't that good at memorizing random passwords, especially if you don't recall them often.

Here, the password managers come to play. Password managers are software, either online or offline, to store passwords and other notes and secrets safely and securely using encryption. The content inside them will be accessible through one password, usually known as the master password. So when using a password manager, you will memorize a complex password as your master password, and that will be used to access other passwords inside your password manager's vault. Now you don't need to remember any other password or secret.

A good password manager should have these characteristics, in my opinion:

1. They need to be encrypted. Never use a password manager that you're unsure of its encryption.
2. They need to be open-source. Not that open-source software is necessarily safer, but with them being open-source, we can check their codes and the implementation of encryptions and make sure they're safe.
3. They must be audited independently. We're not cryptography analysis experts. An audit will show if there are any flaws in the cryptography implementation of a software encryption.
4. They better be offline or self-hosted. There is no problem with a cloud-based password manager if it is implemented correctly. Even if their database gets leaked, the passwords should still be encrypted and secure. But when using a self-hosted or offline password manager, like Bitwarden (which can be self-hosted) or Keepass, you minimize the risk of leakage because it is far less likely that you will be more targeted than a password manager's server with thousands of users.

### Choosing a Secure Master Password

But how can you generate a secure master password? You need to forget the passwords first. Passwords are a string of random letters, numbers, and punctuation characters. They will get really hard really fast for humans to memorize but not as much for computers to crack and guess through brute force attacks. But on the other hand, the passphrases can be a list of words separated by a character, which is easy to remember for humans but a lot harder for a computer to crack because they're usually way longer and have more entropy than a password. They're easier to remember because they are words, and words to us have meanings but not to computers. They see random strings still.

These passphrases are called Diceware Passphrases. An example of a Diceware passphrase is: `Batboy Wielder Defective Squire Facial Reptilian Monologue Avatar`.

![XKCD's password strength meme](./pictures/xkcd-password-strength.png)

Avoid changing your master passwords too often unless you suspect that it is compromised to minimize the risk of forgetting it. Also, a good practice would be having an encrypted back of your passwords somewhere safe, ideally outside your devices and with a different password (in case you forget the main password) so you can restore your password and minimize the risk of losing access to your accounts.
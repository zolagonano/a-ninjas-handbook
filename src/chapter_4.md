# Chapter 4

Continuing with the Minecraft analogy from Chapter 2, imagine you're still in the game. You've become quite familiar with it now—you've even got your locations written down, and you've gathered some wood and set up a crafting table. With these resources, you can start crafting essential tools like wooden axes, shovels, swords, a bed, and a shelter to survive the night. You're ready to take on mobs, gather rocks and stones, and explore your surroundings.

As you become more skilled, you'll progress to stone tools, then iron, and maybe even diamond if you're up for the challenge. Just like in the game, reaching the diamond level requires embarking on deep adventures into scary caves, requiring time and dedication.

But this chapter focuses on the essentials—the wooden and stone tools—of the privacy world. These are the basic building blocks of your digital privacy and security. The essentials in the privacy world include encryption tools, anonymity tools, VPNs, emails, secure messengers, password managers, and multi-factor authentication tools. These are the bare minimums for privacy, aligning with the threat models of most individuals.

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

## Email Security
Email services aren't secure by nature. New technology usually comes before security, and that's true for email as well as the earliest protocols of the internet. But this lack of security can be overcome to some extent by adding layers of encryption to email services.

The first layer of encryption needs to be added to the communication channel. By communication channel, I mean the channel that the data needs to go through to get to the destination, not the email content. This can be done by adding TLS to the transport layer of the email protocol. Nowadays, most email service providers have TLS enabled by default. But if you self-host your email service, you'd need to make sure transport layer encryption is enabled.

The second layer of encryption would be for the email content. This can be done through using PGP or S/MIME encryption. But we would need to have our recipient's public key in order to send them encrypted emails. There are encrypted and privacy-focused email providers like ProtonMail and Tutanota which can eliminate this need for having the public key, only if our recipient uses the same email provider as us. For example, two ProtonMail users can send each other encrypted emails without having to know each other's public keys.

And even if you encrypt the content of the email, the metadata would still be unencrypted. These metadatas can include:

1. **Sender Email Address:** The email address of the person sending the email.
2. **Recipient Email Address(es):** The email address(es) of the recipient(s) of the email.
3. **Timestamps:** The date and time when the email was sent and sometimes when it was received.
4. **Subject Line:** The subject line of the email, which summarizes its content.
5. **Message-ID:** A unique identifier for the email message.
6. **Return-Path:** The email address to which bounced emails are returned.
7. **Received:** Information about the email servers and networks through which the email passed during transmission.
8. **X-Mailer:** Optional field indicating the email client or software used to compose the email.
9. **MIME-Version:** Version of the Multipurpose Internet Mail Extensions (MIME) protocol used in the email.
10. **Content-Type:** The type and format of the message content, such as text/plain for plain text or text/html for HTML-formatted content.

## Messaging Security

Most chat messages aren't secure either. For instance, Telegram, a messaging app that claims to be encrypted and secure, doesn't even have E2EE (end-to-end encryption) enabled by default. And even when it allows E2EE, it is only for mobile clients, meaning you cannot use Telegram securely on a desktop client. Worse yet, Telegram breaks the first and most important rule of cryptography, which states, "Do not roll your own crypto," by using a self-rolled cryptography scheme for its E2EE chats. Additionally, Telegram servers are all closed-source; nobody has any idea how the messages and data on Telegram are stored. Are they encrypted? Who has access to these servers? Nobody knows. Telegram is the perfect example of a bad messaging app in my opinion. I know there are messaging apps worse than Telegram, but none of them claim to be private and secure. So, I will use Telegram as a bad example of a messaging app to explain what a messaging app needs to have.

- **End-to-end Encryption:** A secure messaging app would allow E2EE messages with a known and audited cryptography scheme and implementation. Telegram allows it to some degree, but its cryptography is questionable.
- **Anonymous Sign-up:** A private messaging app would allow you to sign up anonymously, usually using an email. Telegram and Signal use phone numbers, which is reasonable for reducing spam. However, there are ways around this, like buying an anonymous VoIP number using Monero or cash.
- **Transparency:** A secure messaging app should be transparent about how they store data, what data they store, and in what scenarios the data can be handed over to authorities.
- **Metadata Collection:** Every message and account has some metadata that usually isn't encrypted. Telegram collects a lot about you, like your name, sign-up date, IP addresses, 2FA email, phone number, contacts, people you frequently talk to, and all your messages (if you do not use E2EE). They can hand this data over to authorities if they have to. Signal, on the other hand, collects little to no metadata about you and doesn't have much to hand over even if a court order compels them to do so.
- **Popularity:** We can't make people use what we use. If everyone I know uses Telegram, I have to use Telegram too, and that's a big part of a messaging app. I might prefer Matrix over Signal, though Signal has better security and collects less metadata than Matrix, but most people I talk to use Matrix, so I have to make some sacrifices here.

Your threat model plays a huge role here. You might not care at all if your messages with your friends can be read by Telegram or any other company. It depends on you and your threat model.
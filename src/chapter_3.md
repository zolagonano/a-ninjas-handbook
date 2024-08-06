# Chapter 3

In 2012, the FBI caught a hacker with the nickname w0rmer after he hacked several U.S. law enforcement websites and released their data online. You might think there was a big and complicated operation to catch this hacker, but no, w0rmer just had bad opsec. He handed the FBI his exact geo-location simply because he replaced the FBI's database with a picture of his girlfriend from the neck down in a bikini, holding a sign saying "PwNd by w0rmer & CabinCr3w, <3 u BiTch's!" It wasn’t that they figured out who the girl was from that picture; w0rmer forgot to (or didn’t care to) erase the EXIF metadata of the picture. The FBI looked at the picture, and in its metadata, they found that it was taken with an iPhone 4, with GPS coordinates of an outer-Melbourne suburb. w0rmer had overshared his location through a picture.

The electrical tape on your webcam and your Tor browser inside Whonix OS can't help you if you share too much about yourself, if you over time tend to expose your real identity piece by piece. Having good opsec often means having control and awareness of what you're sharing when talking to people or when posting online.

## Identify the sensetive data and information

The first step in improving your OPSEC is identifying the data that is sensitive to you. To do this, you need to refer to your threat model. Assess what threats are common and which data would have the most severe consequences if it falls into the wrong hands. Then, prioritize the information based on the severity of the consequences.

Having this plan in place would reduce the unnecessary caution you need to take. Being overly cautious about everything you say or share can consume a lot of mental energy and increase the chance of slipping up. By focusing on what is sensitive based on your unique situation and threat model, you can minimize the mental effort required to maintain OPSEC.

### Common Sensitive Information

These are some of the most common types of sensitive information that an individual might want to protect, but it all depends on your unique situation and whether these match your threat model.

- **Personally Identifiable Information (PII):** Information that can uniquely identify an individual.
  - **Full legal name:** Your complete legal name as recorded on your identification documents.
  - **Addresses:** Your physical location where you live or work.
  - **Phone numbers:** Numbers assigned to your phone lines, including mobile and landline numbers.
  - **Email addresses:** Email accounts that are tied to your personal identity.
  - **Date of birth:** The date you were born, typically used for verification purposes, and can be used to narrow down your identity.
  - **National identification numbers:** Unique numbers issued by governments to identify citizens of a country, but even something like a library card number can be sensitive if tied to your personal identity.

- **Financial Information:** Data related to your financial transactions and accounts. Some of this information can be PII as well.
  - **Bank account numbers:** Unique numbers assigned to your bank accounts for transactions.
  - **Credit/debit card numbers:** Numbers found on your payment cards used for purchasing goods and services.
  - **Payment information (PayPal, Venmo, etc.):** Details used to process financial transactions through payment services, like your PayPal email or Venmo username.
  - **Financial statements:** Documents detailing your financial transactions and balances.
  - **Tax information:** Details related to your tax filings and records.

- **Account Credentials:** Information used to access online accounts.
  - **Usernames**
  - **Passwords**
  - **Security questions and answers:** Predefined questions with answers used for account recovery.
  - **Two-factor authentication (2FA) codes:** Temporary codes used in conjunction with passwords for additional security.

- **Digital Footprint and Metadata:** Information that can be used to trace your online activities.
  - **IP addresses:** Unique numerical labels assigned to your devices on a network.
  - **MAC addresses:** Hardware identifiers assigned to network interfaces.
  - **Browser fingerprints:** Unique configurations and settings of your browser that can be used to track you.
  - **Device information (model, OS, etc.):** Details about the devices you use to access the internet.
  - **Geolocation data:** Information about your physical location derived from your devices.
  - **Cookies and tracking scripts:** Small files and code snippets used to track your activity online.

- **Communication Content:** The actual content of your communications.
  - **Emails:** Digital messages sent through email services.
  - **Text messages:** Short messages sent via SMS or messaging apps.
  - **Social media posts:** Content shared on social networking platforms.
  - **Chat logs:** Recorded conversations from instant messaging services.
  - **Voice and video call recordings:** Audio and video data from calls made over VoIP services.

- **Behavioral Information:** Data about your online behavior and habits.
  - **Browsing history:** Record of websites you have visited.
  - **Search queries:** Terms and phrases you have searched for on search engines.
  - **Online shopping habits:** Patterns and preferences in your online purchasing behavior.
  - **Social media activity:** Your interactions and engagement on social media platforms.
  - **Writing style:** The way you write or speak.
  - **App usage patterns:** Information about how you use mobile and web applications.

- **Professional Information:** Work-related information.
  - **Employment details:** Information about your job and employer.
  - **Work-related documents:** Files and records related to your professional activities.
  - **Business contacts:** Information about your professional network.
  - **Project information:** Details about the projects you are working on.
  - **Client data:** Information about the clients you interact with in a professional capacity.

- **Biometric Information:** Unique biological traits used for identification.
  - **Fingerprints:** Unique patterns of ridges and valleys on your fingertips.
  - **Facial recognition data:** Digital mapping of your facial features.
  - **Voiceprints:** Unique characteristics of your voice used for identification.
  - **Iris scans:** Detailed images of the colored part of your eye.

- **Personal Preferences and Opinions:** Information about your beliefs, preferences, and opinions. This can be critical if you live under a dictatorship or in a highly repressive environment.
  - **Political views:** Your beliefs and stances on political issues.
  - **Religious beliefs:** Your faith and religious practices.
  - **Sexual orientation:** Your sexual preferences and identity.
  - **Health information:** Data about your medical history and current health status.
  - **Memberships in various organizations:** Affiliations with clubs, societies, and other groups.

## Protect the Sensitive Information

Now that we know some of the common sensitive information in OPSEC, we can move on to approaches to protect this information. These protections also vary greatly based on your personal situation and your unique threat model. Always take a look at your threat model.

### **Personal Identifiable Information (PII)**

- Encrypt files and documents containing PII using strong encryption algorithms such as AES. Never create your own encryption; use an algorithm that has been proven to be secure and an implementation that has been audited.
- Minimize the collection and retention of unnecessary PII. Provide your PII only if you have to, and there is no other way around it. If you have the chance to avoid providing your PII and use a pseudonym or a fake identity, do it.
- Store physical documents containing your PII, like your passport, in a safe place with surveillance systems like CCTVs.

### Financial Information

- Use secure connections (HTTPS, for example) when accessing your bank website or any other financial website.
- Regularly monitor your financial accounts for unauthorized access and enable warning features if your bank provides them.
- Enable transaction notifications for all transactions so you are alerted to any suspicious activity on your accounts.
- In the case of cryptocurrencies, use cryptocurrencies that are decentralized and provide anonymity, like ZCash and Monero. Most cryptocurrencies aren't anonymous; they're pseudonymous. Nobody would know the owner of the address, but as soon as you spend the money in the real world, it will be traced back to your real identity. This is not true for privacy coins like Monero.

### Account Credentials

- Use an audited and reputable password manager to store your passwords and account credentials. Never try to remember your passwords or, worse, use the same password everywhere. Each website should have its unique password to prevent unauthorized access to other accounts if one account's password gets leaked.
- Enable 2FA whenever possible to add an additional layer of security to protect your accounts. You can use physical devices for 2FA or audited open-source apps for TOTP codes. Also, make sure you protect your 2FA credentials as well as your passwords.
- Never share your account credentials via email or unencrypted messaging platforms. If you must share them, use encryption or a secure messaging app like Signal and enable auto-delete for the message.
- Periodically review and update account passwords. You can also sign up for services that check the dark web or database breaches for your account and notify you if your account is found in these breaches.

### Digital Footprint and Metadata

- Use a pseudonymous VPN or Tor (highly depending on your threat model) to mask your IP address by encrypting and rerouting your internet traffic.
- Harden your browsers or use Tor Browser to limit the collection of browser history, cookies, and other metadata. You can also configure your browser to minimize its fingerprintability, but using Tor Browser is generally better if you want to avoid fingerprinting.
- Use privacy-friendly search engines like DuckDuckGo and StartPage or host your own search engine like Searx.
- Disable location services on your device when you don't need them. The location, when enabled, can be stored in the pictures you take as well.
- Remove the EXIF metadata from pictures before sharing, or use a camera app that does this by default.

### Communication Content

- Always use end-to-end encryption when communicating. Use messaging apps like Session and Signal, which have strong encryption and store little metadata.
- Use encrypted emails like Tutanota and ProtonMail or use PGP to encrypt your emails before sending. However, emails will always have a lot of unencrypted metadata.
- Avoid sharing sensitive information over unencrypted channels, such as public Wi-Fi. Ensure your communication channels are encrypted.

### Behavioral Information

- Use privacy-friendly search engines to minimize tracking of online activities. Also, disable search suggestions in your browser to prevent leaking your searches to third-party services.
- Regularly clear browser history, cookies, caches, etc., to ensure you don't leave any traces of your activities on your browser. Alternatively, use Tor Browser if it aligns with your threat model.
- Review and adjust privacy settings on social media platforms and websites you sign up for to minimize the collection of personal data.

### Professional Information

- Encryption overlaps here as well, so encrypt work-related documents and files using strong encryption, just as you would for other data.
- Use secure, encrypted collaboration tools for sharing sensitive work-related information.
- Implement access controls and permissions to restrict access to confidential work data.

### Biometric Information

- Again, store biometric information encrypted using a strong and known encryption algorithm and implementation.
- Limit the collection and storage of biometric data to what is necessary for authentication purposes. If possible, avoid using biometric data for authentication.

### Personal Preferences and Opinions

- Be cautious about sharing personal preferences and opinions on public platforms, or at least avoid using your real name.
- Adjust privacy settings on social media to limit the visibility of personal preferences and opinions.
- Use pseudonyms or anonymous accounts for discussions on sensitive topics. This can sometimes be crucial depending on where you live.

---

Effective OPSEC goes way beyond implementing some techniques; it's about shifting your mindset. It demands a heightened awareness of the information we share and a commitment to continuous learning and adaptation. The threats are always evolving, and these techniques may become deprecated, but if you set your mindset to the fact that what you put online may stay there forever and will be read someday, you will find the techniques.

> "If you know the why, you can live any how."
>
> ― Friedrich Nietzsche  

The next chapter will be about privacy and security's essentials. Now that the myths are busted, the roadmap is ready, and the mindset is set, we can move on to the essentials of the privacy world: the tools and techniques that can be used to enhance your privacy.
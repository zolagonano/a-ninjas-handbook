# Chapter 3

In 2012, the FBI nabbed a hacker known as w0rmer. He'd hacked several U.S. law enforcement websites and leaked their data online. You might think it took a big, complicated operation to catch him, but nope! w0rmer just had terrible operational security (opsec). He gave away his exact location to the FBI by replacing their database with a picture of his girlfriend from the neck down in a bikini, holding a sign that said "PwNd by w0rmer & CabinCr3w, <3 u BiTch's!" It's not like they identified the girl from the picture; w0rmer forgot (or didn't care) to erase the GPS coordinates from the picture's metadata. The FBI saw the coordinates were from an iPhone 4 in an outer Melbourne suburb. w0rmer overshared his location through a picture.

Having electrical tape on your webcam and using Tor browser inside Whonix OS won't save you if you share too much about yourself over time. Having good opsec often means being in control and aware of what you're sharing when talking to people or posting online.

## Identify the sensetive data and information

The first step to improving our OPSEC is identifying the data that's sensitive to us. To do that, we need to check our threat model. We figure out what threats are common and which data would cause the most trouble if it fell into the wrong hands. Then, we prioritize the information based on how severe the consequences would be.

With this plan, we can cut down on unnecessary caution. Being overly cautious about everything we say or share can drain a lot of mental energy and increase the chances of slipping up. But if we focus on what's sensitive based on our own unique situation and threat model, we can reduce the mental energy needed to maintain our OPSEC.

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

## Protecting Sensitive Information

Now that we're familiar with some common types of sensitive information in OPSEC, let's explore approaches we can take to protect this data. These protections vary widely based on your personal situation and unique threat model, so always refer to your threat model.

### Personal Identifiable Information (PII)

- Encrypt files and documents containing PII using robust encryption algorithms like AES. Avoid rolling your own encryption; use proven algorithms and audited implementations.
- Minimize the collection and retention of unnecessary PII. Provide your PII only when absolutely necessary, and consider using a pseudonym or fake identity where possible.
- Store physical documents containing PII, such as passports, in secure locations with surveillance systems like CCTV.

### Financial Information

- Use secure connections (HTTPS) when accessing financial websites like banks.
- Regularly monitor your financial accounts for unauthorized access and enable warning features where available.
- Enable transaction notifications for all transactions to stay informed about any suspicious activity.
- For cryptocurrencies, use decentralized and anonymous options like Zcash and Monero for enhanced privacy.

### Account Credentials

- Utilize a reputable password manager to securely store passwords and account credentials. Avoid using the same password across multiple accounts.
- Enable two-factor authentication (2FA) whenever possible for an added layer of security.
- Never share account credentials via email or unencrypted messaging platforms. Use encryption or secure messaging apps like Signal for sensitive information.
- Periodically review and update account passwords, and consider signing up for services that monitor for data breaches.

### Digital Footprint and Metadata

- Use a pseudonymous VPN or Tor (depending on your threat model) to mask your IP address and encrypt internet traffic.
- Configure browsers to minimize browser history, cookies, and other metadata. Consider using Tor Browser for enhanced privacy.
- Use privacy-focused search engines like DuckDuckGo or StartPage, or host your own search engine like Searx.
- Disable location services on your devices when not needed to prevent location data from being stored in images.

### Communication Content

- Always use end-to-end encryption when communicating. Choose messaging apps like Session and Signal for strong encryption and minimal metadata storage.
- Use encrypted email services like Tutanota and ProtonMail, or utilize PGP encryption for emails.
- Avoid sharing sensitive information over unencrypted channels like public Wi-Fi networks.

### Behavioral Information

- Use privacy-friendly search engines and disable search suggestions to minimize tracking.
- Regularly clear browser history, cookies, and caches, or consider using Tor Browser.
- Review and adjust privacy settings on social media platforms to minimize personal data collection.

### Professional Information

- Encrypt work-related documents and files using strong encryption methods.
- Use secure, encrypted collaboration tools for sharing sensitive work-related information.
- Implement access controls and permissions to restrict access to confidential work data.

### Biometric Information

- Store biometric information encrypted using strong encryption algorithms.
- Limit the collection and storage of biometric data to what is necessary for authentication purposes, or avoid biometric authentication if possible.

### Personal Preferences and Opinions

- Exercise caution when sharing personal preferences and opinions on public platforms, especially under your real name.
- Adjust privacy settings on social media to limit the visibility of personal preferences and opinions.
- Consider using pseudonyms or anonymous accounts for discussions on sensitive topics, which can sometimes be crucial depending on your location.

---

Effective OPSEC goes beyond implementing techniques; it's about shifting your mindset. It demands a heightened awareness of the information we share and a commitment to continuous learning and adaptation. Threats are always evolving, and techniques may become deprecated, but if you set your mindset to understand why what you put online may stay there forever and be read someday, you'll find the right techniques.

> "If you know the why, you can live any how."
>
>   ― Friedrich Nietzsche  

The next chapter will explore the essentials of privacy and security. With the myths debunked, the roadmap established, and the mindset in place, we can delve into the tools and techniques that enhance your privacy in the digital world.
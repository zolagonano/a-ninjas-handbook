# Appendix A

## VPNs and Anonymity

### **1. VPN**

**Traffic Encryption:**

- **Protocols:** VPNs use encryption protocols such as **OpenVPN**, **IKEv2/IPsec**, and **WireGuard**. Encryption algorithms include:
  - **AES-256-CBC** or **AES-256-GCM** for symmetric encryption.
  - **RSA-2048** for asymmetric key exchange.

**IP Masking:** VPNs mask the client’s IP address with the VPN server’s IP. This does not anonymize the user but shifts the visible IP from the ISP to the VPN provider.

**Logging Policies:**

- **No-Logs Claims:** Providers like **Mullvad** and **ProtonVPN** claim not to log user activities. Verification relies on independent audits and court cases.
- **Data Exposure:** VPN providers can be compelled to disclose logs if they exist, which can include connection timestamps, IP addresses, and usage data.

**Traffic Analysis:**

- **Correlation Attacks:** Analyzing traffic patterns, timing, and volume can potentially link VPN traffic to specific users, despite encryption.

**Fingerprinting:**

- **Browser/OS Fingerprinting:** VPNs do not protect you against fingerprinting. Unique device and browser characteristics (e.g., user agent, screen resolution) can still be used for fingerprinting.

### **2. Tor Network**

**Onion Routing:**

- **Encryption Layers:** Data is encrypted in three layers, with each Tor relay removing one layer of encryption. This process ensures end-to-end encryption with the following layers:
  - **Layer 1:** Encrypted between the client and the first relay.
  - **Layer 2:** Encrypted between successive relays.
  - **Layer 3:** Encrypted until reaching the exit node.

**Exit Node:**
- **Data Visibility:** Exit nodes decrypt the final layer and see the unencrypted data but cannot see the originating IP. Control of all relays is required to trace originating IP, which is theoretically and practically really costly to do.

**End-to-End Encryption:**
- **.onion Sites:** Use **Elliptic Curve Cryptography** (ECC) with a public/private key pair for end-to-end encryption.

### **3. Alternatives**

**I2P:**
- **Routing:** Uses **Garlic Routing**, similar to onion routing but with packet encapsulation.
- **Node Count:** Limited nodes compared to Tor, making it less resilient to attacks.

**Lokinet:**
- **Network Topology:** Uses **DHT (Distributed Hash Table)** for node discovery and routing.
- **Node Limitations:** Smaller node network than Tor, affecting it's anonymity.



## Password Security and Password Managers

### Password Security

**Entropy Calculation:**
Entropy is the randomness or unpredictability of a password, which directly affects its strength against attacks. It is measured in bits and calculated as:
$$
\text{Entropy} = \log_2(N^L)
$$
where:

- \( N \) = Number of possible symbols (e.g., 95 for a character set including uppercase, lowercase, digits, and symbols).
- \( L \) = Length of the password.

For example, a password of length 12 using 95 characters has:

$$
\text{Entropy} = \log_2(95^{12}) \approx 78.7 \text{ bits}
$$
### Passphrase Security:

- **Design and Strength:** Passphrases are longer and easier to remember compared to traditional passwords. For example, “Name-Seat-Look-Chair-Plane7-Stree7” has high entropy because it combines multiple words and symbols.

  The entropy of a passphrase with six words and special characters can be calculated by:

  $$
  \text{Entropy} \approx \log_2(W^L)
  $$
  where \( W \) is the number of possible words (e.g., a large dictionary of words) and \( L \) is the number of words. For a passphrase with a dictionary of 10,000 words and 6 words in length:
  
  $$
  \text{Entropy} = \log_2(10,000^6) \approx 79.6 \text{ bits}
  $$
  



## Big Tech Security and Privacy

###  Big Tech Security Measures

**Security Practices:**

- **Advanced Security Protocols:** Companies like Google and Microsoft implement good security measures, including multi-factor authentication (MFA), end-to-end encryption for specific services, and regular security audits.
- **Enterprise-Level Infrastructure:** These companies use enterprise-grade security technologies such as intrusion detection systems (IDS), firewalls, and advanced threat protection to protect user's data.
- **Vulnerability Management:** Regular patching and updates are applied to address security vulnerabilities. Bug bounty programs are often set to identify and fix security flaws.

**Transparency and Trust Issues:**

- **Lack of Transparency:** The specific details of their security implementations are not publicly disclosed, limiting the ability to fully verify their claims.
- **Closed Source:** Security measures and protocols are proprietary, making it difficult for independent verification and audit.

## Email Security

### Transport Layer Encryption (TLS)

- **TLS Handshake**: When an email is sent, the sending server initiates a TLS handshake with the receiving server. This handshake involves:
  - **Server Authentication**: The receiving server presents its TLS certificate, which is verified by the sending server using a trusted Certificate Authority (CA).
  - **Session Key Agreement**: The servers exchange a symmetric session key using asymmetric encryption to establish a secure channel. The session key encrypts following datas.
  - **Certificate Management**: Ensures that certificates are up-to-date and valid. Misconfigured or expired certificates can lead to vulnerabilities. Tools like Let's Encrypt can automate certificate issuance and renewal.

### Content Encryption

**PGP (Pretty Good Privacy)**:

- **Key Generation**: Works by creating a pair of keys (public and private) using algorithms such as RSA (Rivest–Shamir–Adleman) or ECC (Elliptic Curve Cryptography). Key lengths typically range from 2048 to 4096 bits for RSA, or 256 bits for ECC.
- **Encryption Process**:
  - **Symmetric Encryption**: The email content is encrypted with a symmetric key (e.g., AES-256). The symmetric key itself is encrypted with the recipient's public key.
  - **Signature**: A digital signature is created using the sender's private key, allowing the recipient to verify integrity of the email.

- **Key Management**: PGP requires manual exchange of public keys, often through key servers or direct exchange. Key management can be handled using tools like Gpg4win (Windows) or GpgTools (macOS).

**S/MIME (Secure/Multipurpose Internet Mail Extensions)**:

- **Certificate Authority (CA)**: S/MIME relies on X.509 certificates issued by trusted CAs. These certificates include the user’s public key and are used for encryption and signing.
- **Encryption Process**:
  - **Symmetric Encryption**: Email content is encrypted using a symmetric algorithm (e.g., AES-256), and the symmetric key is encrypted with the recipient’s public key.
  - **Digital Signature**: The sender’s private key is used to sign the email, for authentication and integrity.

- **Certificate Management**: Certificates must be obtained and managed through a CA. They include public and private keys and are often stored in secure keystores or hardware security modules (HSMs).

### Metadata Exposure

- **Sender and Recipient Email Addresses**: These addresses are visible in the email headers and can reveal communication patterns and relationships.
- **Timestamps**: Include sending and receiving times. These timestamps are recorded in the `Date` and `Received` headers.
- **Subject Line**: Visible in the email headers and can provide a summary of the email’s content.
- **Message-ID**: A unique identifier assigned to each email message, useful for tracking.
- **Return-Path**: Shows where bounce messages are sent, indicating the sender’s address.
- **Received Headers**: Trace the path of the email through various servers, revealing server locations and potential network information.
- **X-Mailer**: Optional field showing the email client or software used, which can sometimes disclose information about the user’s environment.
- **MIME-Version and Content-Type**:  The MIME protocol version and the type of content, such as `text/plain` or `text/html`.

**Minimizing Metadata Risks**:

- **Email Content**: Avoid putting sensitive information in the subject line or body if metadata is a concern.
- **Email Providers**: Use services that focus on minimizing metadata leakage, such as ProtonMail or Tutanota.

### Best Practices for Securing Email

- **Use Encryption**: Ensure that both transport layer (TLS) and content encryption (PGP/S/MIME) are properly configured and encrypted.
- **Regular Certificate Updates**: Keep TLS certificates up-to-date and manage encryption keys securely.
- 

## Operating Systems

**Android Open Source Project (AOSP)**:
- **Verified Boot**: Ensures that the device boots using only trusted software, preventing unauthorized modifications.
- **App Sandboxing**: Apps are isolated from each other and the system, reducing the risk of malicious apps affecting other apps or system functionality.
- **Permission Management**: Users can control app permissions to limit access to sensitive data and features.

- **Updates**: Ensure that the device receives timely security patches. Regular updates fix vulnerabilities and improve security.
- **Rooting**: Rooting can compromise security by breaking app sandboxing and granting elevated privileges to apps, making the device more vulnerable to exploits.

- **Install Custom ROMs**: Consider using custom ROMs such as GrapheneOS on devices like Google Pixels.
- **Disable Unnecessary Features**: Turn off or uninstall pre-installed apps and features that may collect data.
- **Keep Software Updated**: Regularly update the device to ensure it has the latest security patches.

**iOS:**

- **Closed Source**: iOS is not open-source, which limits the ability to audit its source code for vulnerabilities.
- **Security Features**: Includes app sandboxing, data encryption, and secure boot. Apple controls app distribution through the App Store, reducing the risk of malicious apps.

- **Limited Customization**: Users have limited ability to alter core settings or install third-party software outside the App Store.
- **Data Collection**: Apple collects a lot of user data.

- **Review Privacy Settings**: Regularly check and adjust privacy settings to limit data sharing and access.
- **Keep iOS Updated**: Ensure that the device runs the latest version of iOS to have latest security patches.
- **Use Strong Passcodes**: Use strong passcodes and enable two-factor authentication to increase device security.

**Windows:**

- **Telemetry Data**: Windows collects telemetry data, which may include information about system usage and errors.
- **Closed Source**: Windows source code is not open for public review, making it harder to detect and fix vulnerabilities.

- **Zero-Day Vulnerabilities**: Because Windows is closedsources it means that vulnerabilities can exist before they are discovered and patched.
- **Privacy Settings**: Windows offers settings to control privacy and data collection, but these settings cannot not fully prevent data sharing.

- **Consider Linux**: For enhanced security and privacy, consider using a Linux distribution for regular tasks and only use Windows in a virtual machine if absolutely necessary.
- **Adjust Privacy Settings**: Configure privacy settings to limit data collection and sharing with Microsoft.
- **Use Security Tools**: Use additional security tools, such as firewalls to protect the system.

**Linux:**

- **Open Source**: The open-source nature of Linux allows for bugs and vulnerabilities to be found sooner than Windows, reducing the risk of unpatched vulnerabilities.
- **Customization**: Users can choose from thousands of distributions and variations of the Linux kernel.

- **Kernel Variations**: Specialized kernels like linux-hardened include extra security features to enhance system protection.

- **Select a Security-Focused Distribution**: Choose distributions like Qubes OS or Whonix for more security and privacy features.
- **Regular Updates**: Keep the system and software updated to protect against known vulnerabilities.

## Encrypyion 

**Cryptographic Analysis**: Validated algorithms gone through extensive cryptanalysis, including:

- **Differential Cryptanalysis**: Analyzes how differences in input affect differences in output.
- **Linear Cryptanalysis**: Uses linear approximations to describe the behavior of the encryption algorithm.
- **Algebraic Attacks**: Exploits algebraic structures in the cryptographic algorithm.
- **Sieve Attacks**: Finds solutions to equations used in cryptographic schemes.

**Example Algorithms**:

- **AES**: Operates on 128-bit blocks with 10, 12, or 14 rounds of processing, using SubBytes, ShiftRows, MixColumns, and AddRoundKey operations.
- **ChaCha20**: A stream cipher with 20 rounds of processing, using a quarter-round function for high-speed encryption.

**The Encryption Pitfalls**:

- **Security Through Obscurity**: Algorithms should be secure based on their design and resistance to cryptanalysis, not on secrecy.

**Techniques to prevent some implementation attacks**:

- **Constant-Time Algorithms**: Implementations that ensure constant execution time, can reduce the risk of timing attacks.
- **Noise Generation**: Uses randomness to mask power consumption patterns.

**Hardware Performance Factors**:

- **AES-NI**: Hardware acceleration for AES encryption, improving performance with modern CPUs.
- **TPM**: Provides hardware-based protection for cryptographic keys, ensuring they are not exposed even if the system is compromised.

## **Backups**

**Backup Technologies**:

- **RAID Levels**:
  - **RAID 1**: Mirroring for redundancy.
  - **RAID 5/6**: Striping with parity for data redundancy.
- **Snapshot Technologies**:
  - **ZFS Snapshots**: Efficient point-in-time copies of data.
  - **LVM Snapshots**: Logical volume snapshots for incremental backups.

**Encryption Tools**:

- **VeraCrypt**: Provides both container and volume encryption.
- **Cryptsetup**: Utilizes LUKS (Linux Unified Key Setup) for disk encryption.



## Advanced Anonymity Techniques and Tools

- **VPN Usage**
   - **Multi-Hop VPN**: Combining multiple VPN servers in different countries to add layers of obfuscation. Services like ProtonVPN offer this feature.
   - **Onion Over VPN**: Routing your VPN traffic through the Tor network for added security. This can be set up on some VPN providers’ platforms.
- **Secure Operating Systems**
   - **Qubes OS**: Offers security through virtualization. Each application runs in a separate virtual machine, which limits the impact of any potential bad code.
   - **Whonix**: Uses a split-design where the Tor gateway and the workstation are isolated to enhance security. 
- **Secure Communication**
   - **PGP (Pretty Good Privacy)**: For encrypting emails and files. The OpenPGP standard can be used with email clients like Thunderbird with the Enigmail plugin.
   - **GPG (GNU Privacy Guard)**: An open-source implementation of PGP. It's widely used for encrypting data and communications.
- **Metadata Removal**
   - **MAT2 (Metadata Anonymisation Toolkit)**: A toolkit for removing metadata from files in batch. Useful for handling multiple files at once.
   - **ExifTool**: A command-line tool for removing metadata from various file types, including images and documents.
- **Data Encryption**
   - **VeraCrypt**: For encrypting data stored on your devices. It allows creating encrypted virtual disks and encrypting entire partitions.
   - **EncFS**: A FUSE-based filesystem that transparently encrypts files.
- **Behavioral Analysis Tools**
   - **Keystroke Dynamics**: Tools like KeyTracer can help analyze typing patterns, and avoiding these patterns can enhance anonymity.
   - **Mouse Gestures**: Tools that randomize mouse movement or use scripts to obfuscate typical mouse patterns.
- **Network Security**
   - **DNS-over-HTTPS (DoH)**: Encrypts DNS queries to protect against eavesdropping and tampering. Supported by browsers like Firefox and Chrome.
   - **DNS-over-TLS (DoT)**: Another encryption method for DNS queries, supported by many VPNs and network configurations.
- **Data Sanitization**
   - **BleachBit**: An open-source tool for cleaning up disk space and removing traces of activities.
   - **CCleaner**: For Windows users to clean temporary files and system traces.

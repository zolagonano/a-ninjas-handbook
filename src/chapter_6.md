# Chapter 6

Everything you touch leaves your fingerprint on it, and everywhere you go, you leave your footprints behind, making you identifiable and your actions traceable back to you. Unless you're wearing gloves, are cautious of not leaving your DNA behind, and wipe your footprints as you go forward, the same goes for you when you use the internet.

On the internet, we all have unique fingerprints and leave footprints behind as we use it. The more you use it, the more unique your fingerprints become and the clearer your footprints become.

This chapter is all about making yourself as less unique as possible and covering your footprints as much as possible. It might be impossible to fully wipe your old footprints because anything you put out there on the internet can stay there forever, and it's impossible to not have a fingerprint at all. The key is to create multiple unique fingerprints and keep them separated from each other. This strategy will save you a lot of energy, time, and anxiety, and make it sustainable for the long run.

## Separating Fingerprints

We all have real identities in the real world, and we have to use the internet with our real identity too. We can't stop using credit cards and banks and buy everything on Tor using Monero. That is simply not possible. But we can separate our real identity fully, giving it its unique fingerprint, unique behavior, and unique writing style, and for our other identities, we can separate them as well.

For example, an activist who wants to remain anonymous can still have two unique fingerprints: one for their real identity and one for their activist identity. The uniqueness of the fingerprint is never the problem in such scenarios as long as you keep these fingerprints separated. If you use your activist fingerprint to do your real-world stuff, then it's a problem. Now you've cross-contaminated the identities. But if you don't, it won't be a problem. Even if they start tracking your activist identity, it won't lead them to your real identity. It has its own footprint, which traces nowhere near your real identity, and it has its own unique behavior, unique writing style, etc.

However, sometimes you truly need to look like others, such as when someone buys stolen data off the dark web (not that I encourage illegal activities as such). Then it will be best to look like everyone else on that website. Again, it all depends on your threat model.

How can you separate your fingerprints? Here are some tips, but you should take a look at your threat model and build a strategy based on that.

- **Create separate working environments**: It can be having multiple different accounts on your computer, phone, etc., or having fully separated virtual machines set up for each different identity.
- **Create separate accounts**: Have different emails, cloud storages, VPN accounts, etc., for each identity.
- **Create separate backstories**: Have different identities, and give them separate lives and backstories. This will make it easier to keep up with them.
- **Create separate behavior patterns**: Your typing style (speed, accuracy, etc.), writing style, expressions and words you use, the way you respond, your clicking and mouse movement patterns, the websites you usually visit—these are all behavior patterns that can cross-contaminate identities.
- **Use fingerprint-resistant tools**: Use tools like Tor Browser, a hardened Firefox, Whonix OS, etc.

There are analysis algorithms to match these unique behaviors to other users and accurately pinpoint the user who has the same behaviors and fingerprint. Even if such algorithms are not used by authorities, they exist, and they can be used. So they might and will be used, just like how they're used nowadays for marketing and advertisement purposes. Most of the time, privacy is about preventing such things from happening.

## Erasing Your Old Footprints

Although it is hard, it is not fully impossible. You can still remove some of your footprints that you left behind years before. First, you need to see what identity you want to wipe out. Then start creating a full list of everywhere you have signed up, posted something, or bought something. An easy way to gather this data would be going through your emails—all of them—and seeing what websites have sent you emails for logins and sign-ups. List them all.

Then you can go to each website. If they allow you to delete your account, delete it. For cases like Twitter and other social media, the best approach would be to first delete everything—comments, posts, profile pictures, bio, location, etc.—and wait for a few weeks. Then delete the account. This will allow the crawlers and search engines to update their information on the account, so your old posts won't show up in search results after you delete your account.

For some websites and services that don't allow you to delete your account, first change all your information on them, then email them to delete your data. In most cases, they will. For the data that you didn't put out there, you can send a DMCA notice and ask them to take down your data. You can do this to take down your data off the search engines as well.

There are some services that can automatically delete you off the internet as well. After you manually delete everything, you can use services like "DeleteMe" to delete everything else. They can also delete and notify you if future information is out on you.

After deleting everything, try to forget it. Do not play around with it anymore if you want the identity to be erased from the internet. Live your life and let it die, hopefully. Also, take notes for the next identity so you won't need to do this again. Make sure you always provide little to no sensitive and unnecessary information when you create and use accounts, and be very minimalist about creating accounts. Only create one if you absolutely need to. Most of the time, you don't. Or if you want to try it out, create a quick one-time identity to test things out.

## Your Digital Identifiers

Like in the real world, where our fingertips are unique identifiers or our other biometric features, in the digital world we have those identifiers too. When these digital identifiers are combined together, they can create a fingerprint more unique than those on our fingertips. And this is not only about your software; each piece of hardware that you use has a unique identifier as well.

The good news is most of these identifiers, both at the hardware level and the software and network level, are spoofable and changeable. It's really easy to change a fingerprint in the digital world; the hard thing, and almost impossible thing, is to not have one.

### Hardware Identifiers

Each hardware component manufactured comes with a unique identifier, which has been used for device management, network administration, security, etc. But now they can be used to identify users, just like when police gather fingerprints of someone from a crime scene. They can now get your MAC address and see where else you have been with your laptop.

A MAC address, or Media Access Control address, is a unique identifier set by manufacturers for network interfaces for communications on the physical network segment. It is used for identifying devices on local networks, network access control, and tracking devices. It can be changed quite easily on the software level. For example, my Android 13 Nokia phone allows me to have a random MAC address whenever I connect to a Wi-Fi network that I don’t know. MAC address spoofing is relatively easy, and to be honest, it is not that much of a concern. A MAC address is only used on local networks, not the internet, so tracking it is really hard and pointless. However, it is something to keep in mind if you use a network that is not yours; it is always a good idea to spoof your MAC address.

But there’s an identifier in all of our phones that is not changeable, and in some countries, is tied to your real identity. It can leak your approximate location even if your phone has no SIM card in it, and that’s your IMEI and IMSI. The IMEI (International Mobile Equipment Identity) and the IMSI (International Mobile Subscriber Identity) are unique numbers created by phone manufacturers. Every time your phone connects to a mobile network, it registers with your IMEI and IMSI. Even if there’s no SIM card in your phone, because of emergency calls, you still connect to cell phone towers.

The mobile network can log and store the timing of your connection to each cell phone tower, and based on your signal strength, how far you were from it. This means that, at any given time, the network can determine where your phone has been. Your IMSI, in some countries, is directly tied to your real identity because you need to buy SIM cards with your real ID, which automatically links the phone to your actual identity whenever you use it. Also, the IMEI can be traced back to your real identity if you didn’t buy the phone in an anonymous way. Additionally, operating system companies like Google and Apple keep logs of your IMEI and IMSI identifiers tied to your Google/Apple accounts, so they can trace back and see what other accounts have been tied to this phone before.

It is possible to change your IMEI/IMSI, but in some countries, it might not be legal, and in others, it can break the functionality of your phone because they link your IMSI to your SIM card number, and you won’t receive any services if you change it.

Another identifier is your CPU. Each CPU has a CPUID that can reveal information about details of the CPU to software, such as processor type and what features it implements. Also, almost all modern CPUs, including Intel and AMD, have a hidden management platform such as Intel Management Engine for Intel processors and AMD Platform Security Processor for AMD processors. These management platforms are literally small operating systems running on your CPU and have full access to your computer’s network. They could be accessed to de-anonymize users. For Intel CPUs, there’s no good way to turn its management platform off other than buying an old CPU that doesn’t have this feature, but for some AMD CPUs, it can be turned off in the BIOS.

Also, your Bluetooth devices have identifiers like your network interfaces, but that is less of a concern than the network since Bluetooth addresses are often randomized, and most operating systems randomize those addresses. A good practice is to disable Bluetooth when you don’t need it.

### Software Identifiers

Your browser has the most software identifiers, which alone can make you unique, and most of the time they are combined with physical identifiers like the CPU you use or the details of your monitor, etc.

One of these identifiers is the user agent string. The user agent string is sent by the browser to the server and identifies the browser type, version, and operating system. It is quite easy to change by hardening your browser or using Tor Browser.

Also, if JavaScript is allowed on your browser, it can read a lot of data from your browser, such as browser type, time zone and language, fonts installed, operating system and version, screen resolution, and color depth. If JavaScript is enabled, it can also perform canvas fingerprinting, WebGL fingerprinting, and AudioContext fingerprinting.

Canvas fingerprinting is a technique that uses the HTML5 canvas element to draw graphics and capture the unique rendering characteristics of a device. The website uses JavaScript to instruct the browser to draw a hidden image or text on a canvas element. This drawing operation can include various shapes, colors, text fonts, and sizes. Once the drawing operation is complete, the browser extracts the pixel data from the rendered image or text. This data is essentially a long string of numbers representing the color and brightness of each pixel. Different browsers may render graphics slightly differently due to variations in their rendering engines. The same browser may produce different results on different operating systems. Additionally, hardware differences like graphic cards can affect the rendering process, leading to unique variations, and variations in installed fonts and how they are rendered can contribute to uniqueness.

WebGL is used for rendering interactive 3D and 2D graphics within any compatible web browser without the use of plugins, but it can be used to fingerprint users as well. The way it works is that the website uses JavaScript to instruct the browser to render a 3D object or scene using the WebGL API. This rendering involves various aspects such as textures, lighting, shading, and other graphical effects. After rendering, the browser extracts data from the rendered image or scene. This data can include the pixel values, but also more complex information about the rendering process, such as the attributes of the graphics card and drivers. Then, like canvas fingerprinting, the rendering data is hashed using a cryptographic hash function, creating a unique fingerprint. This fingerprint is unique due to the differences in how different devices render the same 3D object.

AudioContext fingerprinting uses the AudioContext API to generate a unique identifier based on the audio processing capabilities of a user's device. It works based on the fact that different devices and environments will process audio signals in slightly different ways due to hardware and software variations. First, the website uses JavaScript to create an instance of the AudioContext object and generate an audio signal, typically using oscillators or other sound sources. Then, the generated audio signal is passed through various audio processing nodes, such as gain nodes, filters, or analyzers. These nodes modify the audio signal in ways that are subtly influenced by the hardware and software environment. After that, the processed audio signal is captured, often by using an AnalyserNode to capture the audio data in the form of frequency or time-domain data. Lastly, the captured audio data is hashed and used as a unique fingerprint.

Also, the Battery Status API, Device Memory and Hardware Concurrency, Installed Fonts, Network Information API, Touch and Pointer Events, Applications and Uses, and user behaviors such as the way they use the mouse and keyboard, etc., can be used to create a unique fingerprint as well.

## Browser Hardening or Tor Browser

You don't need to use Tor Browser for activities that are tied to your real identity or that are not meant to be anonymous. But hardening a browser, on the other hand, can help a lot more with your privacy concerns by making each browser profile dedicated to one identity and hardening it based on that identity's needs and your threat models.

The way that Tor Browser works is to make you like everybody else on the Tor network. If you use Tor Browser to check in on your bank account or anything else that is tied to a real identity, then you're even more unique than before. Also, the important thing is that you should not change anything in Tor Browser; any slight changes, like installing a plugin or changing settings, can make you much more unique than you would have been without Tor Browser.

But hardening a browser does give you a unique fingerprint, and that is right. However, it also can provide you more security and privacy if you use it correctly, meaning each browser profile should be set up for one specific task or identity. For example, you can have one hardened Firefox profile for watching YouTube and listening to music on SoundCloud, one for your online identities and anything related to that, and one for your real identity. This way, you can choose what task or identity needs are and set up your browser based on those needs.

For hardening browsers, there are a lot of resources out there, especially for Firefox. For example, for Firefox, there is Arkenfox, which provides you a list of carefully selected options and settings for Firefox to enhance its privacy. Using something like Brave for general usage is good too, as it has pretty decent privacy settings and features by default.

You can have multiple browsers for different needs as well, for example, hardened Firefox profiles for different tasks that require specific setups, Brave for general usage, and Tor Browser for when you need to stay anonymous.

It always boils down to your threat model and your specific needs, so always take actions based on that and save yourself a lot of hassles and mistakes too.


---


Cybercriminals employ a structured approach to targeting computer systems, which involves several forms of attack.

**Forms of Attack:**

1. **Initial Uncovering (Reconnaissance)**: This is the preparatory phase, often referred to as "footprinting" in hacking. It involves gathering information about the target's environment and computer architecture to find intrusion points. This can be done passively by searching public websites, news articles, online community groups (like Facebook), organization websites, blogs, newsgroups, and even job postings to learn about employees. Network sniffing can also be used in this phase to gather information on IP address ranges, hidden servers, or services without the target's knowledge.
2. **Network Probe (Investigation)**: After initial reconnaissance, attackers use more invasive techniques like "ping sweeps" and port scanning to discover individual hosts and confirm information about IP addresses, operating system types, versions, and services running on the network. This is also called "Rattling the Doorknobs" or "Active Reconnaissance".
3. **Crossing the Line toward E-crime**: At this stage, attackers exploit identified vulnerabilities in the target system to gain unauthorized access, often aiming for "root access," which provides full system privileges.
4. **Capturing the Network**: This involves taking control of the network. The attacker quickly gains internal network access and may replace existing files and services with malicious ones, such as Trojan files with backdoor passwords.
5. **Grab the Data**: Once the network is compromised, the attacker proceeds to steal confidential data, credit card information, deface webpages, alter processes, or launch further attacks from the compromised network.
6. **Covering Tracks**: This final step aims to extend the misuse of the system without detection. Attackers meticulously hide their identity and erase any traces of illicit activity, such as deleting access logs. Tools like ELSave, WinZapper, Evidence Eliminator, Traceless, and Tracks Eraser Pro are used for this purpose.

**Types of Malicious Software and Deception Tactics:**

- **Scareware**: This is scam software that uses social engineering by displaying pop-up messages (e.g., "your computer may be infected with harmful spyware programs") to create anxiety and trick users into purchasing or downloading non-beneficial, often malicious, software. Some forms of spyware and adware use scareware tactics.
- **Malvertising**: This involves malicious advertising, where malware is hidden within advertisements or embedded into webpages, subtly installing unwanted media or other malicious software when users interact with them.
- **Clickjacking**: This technique tricks users into revealing confidential information or taking control of their system by clicking on seemingly innocuous webpages. It executes embedded malicious code without the user's knowledge.
- **Ransomware**: This is a type of malware that holds a computer system or its data hostage, demanding a ransom for its restoration. It typically propagates as a computer worm, entering systems through email attachments or network vulnerabilities, disabling essential system services, and encrypting personal files.

Attackers use various websites to obtain information on system vulnerabilities, including US-CERT, CVE, Secunia, Hackstorm, Hackerwatch, Zone-H, Milworm, OSVDB, Metasploit, LibExploit, Canvas, and Core Impact.

### Proxy Servers and Anonymizers

Proxy servers and anonymizers are crucial tools for cybercriminals to obscure their digital footprint and maintain anonymity.

**Proxy Servers:** A proxy server acts as an intermediary for connections between computers on a network. Its purposes include:

- **Hiding Identity**: It allows an attacker to conceal their IP address and identity.
- **Speeding Up Access**: It can cache webpages from a web server, thereby speeding up access to resources.
- **Filtering Content**: Specialized proxy servers are used to filter unwanted content, such as advertisements.
- **IP Address Multiplexing**: It can be used as an IP address multiplexer, allowing multiple computers to connect to the internet using a single IP address. Examples of websites offering free proxy services include proxy4free.com, proxz.com, anonymitychecker.com, surf24h.com, and hidemyass.com.

**Anonymizers:** An anonymizer, also known as an anonymous proxy, is a tool designed to make internet activity untraceable. It accesses the internet on behalf of the user, protecting personal information by hiding the source computer's identifying data. These sites are used by individuals who wish to avoid leaving traces of their identity online, thereby preventing unsolicited emails from spammers or contact from cyberstalkers. Websites providing anonymizer services include anonymizer.com, browzar.com, anonymize.net, and anonymouse.ws.

**Being Anonymous while Searching on Google:** When searching online, even common tools can record user data:

- **Google Cookie**: Google was one of the first search engines to use cookies, placing a unique ID number on a user's hard disk. This cookie reads and records the unique ID number each time a user visits Google, allowing Google to build a detailed list of search terms over many years. These cookies are set to expire in 2038 unless deleted by the user.
- **Cookie (HTTP/Browser Cookie)**: A small text file containing alphanumeric characters, used for storing website preferences or authentication. Attackers can exploit these cookies as "Spyware." Cookies can be persistent (stored on the PC's hard disk) or session-based (temporary, deleted when the browser closes).
- **DoubleClick**: A Google subsidiary that provides internet ad-serving services and paid search. It utilizes "DART cookies" to facilitate these services.
- **G-Zapper**: A utility that helps users maintain anonymity while searching Google. It protects users' search history and displays information about their Google cookie (installation date, tracking duration). G-Zapper allows users to automatically delete or block the Google search cookie from future installations, preventing it from compiling reports, tracking user habits, or testing features.

---

Phishing is a deceptive cybercrime technique primarily aimed at tricking individuals into revealing sensitive information, such as usernames, passwords, and credit card details. It was introduced around 1996.

### Definition and Purpose

Phishing is defined as a criminally fraudulent process that attempts to acquire sensitive information by masquerading as a trustworthy entity in electronic communication. It involves sending emails that falsely claim to be from established, legitimate enterprises to scam users into surrendering private information for identity theft. The emails often direct users to bogus websites that mimic legitimate ones, set up solely to steal user information. Phishers aim to gain valuable, sometimes invaluable, information from their victims.

### How Phishing Works (Attack Phases)

Phishing attacks typically follow a structured approach involving several steps:

1. **Planning**: Criminals, known as "phishers," select their target and determine how to obtain email addresses.
2. **Setup**: Phishers identify a business or entity to spoof and create methods to deliver their deceptive messages and collect data from the target.
3. **Attack**: A phony message, appearing to be from a reputable source, is sent to the victims.
4. **Collection**: Phishers record the information victims enter on fake webpages or pop-up windows.
5. **Identity Theft and Fraud**: The collected information is then used to make illegal purchases or commit other forms of fraud.

This entire process involves the attacker taking optimum care to hide their identity from the very first step.

### Forms of Attack and Deception Tactics

Phishing is closely related to various forms of attack and deception tactics:

- **Scareware**: Scam software that uses social engineering with pop-up messages (e.g., "your computer may be infected") to create anxiety and trick users into purchasing or downloading malicious software.
- **Malvertising**: Malicious advertising where malware is hidden within ads or embedded into webpages, subtly installing unwanted media or other malicious software when users interact with them.
- **Clickjacking**: A technique that tricks users into revealing confidential information or taking control of their system by clicking on seemingly innocuous webpages, executing embedded malicious code without their knowledge.
- **Ransomware**: Malware that holds a computer system or its data hostage, demanding a ransom for restoration. It often propagates as a computer worm through email attachments or network vulnerabilities, disabling system services and encrypting personal files.
- **Spoofing**: Often used in phishing, where phishers create fake emails. Spoofing itself is not intended to steal information but to make the victim perform an action for the phisher. Phishing may require spoofing to entice victims to reveal information.

### Methods and Techniques of Phishing

Phishers use a variety of sophisticated methods and techniques:

**1. Four Core Methods:**

- **Dragnet**: Involves mass-spammed emails with falsified corporate identification (logos, names) sent to large groups, relying on false information to trigger an immediate response like clicking links to fake websites for data entry. Phishers do not identify specific victims in advance.
- **Road-and-reel**: Phishers identify specific victims in advance and convey false information to prompt their disclosure of personal and financial data. For example, a phony webpage might display a similar item for a better price to entice data entry.
- **Lobsterpot**: Focuses on spoofed websites. This involves creating bogus websites similar to legitimate corporate ones, targeting a narrowly defined class of victims. A weblink in an email leads the victim to a fake scam site that looks legitimate.
- **Gillnet**: Relies less on social engineering and more on introducing malicious code into emails and websites. This code can subtly install unwanted media, redirect users to fake sites, or record keystrokes without the user's knowledge.

**2. Phishing Techniques (UFWFSP):**

- **URL (weblink) Manipulation**: Phishers provide misspelled URLs (e.g., `www.abcbank1.com` instead of `www.abcbank.com`) to redirect users to fake sites. This includes **Homograph Attacks**, which exploit similar-looking characters in internationalized domain names (e.g., '0' for 'O').
- **Filter Evasion**: Uses graphics instead of text in emails to bypass anti-phishing filters in web browsers like Internet Explorer, Firefox, and Opera.
- **Website Forgery**: Attackers direct users to a website designed by them, altering the browser's address bar through JavaScript commands. This can also involve "cloaked" URLs or domain forwarding.
- **Flash Phishing**: Emulates legitimate websites using Flash objects, bypassing anti-phishing toolbars that do not analyze Flash content.
- **Social Phishing**: Entices sensitive data through other means, such as fake calls requesting a callback due to a "security breach." The victim calls a false number, is redirected to the phisher, who then impersonates a bank employee to collect information.
- **Phone Phishing (Mishing)**: Uses fake caller ID data to appear as a trusted organization. This includes **Vishing** (VoIP phishing) and **Smishing** (SMS phishing).
- **Innovative Phishing Attacks**: Examples include malware hidden in mobile applications (e.g., 09Droid on Android Market) that steal online banking credentials.

**3. Targeted Phishing:**

- **Spear Phishing**: A highly targeted phishing message sent to a specific organization, company, or group to gain organizational information for more focused social engineering. These emails appear genuine, as if from an employer or colleague, but the sender information is faked. The goal is often to gain access to the company's entire computer system.
- **Whaling**: A specific form of phishing or spear phishing that targets top-level executives in organizations. The emails are designed to look like critical business communications and aim to swindle confidential information. An example includes forged FBI subpoena emails that, when clicked, install keyloggers to record executive passwords.

### Types of Phishing Scams

- **Deceptive Phishing**: Broadcasts deceptive email messages (e.g., about bank account verification or system failures) to a wide group of people to entice them to reveal information.
- **Malware-based Phishing**: Involves running malicious code on the victim's system, often through email attachments, downloadable files, or by exploiting security vulnerabilities.
- **Keyloggers**: Small programs that steal information (like keystrokes) and transmit it to the phisher. They can be embedded in browsers or system holes.
- **Session Hijacking**: Monitors a user's activities until they establish legitimate credentials, then the malicious code takes over to perform unauthorized actions like transferring funds.
- **In-session Phishing**: A pop-up window launched in a parallel browser session that pretends to be from the targeted session (e.g., an online banking website).
- **Web Trojans**: Pop up to collect user credentials and transmit them to the phisher during the login process.
- **Pharming**: A new threat that aims to redirect website traffic to bogus websites. It can involve **Hosts File Poisoning** (altering a computer's hosts file to redirect legitimate website requests to a fake site) or **DNS-based Phishing** (tampering with DNS to redirect URLs to fake sites, also known as DNS hijacking).
- **System Configuration Attacks**: Phishers intrude into a user's system to modify settings for malicious purposes, such as changing saved URLs in browser favorites to redirect to fake sites.
- **Data Theft**: Stealing critical and confidential data from corporate servers and the web, often used in business espionage.
- **Content Injection Phishing**: Replaces parts of a legitimate website's content with false information.
- **Man-in-the-Middle Phishing**: The phisher positions themselves between the user and a legitimate website, recording input while still passing it to the server so the user's transactions appear unaffected.
- **Search Engine Phishing**: Phishers create attractive, often too-good-to-be-true, websites that are legitimately indexed by search engines. Users find these sites during normal searches and are then tricked into revealing personal information.
- **SSL Certificate Phishing**: Targets web servers with SSL certificates to create deceptive websites displaying familiar "lock" icons, even though the site is fraudulent. While the SSL certificate may appear legitimate, smart users can detect the deception by checking for an extended validation SSL certificate.

### Three P's of Cybercrime

Phishing is part of a broader group known as the "Three P's of Cybercrime":

- **Phishing**: As described above, to steal personal information.
- **Pharming**: Redirects website traffic to bogus sites, often by cracking ISP or DNS server vulnerabilities.
- **Phoraging**: The process of collecting data from various online sources (like matrimonial or social networking sites) to build a victim's identity, with the ultimate goal of identity theft.

### Advanced Forms of Phishing

- **Tabnapping or Tabjacking**: Invades web browser tabs that are not in use ("napping") and redirects them to a phished webpage if the tab has been idle. This is judged by the absence of mouse movement, scrollbar movement, or keystrokes. Common targets include banking/financial institutes, Gmail, Facebook, Instagram, and WhatsApp.
- **DNS Hijacking**: An illegal change to a DNS server that redirects a URL to a different, often malicious, website. Attackers use Trojans to replace legitimate DNS server assignments with bogus ones, making the redirection go unnoticed.
- **Click Fraud**: An internet crime in pay-per-click online advertising where a person or automated program imitates legitimate user clicks to generate charges without actual interest in the advertisement's target. It can be done by manually clicking ad hyperlinks or using automated software/bots.

### Statistics and Trends

- Phishing attacks are monitored daily on websites like phishtank.com.
- In May 2009, over 3,650 non-English phishing websites were recorded. The most common top-level domains used were ".com" (50%), ".net" (9%), and ".org" (5%).
- According to a Q4-2009 report, financial organizations, payment services, and auction websites were the most targeted industries. Ports 80 (HTTP), 443 (S-HTTP), and 8080 (WEB SERVER) were commonly used by phishers.
- The number of phishing hosts showed a significant rise between July 2006 and July 2007.

### Countermeasures and Protection

Several measures can be taken to prevent becoming a victim of phishing attacks:

- **Keep Antivirus Up-to-Date**: Ensure security software is current.
- **Do Not Click on Hyperlinks in Emails**: Avoid clicking suspicious links.
- **Use Anti-Spam Software**: Utilize tools to filter unwanted emails.
- **Verify HTTPS (SSL)**: Check for secure connections when entering sensitive information.
- **Use Anti-Spyware Software**: Protect against spyware, which can be part of phishing attacks.
- **Get Educated**: Understand phishing tactics.
- **Use Microsoft Baseline Security Analyzer (MBSA)**.
- **Firewall**: Employ firewalls for network protection.
- **Use Backup System Images**: Have backups to restore systems if compromised.
- **Do Not Enter Sensitive Information in Pop-up Windows**: Avoid disclosing data in unexpected pop-ups.
- **Secure the Hosts File**: Protect this file from malicious alterations.
- **Protect Against DNS Pharming Attacks**.
- **Avoid Online Financial Transactions in Cybercafes**: If urgent, change passwords immediately after using a more trusted computer.
- **Always Logout**: Ensure logging out of services in public computers, not just closing the browser.
- **Clear History and Temporary Files**: Delete browsing history and temporary files on public computers.
- **Be Alert for Shoulder Surfing**: Be aware of surroundings when entering information in public.
- **Use Virtual Keyboard**: Many banks offer virtual keyboards to avoid keylogger attacks.

**Recognizing Legitimate Websites**: Tools like McAfee Site Advisor provide security ratings for websites. The SPS (Sanitizing Proxy System) algorithm offers a robust approach to thwart phishing with two-level filtering and flexibility.

**Reducing Spam Emails**:

- Limit sharing personal email addresses on public platforms.
- Never reply to or open spam emails, as this confirms the email address's validity.
- Disguise email addresses when posting publicly (e.g., "RajeevATgmailDOTcom").
- Use alternate email addresses for personal or shopping websites, not business ones.
- Do not forward emails from unknown recipients.
- Preview emails before opening them.
- Never use an email address as a screen name in chat groups.
- Never respond to "remove from mailing list" requests in spam emails.

### Organizations and Tools

- **Anti-Phishing Working Group (APWG)**: An international consortium founded in 2003, with over 3,200 members, dedicated to combating phishing and identity theft.
- **US-CERT, CVE, Secunia, Hackstorm, Hackerwatch, Zone-H, Milworm, OSVDB, Metasploit, LibExploit, Canvas, and Core Impact**: Websites and tools cybercriminals use to obtain information on system vulnerabilities.
- **Microsoft phishing filter, Google Phishing filter (Firefox), Opera Fraud Protection**: In-built anti-phishing filters in web browsers.

---


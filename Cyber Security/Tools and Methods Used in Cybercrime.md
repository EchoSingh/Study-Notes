
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

## Phishing

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

## Password cracking

Password cracking is the process of recovering passwords that have been stored in or transmitted by a computer system. It is a key topic in cybersecurity, particularly within the context of cybercrime tools and methods.

**Purpose of Password Cracking** The main purposes of password cracking include:

1. **Recovering forgotten passwords**.
2. **Preventive measure** by system administrators to identify easily crackable passwords.
3. **Gaining unauthorized access** to a system.

**Manual Password Cracking Steps** An attacker attempting to manually crack a password will typically follow these steps:

1. Find a valid user account, such as an Administrator or Guest account.
2. Create a list of possible passwords.
3. Rank the passwords from high to low probability.
4. Key-in each password.
5. Repeat the process until a successful password is found.

**Password Cracking Tools** Various tools are available for password cracking:

- **Cain & Abel**: A password recovery tool for Microsoft Operating Systems that can recover many password types, decrypt scrambled passwords, and recover wireless network keys.
- **John the Ripper**: A free and open-source software that detects weak Unix passwords.
- **THC-Hydra**: A network logon cracker supporting many different protocols.
- **Aircrack-ng**: A set of tools for wireless networks, enabling WEP key cracking.
- **LOphtCrack**: A password auditing and recovery tool for Windows, allowing local password hashes to be retrieved and audited.
- **AirSnort**: A wireless LAN (WLAN) tool for recovering encryption keys.
- **Solar Winds**: Provides network discovery/monitoring/attack tools.
- **Pwdump**: A Windows password recovery tool that can dump local and remote NT LAN Manager (NTLM) hashes.
- **RainbowCrack**: A hash cracker that creates large-scale time-memory trade-offs.
- **Brutus**: A fast, flexible remote password cracker.
- **Solarwinds**: Tools for network discovery/monitoring/attack, designed to identify security vulnerabilities.
- **Hash Crack**: A hash cracker for large-scale time-memory trade-offs.

**Types of Password Cracking Attacks** Password cracking attacks can be classified into three main categories:

1. **Online Attacks**: Involve executing an automated program to try each password in a list until a match is found.
    
    - **Man-in-the-middle (MITM) attack** (also known as "bucket-brigade attack" or "Janus attack"): The attacker establishes a connection between the victim and the server, intercepting communications, hashing passwords, and passing the connection to the legitimate server. This method is used to obtain passwords for email accounts on public websites (like Yahoo, Hotmail, Gmail) and financial websites to gain access to banking services.
2. **Offline Attacks**: Performed from a location other than the target system, often requiring physical access to the computer to copy the password file onto removable media. The goal is to obtain passwords in clear text format.
    
    - **Dictionary Attack**: Attempts to match all words from a dictionary to crack the password (e.g., "Administrator").
    - **Hybrid Attack**: Substitutes numbers and symbols to dictionary words (e.g., "Adm1n1strator").
    - **Brute Force Attack**: Attempts all possible permutations and combinations of letters, numbers, and special characters (e.g., "Adm!n@09").
3. **Non-electronic Attacks**: These include social engineering, shoulder surfing, and dumpster diving, which are explained in Chapter 2.
    

**Password Strength**

- **Weak Passwords**: Easily guessed, short, common, or system default passwords. Examples include common personal names ("Susan"), repeated letters ("aaaa"), pet names ("rover"), simple sequences ("abc123", "1234"), common terms ("admin", "password"), keyboard sequences ("QWERTY"), dates ("12/3/75"), usernames ("nbusr123"), or simple letter substitutions ("p@S$V/ord").
- **Strong Passwords**: Long, random, or otherwise difficult to guess. They are chosen by the user and their crack time varies based on the attacker's resources and the password's value. Examples include phrases ("Convert £100 to Euros!"), mixed numbers and letters used on mass user accounts ("382465304H"), or non-dictionary words with mixed alpha, numeric, and punctuation characters ("PIeai@3", "MoOoOfln245679", "t3wahSetyeT4").
- **Random Passwords**: Stronger as they include a mix of upper and lower case letters, numbers, and other symbols. However, their difficulty in remembering increases the chance of users writing them down, making them vulnerable to other attacks.

**Password Policies and Security Measures** General guidelines for password policies that can be implemented organization-wide include:

- Passwords and user logon identities (IDs) should be unique for each authorized user.
- Passwords should consist of a minimum of eight alphanumeric characters, avoiding common names or phrases.
- Computer-controlled lists of prescribed password rules and periodic testing (e.g., for letter and number sequences, character repetition, initials, common words, and standard names) should be used to identify weaknesses.
- Passwords should be kept private, not shared with friends or colleagues, and not coded into programs or written down anywhere.
- Passwords should be changed every 30/45 days or less. Most operating systems (OS) can enforce automatic expiration and prevent reuse.
- User accounts should be frozen after five failed logon attempts, and erroneous password entries should be recorded in an audit log.
- Sessions should be suspended after 15 minutes (or a specified period) of inactivity, requiring re-entry of passwords.
- Successful logons should display the date and time of the last logon/logoff.
- Logon IDs and passwords should be suspended after a specified period of non-use.
- For high-risk systems, excessive violations should trigger an alarm and allow for simulation of a continuing session with dummy data for the failed user.

For netizens, specific advice to avoid falling victim to hacked email or financial accounts includes:

- Keep business, personal, and banking email/financial accounts separate.
- Passwords should not be shared with relatives or friends.
- Do not reuse previously used passwords when renewing.
- Do not store passwords on mobile phones or PDAs, as these devices are prone to cyberattacks.
- Before clicking web links in emails from banking/financial institutions, ensure the email's legitimacy to avoid phishing attacks.
- Similarly, for SMS from banking/financial institutions, ensure legitimacy to avoid smishing attacks.
- If accounts are hacked, contact the respective agencies/institutes immediately.

---

## Keyloggers and Spywares

Keyloggers and Spywares are significant tools and methods used in cybercrime, primarily designed to intercept and collect information from computer systems.

### Keyloggers

**Definition and Purpose** Keystroke logging, commonly known as keylogging, is the practice of covertly noting or logging the keys struck on a keyboard without the user's awareness. Keyloggers offer a quick and easy way to capture passwords and monitor a victim's IT-savvy behavior. The purpose of keyloggers in cybercrime is to gain unauthorized access to systems by stealing credentials.

**Classification** Keyloggers can be classified into two main types:

1. **Software Keyloggers**
    
    - These are software programs installed on computer systems, typically located between the operating system (OS) and the keyboard hardware.
    - They record every keystroke made by the user.
    - Often, software keyloggers are installed onto a system by Trojans or viruses without the user's knowledge.
    - Cybercriminals frequently install these tools on insecure public computers, such as those in cybercafes or libraries, to easily obtain information about victims.
    - A typical software keylogger might consist of two files installed in the same directory: a Dynamic Link Library (DLL) file that performs the recording, and an executable (EXE) file that installs the DLL and triggers its operation.
    - Examples include All-in-One Keylogger, Stealth Keylogger, Perfect Keylogger, KGB Spy, Spy Buddy, Elite Keylogger, Cyberspy, Powered Keylogger, XPC Spy, Spytech Spyagent, and Stealth.
2. **Hardware Keyloggers**
    
    - These are small physical hardware devices that require physical access to the computer system for installation.
    - They are connected to the PC and/or keyboard and save every keystroke to a file or the device's memory.
    - Cybercriminals have been known to install these devices on ATM machines to capture ATM card PINs, as each keypress on the ATM keyboard is registered by the keylogger.
    - These keyloggers are designed to look like an integrated part of the systems, making their presence unnoticed by users.
    - Examples of websites providing information on hardware keyloggers include keyghost.com, keelog.com, keydevil.com, and keykatcher.com.

**Anti-Keyloggers** Anti-keyloggers are tools designed to detect and remove keyloggers installed on a computer system. Their advantages include:

- Firewalls typically cannot detect keylogger installations, whereas anti-keyloggers can.
- Unlike some antivirus and anti-spyware programs, anti-keyloggers do not require regular updates of signature bases to function effectively.
- They help prevent Internet banking fraud by thwarting password capture by keyloggers.
- They aid in preventing identity (ID) theft and securing email and instant messaging/chatting.

### Spywares

**Definition and Function** Spyware is a type of malicious software (malware) that is installed on computers to collect information about users without their knowledge. Its presence is usually hidden from the user, and it is secretly installed on the user's personal computer. In some cases, spyware, including keyloggers, might be intentionally installed by the owner of a shared, corporate, or public computer to secretly monitor other users.

**Information Collected and Impact** Spyware programs secretly monitor the user and collect personal information about the victim, such as Internet surfing habits, patterns, and visited websites. These programs can alter internet settings, leading users to complain about slower internet speeds.

**Examples** Examples of spyware include 007 Spy, Spector Pro, eBlaster, Remotespy, Stealth Recorder Pro, Stealth Website Logger, Flexispy, Wiretap Professional, PC PhoneHome, and SpyArsenal Print Monitor Pro.

**Relationship with Malware** Keyloggers and Spyware fall under the broader category of "malware" (malicious software), which is designed to infiltrate a computer system without the owner's informed consent. Malware represents various forms of hostile, intrusive, or annoying software or program code.

---

## **Virus and Worms**

Viruses and worms are both types of malicious software (malware) designed to infiltrate computer systems. They are often used by criminals for various attacks.

**Computer Viruses** A computer virus is a program that "infects" legitimate programs by modifying them to include a copy of itself, which can then "evolve". Viruses spread without the user's knowledge or permission. They contain malicious instructions that can cause damage or annoyance. A virus passes from computer to computer similar to how a biological virus spreads from person to person. They can be triggered by specific events (e.g., after a certain number of executions), time-driven effects (e.g., a specific date like Friday the 13th), or occur randomly.

**Typical actions of a virus include:**

- Displaying a message to prompt an action that may set off the virus.
- Deleting files within the infected system.
- Scrambling data on a hard disk.
- Causing erratic screen behavior.
- Halting the system (PC).
- Replicating themselves to propagate further harm.
- Modifying themselves to potentially escape detection.

**Types of Viruses:** Viruses can be categorized based on their attack methods on various system elements:

- **Boot Sector Viruses:** These infect the storage media where the operating system (OS) is stored and used to start the computer. They spread to other systems through shared infected disks and pirated software.
- **Program Viruses:** These become active when program files (usually with extensions like .bin, .com, .exe, .ovl, .drv) are executed, and they make copies of themselves.
- **Multipartite Viruses:** A hybrid of boot sector and program viruses, infecting program files along with the boot record when the infected program is active.
- **Stealth Viruses:** These camouflage or mask themselves, making detection difficult for antivirus software. An example is the Brain virus.
- **Polymorphic Viruses:** These act like "chameleons," changing their binary pattern (signature) each time they spread (multiply and infect new files), making them hard for antivirus programs to detect. Polymorphic generators are routines that link with existing viruses to hide them under polymorphism.
- **Macro Viruses:** These are programmed as macros embedded in documents and spread when the document is opened. Once on a victim's computer, every document produced will become infected.
- **Active X Java Control:** Web browsers have settings for Active X and Java Commands; unawareness of managing these settings can invite threats from unwanted software.

**Examples of Viruses:** Conficker, INF/AutoRun, Win32 PSW, OnLineGames, Win32/Agent (Trojan), Win32/FlyStudio (Trojan with backdoor characteristics), Win32/Pacex.Gen, Win32/Qhost, WMA/TrojanDownloader.GetCodec.

**Computer Worms** A computer worm is a self-replicating malware program that spreads through a network without needing a host program. Unlike viruses, worms do not need to attach themselves to an existing program. They can send copies of themselves to other nodes on the network without user intervention. Worms typically cause some harm to the network, often by consuming bandwidth, while viruses tend to corrupt or modify files on a targeted computer.

**Examples of Worms:** Morris Worm, ILOVEYOU, Nimda, Code Red, Melissa, MSBlast, Sobig, Storm Worm, Michelangelo, Jerusalem.

**Distinction between Viruses and Worms** The sources highlight key differences between viruses and worms:

|Facet|Virus|Worm|
|:--|:--|:--|
|**Different types**|Stealth virus, self-modified virus, encryption with variable key virus, polymorphic code virus, metamorphic code virus.|E-Mail worms, instant messaging worms, Internet worms, IRC worms, file-sharing, networks worms.|
|**Spread mode**|Needs a host program to spread.|Self-spreading, without user intervention.|
|**What is it?**|A software program that copies itself and infects data or information without user knowledge; needs a host program to carry it for spreading.|A self-replicating software program that spreads through a network; can send copies through the network.|
|**Inception**|Creeper virus (early 1970s, ARPANET).|Shockwave Rider (science fiction novel, 1975).|
|**Prevalence**|Very high.|Moderate.|

Both viruses and worms are typically delivered as E-Mail attachments or downloaded files. Worms specifically use holes in network protocols directly for propagation.

## Virus spread via :-

![](images/2.1.png)

![](images/2.2.png)


---

## Trojan Horses and Backdoors

Trojan Horses and Backdoors are both types of malicious software (malware) used by cybercriminals to gain unauthorized access and control over computer systems.

**Trojan Horses** A Trojan Horse is a type of malware that disguises itself as, or is contained within, seemingly harmless programming or data. Its primary goal is to gain control of a system and cause harm once activated. Unlike viruses, Trojan Horses do not self-replicate; they require a user to execute them, often by being enticed to open an attachment or download a file. They can be delivered via web browsers, email attachments, or downloaded software.

**Typical actions of a Trojan Horse include:**

- Erasing, overwriting, or corrupting data on the computer.
- Helping to spread other malware.
- Deactivating or interfering with antivirus software and firewalls.
- Allowing remote access to your computer.
- Uploading and downloading files without the user's knowledge.
- Gathering email addresses and using them for spam.
- Causing the system to slow down, restart, or shut down.
- Reinstalling themselves after being disabled.
- Disabling the task manager or control panel.
- Copying fake links to false websites.
- Displaying pornographic sites, playing sounds/videos, or displaying images.
- Logging keystrokes to steal information such as passwords or credit card numbers.

Trojan Horses are often delivered as email attachments or can be installed by hackers to commandeer a computer. Some phishing techniques, like Gillnet, can inject a Trojan Horse into a system, which then logs user actions and sends stolen data to the phisher. Blended threats can bundle Trojan Horses with other malware like viruses and worms.

**Backdoors** A backdoor is a method of accessing a computer program or system that bypasses normal security mechanisms or authentication procedures. Programmers might initially create backdoors for troubleshooting, but attackers can detect or install them as part of an exploit. Backdoors operate in the background, remain hidden from the user, and are considered highly dangerous because they allow a malicious person to perform virtually any action on the compromised system.

**A backdoor can enable an attacker to perform various actions, such as:**

- Creating, deleting, renaming, copying, or editing files.
- Changing system settings and altering the Windows registry.
- Running, controlling, and terminating applications.
- Installing arbitrary software.
- Controlling computer hardware devices and modifying related settings.
- Shutting down or restarting a computer without user permission.
- Stealing sensitive personal information.
- Logging user activity and tracking web browsing habits.
- Recording keystrokes and capturing screenshots.
- Sending all gathered data to a predefined email address.
- Infecting files, corrupting installed applications, and damaging the entire system.
- Distributing infected files to remote computers and performing attacks against hacker-defined remote hosts.
- Installing hidden FTP servers that malicious persons can use.
- Degrading Internet connection speed and overall system performance.
- Providing uninstall features and hiding processes, files, and other objects to complicate its removal.

**Examples of Backdoor Trojans include:**

- **Back Orifice:** Enables a user to control a computer running Microsoft Windows OS from a remote location.
- **Bifrost:** Infects Windows 95 through Vista.
- **SAP backdoors:** Exploits vulnerabilities in SAP (Enterprise Resource Planning) systems, which are central to business processes.
- **Onapsis Bizploit:** An open-source ERP penetration testing framework that assists security professionals in discovering and exploiting ERP vulnerabilities.

**Distinction and Relationship:** While backdoors are a method of access, Trojan Horses are a _delivery mechanism_ that often _contain_ or _install_ backdoors. A Trojan Horse brings the malicious payload (which could be a backdoor) into the system, and once executed, that payload can then create persistent unauthorized access via a backdoor.

**Protection against Trojan Horses and Backdoors:** To protect against these threats, it is recommended to:

- **Avoid suspect websites and weblinks:** Do not download free or pirated software from untrusted sources, as these often contain Trojans.
- **Surf the web cautiously:** Be careful when connecting to or downloading information from peer-to-peer (P2P) networks, as they are known to spread malicious software like Trojans.
- **Install and maintain antivirus/Trojan remover software:** Antivirus software often has built-in features to protect against various malware, including Trojans.

---

## Steganography

Steganography is an art and science that focuses on "sheltered writing," meaning it involves hiding the existence of a message or communication. The term originates from two Greek words: "Steganos," meaning "covered," and "graphein," meaning "to write" or "concealed writing". It is a method of attempting to conceal information.

**How Steganography Works** In steganography, a secret message is embedded within a "cover medium" in such a way that its presence is not obvious. The cover medium can be various forms of innocent data, such as audio, still images, or video. For example, in a digital image, the least significant bit of each word can be used to form a message without causing any noticeable change to the image. A "stegokey" or password is required for this process.

![](images/2.3.png)

**Purpose and Use** Steganography is used to embed a hidden "trademark" in images, music, and software, a technique also referred to as watermarking. This digital watermarking can be used to detect illegal copying of digital images.

**Steganalysis** Steganalysis is the art and science of detecting messages that have been hidden using steganography. Its primary goal is to identify suspected packages and determine whether they contain an encoded payload, and if possible, to recover that payload. Automated tools are available to help detect steganographed data/information hidden in image, audio, and video files.

**Relationship with Cryptography** The source material does not explicitly detail the _difference_ between steganography and cryptography in a dedicated section, but it can be inferred that while cryptography focuses on securing the _content_ of a message, steganography focuses on securing its _existence_.

**Tools for Steganography** The sources provide a list of websites that offer steganography tools:

- DiSi-Steganograph: http://www.securityfocus.com
- Invisible Folders: http://www.brothersoft.com/invisible-folders/
- Invisible Secrets: http://www.programurl.com/stealth-files.htm
- Stealth Files: http://www.programurl.com/hermetic-stego.htm
- DriveCrypt Plus (DCPP): http://www.petitcolas.net/fabien/steganography/mp3stego
- MP3Stego: http://compression.ru/video/stego_video/index_en.html

An advanced form of information hiding mentioned is using Sudoku puzzles and SMS. Messages can be concealed within a Sudoku puzzle image and communicated via SMS; the recipient solves the puzzle to extract the hidden data.

![]()
---


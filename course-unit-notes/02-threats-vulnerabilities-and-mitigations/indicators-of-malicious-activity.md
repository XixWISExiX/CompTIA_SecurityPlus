---
Unit: Indicators of Malicious Activity
Domain: 2.0 Threats, Vulnerabilities, and Mitigations (sub-objective 2.4 — Given a scenario, analyze indicators of malicious activity)
Source: Pt2 p.80-100 and Pt3 p.1-30 (global 180-230; printed slide numbers 2-57 to 2-107). Boundaries: Pt2 p.80 = 2.4 roadmap (2-57, "Indicators of malicious activity" highlighted); Pt3 p.31 (2-108) is the next roadmap slide with "Mitigation techniques used to secure the enterprise" highlighted (viewed at validation), so 2.4 ends at Pt3 p.30
Extraction_Status: Fully Extracted (all 51 pages, Pt2 p.80-100 + Pt3 p.1-30, read via vision at 100 dpi)
Pages_Done: Pt2 p.80-100; Pt3 p.1-30
Pages_Remaining: none
Validation_Status: Validated (2026-10-16) — all 51 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt2 p.80-81)

- Pt2 p.80 (2-57) is the Domain 2 roadmap slide with "Indicators of malicious activity" highlighted. (Source: Pt2 p.80)
- Pt2 p.81 (2-58) is the 2.4 Section Topics slide, "2.4 Given a scenario, analyze indicators of malicious activity." (Source: Pt2 p.81)
  - **Malware attacks:** Ransomware; Trojan; Worm; Spyware; Bloatware; Virus; Keylogger; Logic bomb; Rootkit
  - **Physical attacks:** Brute force; Radio frequency identification (RFID) cloning; Environmental
  - **Network attacks:** Distributed denial-of-service (DDoS) (Amplified; Reflected); Domain Name System (DNS) attacks; Wireless; On-path; Credential replay; Malicious code
  - **Application attacks:** Injection; Buffer overflow; Replay; Privilege escalation; Forgery; Directory traversal
  - **Cryptographic attacks:** Downgrade; Collision; Birthday
  - **Password attacks:** Spraying; Brute force
  - **Indicators:** Account lockout; Concurrent session usage; Blocked content; Impossible travel; Resource consumption; Resource inaccessibility; Out-of-cycle logging; Published/documented; Missing logs

## Malware (Source: Pt2 p.82)

- **Malware** (malicious software) — software that enters a computer system without the user's knowledge or consent and is perceived to have a malicious intent in its function. (Source: Pt2 p.82)
  - Several classifications exist to help categorize types of malware; this can be difficult because malware keeps evolving and becoming more complex, producing many different instances. (Source: Pt2 p.82)
  - Some versions of malware have more than one trait; for classification purposes the **primary trait** is used. (Source: Pt2 p.82)

## Viruses (Source: Pt2 p.83-85)

- **Virus** — malicious code that runs on a user's computer without their knowledge and replicates by attaching itself to other executable code; when the infected code is run it may also spread to other files. (Source: Pt2 p.83)
  - Like a biological virus, it infects the host and then replicates itself (or an evolved copy) **with human interaction**. (Source: Pt2 p.83)
- **Virus types** (Source: Pt2 p.84-85):
  - **Armored virus** — protects itself from antivirus by disguising where it is located on the system; also has mechanisms to thwart attempts to examine the code. (Source: Pt2 p.84)
  - **Boot** — loads into the boot sector or partition table of the HDD/USB media; loaded into memory when the system boots. (Source: Pt2 p.84)
  - **Script** — often stored as part of a data file and executed when the file is opened; often seen in PowerShell, Windows Management Instrumentation (WMI), JavaScript, Microsoft Office documents with Visual Basic for Applications (VBA) code enabled, or PDF documents with JavaScript enabled. (Source: Pt2 p.84)
  - **Macro** — infects template files created by Microsoft Office, VBA, Access, Visual Basic, Word and Excel. (Source: Pt2 p.84)
  - **Non-resident / File infector** — the virus is contained within a host executable file and runs with the host process. (Source: Pt2 p.85)
  - **Memory resident** — when the host file is executed, the virus creates a new process for itself in memory, even if the host process is terminated. (Source: Pt2 p.85)
    - **Fileless** — does not write its code to disk; instead uses lightweight shellcode to achieve a backdoor mechanism on the host. May use "live off the land" techniques rather than compiled executables to evade detection. [CONFLICT/NOTE: slide spells it "complied executables"; read as "compiled".] (Source: Pt2 p.85)
    - **Live Off The Land (LotL)** — refers to attacker (APT) behavior that uses fileless, malware-less attacks that turn a system's own native tools against it. (Source: Pt2 p.85)
  - **Stealth virus** — uses several different techniques to go unnoticed by antivirus programs. (Source: Pt2 p.85)
  - **Polymorphic virus** — completely rewrites its code whenever it is executed; mutates itself with many forms to evade detection. (Source: Pt2 p.85)
  - **Metamorphic virus** — rewrites its code after it infects a new file. (Source: Pt2 p.85)
  - **Multipartite virus** — a hybrid that uses multiple infection vectors at the same time. (Source: Pt2 p.85)
  - Picture: shield with a bug icon; decorative. (Source: Pt2 p.85)

## Worms (Source: Pt2 p.86)

- **Worm** — malware that self-replicates, does not require user interaction, and can quickly travel across networks and severely degrade resources. (Source: Pt2 p.86)
  - Sometimes called **network viruses**. (Source: Pt2 p.86)
  - Designed to enter a computer through the network, then exploit a vulnerability in an application or OS on the host. (Source: Pt2 p.86)
  - Once it has exploited one system, it immediately searches for another computer on the network with the same vulnerability. (Source: Pt2 p.86)
  - Can slow the network by replicating so quickly that they consume all network resources; some leave a payload on infected systems that causes harm. (Source: Pt2 p.86)
  - Virus vs. worm: both automatically self-replicate but differently — a **virus** self-replicates *on* the host computer and does not spread to other computers by itself; a **worm** self-replicates *between* computers. (Source: Pt2 p.86)

## Trojans and RATs (Source: Pt2 p.87)

- **Trojan** — software that appears to do one thing but hides other, malicious functionality; often opens a port that an attacker can use to connect to a system. (Source: Pt2 p.87)
  - Can be considered a delivery vehicle for payloads (RAT, spyware, adware, rootkit, ransomware). (Source: Pt2 p.87)
- **Remote Access Trojan (RAT)** — the most common type of Trojan; has the basic Trojan functionality but also gives the threat agent unauthorized remote access to the victim's computer using specially configured communication protocols. (Source: Pt2 p.87)
  - Creates an opening into the victim's computer allowing unrestricted access. (Source: Pt2 p.87)
  - Attacker can monitor the user, change computer settings, browse and copy files, access the camera/microphone, and use the computer to access other computers on the network. (Source: Pt2 p.87)
- Callout bar: a **"wrapper" or "binder"** is a program that allows you to bind an executable (Trojan) with a legitimate application. (Source: Pt2 p.87)

## Backdoors and rootkits (Source: Pt2 p.88)

- **Backdoor** — a program installed by an attacker that bypasses normal authentication on a system and gives access to a computer, program, service, or cryptosystem. (Source: Pt2 p.88)
  - After initial compromise an attacker can return later, bypassing security settings. (Source: Pt2 p.88)
  - **Maintenance hook** — a backdoor installed by a developer/vendor that bypasses normal authentication; used for maintenance purposes. (Source: Pt2 p.88)
- **Rootkit** — malware designed to gain administrator-level control of a system without being detected. (Source: Pt2 p.88)
  - Can avoid OS security controls and hide their activities very well; can hide within the kernel, firmware, and even hypervisors; activated before the OS has fully booted. (Source: Pt2 p.88)
  - Five basic types: **Firmware** (infects device firmware); **Virtual** (infects the hypervisor of a VM); **Kernel** (infects at the lowest level of an OS); **Library** (infects DLL files of the OS); **Application** (infects portions of an application). (Source: Pt2 p.88)

## Data collection malware: spyware and keyloggers (Source: Pt2 p.89)

- **Spyware** — tracking software deployed without the consent or control of the user. (Source: Pt2 p.89)
  - Secretly monitors users, using the computer's resources to collect and distribute personal or sensitive information; may include keylogging software recording keystrokes, mouse clicks, and screenshots. (Source: Pt2 p.89)
- **Keylogger** — a type of spyware that silently captures and stores each keystroke typed; also capable of capturing mouse clicks, screenshots, and active video feeds. (Source: Pt2 p.89)
  - **Physical keyloggers** — require physical access to install/remove the device between the keyboard and the computer. (Source: Pt2 p.89)
  - **Software keyloggers** — no physical access needed; often installed remotely via a Trojan or virus; often send captured data to the attacker via online communication channels. (Source: Pt2 p.89)

## Grayware, PUPs, adware, bloatware (Source: Pt2 p.90)

- **Grayware** — software in the "gray area" between outright malware and legitimate conventional software; sometimes referred to as potentially unwanted programs (**PUPs**). The two most common types are **adware** and **trackware**. (Source: Pt2 p.90)
- **PUP / PUA** (Potentially Unwanted Programs/Applications) — software installed alongside a package selected by the user or bundled with a new computer system. (Source: Pt2 p.90)
- **Adware** — delivers advertising content in a way that is unexpected and unwanted. (Source: Pt2 p.90)
  - Can reconfigure browser settings to allow tracking cookies, change default search engines, open sponsor pages at startup, add bookmarks; typically displays banners, pop-ups, or opens new browser windows at random intervals. (Source: Pt2 p.90)
- **Tracking cookies** — plaintext files containing sites visited, search queries, browser metadata and IP address. (Source: Pt2 p.90)
- **Bloatware** — unwanted pre-installed software on a computer or device; started with OEMs installing software by default to make money and give consumers additional software they may want. (Source: Pt2 p.90)

## Advertising attacks, malvertising, ad fraud (Source: Pt2 p.91-93)

- Online advertising is very profitable for websites; site owners are paid for showing ads (analogy: landowners leasing land near highways). The website itself does not contain the ads; it connects to third-party advertising network sites that provide banners, pop-ups, video and pictures and displays them in the user's browser. (Source: Pt2 p.91)
- Diagram: a victim laptop connected by black lines to two "Legitimate Ad Server" icons and by a red line to a "Malicious Ad Server" (hooded figure). Credited "Images created by an Education Ecosystem Instructor". (Source: Pt2 p.91)
- **Malvertising** (malicious advertising) — attacker takes advantage of third-party advertising network sites to spread malware. (Source: Pt2 p.92)
  - Normal operation: page connects to third-party ad networks to retrieve ads, which are tracked and displayed. (Source: Pt2 p.92)
  - Malicious operation: attackers use ad networks to distribute malware by (a) infecting the third-party advertiser so malware goes out via the ads, or (b) promoting themselves as reputable third-party advertisers while purposely distributing malware through their ads. (Source: Pt2 p.92)
  - Well-known websites have been targeted as well as smaller ones. Table "Monthly Visitors": msn.com 1,300,000,000; Nytimes.com 313,100,000; BBC.com 290,600,000; NFL.com 60,700,000. (Source: Pt2 p.92)
- **Ad fraud** — attackers manipulate the advertising auction process using a "robo-browser" called a **Methbot**. (Source: Pt2 p.93)
  - Methbot spoofs interactions between the browser and the ad auction site and redirects the ad revenue from the advertiser back to the attacker rather than to the website. (Source: Pt2 p.93)
  - Ad locations (banner, in-line, sides) are awarded by an automated auction to the highest bidder within milliseconds; the browser receives the ad, verifies the site being viewed and that the ad was received and played/displayed; the site owner is then paid. Average rate about 1.3 cents per view; a website with a lot of traffic can generate a significant amount of revenue from ads. (Source: Pt2 p.93)

## Ransomware (Source: Pt2 p.94-96)

- **Ransomware** — malware that encrypts data in such a way that it cannot be bypassed and prevents the computer from properly and fully functioning until a fee is paid; one of the fastest-growing forms of malware. (Source: Pt2 p.94)
- **Scareware** — malware that attempts to convince a user a threat exists (when there is none); similar to ransomware but **no encryption** of user data. (Source: Pt2 p.94)
- **Blocker ransomware** — appears to come from a legitimate/reputable source and gives a "valid" reason for blocking the computer. Examples: law enforcement ("you accessed a prohibited site and must immediately pay a fine online"); software vendor ("your software license has expired or there is a hardware problem or malware infection"). (Source: Pt2 p.94)
- **WannaCry/Wcry** — a **cryptoworm** targeting Microsoft Windows, encrypting data and demanding ransom in Bitcoin. (Source: Pt2 p.95)
  - Exploited a security vulnerability in **SMB**; the system was unusable until ransom paid. (Source: Pt2 p.95)
  - The vulnerability was first discovered by the **NSA**, which never reported it publicly and used it in its attack/spying tool arsenal ("**EternalBlue**"). EternalBlue code was stolen by a group calling themselves the **Shadow Brokers**, who claim to have 75% of the current NSA arsenal and sell via subscription for 100 Zcash (~$21,000). Portions of EternalBlue code were copied verbatim into WannaCry. (Source: Pt2 p.95)
- **Crypto-malware** — a much more malicious version of ransomware that encrypts all files on a device, preventing the user from opening them. (Source: Pt2 p.96)
  - Recent attacks: cost for the key increases if payment is not received within a set number of hours; encrypted files start to be deleted after a set time and can only be stopped with the key; encrypts all files on any network or attached device (USB keys, external HDD, network servers/drives, cloud repositories); mobile devices can also be targets. (Source: Pt2 p.96)
  - **Operation:** once infected, the software connects to the command and control (C&C) server for instructions/updated data; a locking key is generated for the encrypted files and then encrypted with another key from the C&C; the second locking key is what is sent to victims once they pay. (Source: Pt2 p.96)

## Logic bomb (Source: Pt2 p.97)

- **Logic bomb** — malware that sits dormant until a pre-determined event (e.g. time, network activity, security event) causes it to trigger. (Source: Pt2 p.97)
  - Not to be confused with **Easter eggs** — undocumented but benign features inserted by developers (for recreation or notoriety) during development. (Source: Pt2 p.97)
- Picture: countdown-timer dynamite (00:00:05); decorative. (Source: Pt2 p.97)

## RFID and NFC (Source: Pt2 p.98)

- **Radio Frequency Identification (RFID)** — special tags attached to objects respond to specific radio frequencies and can be used to identify and track them. Range from 10 cm up to 200 m, therefore susceptible to MITM attacks. (Source: Pt2 p.98)
- **Near Field Communication (NFC)** — a newer RF-based technology requiring transmitting and receiving devices to be within **4 cm** of each other; commonly used for contactless payment, proximity readers, other non-contact communication between devices. (Source: Pt2 p.98)

## Physical attacks (Source: Pt2 p.99)

- A physical attack is directed against cabling infrastructure, hardware devices, or the environment of the site facilities hosting the network. (Source: Pt2 p.99)
- **Brute force** — smashing a hardware device to perform a physical DoS; breaking into premises or cabinets by forcing a lock or gateway; likely an indicator of theft or tampering. (Source: Pt2 p.99)
- **RFID cloning and skimming** (Source: Pt2 p.99)
  - **Cloning** — making one or more copies of an existing card; a lost/stolen card with no cryptographic protections can be physically duplicated; card loss should be reported immediately so it can be revoked and a new one issued. Sub-bullet: **Digital pickpocketing**.
  - **Skimming** — using a counterfeit reader to capture card or badge details, which are then used to program a duplicate.
- **Environmental** — perform DoS; a threat actor could try to destroy power lines, cut network cables, or disrupt cooling systems. (Source: Pt2 p.99)

## Denial of Service (Source: Pt2 p.100)

- **Denial of Service (DoS)** — disrupt or deny services to legitimate users, networks, or systems by exhausting system resources. (Source: Pt2 p.100)
  - **Application level** — attacker sends more traffic to an application than it can handle; though the traffic is often "legitimate", the service fails (e.g. web server attack). (Source: Pt2 p.100)
  - **Ping of Death** — an ICMP message is fragmented and sent to a target; upon re-assembly the message is larger than the system can handle (greater than 65,536 bytes), causing a crash. (Source: Pt2 p.100)
  - **Teardrop attack** — attacker sends mangled IP fragments with overlapping and oversized payloads, causing the receiving computer to crash/reboot due to a vulnerability in TCP/IP fragmentation reassembly code. (Source: Pt2 p.100)
  - **SYN flooding** — a large number of TCP SYN packets are sent to a target very quickly, using up open connections and preventing legitimate users from accessing a system. (Source: Pt2 p.100)

## Botnets and command & control (Source: Pt3 p.1-2)

- **Bots (agents, zombies)** — small pieces of software installed on hosts that run autonomously and allow the system to be used in large-scale malicious activity such as DDoS or data mining; the compromised system can be placed under the attacker's remote control. (Source: Pt3 p.1)
- **Botnet** — hundreds of thousands or even millions of bot-controlled computers gathered into a logical computer network. (Source: Pt3 p.1)
  - **Bot herder (handler)** — the system that controls the compromised computers and issues commands, launches attacks, etc. (Source: Pt3 p.1)
- **Command & control structure** (Source: Pt3 p.2):
  - **Website** — bot automatically signs into a website the bot herder controls and is programmed to locate commands placed there.
  - **Blogs, Twitter (X), Facebook** — commands sent via blogs, specially coded attack commands in Twitter (X) posts, or notes posted on Facebook.
  - **Dead drop C&C** — herder creates draft email messages (never sent) containing commands; bots log into the email account, read the draft, and execute the commands.
  - Picture: rows of laptops with skull icons above a central laptop; decorative.

## DDoS, DRDoS, amplification (Source: Pt3 p.3-4)

- **Distributed Denial-of-Service (DDoS)** — an attack using infected Internet-connected computers and devices to disrupt the normal flow of traffic of a server or service by overwhelming the target with traffic. (Source: Pt3 p.3)
- **Distributed Reflected DoS (DRDoS)** — a malicious request to a legitimate server is created and sent as a link to the victim so that a server-side flaw causes the malicious component to run on the target's browser. (Source: Pt3 p.3)
  - The threat actor spoofs the victim's IP address and tries to open connections with multiple third-party servers; those servers direct their SYN/ACK responses to the victim host; this rapidly consumes the victim's bandwidth. (Source: Pt3 p.3)
  - [CONFLICT/NOTE] The first sentence (link running in the target's browser) reads like a reflected-XSS description; the sub-bullets describe the reflection via spoofed SYN/ACK. Kept as printed.
- **Amplification attack** — a network-based attack where the attacker dramatically increases the bandwidth sent to a victim during a DDoS by implementing an amplification factor. (Source: Pt3 p.3)
  - A type of reflected attack targeting weaknesses in specific application protocols to be more effective at consuming bandwidth; exploits protocols that let the attacker manipulate the request so the target is forced to respond with a large amount of data; examples: **DNS, NTP, and Connectionless LDAP (CLDAP)**. (Source: Pt3 p.3)
- **Diagram "DDoS – continued"** (Source: Pt3 p.4): an Attacker (masked figure on a laptop screen) at top points to three HANDLER laptops; each handler points to three AGENT laptops (nine agents total); all agents' arrows converge on a Victim computer inside a cloud. Credited to an Education Ecosystem Instructor.

## Smurf and Fraggle (Source: Pt3 p.5)

- **Smurf attack** — attacker sends an ICMP ECHO Request (ping) to a network's broadcast IP address using a spoofed IP address of the target; the entire subnet then responds to the target IP with an ICMP ECHO Reply. (Source: Pt3 p.5)
- Callout: Microsoft Windows-based machines will not generate an answer (ICMP ECHO Reply) to an ICMP ECHO Request aimed at the broadcast address or the network address. (Source: Pt3 p.5)
- Diagram: Attacker Address 172.68.10.1 sends an ECHO request (SRC: 10.10.1.2, DST: 192.168.10.255) to Router 192.168.10.1; hosts 192.168.10.2 … 192.168.10.254 each send an ECHO reply (DST: 10.10.1.2) to the Target 10.10.1.2. (Source: Pt3 p.5) [Note: the attacker address and the spoofed source are different addresses as printed.]
- **Fraggle attack** (banner) — works similarly to Smurf but uses **UDP** packets instead of ICMP. (Source: Pt3 p.5)

## Poisoning attacks: ARP and cache (Source: Pt3 p.6)

- **Cache** — stored information on servers and hosts that can be accessed in the future. (Source: Pt3 p.6)
- **ARP poisoning** — ARP resolves MAC addresses with IP addresses; attackers can poison an ARP table to support active sniffing and man-in-the-middle attacks. (Source: Pt3 p.6)
- **ARP spoofing** — a simple way around switch limitations and collision domains: by making the default gateway MAC permanent (`arp -s`) on each device and setting it as your MAC, all broadcasts to that default gateway are sent to your own machine. (Source: Pt3 p.6)
- **ARP (MAC) flooding** — attacker connects to a switch and injects thousands of random MAC addresses; eventually the **CAM table** fills and no new MAC addresses can be learned, so the switch floods traffic from new hosts out all ports. (Source: Pt3 p.6)
  - Turns a switch into a virtual hub, enabling eavesdropping and MITM attacks. (Source: Pt3 p.6)
- Pictures: three yellow hazard signs (radiation, biohazard, skull); decorative.

## DNS attacks (Source: Pt3 p.7-9)

- **Domain Name System (DNS)** — correlates canonical names (e.g. google.com) to IP addresses; "like a phone book for websites." (Source: Pt3 p.7)
- **DNS cache poisoning** — altering the information stored in the DNS cache to redirect the computer to another device (IP address). (Source: Pt3 p.7)
- **Pharming** — redirecting traffic of a legitimate website to a malicious or fraudulent website. (Source: Pt3 p.7)
  - Uses DNS cache poisoning at the DNS server and/or Hosts file modification of the host to redirect the victim. (Source: Pt3 p.7)
  - Example: the victim enters the correct www.goodsite.com but is directed to the IP address of www.badsite.com because of the change to the Hosts file. (Source: Pt3 p.7)
  - Screenshot: Windows Notepad showing the sample HOSTS file (Microsoft Corp. 1993-2009; example entries `102.54.94.97 rhino.acme.com`, `38.25.63.10 x.acme.com`; `127.0.0.1 localhost`, `::1 localhost`). (Source: Pt3 p.7)
- **Diagram "DNS Cache Poisoning / Pharming"** (Source: Pt3 p.8): (1) Attacker asks the DNS Server "What is the address of www.badguy.net?"; (2) the DNS server asks the Attacker's DNS server ns.badguy.net "Send IP address of www.badguy.net"; (3) the attacker's server replies "Here are all badguy addresses" — a table mapping www.good.net, www.better.net, www.best.net all to 192.168.1.4; (4) Victim asks "What is the address of www.good.net?"; (5) DNS server answers 192.168.1.4 (an attacker's address).
- **DNS amplification attack** — similar to Smurf; the attacker sends DNS query requests with the spoofed source IP of the target server so DNS responses go to the target. (Source: Pt3 p.9)
  - DNS query requests are typically much smaller than the responses; lets an attacker use relatively small bandwidth to generate a large attack. (Source: Pt3 p.9)
  - Diagram: Attacker → Attacker's Botnet → "Spoofed DNS Requests" to six DNS servers → "Amplified DNS Responses" to the Victim Server. (Source: Pt3 p.9)

## Wireless attacks (Source: Pt3 p.10)

- **Evil twin** — a rogue, counterfeit, unauthorized WAP that uses the same SSID as a nearby wireless network, often public hotspots. (Source: Pt3 p.10)
- **Jamming** — radio waves disrupt 802.11 wireless signals. (Source: Pt3 p.10)
- **Initialization Vector (IV) attacks** — a related-key attack in which the attacker monitors the operation of a cipher using several keys to determine a mathematical relationship between the keys and eventually decipher the data. (Source: Pt3 p.10)
- **Wi-Fi disassociation/de-authentication attack** — attacker targets a wireless user with a scanner, then uses special software to force the user to disassociate from the network; the attacker then monitors the client's re-association to the WAP to gather the SSID and WPA/WPA2 handshake information and eventually the passphrase. (Source: Pt3 p.10)

## Interception / on-path attacks (Source: Pt3 p.11-13)

- **Interception attacks** — rely on the attacker inserting themselves into the communication path. (Source: Pt3 p.11)
- **Man-in-the-middle (on-path) attack** — attacker positions between the communication of network devices, allowing them to forge a fictitious response to the sender; **passive** attack — record/sniff transmitted data without altering it; **active** attack — alter contents of data before sending to the recipient. (Source: Pt3 p.11)
  - Diagram: (1) User A attempts to establish an encrypted session with User B; (2) attacker intercepts the transmission, poses as User B and exchanges his own keys with User A, who thinks the attacker's keys are User B's; (3) User B sends all messages to the attacker, who receives, decrypts, copies, and forwards copies to User A. (Source: Pt3 p.11) [Note: step 3 text as printed.]
- **Replay attack** — attacker makes a copy of the data and sends it to the recipient at a later time. (Source: Pt3 p.12)
  - Can be prevented with random keys valid only for a short time, or by ending sessions. (Source: Pt3 p.12)
  - Underlined sub-bullet: **credential, token, session ID, or cookie replay**. (Source: Pt3 p.12)
- **Man-in-the-browser attack** — like MITM, but the attacker intercepts communications between the browser and the underlying computer. (Source: Pt3 p.12)
  - Typically begins with a Trojan or XSS infecting the computer and installing an extension/add-on into the browser configuration that launches with the browser and monitors sites visited. (Source: Pt3 p.12)
  - The browser sends data to the server, which processes the transaction and returns a receipt; the malicious extension captures the receipt and modifies it with the data the user originally entered so a legitimate transaction appears to have occurred. (Source: Pt3 p.12)
- **TCP session hijacking** — a spoofing attack that predicts the sequence and acknowledgement numbers of a TCP connection and then takes over the connection. (Source: Pt3 p.12)
- **SSL stripping** — a website is downgraded from HTTPS to HTTP. (Source: Pt3 p.13)
  - To prevent clients being exploited, sites can use **HTTP Strict Transport Security (HSTS)**. Also listed: MITM via ARP poisoning; spoofing to masquerade as default gateway; sniff credentials in plaintext; create XSS attacks. (Source: Pt3 p.13)
  - Diagram: Victim's System ↔(red X)↔ SSL Encrypted Website (https://); victim talks HTTP to the Attacker, attacker talks HTTPS to the website. (Source: Pt3 p.13)

## Malicious code indicators (Source: Pt3 p.14)

- **Shellcode** — a minimal program designed to exploit a vulnerability in the OS or a legitimate app to gain privileges, or to drop a backdoor on the host if run as a Trojan; followed by some type of network connection to download additional tools. (Source: Pt3 p.14)
- **Credential dumping** — access the credentials file (**SAM** on a local Windows workstation) or sniff credentials held in memory by the **lsass.exe** system process. (Source: Pt3 p.14)
  - A **DCSync** attack tries to trick a domain controller into replicating its user list and credentials with a rogue host. (Source: Pt3 p.14)
- **Pivoting / lateral movement / insider attack** — execute a process remotely using a tool such as **PsExec or PowerShell**; these commands can blend in with ordinary network operations though they could be anomalous for that account. Actions: seek data assets; change the system security configuration; open a firewall port; create an account. (Source: Pt3 p.14)
- **Persistence** — a mechanism that lets the threat actor's backdoor restart if the host reboots or the user logs off: use **AutoRun keys in the registry**; add a **scheduled task**; use **WMI event subscriptions**. (Source: Pt3 p.14)

## Injection attacks (Source: Pt3 p.15)

- **LDAP injection** — similar to SQL injection; LDAP query strings can be manipulated to execute commands, modify content, or return results to unauthorized queries. (Source: Pt3 p.15)
  - **LDAP** — protocol used in Microsoft Active Directory to query the database for information about specific users (names, accounts, access, department, phone number etc.). (Source: Pt3 p.15)
- **XML injection** — attacker uses vulnerabilities in XML implementation to query XML using **XPath** and can return entire documents; similar to SQL injection in application but does not have the same levels of access controls as SQL. (Source: Pt3 p.15)
- **DLL injection** — a Dynamic Link Library (DLL) is a set of functions applications can call to carry out procedures. (Source: Pt3 p.15)
  - **Shimming** — developing and implementing additional code between an application and the OS to enable functionality otherwise unavailable, by calling the Application Compatibility Framework.
  - **Refactoring** — evades AV detection altogether by using different methods.

## Spoofing and clickjacking (Source: Pt3 p.16-17)

- **Spoofing** — causes data to appear as if from another source and could take advantage of "**transitive trust**." (Source: Pt3 p.16)
  - **E-mail spoofing** — sent with a "From" address different from the actual sender; **IP address spoofing** — obfuscates the source IP address; **MAC address spoofing** — obfuscates the client's MAC address. (Source: Pt3 p.16)
- **Clickjacking** — user is tricked into clicking something different from what they thought they were clicking on; typically implemented as a concealed link or embedded code/script that executes when clicked. (Source: Pt3 p.17)
  - Diagram: a login form (Username / Password / LOGIN) labelled "Fake input controls positioned under the hijacked web controls"; "Attacked website is transparent"; "User provides username and password. All these clicks are hijacked by the invisible frame." (Source: Pt3 p.17)

## Privilege escalation (Source: Pt3 p.18)

- A buffer overflow can result in **escalation of privilege** attacks: code runs with higher privileges and can give an end user administrator or root access. (Source: Pt3 p.18)
  - **Vertical escalation** — a lower-privilege user accesses functions reserved for a higher-privileged user. (Source: Pt3 p.18)
  - **Horizontal escalation** — a normal user accesses functions reserved for another normal user. (Source: Pt3 p.18)
  - Diagram: triangle with Administrator at the apex; dashed arrow Bob → Administrator labelled "Vertical Escalation"; dashed arrow Bob → Alice labelled "Horizontal Escalation". (Source: Pt3 p.18)

## Directory traversal (Source: Pt3 p.19)

- **Directory traversal attack** — common and very successful on older web servers; also known as the "**dot-dot-slash attack**." (Source: Pt3 p.19)
  - A web server is a set of directories and files granted to authorized users; an attacker tries to access files that are NOT authorized. By concatenating `../` in a URL, an attacker can potentially access directories not meant to be traversed. (Source: Pt3 p.19)
  - Diagram: folder tree (Windows → System32; Inetpub → wwwroot) with example URL `http://www.example.com/../../Windows\System32\cmd.exe`; a "../" label above a blank parent folder; blue arrows go up from wwwroot (and from Inetpub to the parent folder), red arrows go from the parent folder to Windows and down to System32. (Source: Pt3 p.19)
- Slide title also names "Command Injection Attacks"; no separate command-injection content appears on this slide. [GAP] (Source: Pt3 p.19)

## Cryptographic attacks (Source: Pt3 p.20-23)

- Cryptographic attacks fall within two main types: **algorithm attacks** (target weaknesses in the algorithms or their implementations) and **collision attacks** (generate then exploit collisions). (Source: Pt3 p.20)
- **Algorithm attacks** (Source: Pt3 p.21):
  - **Brute force** — trying every possible key; will always succeed but likely takes so long it is not usable.
  - **Frequency analysis** — study of the frequency of letters or groups of letters in a ciphertext; an aid to breaking classical ciphers. The cryptanalyst looks for common words (is, that, the) to determine a pattern and deduce the method used (decoder ring); looks at blocks of the encrypted message for common patterns; **does not work on modern algorithms**.
  - **Related key attack** — similar to chosen plaintext except the attacker can obtain ciphertexts encrypted under two different keys.
  - **Downgrade attack** — attacker forces the system to abandon the current version of the security mode within the hardware/software and revert to an older, less secure version; for this to succeed the hardware/software must be **backwards compatible**.
- **Collision attacks** — an attempt to find two input strings of a hash function that produce the same hash result; when two variable inputs result in the same fixed-length output (hash), this is a **collision**. (Source: Pt3 p.22)
- **Birthday attack** — based on the **birthday paradox**: for a 50 percent chance that someone in a room shares *your* birthday, **253** people would be needed; for a greater than 50 percent chance that *any two* people share a birthday, only **23** people are needed because matches are based on pairs. (Source: Pt3 p.22)
- **Cryptanalytic attacks** (Source: Pt3 p.23):
  - **Known ciphertext (ciphertext only)** — all that is known to the attacker is the ciphertext, which can still reveal clues; "most common type of active attack because it is very easy to get ciphertext by sniffing someone's traffic"; also "most difficult, attacker only has ciphertext from sniffing." [Note: both statements printed on the slide; sniffing is passive in other contexts — kept as printed.]
  - **Known plaintext** — attacker has access to both ciphertext and plaintext; messages usually start with the same type of beginning and close with the same type of ending.
  - **Chosen plaintext** — attacker obtains the ciphertext associated with a set of plaintexts of their choosing ("send a message and hope they encrypted it and send it to others"); **offline** (attacker prepares a list of plaintexts) or **online** (attacker chooses plaintext based on ciphertext already received).
  - **Chosen ciphertext** — attacker has access to the decryption device and can modify the ciphertext before putting it into the device; attacker chooses both plaintext and ciphertext values, chooses the ciphertext to be decrypted and has access to the resulting decrypted plaintext.

## Password attacks (Source: Pt3 p.24-28)

- **Terminology** (Source: Pt3 p.24):
  - **Brute-force attack** — every possible combination of characters; always effective given adequate time and resources.
  - **Shoulder surfing** — social engineering technique. **Rubber hose** — physical coercion.
  - **Password cracker** — uses comparative analysis and systematically guesses until it cracks the password.
  - **Dictionary attack** — uses a prearranged list of likely words per victim and attempts each one at a time.
  - **Rainbow table / cryptanalysis attack** — a type of dictionary attack using precomputed hashed passwords. **Salting** — defeats Rainbow Table attacks by adding random or pseudorandom data to the end of the password before hashing.
  - **Password spraying** — a brute-force *online* attack that uses the same password on different accounts to bypass system lockout.
  - **Pass the hash** — using the password hash itself to authenticate; not really cracking or determining the password.
- **Password authentication steps** (diagram, Source: Pt3 p.25): (1) user provides username and password (example: bob / apple); (2) password is hashed by the system (example hash A90BC322, "Hash Algorithm (MD5, SHA, etc.)"); (3) system compares the entered hash with the stored hash; if they do not match, access is refused (example: p@ssw0rd → 6A24CC98 struck out); (4) if hashes match, access is granted (apple → A90BC322 = stored A90BC322).
- **Brute force attack** (diagram, Source: Pt3 p.26): (1) attacker guesses by entering every possible combination of characters (a, A, aa, AA … apple); (2) system hashes entries and compares with the stored hash (example mismatches 98CD367F, 4FE21C90, 004239EF, 46ADE108); (3) once the correct password is entered, the hashes match and access is granted.
- **Dictionary attack** (diagram, Source: Pt3 p.27): (1) attacker enters words from a "dictionary" or "word list" (banana, orange, lemon, apple) — NOTE: can be actual dictionary words or a customized word list based on social engineering; (2) system hashes entries and compares with the stored hash; (3) on the correct password the hashes match and access is granted.
- **Rainbow table attack** (diagram, Source: Pt3 p.28): (1) similar to a dictionary attack but the attacker uses a table of pre-computed hashes rather than a wordlist; used with a password-cracking utility to crack passwords "offline"; (2) the utility compares hashes and uses an algorithm to match them quickly; (3) once the matching hash is identified the associated password is presented to the attacker.

## Indicators of compromise (IoC) (Source: Pt3 p.29-30)

- **Indicator of Compromise (IoC)** — a residual sign that an asset or network has been successfully attacked or is continuing to be attacked; "in other words, an IoC is evidence of a TTP." (Source: Pt3 p.29)
  - **Account lockout** — policy that prevents access to an account under certain conditions such as an excessive number of failed authentication attempts. Indicators: the system has prevented access because of too many failed attempts; the user's password no longer works because a threat actor changed it. (Source: Pt3 p.29)
  - **Concurrent session usage** — an account has started multiple sessions on one or more hosts; the threat actor has obtained the credentials and is signed in on another workstation or over a remote access connection. (Source: Pt3 p.29)
  - **Blocked content** — audit logs show unauthorized attempts to read or copy a file or other data. (Source: Pt3 p.29)
  - **Impossible travel** — authentication attempts from different geographical locations within a short timeframe; the actor uses remote access to sign in from a location they could not have physically reached since their last sign-in. (Source: Pt3 p.29)
  - **Resource inaccessibility** — a network, host, file, or database is not available; typically an indicator of a DoS attack; host and network gateways might be unavailable due to excessive **resource consumption**; a network attack often creates large numbers of connections; malware might disable scanning and monitoring utilities to evade detection. (Source: Pt3 p.30)
    - [GAP] "Resource consumption" appears only as a bolded phrase inside the resource-inaccessibility bullet; there is no separate definition. (Source: Pt3 p.30)
  - **Out-of-cycle logging** — event dates or timestamps are not consistent; a threat actor might manipulate system time or change log timestamps to hide activity. (Source: Pt3 p.30)
  - **Published/documented** — known tactic, technique, or procedure (TTP) documented and published by threat researchers; example: **MITRE ATT&CK** database (attack.mitre.org). (Source: Pt3 p.30)
  - **Missing logs** — events or log files are deleted or tampered with: deleted log files by a threat actor; unusual gaps between log entry times; spoofed log entries to conceal activity. (Source: Pt3 p.30)

## Official-objective gap check (2.4)

Official bullets are those listed on the Section Topics slide (Source: Pt2 p.81). Table re-checked against the slide and note content at validation (2026-10-16); the objective-coverage judgment itself is made in objective_mapping.md, not here.

| Official bullet | Result | Notes |
|---|---|---|
| Malware: ransomware, Trojan, worm, spyware, bloatware, virus, keylogger, logic bomb, rootkit | Covered | Pt2 p.82-97 |
| Physical: brute force, RFID cloning, environmental | Covered | Pt2 p.98-99 (RFID/NFC intro, skimming) |
| Network: DDoS (amplified, reflected) | Covered | Pt3 p.3-5 (DRDoS wording odd — see CONFLICT) |
| Network: DNS attacks | Covered | Pt3 p.7-9 (cache poisoning, pharming, amplification) |
| Network: wireless | Covered | Pt3 p.10 (evil twin, jamming, IV, disassociation) |
| Network: on-path | Covered | Pt3 p.11 |
| Network: credential replay | Weak | Replay defined with "credential, token, session ID, or cookie replay" as one underlined sub-bullet (Pt3 p.12) |
| Network: malicious code | Covered | Pt3 p.14 (shellcode, credential dumping, lateral movement, persistence) |
| Application: injection | Covered | LDAP/XML/DLL injection Pt3 p.15 (SQL injection is only referenced; defined in 2.3 note) |
| Application: buffer overflow | Covered | Here via privilege escalation (Pt3 p.18); defined in 2.3 note (Pt2 p.54) |
| Application: replay | Covered | Pt3 p.12 |
| Application: privilege escalation | Covered | Pt3 p.18 |
| Application: forgery | Not in slides | No request-forgery (CSRF/SSRF) content in this range; clickjacking and spoofing only (Pt3 p.16-17) |
| Application: directory traversal | Covered | Pt3 p.19 |
| Cryptographic: downgrade, collision, birthday | Covered | Pt3 p.21-22 |
| Password: spraying, brute force | Covered | Pt3 p.24-26 |
| Indicators: account lockout, concurrent session usage, blocked content, impossible travel, resource inaccessibility, out-of-cycle logging, published/documented, missing logs | Covered | Pt3 p.29-30 |
| Indicators: resource consumption | Weak | Only mentioned inside resource inaccessibility (Pt3 p.30) |

Suggested objective status: **Weakly Covered** (forgery absent; credential replay and resource consumption thin).

## Validation log

- **Date:** 2026-10-16. **Method:** every page Pt2 p.80-100 and Pt3 p.1-30 (51 pages) rendered with pdftoppm at 130 dpi and opened with vision; each compared bullet-by-bullet, diagram label, number, and citation against the note section. Also viewed Pt3 p.31 (next roadmap, "Mitigation techniques used to secure the enterprise" highlighted; confirms 2.4 ends at Pt3 p.30) and Pt2 p.54 (confirms "Buffer Overflow" slide cited in the gap table).
- **Pages checked, no correction needed:** Pt2 p.80-92, 94-100; Pt3 p.1-3, 5-13, 15-18, 20-30. Citations (Pt2/Pt3 page numbers, not printed slide numbers) all correct.
- **Corrections made:**
  1. Front matter Source: replaced the unverified "Pt3 p.31 not yet viewed; roadmap identity inferred from OCR" with the confirmed Pt3 p.31 roadmap; added printed slide-number range 2-57 to 2-107.
  2. Pt2 p.85: marked slide typo "complied executables" as [CONFLICT/NOTE] (note had silently said "compiled").
  3. Pt2 p.93 (Ad Fraud): added omitted last bullet (website with a lot of traffic can generate significant ad revenue).
  4. Pt3 p.4 (DDoS diagram): "hooded figure" corrected to masked figure on a laptop screen (3 handlers x 3 agents = 9 agents confirmed).
  5. Pt3 p.14: added omitted word "system" ("lsass.exe system process").
  6. Pt3 p.19 (directory traversal diagram): description made accurate (../ label, blue arrows up from wwwroot and Inetpub to the parent folder, red arrows parent -> Windows -> System32).
  7. Official-objective gap check intro: removed "provisional until validation completes" wording; objective-coverage status is left to objective_mapping.md.
- **Gap-check table verification:** Section Topics slide (Pt2 p.81) lists all official bullets exactly as in the note's first section. Table rows confirmed against content: forgery absent (no CSRF/SSRF on any of the 51 pages; Pt3 p.19 title mentions "Command Injection" but has no separate content), credential replay only as one underlined sub-bullet (Pt3 p.12), resource consumption only as a bold phrase inside resource inaccessibility (Pt3 p.30). Page ranges in the table are correct.
- **Slide oddities left as printed and flagged in the note:** DRDoS first sentence reads like reflected XSS (Pt3 p.3); Smurf diagram attacker address 172.68.10.1 vs spoofed SRC 10.10.1.2 (Pt3 p.5); known-ciphertext "most common active attack" via sniffing (Pt3 p.23). Trivial slide typos not marked: "doesnot" (Pt2 p.86), "adware rootkit" missing comma (Pt2 p.87), "makes of copy" (Pt3 p.12).
- **Unresolved doubts:** none material. The printed "global 180-230" page range in front matter was not independently verified (depends on page counts of Pt1/Pt2, outside this check); the Pt2/Pt3 page numbers used for every citation are verified.

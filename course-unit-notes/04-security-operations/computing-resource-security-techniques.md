---
Unit: Common Security Techniques to Computing Resources
Domain: 4.0 Security Operations (sub-objective 4.1 — Given a scenario, apply common security techniques to computing resources)
Source: Pt4 p.88-100 + Pt5 p.1-22 (global 388-422; course slides 4-3 to 4-37). Boundaries confirmed: Pt4 p.88 = 4.1 roadmap (4-3); Pt5 p.23 = 4.2 roadmap (4-38)
Extraction_Status: Fully Extracted (all 35 pages, Pt4 p.88-100 and Pt5 p.1-22, read via vision; boundaries confirmed: Pt4 p.88 and Pt5 p.23 are roadmap slides)
Pages_Done: Pt4 p.88-100; Pt5 p.1-22
Pages_Remaining: none
Validation_Status: Validated (2026-10-16) — all 35 pages re-opened at 100 dpi and compared with the note; see Validation log. Coverage vs. official objective is incomplete — see gap check.
---

## Module roadmap and Section Topics (Source: Pt4 p.88, Pt4 p.89)

- Pt4 p.88 (slide 4-3) is the Domain 4 roadmap slide, with "Common security techniques to computing resources" highlighted. The other roadmap entries, in order: Hardware, software, and data asset management; Vulnerability management; Security alerting and monitoring concepts and tools; Modify enterprise capabilities to enhance security; Identity and access management; Automation and orchestration related to secure operations; Incident response activities; Data sources to support an investigation. (Source: Pt4 p.88)
- Pt4 p.89 (slide 4-4) is the 4.1 Section Topics slide. It lists:
  - Secure baselines: Establish, Deploy, Maintain
  - Hardening targets: Mobile devices, Workstations, Switches, Routers, Cloud infrastructure, Servers, ICS/SCADA, Embedded systems, RTOS, IoT devices
  - Wireless devices: Installation considerations (Site surveys, Heat maps)
  - Mobile solutions: Mobile device management (MDM); Deployment models (BYOD, Corporate-owned/personally enabled (COPE), Choose your own device (CYOD)); Connection methods (Cellular, Wi-Fi, Bluetooth)
  - Wireless security settings: Wi-Fi Protected Access 3 (WPA3); AAA/Remote Authentication Dial-In User Service (RADIUS); Cryptographic protocols; Authentication protocols
  - Application security: Input validation, Secure cookies, Static code analysis, Code signing
  - Sandboxing
  - Monitoring
  (Source: Pt4 p.89)
- Slide-order note: the slides in this range do not follow the Section Topics order exactly (e.g. the 802.11 table and site survey come before mobile management). Each item below is cited to the page where it actually appears.

## Secure baselines (Source: Pt4 p.90)

- **Secure Baseline** — configuration guides, benchmarks, and best practices for deploying and maintaining a network device or application server in a secure state for its given role. (Source: Pt4 p.90)
  - Represents a starting point for security measures, offering a defined minimum level of security that all systems must meet. (Source: Pt4 p.90)
  - A collection of standard configurations and settings for network devices, software, patching and updates, access controls, logging, monitoring, password policies, encryption, endpoint protection, and many others. (Source: Pt4 p.90)
- [GAP] The Section Topics slide lists the baseline lifecycle as Establish / Deploy / Maintain (Pt4 p.89). No slide in the range (Pt4 p.88-100, Pt5 p.1-22) elaborates those three steps.

## Hardening (Source: Pt4 p.91)

- **Hardening** — a process of making a host or app configuration secure by reducing its attack surface, through running only necessary services, installing monitoring software to protect against malware and intrusions, and establishing a maintenance schedule to ensure the system is patched to be secure against software exploits. (Source: Pt4 p.91)
  - Methods to improve a device's security by changing its default configuration, often by implementing the recommendations in published secure baselines. (Source: Pt4 p.91)
  - The process of reducing system vulnerabilities to make IT resources more resilient to attacks. (Source: Pt4 p.91)
  - Involves disabling unnecessary services, configuring appropriate permissions, applying patches and updates, and ensuring adherence to secure configurations defined by the secure baselines. (Source: Pt4 p.91)

### Switches and routers hardening (Source: Pt4 p.92)

Examples of changes from default settings:

- Change default credentials
- Disable unnecessary services and interfaces on a switch or router (not every service or interface is needed; services like HTTP or Telnet should be avoided)
- Use secure management protocols: SSH instead of Telnet; HTTPS instead of HTTP
- Implement access control lists (ACLs)
- Enable logging and monitoring
- Configure port security
- Strong password policies
- Physically secure equipment

(Source: Pt4 p.92)

### Server hardware and operating systems hardening (Source: Pt4 p.93)

Examples of changes from default settings:

- Change default credentials
- Disable unnecessary services
- Apply software security patches and updates regularly
- Least privilege principle
- Use firewalls and intrusion detection systems (IDS)
- Secure configurations — use baseline configurations provided by CIS or STIGs
- Strong access controls — strong password policies; multifactor authentication (MFA); privileged access management (PAM)
- Enable logging and monitoring
- Use antivirus and antimalware solutions
- Physical security

(Source: Pt4 p.93)

## Wireless networking (Source: Pt4 p.94)

- Wireless networking is the transmission of packetized data by means of a physical topology that does not use direct physical links/cabling, but rather radio waves to carry the signals over public or private bands. (Source: Pt4 p.94)
- **802.11 Standard** — IEEE has standardized the protocol for wireless local area networks (WLANs). (Source: Pt4 p.94)

| IEEE Standard | Frequency | Max Data Rate | Max Range |
|---|---|---|---|
| 802.11a | 5 GHz | 54 Mbps | 400 ft. |
| 802.11b | 2.4 GHz | 11 Mbps | 450 ft. |
| 802.11g | 2.4 GHz | 54 Mbps | 450 ft. |
| 802.11n (Wi-Fi 4) | 2.4 & 5 GHz | 600 Mbps | 825 ft. |
| 802.11ac (Wi-Fi 5) | 5 GHz | 1 Gbps | 1000 ft. |
| 802.11ac Wave 2 | 5 GHz | 3.47 Gbps | 30 ft. |
| 802.11ad | 60 GHz | 7 Gbps | 30 ft. |
| 802.11af | 2.4 & 5 GHz | 26.7 – 568.9 Mbps | 3,000 ft. |
| 802.11ah (Wi-Fi HaLow) | 2.4 & 5 GHz | 347 Mbps | 3,000 ft. |
| 802.11ax (Wi-Fi 6) | 2.4 & 5 GHz | 10 Gbps | 1,000 ft. |
| 802.11ay | 60 GHz | 100 Gbps | 900-1500 ft. |
| 802.11az | 60 GHz | 0.1 – 0.5 Hz | <3 ft. - <0.3 ft. |

(Source: Pt4 p.94)

- The 802.11ac (Wi-Fi 5) row looked clipped at 70 dpi; re-read at 130 dpi and confirmed as 5 GHz / 1 Gbps / 1000 ft.
- [CONFLICT/ODD] The slide shows 802.11af frequency as "2.4 & 5 GHz" and 802.11az data rate as "0.1 – 0.5 Hz" exactly as printed. These look like slide errors (the real 802.11af uses TV white space and the az rate is not given in Hz), but this note records the slide as shown and does not correct it. [OUTSIDE-SLIDES] Do not study these two cells from the slide.

## Site survey (Source: Pt4 p.95)

- **Site Survey** — the process of developing a wireless coverage map of an organization's building/site. (Source: Pt4 p.95)
  - Used to measure signal strength and channel usage throughout the area to cover. (Source: Pt4 p.95)
  - Readings are combined and analyzed to produce a **heat map**. (Source: Pt4 p.95)
  - Typical steps: map the floor plan; test RF interference (walls, floors, etc.); test RF coverage; signal strength; analysis of signal-to-noise ratios; re-test to verify antenna placement and signal coverage. (Source: Pt4 p.95)

## Mobile management (Source: Pt4 p.96)

- **Enterprise Mobility Management (EMM)** — a class of management software designed to apply security policies to the use of mobile devices and apps in the enterprise. (Source: Pt4 p.96)
  - **Mobile Device Management (MDM)** — the process and supporting technologies for tracking, controlling, and securing the organization's mobile infrastructure. Sets device policies for authentication, feature use (camera and microphone), and connectivity; can also allow device resets and remote wipes. (Source: Pt4 p.96)
  - **Mobile Application Management (MAM)** — enterprise management function that enables control over apps and storage for mobile devices and other endpoints. Sets policies for apps that can process corporate data and prevents data transfer to personal apps; configures an enterprise-managed container or workspace. (Source: Pt4 p.96)
  - **Unified Endpoint Management (UEM)** — enterprise software for controlling device settings, apps, and corporate data storage on all types of fixed, mobile, and IoT computing devices. (Source: Pt4 p.96)

## Mobile device in the enterprise (Source: Pt4 p.97)

- **iOS in the enterprise** — apps must be submitted to and approved by Apple before they are released to users via the App Store. (Source: Pt4 p.97)
- **Android in the enterprise** (Source: Pt4 p.97):
  - Open-source basis means more scope for vendor-specific versions.
  - The app model is more relaxed, with apps available from both Google Play and third-party sites, such as Amazon's app store.
  - The SDK is available on Linux, Windows, and macOS.
  - **SEAndroid** — Android 4.3+ has integrated Security-Enhanced Linux, enabling granular permissions for apps, container isolation, and storage segmentation. Uses Mandatory Access Control (MAC) policies to run apps in sandboxes.
- **MicroSD HSM** — a small form factor hardware security module designed to store cryptographic keys securely. Key and credential management for mobile devices; allows the cryptographic material to be used with different devices, such as a laptop and smartphone. (Source: Pt4 p.97)

## Mobile device security policies and procedures (Source: Pt4 p.98-99)

| Control | Slide definition | Page |
|---|---|---|
| Screen lock | Display automatically times out after a short period of inactivity and the screen is locked with a password | Pt4 p.98 |
| Strong password | Critical for mobile devices as they can be stolen and give the user unlimited access | Pt4 p.98 |
| Full device encryption | Data encrypted on the device so that if it falls into the wrong hands it cannot be accessed in a usable form without the correct passwords | Pt4 p.98 |
| Voice encryption | Adding cryptography to the digitized voice communication | Pt4 p.98 |
| GPS tracking | Can assist in recovery of lost devices and support other apps, but can also allow the device to be tracked by attackers | Pt4 p.98 |
| Remote wipe | Ability to send a command to the device that will remotely clear the data on the phone | Pt4 p.98 |
| Geo-location | Use of network attributes to identify the physical location of a device | Pt4 p.99 |
| Geo-tagging | Automatically adding location information to files and photos; should be disabled on all mobile devices | Pt4 p.99 |
| Geo-fencing | Using a device's GPS location to restrict device operation outside of a geographic location | Pt4 p.99 |
| Application control / app whitelisting | As on a traditional workstation, a device can be locked down to only allow authorized apps to be installed | Pt4 p.99 |
| Storage segmentation | Separates an employee's personal data from business data on a mobile device | Pt4 p.99 |
| Asset tracking | Tracks and monitors the devices assigned to each employee within an organization | Pt4 p.99 |
| Device access control | Controlling access to mobile devices | Pt4 p.99 |

## Mobile device deployment models (Source: Pt4 p.100)

| Model | Slide definition |
|---|---|
| Bring Your Own Device (BYOD) | Mobile device is owned by the employee |
| Corporate-Owned Business Only (COBO) | Mobile device is owned by the company and used for company business only |
| Corporate-Owned Personally Enabled (COPE) | Mobile device is owned by the company and enabled for personal use |
| Choose Your Own Device (CYOD) | Mobile device is owned by the company; employee chooses from the list of devices |
| Virtual Desktop Infrastructure (VDI) | Provisioning VM (Citrix, Workspace, VMware Horizon client, Remote Desktop) can be accessed with any personal device |

(Source: Pt4 p.100)

- Note: COBO is on the slide but is not in the Section Topics list (Pt4 p.89), which names BYOD, COPE, CYOD only. VDI is also an extra here.

## BYOD concerns (Source: Pt5 p.1-2)

Security concerns (Source: Pt5 p.1):
- **Forensics** — in the event of an incident, your device may be seized for a forensics investigation to be conducted.
- **On-board/Off-boarding** — a process of provisioning a mobile device to an employee and then the return, removal, or performing a secure wipe of a mobile device when an employee exits, in accordance with the policy.
- **Adherence to corporate policies** — BYOD devices should not be exempt from corporate security and usage policies. Employees must feel comfortable submitting their personal devices to these policies; a balance must be maintained between corporate desires and user acceptance.

Business concerns (Source: Pt5 p.2):
- **Architecture/Infrastructure** — securely connecting a BYOD to the existing IT resources in accordance with security policies.
- **Legal** — all BYOD policies should be reviewed by legal so the interests of the business and employees are adequately and fairly represented.
- **Acceptable Use Policy (AUP)** — if a BYOD device is used for both personal and business functions, an agreeable AUP must clearly spell out what activities are authorized on the device.
- **Privacy** — because BYOD allows personal devices to be used, adequate protections must be in place to protect the user's private information.
- **On-board camera/video** — photos and videos extend the privacy concern; adequate protections must be considered for onboard cameras and microphones used in a secure/closed area.

(The slide spells "BYOD" as "BOYD" once on Pt5 p.2, a slide typo.)

## Connection methods (Source: Pt5 p.3-5)

- **Wi-Fi** — a family of wireless network protocols based on the IEEE 802.11 family of standards, commonly used for local area networking of devices and Internet access, allowing nearby digital devices to exchange data by radio waves. (Source: Pt5 p.3)
- **Z-Wave** — low-power wireless communications protocol used primarily for home automation; uses radio mesh topology frequencies in the high 800 to low 900 MHz. (Source: Pt5 p.3)
- **Zigbee** — low-power wireless communications open-source protocol used primarily for home automation; uses radio mesh topology frequencies in the 2.4 GHz band. (Source: Pt5 p.3)
- **Cellular** (Source: Pt5 p.4):
  - Cellular networks (baseband radio) enable long-distance communication over the same system that supports mobile and smartphones.
  - **Subscriber Identity Module (SIM)** — a small chip card that identifies the user and phone number of a mobile device via an International Mobile Subscriber Identity (IMSI).
  - **4G/4G LTE (Long-Term Evolution)** — increased speeds to keep up with mobile data demand; networks use frequencies below 6 GHz. **Narrowband-IoT (NB-IoT)** refers to a low-power version of the LTE or 4G cellular standard.
  - **5G (Fifth-Generation)** — a complete transformation of telecommunication networks; networks use higher frequencies, typically 30 GHz or more. Benefits: higher data rates (extremely fast download speeds); ultra-low latency (near real-time interactivity); increased network capacity (connectivity of many more devices at once).
- **Bluetooth** (Source: Pt5 p.5):
  - A short-range wireless technology standard for exchanging data between fixed and mobile devices over short distances and building a personal area network.
  - Can be used by small low-power devices such as cell phones to transmit data over short distances.
  - IEEE 802.15 — Personal Area Network (PAN); uses the 2.4 GHz band.
  - Uses the 128-bit E0 symmetric stream cipher. Cryptanalysis has shown E0 is weak; true strength is 38 bits or less.
  - Disable automatic discovery when not in use.
  - An attacker can discover the device by guessing its MAC address.

## Wireless access point, SSID, channels (Source: Pt5 p.6)

- **Wireless Access Point (WAP)** — an infrastructure-based wireless network comprises one or more WAPs. Each is connected to a wired network and forwards traffic to and from the wired switched network. Each WAP is identified by its MAC address, aka **Basic Service Set Identifier (BSSID)**. Each wireless network is identified by its name, or **Service Set Identifier (SSID)**. (Source: Pt5 p.6)
- **SSID** — broadcast is on by default and is transmitted in beacon frames that announce the wireless network's presence, capabilities, and configuration; used to connect clients to the WAP. (Source: Pt5 p.6)
- **Channels** — a wireless network can operate in either the 2.4 GHz or 5 GHz radio band; each band is divided into several channels; each WAP must be configured to use a specific channel. (Source: Pt5 p.6)

## Wireless security (Source: Pt5 p.7-10)

### Weak measures and WEP (Source: Pt5 p.7)
- **MAC address filtering (Open System Authentication)** — a weak security measure (whitelisting/blacklisting); MACs can be sniffed and spoofed; administrator overhead.
- **SSID and pre-shared key** — SSID can be discovered; the passphrase can be cracked/guessed; the key can be discovered; with a pre-shared key, everyone has the same key.
- **WEP (Wired Equivalent Privacy) (RC4)** — a 32-bit Integrity Check Value (ICV) is appended to the end of a data payload; a 24-bit Initialization Vector (IV) is combined with a key and entered into an RC4 algorithm, creating a "keystream"; this keystream is encrypted using an XOR operation and combined with the ICV to produce "encrypted" data; weakness listed: reused the key.

### WPA and WPA2 (Source: Pt5 p.8)
- **WPA (Wi-Fi Protected Access) (RC4+TKIP)** — uses RC4 encryption for confidentiality; uses **Temporal Key Integrity Protocol (TKIP)**, a 128-bit key for integrity (encryption); about every 10,000 packets or so the key is changed and NOT re-used as in WEP. Modes: WPA-PSK; WPA-Enterprise — 802.1x, can easily integrate EAP or RADIUS server authentication.
- **WPA2 (Wi-Fi Protected Access 2) (802.11i) (AES-CCMP)** — replaced TKIP with **CCMP** (Counter Mode with Cipher Block Chaining Message Authentication Code Protocol); replaced RC4 with **AES** (Advanced Encryption Standard). Modes: WPA2-Personal; WPA2-Enterprise — 802.1x; defines a Robust Security Network (RSN) — 802.11i; can easily integrate EAP or RADIUS server authentication.

### WPA3 (Source: Pt5 p.9)
- **WPA3 (Wi-Fi Protected Access 3) (AES-GCMP)**:
  - Replaced CCMP with **Galois Counter Mode Protocol (GCMP-256)**.
  - Stronger brute-force attack protection using DH.
  - **Enhanced Open** enables encryption for the open authentication method.
  - Key derivation uses 384-bit Hashed Message Authentication Mode (HMAC) with Secure Hash Algorithm (SHA).
  - Key establishment uses Elliptic Curve Diffie-Hellman (ECDH) exchange and Elliptic Curve Digital Signature Algorithm (ECDSA).
  - Frame protection based on 256-bit Broadcast/Multicast Integrity Protocol Galois Message Authentication Code (BIP-GMAC-256).
  - **WPA3-Personal**: uses 128-bit or 192-bit encryption key; **Simultaneous Authentication of Equals (SAE)** replaced Pre-shared Key (PSK) — replaced the WPA 4-way handshake authentication and association mechanism with a protocol based on Diffie-Hellman key agreement; still uses a passphrase to authenticate stations — **Password Authenticated Key Exchange (PAKE)**.
  - **WPA3-Enterprise**: uses 192-bit encryption key.

### Wireless standards comparison (Source: Pt5 p.10)

| | WEP | WPA | WPA2 | WPA3 |
|---|---|---|---|---|
| Encryption | RC4 | RC4+TKIP | AES-CCMP | AES-GCMP |
| IV size (bits) | 24 | 48 | 48 | 48 |
| Authentication | WEP-Open, WEP-Shared | WPA-PSK, WPA-Enterprise | WPA2-Personal, WPA2-Enterprise | WPA3-Personal, WPA3-Enterprise |
| Key management | none | 4-way handshake | 4-way handshake | ECDH and ECDSA |

- Note: the table lists WPA3 key management as "ECDH and ECDSA" (matching the key-establishment bullet on Pt5 p.9); SAE for WPA3-Personal appears only on Pt5 p.9. Recorded as shown.

## Remote Access Service (RAS) (Source: Pt5 p.11)

- **Remote Access Service (RAS)** — a portion of the Windows OS functionality that allows the connection between a client and a server via a dial-up telephone connection. Slower than DSL/cable; uses a series of remote access protocols for authentication and authorization.
- **Remote Access Server (RAS)** — a server designed to permit remote users access to the network and to regulate their access; typically done through secure VPNs and remote desktop software.
- Both are named "RAS" on the slide (service vs. server); the slide uses the same acronym for both.

## AAA / remote authentication (Source: Pt5 p.12-14)

### RADIUS and Diameter (Source: Pt5 p.12)
- **Remote Authentication Dial-In User Service (RADIUS)** — a connectionless protocol used for the authentication of remote and other network connections.
  - Designed for use on dial-up connections, but has evolved and is now implemented by most of the major operating system manufacturers.
  - Authentication takes place on **UDP port 1812**; authorization and accounting functions are performed as separate functions and use **UDP port 1813**.
  - Slide also lists "UNIX" and "AAA server" as bullets (no further explanation given).
  - Mnemonic box on the slide: "RADIUS — UNIX — UDP" (underlined U-letters). A circle diagram (diameter, radius, circumference) illustrates the name pun, credited as "Source: Graphic created by an Education Ecosystem instructor".
- **Diameter** is RADIUS' successor. "Diameter is double the Radius" (slide wording). Uses TCP and can manage policies for many services from a single server. Most commonly used by cellular service providers.

### TACACS+ (Source: Pt5 p.13)
- **Terminal Access Controller Access Control System+ (TACACS+)** — a Cisco proprietary remote access authentication protocol using client/server architecture.
  - Uses TCP and may use UDP over **port 49**.
  - Encrypts the entire access-request packet from the client to the server.
  - Allows two-factor authentication; includes stronger encryption for authentication traffic.
  - Uses PKI credentials — digital certificates.
  - Separates the Authentication, Authorization, and Accounting functions into three separate operations.
  - Not backward compatible with TACACS.
  - Mnemonic box: "TACACS — TCP — Cisco".
- [CONFLICT/ODD] The slide says TACACS+ "uses TCP and may use UDP over port 49". Recorded as printed; the "may use UDP" wording is the slide's.

### Authentication protocols (Source: Pt5 p.14)
- **Password Authentication Protocol (PAP)** — old, unsecure method of authentication that uses a two-way handshake with the username and password sent in clear text. Vulnerable to sniffing, replay, and session hijacking attacks.
- **Challenge Handshake Authentication Protocol (CHAP)** — used to provide RAS authentication using the point-to-point protocol (PPP). Uses a challenge-response mechanism with one-way encryption, making it unable to be used for mutual authentication.

### Other authentication services (Source: Pt5 p.15-16)
- **Remote Desktop Services** — enables remote control of Windows computers, or access to specific applications, from a client computer on the LAN or across the Internet. Operates on **port 3389**. Vulnerabilities: operates on a well-known port; uses relatively weak encryption; lacks multifactor authentication integration. (Source: Pt5 p.15)
- **Captive portals** — a technique where a user attempting to access a network is presented an authentication page in a walled-off section of the network, blocking access to the Internet (network resources) until the user is successfully authenticated. An HTTP client handles authentication by intercepting all packets from the client and then returns a login page before allowing traffic to pass through. Often used in public hotspots, hotels, airports, coffee shops, etc. (Source: Pt5 p.15)
- **CAPTCHA** (Completely Automated Public Turing test to tell Computers and Humans Apart) — used to verify human presence during an online registration process through the use of images that contain words/pictures which the user must properly identify prior to being granted access. (Source: Pt5 p.16)

## Application security / secure coding techniques (Source: Pt5 p.17-21)

### Input and output handling (Source: Pt5 p.17)
| Technique | Slide definition | Slide example |
|---|---|---|
| Input validation | Any technique used to ensure that the data entered into a field or variable in an application is handled appropriately by that application | '<' character is not accepted |
| Output encoding | When user-generated strings are passed through different context in a web application, they are re-encoded safely for the context in which they are used | '<' is converted into '&lt;' |
| Normalization | A string is stripped of illegal characters or substrings and converted to the accepted character set | '<' is removed |
| Error handling | Coding methods to anticipate and deal with exceptions thrown during execution of a process | (none on slide) |

### Web application security: secure cookies and response headers (Source: Pt5 p.18)
- **Web Application Security** — special attention must be paid to secure cookies and options for HTTP response header security.
- **Secure cookies** — an HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to the user's web browser. Key parameters for the SetCookie header:
  - Avoid using persistent cookies (susceptible to session hijacking) for session authentication.
  - Set the **Secure** attribute to prevent a cookie being sent over unencrypted HTTP.
  - Set the **HttpOnly** attribute to make the cookie inaccessible to document object model/client-side scripting.
  - Use the **SameSite** attribute to control from where a cookie may be sent, which helps mitigate request forgery attacks.
- **Response headers** — hold additional information about the response, like its age, location or server. Important security-relevant options the server can set:
  - **HTTP Strict Transport Security (HSTS)** — forces the browser to connect using HTTPS only.
  - **Content Security Policy (CSP)** — mitigates clickjacking, script injection, and other client-side attacks.
  - **Cache-Control** — sets whether the browser can cache responses.
- (The Secure-attribute bullet looked clipped at 70 dpi; confirmed at 130 dpi. The slide's own wording is "Set the Secure attributes".)

### Data exposure, memory management, secure code usage (Source: Pt5 p.19)
- **Data exposure** — a fault that allows privileged information (such as a token, password, or personal data) to be read without being subject to the appropriate access controls.
- **Memory management** — procedures should be checked for processing untrusted input, such as strings, to ensure it cannot overwrite areas of memory, thus preventing attackers from executing their own code.
- **Secure code usage** — to make development faster, developers often use someone else's existing code in these ways:
  - **Code reuse** — using a block of code from elsewhere in the same application or from another application to perform a different function (or the same function in a different context).
  - **Third-party library** — using a binary package (such as a dynamic link library) that implements standard functionality, such as establishing a network connection or performing cryptography.
  - **Software Development Kit (SDK)** — using sample code or libraries of pre-built functions from the programming environment used to create the software or interact with a third-party API.
  - **Stored procedures** — a part of a database that executes a custom query using a pre-built function to perform a database query.
  - **Dead code** — code in an application that is redundant because it will never be called within the logic of the program flow.
  - **Obfuscation** — a technique that essentially "hides" or "camouflages" code or other information so that it is harder to read by unauthorized users.

### SAST and DAST (Source: Pt5 p.20)
| | SAST — Static Application Security Testing | DAST — Dynamic Application Security Testing |
|---|---|---|
| Purpose | Analyze application **source code**, byte code and binaries for coding and design conditions indicative of security vulnerabilities | Detect conditions indicative of security vulnerabilities within an application in its **running state** |
| State | Non-running state; "inside out" | While code is running/executed |
| Method | Source and binary code reviews; a **white-box** method that examines code to find application flaws and weaknesses | A **black-box** method that examines a running application to find vulnerabilities an attacker could exploit |

### Code signing (Source: Pt5 p.21)
- **Code signing** — the method of using a digital signature to verify the integrity and authenticity of programming code: ensures software has not been tampered with since signing; confirms the software publisher's identity.
- **Code signing digital certificate** — certificate used to verify that the code has not been altered or corrupted; also used to verify the publisher or developer of software and scripts.
- **Software Publisher Digital Certificates (Class 3)** — certificates provided by software developers to verify that their programs have not been tampered with.
- **Online Business Transaction Certificates (Class 4)** — special certificates reserved for securing business transactions between companies.
- **Private Organizations/Government Security Certificates (Class 5)** — special certificates used by private/government organizations to secure their communications paths.
- (Classes 3, 4 and 5 are as printed; no Class 1/2 on this slide.)

## Sandboxing and monitoring (Source: Pt5 p.22)

- **Sandboxing** — running apps in restricted memory areas to protect from VM escape should an application crash.
  - Preventing VM escaping is dependent on the virtualization vendor identifying security vulnerabilities in the hypervisor and on these being patched.
  - A security mechanism used in software development and operation to isolate running processes from each other or prevent them from accessing the system they are running on.
- **Monitoring** (per slide title "Sandboxing and Monitoring") — writing code with enhanced monitoring capabilities improves the granularity and effectiveness of logging and alerting systems, which are crucial system monitoring tools. (Source: Pt5 p.22)

## Validation log
- Extraction pass: all 35 pages read at 70 dpi in order and written to this note.
- Validation pass (separate, 2026-10-16): all 35 pages (Pt4 p.88-100, Pt5 p.1-22) plus the boundary slide Pt5 p.23 re-opened at 100 dpi (p.94 and Pt5 p.18 also at 130 dpi) and compared with the note item by item.
- Result: no omitted items, wrong numbers (ports 1812/1813/49/3389, key sizes, class numbers, 802.11 table) or wrong page citations found. Fixes made: removed stale "clipped render" remarks; clarified the Pt5 p.10 table note; front-matter boundary text.
- Wording policy: bold terms and numbers are verbatim. Slide typos were silently normalised in a few definitions ("cannot be access" → "cannot be accessed" on Pt4 p.98; "can be access" → "can be accessed" on Pt4 p.100; "an agreeable AUP must be clearly spell out" on Pt5 p.2; "existing codes" on Pt5 p.19). Slide errors noted in place: "BOYD" (Pt5 p.2), the 802.11af/az cells (Pt4 p.94).
- Not independently checked: Pt4 p.94 row-by-row beyond the two reads above.

## Official-objective gap check (vs. SY0-701 4.1 bullets, as listed on the slides' own Section Topics slide, Pt4 p.89)
| Official bullet | Status in slides | Where |
|---|---|---|
| Secure baselines: establish, deploy, maintain | Weak — definition only; the three steps are not explained | Pt4 p.90 |
| Hardening targets: mobile devices | Covered | Pt4 p.98-99 (policies); Pt4 p.96-97 |
| Hardening targets: workstations | **Not in this range.** Hardening is also discussed around g232-245 (2.5 section, OCR only, not read); check it when 2.5 is extracted | — |
| Hardening targets: switches, routers | Covered | Pt4 p.92 |
| Hardening targets: servers | Covered | Pt4 p.93 |
| Hardening targets: cloud infrastructure | **Not in slides in this range** | — |
| Hardening targets: ICS/SCADA, embedded systems, RTOS, IoT | **Not in this range.** OCR search (unverified, not read) finds these terms on g292-296 (3.1 section, Pt3 p.92-96), so they are probably taught as architecture topics, not as hardening | — |
| Wireless: installation considerations — site surveys, heat maps | Covered (no placement/channel-planning detail) | Pt4 p.95 |
| Mobile solutions: MDM | Covered | Pt4 p.96 |
| Deployment models: BYOD, COPE, CYOD | Covered (also COBO, VDI) | Pt4 p.100, Pt5 p.1-2 |
| Connection methods: cellular, Wi-Fi, Bluetooth | Covered (also Z-Wave, Zigbee) | Pt5 p.3-5 |
| Wireless security settings: WPA3 | Covered | Pt5 p.9-10 |
| AAA / RADIUS | Covered (also Diameter, TACACS+) | Pt5 p.12-13 |
| Cryptographic protocols (wireless) | Covered only as WEP/WPA/WPA2/WPA3 ciphers | Pt5 p.7-10 |
| Authentication protocols | Covered: PAP, CHAP (EAP only mentioned, not explained) | Pt5 p.8, 14 |
| Application security: input validation | Covered | Pt5 p.17 |
| Secure cookies | Covered | Pt5 p.18 |
| Static code analysis | Covered (SAST/DAST) | Pt5 p.20 |
| Code signing | Covered | Pt5 p.21 |
| Sandboxing | Covered | Pt5 p.22 |
| Monitoring | Weak — one bullet on monitoring-oriented code | Pt5 p.22 |

Slide content with no matching official bullet (kept, flagged): 802.11 standards table, RAS, captive portals, CAPTCHA, remote desktop services, memory management / secure code usage list, MicroSD HSM, SEAndroid.

**Gaps against the official objective:** workstation, cloud infrastructure, ICS/SCADA, embedded, RTOS and IoT hardening; baseline establish/deploy/maintain detail; EAP detail. These need outside study or another part of the deck; they are not filled in here.

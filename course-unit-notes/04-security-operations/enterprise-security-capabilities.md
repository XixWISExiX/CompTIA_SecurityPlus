---
Unit: Modify Enterprise Capabilities to Enhance Security
Domain: 4.0 Security Operations (sub-objective 4.5 — Given a scenario, modify enterprise capabilities to enhance security)
Source: Pt5 p.57-84 (global 457-484; course slides 4-72 to 4-99). Boundaries: Pt5 p.57 = 4.5 roadmap (4-72, confirmed in the 4.4 pass); Pt5 p.85 = 4.6 roadmap (4-100)
Extraction_Status: Fully Extracted (all 28 pages read via vision; boundary confirmed: Pt5 p.85 = 4.6 roadmap)
Pages_Done: Pt5 p.57-84
Pages_Remaining: none
Next_Page: none
Validation_Status: Validated (2026-10-16) — all 28 pages re-opened at 130 dpi (Pt5 p.61 at 170 dpi) and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt5 p.57-58)

- Pt5 p.57 (4-72) is the Domain 4 roadmap slide with "Modify enterprise capabilities to enhance security" highlighted. (Source: Pt5 p.57)
- Pt5 p.58 (4-73) is the 4.5 Section Topics slide (Source: Pt5 p.58):
  - **Firewall:** Rules; Access lists; Ports/protocols; Screened subnets
  - **IDS/IPS:** Trends; Signatures
  - **Web filter:** Agent-based; Centralized proxy; Universal Resource Locator (URL) scanning; Content categorization; Block rules; Reputation
  - **Operating system security:** Group Policy; SELinux [list cut off at the footer; completed on Pt5 p.76 — see below]
  - **Implementation of secure protocols:** Protocol selection; Port selection; Transport method
  - **DNS filtering**
  - **Email security:** Domain-based Message Authentication Reporting and Conformance (DMARC); DomainKeys Identified Mail (DKIM); Sender Policy Framework (SPF); Gateway
  - **File integrity monitoring**
  - **DLP**
  - **Network access control (NAC)**
  - **Endpoint detection and response (EDR)/extended detection and response (XDR)**
  - **User behavior analytics**
- Layout note: the left column of Pt5 p.58 runs down to the footer; "SELinux" is the last visible item. Pt5 p.76 covers Group Policy and SELinux, so nothing appears to be missing.

## Rule-based management; explicit allow; implicit deny (Source: Pt5 p.59)

- **Rule-based management** — a common control methodology used by firewalls, proxies, switches, routers, anti-malware, and IDS/IPS to achieve a desired operational state. (Source: Pt5 p.59)
  - Firewall rules (ACL) follow a **top-down** format with the most important rules at the top; the **implicit deny** should always be the last rule.
  - As each packet reaches the device, the rules are applied and interpreted to make a determination on whether particular traffic should pass through or be blocked.
- **Explicit allow** — a rule that specifically allows a particular type of traffic to be granted access to the network.
- **Implicit deny** — a security method that denies all traffic to a network/system resource unless the user is specifically granted access.
- Example rule table on the slide (graphic credited to an Education Ecosystem instructor):

| Rule | Direction | Src address | Dest address | Protocol | Dest port | Action |
|---|---|---|---|---|---|---|
| A | In | External | Internal | TCP | 25 | Permit |
| B | Out | Internal | External | TCP | >1023 | Permit |
| C | Out | Internal | External | TCP | 25 | Permit |
| D | In | External | Internal | TCP | >1023 | Permit |
| E | Either | Any | Any | Any | Any | Deny |

(Source: Pt5 p.59. The slide does not walk through the table; rule E is the final deny-all, matching the "implicit deny last" bullet.)

## Ports (Source: Pt5 p.60)

- **Port** — a logical communication endpoint for a computer or network device. A 16-bit identifier is used for the port number (2^16 = 65536 port numbers).
- **Inbound port** — used when another computer wants to connect to a service or application running on your computer.
- **Outbound port** — used when your computer wants to connect with a service or application running on another computer.
- **Reserved (well-known) ports: 0-1023** — used by system processes; require administrator privileges to use.
- **Registered ports: 1024-49151** — assigned for specific services; do not require administrator privileges to use.
- **Private/dynamic ports: 49152-65535** — private: used for custom purposes; dynamic/ephemeral: short-lived; open for use without restriction.
- Diagram: a client on port 4855 (outbound) → Internet → a server on port 80 (inbound).

(Source: Pt5 p.60; diagram credited to an Education Ecosystem instructor. The slide prints the registered range as 1024-49151 and private as 49152-65535.)

## List of common ports (Source: Pt5 p.61)

| Port # | Protocol | TCP/UDP | Secure version | Description (slide wording) |
|---|---|---|---|---|
| 20/21 | FTP | TCP | FTPS 989/990 | Transfers files between hosts; 20 data / 21 control |
| 22 | SSH | TCP/UDP | — | Secure Shell: remotely admins devices and systems; SCP and SFTP |
| 23 | TELNET | TCP/UDP | — | Remotely administer network devices |
| 25 | SMTP | TCP | SMTP SSL/TLS 465/587 | Simple Mail Transfer Protocol; sends email |
| 49 | TACACS+ | TCP | — | Remote authentication; default is TCP, can use UDP |
| 53 | DNS | TCP/UDP | DNSSEC | Resolves hostnames to IP addresses; vice versa |
| 67/68 | DHCP | UDP | — | Dynamic Host Configuration Protocol; 67 server / 68 client |
| 69 | TFTP | UDP | — | Basic version of FTP |
| 80 | HTTP | TCP/UDP | HTTPS SSL/TLS 443 | Transmit web page data |
| 88 | Kerberos | TCP/UDP | — | Network authentication; ticket based |
| 110 | POP3 | TCP | POP3 w/ SSL/TLS 995 | Receives email |
| 123 | NTP | UDP | — | Network Time Protocol |
| 135 | RPC | TCP/UDP | — | Remote Procedure Call (RPC) |
| 137-139 | NetBIOS | TCP/UDP | — | Legacy file and print sharing |
| 143 | IMAP | TCP | IMAP 4 w/ SSL/TLS 993 | Receives email and has advantages over POP3 |
| 161/162 | SNMP | TCP/UDP | SNMPv3 | Network management; 161 agent receives requests, 162 manager receives notification |
| 389 | LDAP | TCP/UDP | LDAP over SSL/TLS 636 | Directories of users and other objects |
| 445 | SMB | TCP | — | Newer file and print sharing |
| 514 | Syslog | UDP | Syslog-TLS TCP 6514 | Computer message logging |
| 1812/1813 | RADIUS | UDP | — | AAA — Authentication (1812); Auth/Acct (1813) |
| 3389 | RDP | TCP/UDP | — | Remotely view and controls other Windows systems |

(Source: Pt5 p.61; read at 170 dpi. The table is printed as two side-by-side column groups; they are merged here in port order. Values are exactly as the slide shows. Note: the 161/162 row lists "161 agent receives requests, 162 manager receives notification", consistent with Pt5 p.54 (4.4).)

## Protocols (Source: Pt5 p.62)

- **HTTP** — Port 80/TCP — an application protocol that forms the basis of the Web.
- **HTTPS** — Port 443/TCP — encrypted channel over which HTTP traffic is transmitted; most widely used method to secure HTTP traffic.
- **Telnet** — Port 23/TCP — an older plaintext TCP/IP protocol for establishing a command-line console to a remote machine.
- **SSH** — Port 22/TCP — an encrypted remote terminal connection program used for remote connections to a server.
- **SSL (Secure Socket Layer)** — a transport layer protocol that uses public key encryption methods to exchange a symmetric key for use in confidentiality and integrity protection, as well as authentication.
- **TLS (Transport Layer Security)** — a standard for the employment of encryption technology that uses updated public key encryption mechanisms; replaced SSL.
- **NetBIOS** — Ports 137, 138, 139 / TCP&UDP — used in older Windows systems for file and print sharing over a LAN.
- **SMB (Server Message Block)** — Port 445 TCP — also used for file and print sharing over a LAN.

(Source: Pt5 p.62. The slide's port/transport text differs slightly from the table on Pt5 p.61 for SSH (22/TCP here vs TCP/UDP) and Telnet (23/TCP here vs TCP/UDP) — recorded as printed; [CONFLICT/ODD].)

## DNS (Source: Pt5 p.63)

- **Domain Name System (DNS)** — maps a domain name (hostname / website) to an IP address. Somewhat like a directory assistance or a phone book for IP addresses; converts IP addresses into user-friendly names [slide wording; the two statements are as printed].
  - Client question = single UDP packet; server response = single UDP packet.
  - TCP is used when the response data size exceeds 512 bytes or for a zone transfer.
  - Runs on port 53.
- Diagram: user → local name server → authoritative name server; DNS request "Host: www.site.com?" and DNS reply "Answer: 207.25.71.29" (graphic credited to an Education Ecosystem instructor).

(Source: Pt5 p.63)

## Securing DNS (Source: Pt5 p.64)

- **Enable DNSSEC for authentication** — Domain Name Server Security Extensions; adds authentication and integrity to DNS responses; uses public key encryption; no confidentiality; like a digital signature.
- **Split DNS** — internal DNS for locating domain resources (internal network hosts); external DNS for locating Internet resources (public network hosts).
- **Block zone transfers (TCP 53).**
- **Limit DNS interface access.**
- **Use digitally signed secure dynamic updates** — Digital Signature Algorithm (DSA).
- Diagram (credited to an Education Ecosystem instructor): user → internal DNS → external DNS in the DMZ → authoritative name server.

(Source: Pt5 p.64)

## ARP and RARP (Source: Pt5 p.65)

- **Address Resolution Protocol (ARP)** — determines "who has" an IP address. Each machine maintains an ARP table with physical addresses (MAC addresses) and IP addresses. If an entry for an IP address is not found in the machine's ARP table, a broadcast "ARP Request" is sent to the network.
- **Reverse Address Resolution Protocol (RARP)** — finds the IP address if the physical address is already known.
- Diagram: ARP Request "Who has 147.81.12.2?"; ARP Reply "Tell 147.81.12.10 that 147.81.12.2 is at 00:50:04:8c:32:ba".

(Source: Pt5 p.65)

## SNMP (Source: Pt5 p.66)

- **SNMP — Port 161-162/UDP** — used to manage and monitor computers, network devices and other devices on the IP-based network. Each SNMP-managed device has an agent or service that listens for and executes commands. Port 161/UDP is used by management agents; port 162/UDP is used by the manager to receive notifications (trap).
- **SNMP versions:**
  - **SNMPv1** — the original version; no security mechanisms built in; the SNMP password was sent in clear text and was susceptible to interception.
  - **SNMPv2** — replaced SNMPv1; added encryption of the password; however, was not backwards compatible.
  - **SNMPv3** — the most recent version, replaced SNMPv2; added encryption of the packet along with backwards compatibility.
- Callouts: default community strings: 'public' for read access and 'private' for write/management access. SNMP community strings are used only by devices which support SNMPv1 and SNMPv2c; SNMPv3 uses username/password authentication, along with an encryption key.

(Source: Pt5 p.66)

## File transfer protocols (Source: Pt5 p.67)

| Protocol | Port/transport | Slide definition |
|---|---|---|
| FTP | 20&21/TCP | Unsecure, plaintext method of transferring files between machines |
| TFTP | 69/UDP | Simple FTP with no security or authentication mechanisms; used for the automated transfer of configuration files between devices; not typically used over the Internet |
| SFTP | 22/TCP | FTP that uses a single TCP port over an SSH channel to encrypt and compress all data and commands |
| FTPS | 989&990/TCP | Uses SSL or TLS to encrypt commands [slide text "commands" with a stray bold "s"] |
| SCP | 22/TCP | SSH-enabled mechanism to securely transfer files between systems |

(Source: Pt5 p.67)

## Directory access protocols (Source: Pt5 p.68)

- **Lightweight Directory Access Protocol (LDAP)** — a plaintext application layer directory access protocol used to access, query, and modify directory services data; vulnerable to interception. LDAP is the primary protocol used for MS Active Directory on Windows Server domain controllers. Operates on port 389. A subset of the X.500 protocol.
- **MS Active Directory** — Microsoft's proprietary directory service that enables administrators to manage permissions and access to network resources. Operates on port 389; a subset of the X.500 protocol [as printed].
- **Secure LDAP / LDAPS — Port 636** — transmission of LDAP data over SSL/TLS. Remediates the issue of clear text data being transmitted and intercepted; integrity and confidentiality are maintained by encryption of the data being transmitted.

(Source: Pt5 p.68)

## DMZ (screened subnet) (Source: Pt5 p.69)

- **De-Militarized Zone (DMZ)** — acts as a buffer zone between unprotected areas of the network (the Internet) and protected areas (an organization's data stores), allowing for the monitoring and regulation of traffic between these two zones.
  - Considered a semi-trusted zone.
  - Forces outside users to make at least one hop before accessing the trusted network.
  - Hosts: web servers, remote-access servers, external e-mail servers, honeypots, etc.
  - Devices located within a DMZ should have a **hardened operating system**.
- Diagrams (credited to an Education Ecosystem instructor): (left) a single firewall with the Internet, the DMZ (web, email, proxy servers), and the internal network on separate legs; (right) two firewalls — outer firewall between the Internet (untrusted zone) and the DMZ (semi-trusted zone), inner firewall between the DMZ and the trusted zone with servers.
- The slide title calls the DMZ a "Screened Subnet", matching the Section Topics term (Pt5 p.58).

(Source: Pt5 p.69)

## IDS and IPS detection methods (Source: Pt5 p.70)

- **Behavior-based** — relies on a collected set of "normal behavior"; if the behavior does not fit into the "normal" activity it is considered suspicious/malicious. Can potentially detect zero-day attacks, but can have a high false-positive rate.
- **Anomaly-based** — like behavior-based, but must be taught what normal is. Anomalies can be defined and implemented by an artificial intelligence-based engine.
  - **Heuristic** — uses artificial intelligence and fuzzy logic algorithms to detect intrusions and malicious traffic.
  - Examples — Protocol anomaly-based: unencrypted port 443 traffic; encrypted port 80 traffic. Traffic anomaly-based: 50% increase in web traffic towards subnet X; vulnerability scan identified outside normal time frame.

(Source: Pt5 p.70)

## IDS and IPS detection methods, continued (Source: Pt5 p.71)

- **Signature-based detection (pattern-matching)** — a network monitoring system that uses a predefined set of rules provided by a software vendor or security personnel to identify events that are unacceptable. Relies on a set of patterns, trends, signatures, or strings to determine what is malicious; fast and precise, but must have accurate signatures.
- **Trend analysis** — the process of detecting patterns within a dataset over time, and using those patterns to make predictions about future events or to better understand past events.
- **Predictive analysis** — using AI threat intelligence or threat forecasting to identify the signs of a past attack or the presence of live attack tools on a network quickly is valuable.
  - **Artificial Intelligence (AI)** — the science of creating machine systems that can simulate or demonstrate a similar general intelligence capability to humans.
  - **Machine Learning (ML)** — uses algorithms to parse input data and then develop strategies for using that data.

(Source: Pt5 p.71)

## IDS and IPS tools (Source: Pt5 p.72)

- **Snort** — an open-source rule-driven language, which combines the benefits of signature, protocol, and anomaly-based inspection methods, providing robust detection capabilities. Community contributing rules and configurations; modes — sniffer, packet logger, and NIDS; one of the most well-known IDS tools.
- **Suricata** — a high-performance open-source IDS/IPS/NSM engine. Takes full advantage of modern hardware; delivers higher performance and scalability than Snort; can function as an IDS or an IPS; compatible with Snort rulesets, making it a highly flexible option for network security.
- **Security Onion** — a Linux distribution designed for intrusion detection, network security monitoring, and log management. Includes both Snort and Suricata, along with a host of other tools, to provide a complete platform for network security; provides a holistic view of network activity, enabling administrators to correlate data from different tools and obtain a comprehensive understanding of the network's security posture.

(Source: Pt5 p.72)

## Web filtering (Source: Pt5 p.73)

| Term | Slide definition |
|---|---|
| Agent-based | A software agent on desktop computers, laptops, and mobile devices |
| Centralized proxy | An intermediary between end users and the Internet |
| URL scanning | Can block access to specific URLs known to host malicious or inappropriate content, or violates the company's Internet usage policy |
| Content categorization | Classifies websites into various categories (e.g. social networking, gambling, adult content, webmail) |
| Block rules | Based on various factors such as the website's URL, domain, IP address, content category, or even specific keywords within the web content |
| Reputation-based filtering | Leverages continually updated databases that score websites based on their observed behavior and history (e.g. hosting malware, engaging in phishing attacks, or distributing spam) |

(Source: Pt5 p.73)

## SPAM filters (Source: Pt5 p.74)

- **SPAM filter** — used to filter unsolicited or undesired bulk electronic messages.
  - **Content or keyword filtering** — filters e-mail messages for undesirable content based on keywords.
  - **Statistical content filtering** — messages are marked as SPAM by users and the system uses those markings to learn and intercept SPAM.
  - **Rule-based filtering** — looks for matches of certain keywords; used by many popular email clients.
  - **Delay-based filtering** — inserts a deliberate pause between the connection and the banner; any system that sends data during the pause is considered malicious.
  - **Egress filtering** — checking and filtering messages leaving an organization to validate and filter e-mail for SPAM.
  - **Hybrid filtering** — combination of several filtering techniques to combat SPAM.

(Source: Pt5 p.74)

## SPAM defenses (Source: Pt5 p.75)

- **SPAM defenses** — most filtering of incoming/outgoing messages is done at the SMTP level in order to have a centralized solution.
  - **CAN-SPAM Act of 2003** — established penalties for spammers if they violate the law and gives consumers the right to request e-mailers to stop spamming them.
  - **Blacklisting** — notes which domains/systems are known to send SPAM and rejects messages from those addresses.
  - **Trusted servers** — opposite of blacklisting; these are trusted domains/systems.
  - **PTR and reverse DNS checks** — conducts a reverse DNS check to determine the origin address.
  - **Callback verification** — attempts to validate the address of the sending system to detect forged "from" addresses, a common SPAM technique.

(Source: Pt5 p.75)

## Operating system security (Source: Pt5 p.76)

- **Group Policy** — policies that are applied to the specific group to which the user has been assigned. GPOs are able to update settings related to security (user credentials) for the domain.
- **Local policy** — policies that are local to the computer and pertain to the users and service accounts logged into that computer. Policies can include Audit, User Rights Assignments, Security Options, Password and Account Lockout Policies.
- **Hardened operating system** — machines whose functionality is locked down (bastion host) to preserve security but ensures they will work properly in a less secure environment.
  - **Trusted OS (SELinux)** — an operating system with enhanced security features. Adds Mandatory Access Control (MAC) to Linux; Linux traditionally uses Discretionary Access Control (DAC).

(Source: Pt5 p.76. This slide completes the Section Topics item "Operating system security: Group Policy, SELinux" cut off at the footer on Pt5 p.58.)

## Implementing secure protocols (Source: Pt5 p.77)

| Use | Unsecure | Secure |
|---|---|---|
| Terminal communication | Telnet, rlogin, rsh, and rexec | SSH (Secure Shell) |
| Browsers | HTTP | HTTPS (TLS/SSL — Transport Layer Security / Secure Sockets Layer) |
| File transfers | FTP, TFTP | SFTP (Secure (SSH) File Transfer Protocol), FTPS (File Transfer Protocol Secure) |
| Network management | SNMPv1 and SNMPv2 | SNMPv3 |

(Source: Pt5 p.77)

## DNS filtering (Source: Pt5 p.78)

- **DNS filtering (DNS block)** — the process of using the Domain Name System (DNS) to block Internet users from accessing unapproved websites on a server. Ensures company data remains secure; allows companies to have control over what their employees can access on company-managed networks.
- The slide photo (a person using a laptop on a Google page) is decorative.

(Source: Pt5 p.78)

## Email security (Source: Pt5 p.79)

- **Secure Email Gateway (SEG)** — an email security solution that sits inline on the email path from the public Internet to the corporate email server; the control point for all incoming and outgoing email traffic.
- **Sender Policy Framework (SPF)** — an email authentication method which ensures the sending mail server is authorized to originate mail from the email sender's domain. Helps detect and prevent sender address forgery; a DNS TXT record identifying hosts authorized to send mail for the domain.
- **DomainKeys Identified Message (DKIM)** — a cryptographic authentication mechanism for mail utilizing a public key published as a DNS TXT record. [The Section Topics slide (Pt5 p.58) and the DMARC bullet on this slide call it "DomainKeys Identified Mail"; this bullet says "Message". Recorded as printed.]
- **Domain-based Message Authentication Reporting and Conformance (DMARC)** — a framework for ensuring proper application of SPF and DKIM, utilizing a policy published as a DNS TXT record. Uses the results of SPF and DKIM checks to define rules for handling messages (moving messages to quarantine or spam; rejecting the message; tagging the message). Provides reporting capabilities, giving the owner of a domain visibility into which systems are sending emails on their behalf, including unauthorized activity.

(Source: Pt5 p.79)

## File integrity monitoring (Source: Pt5 p.80)

- **FIM (File Integrity Monitoring)** — a type of software that reviews system files to ensure that they have not been tampered with. One of the core features of a HIDS; used to detect changes on endpoints (important files or the operating system configuration).
  - Windows: the **Windows File Protection (WFP)** service runs automatically to prevent programs from replacing critical Windows system files; the **System File Checker (SFC)** tool can be used manually to scan for, verify, and restore corrupted Windows system files.
  - Multi-platform: Tripwire (tripwire.com); OSSEC (ossec.net).

(Source: Pt5 p.80)

## Data loss prevention (Source: Pt5 p.81)

- **Data loss prevention** — systems designed to prevent the loss/leak of confidential information outside of the network.
  - **Endpoint DLP** — typically a software program that is installed and run on an individual computer to monitor and control data in use and transit.
  - **Network DLP** — software or hardware-based systems installed on the perimeter of the network to inspect data in motion.
  - **Storage DLP** — installed in data centers or server rooms to inspect data at rest.
  - **Cloud-based DLP** — offered by cloud providers to protect cloud-based systems against data breaches/misuse.

(Source: Pt5 p.81. The magnifying-glass hex-code picture is decorative.)

## Data Execution Prevention (DEP) (Source: Pt5 p.82)

- **Data Execution Prevention (DEP)** — attempts to ensure memory locations not pre-defined to contain executable content will not have the ability to execute code. Users must approve the execution of an application before it can proceed. Can prevent simple buffer overflow attacks: even if an attacker can inject code into a variable, the injected code will not run.
- Two screenshots (credited to an Education Ecosystem instructor): a Carbon Black Protect security notification for an unapproved executable (application whitelisting), and the Windows "Performance Options > Data Execution Prevention" tab ("Turn on DEP for essential Windows programs and services only" selected; "Turn on DEP for all programs and services except those I select").
- [NOTE] DEP is on the slides but is not one of the Section Topics items (Pt5 p.58). It is kept as extra content.

(Source: Pt5 p.82)

## Network access control (Source: Pt5 p.83)

- **Network Access Control (NAC)** — a set of standards defined by the network for clients attempting to connect; typically requires that the clients are virus free and adhere to specific policies prior to being granted access.
  - The connecting client will have one of two types of agents running that will conduct a **host health check** to ensure the device is meeting the established standards: client security policy settings; software updates and patches; virus scanner.
  - **Permanent agent** — most common; agent installed on the device and runs each time the client attempts to connect to the network; remains on the device (example: Cisco AnyConnect).
  - **Dissolvable agent (agentless)** — agent is installed for that session only and is removed after session ends (examples: browser-based sessions; guest access).
  - **Network Access Protection (NAP) — Microsoft** — uses enforcement agents to assess OS patch levels, AV protection and system policies of clients.
  - **Network Admission Control (NAC) — Cisco** — an extensible system centered around a network appliance that enforces policies across a wide range of equipment.

(Source: Pt5 p.83. The slide uses "NAC" both for Network Access Control (generic) and Cisco's Network Admission Control; recorded as printed.)

## EDR, XDR, and UBA (Source: Pt5 p.84)

- **Endpoint Detection and Response (EDR)** — a software agent that collects system data and logs for analysis by a monitoring system to provide early detection of threats.
- **Extended Detection and Response (XDR)** — expands on EDR by providing broader visibility and response capabilities by extending protection beyond endpoints by incorporating data from the network, cloud platforms, email gateway, firewall, and other essential infrastructure components. Provides a comprehensive view of information technology resources to more effectively identify threats and enable faster responses; commonly includes User Behavior Analytics (UBA).
- **User and Entity Behavior Analytics (UEBA)** — a cybersecurity approach based on monitoring and analyzing the behavior of users within an organization to detect anomalies indicative of potential threats, such as insider threats, compromised accounts, or fraud. A system that can provide automated identification of suspicious activity by user accounts and computer hosts. Also known as User Behavior Analytics (UBA).

(Source: Pt5 p.84)

## Boundary (Source: Pt5 p.85)
- Pt5 p.85 (4-100) is the Domain 4 roadmap slide with "Identity and access management" highlighted, so 4.5 ends at Pt5 p.84. (Source: Pt5 p.85)

## Validation log
- Extraction: 28 pages read at 100 dpi (Pt5 p.61 re-read at 170 dpi because of the dense port table); written in four saves (after p.63, p.70, p.77, p.84).
- Validation (separate pass, 2026-10-16): Pt5 p.58-84 re-opened at 130 dpi and compared item by item (port numbers, protocol versions, table cells, acronyms, definitions, page citations); p.57 and p.85 are boundary slides seen at 100 dpi. No omissions, wrong values or wrong citations found; no content changes needed.
- Slide inconsistencies kept as printed: DKIM = "Identified Mail" (Pt5 p.58, p.79 DMARC bullet) vs "Identified Message" (p.79 DKIM bullet); SSH and Telnet are "TCP/UDP" in the port table (p.61) but "/TCP" on p.62; NAC means Network Access Control and Cisco's Network Admission Control (p.83); the slide text "establish standards" (p.83) and the stray bold "s" in "commands" (p.67).
- Not transcribed: decorative pictures (Pt5 p.67, p.68, p.78, p.81) and the content of the two screenshots on Pt5 p.82 beyond a description.

## Official-objective gap check (4.5 bullets as listed on the slides' Section Topics slide, Pt5 p.58)
| Official bullet | Status | Where |
|---|---|---|
| Firewall: rules | Covered (top-down, explicit allow, implicit deny, example rule table) | Pt5 p.59 |
| Firewall: access lists | Covered (as "firewall rules (ACL)") | Pt5 p.59 |
| Firewall: ports/protocols | Covered | Pt5 p.60-62 |
| Firewall: screened subnets | Covered | Pt5 p.69 |
| IDS/IPS: trends | Covered | Pt5 p.71 |
| IDS/IPS: signatures | Covered | Pt5 p.71 |
| Web filter: agent-based, centralized proxy, URL scanning, content categorization, block rules, reputation | Covered | Pt5 p.73 |
| OS security: Group Policy | Covered | Pt5 p.76 |
| OS security: SELinux | Covered | Pt5 p.76 |
| Secure protocols: protocol selection | Covered (unsecure vs secure pairs, protocol descriptions) | Pt5 p.62, p.66-68, p.77 |
| Secure protocols: port selection | Covered (port table, port ranges) | Pt5 p.60-61 |
| Secure protocols: transport method | **Weak.** TCP/UDP appears in the port table and DNS slide, but no slide explains "transport method" as a selection criterion (e.g. encrypted transport such as TLS) beyond SSL/TLS definitions | Pt5 p.61-63 |
| DNS filtering | Covered (one definition; DNS security on p.63-64 is extra) | Pt5 p.78 |
| Email security: DMARC, DKIM, SPF, gateway | Covered | Pt5 p.79 |
| File integrity monitoring | Covered | Pt5 p.80 |
| DLP | Covered | Pt5 p.81 |
| NAC | Covered | Pt5 p.83 |
| EDR/XDR | Covered | Pt5 p.84 |
| User behavior analytics | Covered (UBA/UEBA) | Pt5 p.84 |

**Gaps against the official objective:** one weak bullet — secure-protocol "transport method". Everything else is present and validated. The coverage rating treats a bullet that the slides only touch indirectly as an open gap, so this objective is Weakly Covered rather than Well Covered. Extra slide content (kept): ARP/RARP, SNMP versions, file-transfer and directory protocols, DNS/DNSSEC, spam filters and defenses, IDS/IPS tools, DEP.

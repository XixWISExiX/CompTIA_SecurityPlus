---
Unit: Mitigation Techniques Used to Secure the Enterprise
Domain: 2.0 Threats, Vulnerabilities, and Mitigations (sub-objective 2.5 — Explain the purpose of mitigation techniques used to secure the enterprise)
Source: Pt3 p.31-45 (global 231-245; course slides 2-108 to 2-122). Boundaries: Pt3 p.31 = 2.5 roadmap (2-108, "Mitigation techniques used to secure the enterprise" highlighted); Pt3 p.46 (2-123) = Domain 2 "Domain Topics" recap and Pt3 p.47 (2-124) = Education Ecosystem logo — neither has unit content, so 2.5 ends at Pt3 p.45
Extraction_Status: Fully Extracted (all 15 pages read via vision at 100 dpi; Pt3 p.46-47 also viewed, no objective content)
Pages_Done: Pt3 p.31-45
Pages_Remaining: none
Validation_Status: Validated (2026-10-16) — all 17 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt3 p.31-32)

- Pt3 p.31 (2-108) is the Domain 2 roadmap slide with "Mitigation techniques used to secure the enterprise" highlighted. (Source: Pt3 p.31)
- Pt3 p.32 (2-109) is the 2.5 Section Topics slide, "2.5 Explain the purpose of mitigation techniques used to secure the enterprise." (Source: Pt3 p.32)
  - Segmentation; Access control (Access control list (ACL); Permissions); Application allow list; Isolation; Patching; Encryption; Monitoring; Least privilege; Configuration enforcement; Decommissioning
  - **Hardening techniques:** Encryption; Installation of endpoint protection; Host-based firewall; Host-based intrusion prevention system (HIPS); Disabling ports/protocols; Default password changes; Removal of unnecessary software

## Segmentation / separation / isolation (Source: Pt3 p.33)

- **Segmentation / Separation / Isolation:** VLANs / subnetting / enclaves. In a segmented network, systems are divided into separate segments or subnets, each with distinct security controls and access permissions. (Source: Pt3 p.33)
- **Isolation** — removing or severely restricting communications paths to a particular device or system; segregating individual devices within a network to limit their interaction with other devices and systems. (Source: Pt3 p.33)

## Subnetting and CIDR (Source: Pt3 p.34-35)

- **Subnetting** — creating subnetworks logically separated through manipulation of IP addresses. (Source: Pt3 p.34)
  - Compartmentalizes portions of the network, increasing security; makes better use of limited IP address space; reduces broadcast traffic and collisions; subnets are typically configured on hosts. (Source: Pt3 p.34)
  - A host on one subnet can only communicate with other hosts on the same subnet, provided they are both on the same side of a single router. (Source: Pt3 p.34)
  - Diagram: Subnet ID 1 hosts 192.168.70.10/16, 70.11/16, 70.12/16; Subnet ID 2 hosts 192.168.70.200/24, 70.201/24, 70.202/24 (the "70.x" portion boxed in red), joined through a switch. (Source: Pt3 p.34)
- **Classless Inter-Domain Routing (CIDR) table** (columns: CIDR, Mask, Classful, IPv4-Addresses) (Source: Pt3 p.35). Highlighted rows:
  - /7 254.0.0.0 — two class A subnets, 2^25 = 33,554,432
  - **/8 255.0.0.0 — class A, 2^24 = 16,777,216**
  - /9 255.128.0.0 — half class A subnet, 2^23 = 8,388,608
  - /15 255.254.0.0 — two class B subnets, 2^17 = 131,072
  - **/16 255.255.0.0 — class B, 2^16 = 65,536**
  - /17 255.255.128.0 — half class B subnet, 2^15 = 32,768
  - /23 255.255.254.0 — two class C subnets, 2^9 = 512
  - **/24 255.255.255.0 — class C, 2^8 = 256**
  - /25 255.255.255.128 — half class C subnet, 2^7 = 128
  - Unhighlighted rows (Classful column blank on all of these), left block:
    - /0 0.0.0.0 — 2^32 = 4,294,967,296
    - /1 128.0.0.0 — 2^31 = 2,147,483,648
    - /2 192.0.0.0 — 2^30 = 1,073,741,824
    - /3 224.0.0.0 — 2^29 = 536,870,912
    - /4 240.0.0.0 — 2^28 = 268,435,456
    - /5 248.0.0.0 — 2^27 = 134,217,728
    - /6 252.0.0.0 — 2^26 = 67,108,864
    - /10 255.192.0.0 — 2^22 = 4,194,304
    - /11 255.224.0.0 — 2^21 = 2,097,152
    - /12 255.240.0.0 — 2^20 = 1,048,576
    - /13 255.248.0.0 — 2^19 = 524,288
    - /14 255.252.0.0 — 2^18 = 262,144
  - Unhighlighted rows, right block:
    - /18 255.255.192.0 — 2^14 = 16,384
    - /19 255.255.224.0 — 2^13 = 8,192
    - /20 255.255.240.0 — 2^12 = 4,096
    - /21 255.255.248.0 — 2^11 = 2,048
    - /22 255.255.252.0 — 2^10 = 1,024
    - /26 255.255.255.192 — 2^6 = 64
    - /27 255.255.255.224 — 2^5 = 32
    - /28 255.255.255.240 — 2^4 = 16
    - /29 255.255.255.248 — 2^3 = 8
    - /30 255.255.255.252 — 2^2 = 4
    - /31 255.255.255.254 — 2^1 = 2
    - /32 255.255.255.255 — 2^0 = 1
  - Highlighted rows show the Classful column text exactly as on the slide: /7 "Two class A subnets", /8 "A", /9 "Half class A subnet", /15 "Two class B subnets", /16 "B", /17 "Half class B subnet", /23 "Two class C subnets", /24 "C", /25 "Half class C subnet". On the /8, /16 and /24 rows the slide shows the address count (16,777,216 / 65,536 / 256) in a second cell beside the class letter, repeating the IPv4-Addresses column. (Source: Pt3 p.35)

## VLANs (Source: Pt3 p.36; slide title "VLAN Management")

- **Virtual Local Area Network (VLAN)** — a logically separate network created using switching technology; a broadcast domain partitioned within a switched (Layer 2) network. (Source: Pt3 p.36)
  - Multiple broadcast domains can exist on a single switch; VLANs can segregate traffic by department (Engineering, HR, Finance, etc.); unused ports can be routed into an isolated, empty VLAN to protect the rest of the network. (Source: Pt3 p.36)
  - Diagram: three Virtual Switches each linked to servers (small orange firewall-style icons beside the servers), a Virtual Router, and a Physical Switch outside the dashed box. (Source: Pt3 p.36)

## Intranets and extranets (Source: Pt3 p.37)

- **Intranet** — an organization's server architecture, operational systems, networks and websites that deploy tools, applications, data only available from within the organization's network. (Source: Pt3 p.37)
- **Extranet** — allows external entities (other companies) access to part of an organization's internal network over a secure internet connection; limited to specific organizations, people, etc. (Source: Pt3 p.37)
- Diagram: Internet and Company B connect to the **Outer Firewall** (labelled zones left to right: **Extranet**, **DMZ — Semi-trusted Zone**, **Intranet**); two DMZ servers sit between the Outer and **Inner Firewall**; two **Intranet** servers sit behind the inner firewall; Company A Telecommuters connect via **VPN** (lines drawn to both firewalls). (Source: Pt3 p.37)

## Access control lists (ACL) — allow list / deny list (Source: Pt3 p.38)

- **Access Control Lists (ACL)** — list of network users and their permitted actions, systems, etc. on the network; "typically use an 'explicit deny' ruleset, opposite of a firewall." (Source: Pt3 p.38)
  - **Whitelisting** — only allow those listed and deny everyone else; **implicit deny / explicit allow** — if you are not on the list to be allowed in, you are denied. (Source: Pt3 p.38)
  - **Blacklisting** — allow everyone except those on the not-allowed list; **explicit deny / implicit allow** — if you are on the list to NOT be allowed in, you are denied. (Source: Pt3 p.38)
  - Pictures: VPN-client screenshot (Cisco Systems), ID badge on keyboard, Windows Event Viewer security log screenshot; illustrative only; no text beyond screenshots. (Source: Pt3 p.38)
- [GAP] The slides do not have a dedicated "application allow list" slide or a "permissions" slide; whitelisting/blacklisting is covered only in the ACL slide and is not tied to applications. (Source: Pt3 p.38)

## Patch / update management (Source: Pt3 p.39)

- **Patch/Update management** — planning, testing, implementing, and auditing of patches to the OS and/or applications installed on the system. (Source: Pt3 p.39)
  - Use a sandbox or isolated system to identify unwanted side effects; should mirror the production environment; apply patches in a timely manner; consider rollback options. (Source: Pt3 p.39)
  - **Patch/update categories** (Source: Pt3 p.39):
    - **Patch** — some additional functionality or non-urgent fix; can be optional.
    - **Hotfix** — an immediate and urgent patch to fix issues; typically not optional.
    - **Security update** — broadly released fix for a product-specific security-related vulnerability.
    - **Critical update** — broadly released fix for a specific problem addressing a critical, non-security-related bug.
    - **Service pack** — cumulative set of hotfixes, security updates, critical updates and other updates or fixes for internal problems since the product's release.
    - **Windows Update** — recommended update to fix non-critical problems that users might encounter; can also add features and updates to features already on the system.
    - **Driver update** — updates to the device drivers of the system.

## Encryption (Source: Pt3 p.40)

- **Full Disk Encryption (FDE)** — encrypts the entire hard drive of a device; all data including the OS and user files protected even while the OS is not running. **BitLocker** for Windows / **FileVault** for macOS; Whole Disk Encryption (WDE) / Encrypted File System (EFS). (Source: Pt3 p.40)
- **Removable media encryption** — data remains protected even when physically removed from devices; SD cards or USB mass storage; many FDE tools also include options for encrypting removable media. (Source: Pt3 p.40)
- **Virtual Private Networks (VPNs)** — a secure tunnel for data transmission that protects against eavesdropping, on-path, and many other attack types. (Source: Pt3 p.40)
- **Email encryption** — protects sensitive information stored in emails: **PGP** (Pretty Good Privacy); **S/MIME** (Secure/Multipurpose Internet Mail Extensions). (Source: Pt3 p.40)

## Monitoring (Source: Pt3 p.41)

- Monitoring plays a vital role in endpoint hardening, helping enforce and maintain the security measures put in place during hardening; once devices are hardened, monitoring helps ensure these conditions remain in place. (Source: Pt3 p.41)
- **Aggregate information from devices:** built-in sensors, separate devices; integrated into servers, switches, routers, firewalls, etc. (Source: Pt3 p.41)
- **Sensors:** intrusion prevention systems, firewall logs, authentication logs, web server access logs, database transaction logs, email logs. (Source: Pt3 p.41)
- **Collectors:** proprietary consoles (IPS, firewall); SIEM consoles, syslog servers; many SIEMs include a **correlation engine** to compare diverse sensor data. (Source: Pt3 p.41)

## Least privilege / least functionality (Source: Pt3 p.42)

- **Least privilege** — everyone in the organization only has the absolute minimum access and privileges needed to perform their assigned tasks. (Source: Pt3 p.42)
  - Reduces the exposure and harm that can be done by accessing property, networks, systems, and data; limit access to what is needed and nothing more; Windows — right-click "Run as administrator"; Linux/Unix — `sudo`. (Source: Pt3 p.42)
- **Least functionality** — the process by which a system is configured and capable of only doing what it is intended to do and no more. (Source: Pt3 p.42)

## Configuration enforcement (Source: Pt3 p.43)

- **Configuration enforcement** — methods used to ensure that systems and devices within an organization's network adhere to mandatory security configurations. (Source: Pt3 p.43)
  - Listed methods only: standardized configuration baselines; automated configuration management tools; continuous monitoring and compliance checks; change management; configuration management. No sub-explanations given. (Source: Pt3 p.43)

## Decommissioning (Source: Pt3 p.44)

- **Decommissioning** — ensures that all data is securely erased or overwritten to reduce the risk of exposure. (Source: Pt3 p.44)
  - Resetting devices to factory settings, eliminating any residual settings; updating inventory records to maintain an accurate account of active assets and support compliance requirements. (Source: Pt3 p.44)

## System hardening practices (Source: Pt3 p.45)

- **System hardening** — the process of configuring systems and networks to ensure they are operating at their best, most secure state. Listed practices (Source: Pt3 p.45):
  - Encryption
  - Installation of endpoint protection and anti-virus software
  - Host-based firewall / Host-based IDS/IPS/IDPS
  - Data Loss Prevention / Data Execution Prevention
  - Patch management / Password management
  - Securing the BIOS/UEFI, hardware, and peripherals
  - Disable protocols such as Telnet, NetBIOS, IPX, and FTP when not needed
  - Disabling services and ports such as ECHO and CHARGEN when not needed
  - Removing unnecessary shares and unnecessary software
  - Controlling physical access to servers
  - Managing remote interfaces: SSH is a better option than Telnet; securing SNMP or disabling it if not used; web-based management interfaces should be restricted to intranet only

## Non-content pages (Source: Pt3 p.46-47)

- Pt3 p.46 (2-123) is the Domain 2 "Domain Topics" recap listing 2.1-2.5 with their full objective statements (2.1 Compare and contrast common threat actors and motivations; 2.2 Explain common threat vectors and attack surfaces; 2.3 Explain various types of vulnerabilities; 2.4 Given a scenario, analyze indicators of malicious activity; 2.5 Explain the purpose of mitigation techniques used to secure the enterprise). Pt3 p.47 (2-124) is an Education Ecosystem logo slide. No objective content. (Source: Pt3 p.46-47)

## Official-objective gap check (2.5)

Official bullets are those on the Section Topics slide (Source: Pt3 p.32). Checked against the Section Topics slide (Pt3 p.32) during validation (2026-10-16); all 18 rows confirmed.

| Official bullet | Result | Notes |
|---|---|---|
| Segmentation | Covered | Pt3 p.33-37 (subnetting, CIDR, VLAN, intranet/extranet/DMZ) |
| Access control — ACL | Covered | Pt3 p.38 (note slide's odd "opposite of a firewall" wording) |
| Access control — permissions | Not in slides | No dedicated permissions content in this range |
| Application allow list | Weak | Whitelisting/blacklisting described for ACLs only, not applications (Pt3 p.38) |
| Isolation | Covered | Pt3 p.33 (definition only) |
| Patching | Covered | Pt3 p.39 |
| Encryption | Covered | Pt3 p.40 |
| Monitoring | Covered | Pt3 p.41 |
| Least privilege | Covered | Pt3 p.42 |
| Configuration enforcement | Weak | Pt3 p.43 — method names only |
| Decommissioning | Covered | Pt3 p.44 |
| Hardening: encryption | Covered | Pt3 p.40, 45 |
| Hardening: endpoint protection | Covered | Pt3 p.45 (listed, not explained) |
| Hardening: host-based firewall | Weak | Listed only (Pt3 p.45) |
| Hardening: HIPS | Weak | Listed as "Host-based IDS/IPS/IDPS" only (Pt3 p.45) |
| Hardening: disabling ports/protocols | Covered | Pt3 p.45 (Telnet, NetBIOS, IPX, FTP; ECHO and CHARGEN) |
| Hardening: default password changes | Weak | Only "password management" listed; default password changes are not stated (Pt3 p.45) |
| Hardening: removal of unnecessary software | Covered | Pt3 p.45 |

Suggested objective status: **Weakly Covered** (permissions absent; allow list, configuration enforcement, host firewall/HIPS, default passwords thin).


## Validation log

Validated 2026-10-16. All 17 pages (Pt3 p.31-47) were rendered at 130 dpi and each image was opened and compared with the note.

Pages checked: Pt3 p.31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47. Printed slide numbers confirmed 2-108 to 2-124 (offset +123); all inline citations use Pt3 page numbers.

Corrections made:
- p.35 (CIDR): replaced the "Masks follow the standard pattern" inference with every unhighlighted row's exact mask and address count read from the slide (all 33 rows /0-/32 now recorded); added exact Classful cell text for highlighted rows. The previously recorded address counts and highlighted rows were all correct.
- p.36: added the slide's actual title "VLAN Management" and corrected diagram description (Virtual Switches / Virtual Router / Physical Switch outside dashed box; orange firewall-style icons).
- p.37: reworded diagram description to match slide (zone labels Extranet / DMZ Semi-trusted Zone / Intranet; two servers per zone; VPN lines to both firewalls).
- p.38: noted the VPN screenshot is a Cisco Systems client.
- p.39: restored omitted words "that users might encounter" in the Windows Update definition.
- p.46: corrected "titles only" to full objective statements 2.1-2.5.
- Front matter and gap-check intro updated.

Pages with no corrections needed: p.31, 32, 33, 34, 40, 41, 42, 43, 44, 45, 47. Official-objective gap check table verified against Pt3 p.32 (all 11 non-hardening items (counting ACL and Permissions separately) plus 7 hardening sub-bullets represented, 18 rows) and content; statuses unchanged. No slide errors found, so no [CONFLICT] marks.

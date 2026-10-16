---
Unit: Audits and Assessments
Domain: 5.0 Security Program Management and Oversight (sub-objective 5.5 — Explain types and purposes of audits and assessments)
Source: Pt7 p.29-46 (global 629-646; course slides 5-71 to 5-88). Boundaries: Pt7 p.29 = 5.5 roadmap (5-71, "Audits and assessments" highlighted); Pt7 p.47 = 5.6 roadmap (5-89, "Security awareness practices" highlighted)
Extraction_Status: Fully Extracted (all 18 pages read via vision at 100 dpi)
Pages_Done: Pt7 p.29-46
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — same-session re-check of the note against the 100 dpi renders; not an independent second reader
---

## Section Topics (Source: Pt7 p.30)

- Attestation
- Internal: compliance; audit committee; self-assessments
- External: regulatory; examinations; assessment; independent third-party audit
- Penetration testing: physical; offensive; defensive; integrated; known environment; partially known environment; unknown environment; reconnaissance (passive, active)

(Source: Pt7 p.30)

## Attestation (Source: Pt7 p.31)

- **Attestation** — provides assurance to stakeholders that an organization's security measures are adequate and effective in protecting sensitive information, mitigating risks, and maintaining data confidentiality, integrity, and availability. (Source: Pt7 p.31)
  - Verifying and validating the accuracy, reliability, and effectiveness of security controls, systems, and processes implemented within an organization.
  - Involves an independent and objective examination by a qualified and trusted entity, such as an auditor or assessor.
  - A formal declaration or confirmation that an organization's security controls and practices comply with specific standards, regulations, or best practices.

## Internal Audits and Assessments (Source: Pt7 p.32)

| Term | Slide definition | Detail bullets |
|---|---|---|
| **Compliance Assessment** | Ensure operating practices align with laws, regulations, standards, policies, and ethical requirements | Evaluate the effectiveness of internal controls, identify noncompliance or risk areas, and communicate findings to stakeholders such as risk managers |
| **Audit Committees** | Provide independent oversight and assurance regarding an organization's financial reporting, internal controls, and risk management practices | Typically composed of board members independent of the organization's management team. Aim to enhance the integrity of financial statements, ensure compliance with legal and regulatory requirements, monitor effectiveness of internal controls, oversee the external audit process, and promote transparency and accountability. Critical in fostering confidence among shareholders, stakeholders, and the public via an independent and objective assessment of financial practices, contributing to sound corporate governance |
| **Self-Assessments** | Allow individuals or organizations to evaluate their performance, practices, and adherence to established criteria against predetermined metrics and measures | Help identify strengths, weaknesses, and areas for improvement, enabling proactive measures. Imply internal personnel with the expertise, knowledge, and understanding of the assessed area are available to complete them |

(Source: Pt7 p.32 for the whole table)

## External Audits and Assessments (Source: Pt7 p.33-34)

| Term | Slide definition | Detail bullets | Source |
|---|---|---|---|
| **Regulatory** authorities or agencies | Perform assessments to ensure compliance with specific laws, regulations, or industry standards | Evaluate whether organizations adhere to mandatory regulatory requirements and promote a culture of compliance. Involve inspections, audits, or reviews of processes, practices, and controls to verify compliance, identify deficiencies, and enforce regulatory obligations. Play a critical role in safeguarding public interests, protecting consumers, maintaining market integrity, and upholding industry standards. Help mitigate risks, ensure fair competition, and enhance transparency and accountability in regulated industries | Pt7 p.33 |
| **Examination** | An independent and formal evaluation conducted by external parties, such as auditors or regulators, to assess the accuracy, reliability, and compliance of an organization's financial statements, processes, controls, or specific aspects of its operations | Focus on verifying information accuracy and ensuring compliance with applicable laws, regulations, or industry standards. Examples: financial statement audits, regulatory compliance audits, and specific assessments of control environments | Pt7 p.33 |
| **Assessment** | A broad evaluation conducted by external experts or consultants to assess an organization's overall performance, practices, capabilities, or specific focus areas | Can encompass strategy, operational efficiency, risk management, cybersecurity, or compliance practices. Goal: an objective and independent perspective on strengths, weaknesses, and opportunities for improvement | Pt7 p.34 |
| **Independent Third-Party Audits** | Provide objective and unbiased assessments of an organization's systems, controls, processes, and compliance | Offer an external perspective, free from any conflicts of interest or bias. Instill confidence among stakeholders (customers, business partners, regulatory bodies, investors) as they attest to an organization's commitment to quality, compliance, and good governance. Help organizations demonstrate transparency, accountability, and adherence to industry standards and regulations | Pt7 p.34 |

## Audit Strategies (Source: Pt7 p.35)

- Companies should ensure that, at minimum, internal and external assessments, testing, and auditing are completed on a regular basis. (Source: Pt7 p.35)
  - **Internal Audit** — carried out by personnel within the organization. Slide shorthand: "Audit yourself". (Source: Pt7 p.35)
  - **External Audit** — carried out by a vendor or contractor that is engaged by the company. Slide shorthand: "Outside (third-party) auditor auditing you". (Source: Pt7 p.35)
  - **Third-party Audit** — carried out by a party completely unrelated to the company and not previously engaged by the company. Uses: standard or regulation compliance; accreditation or certification; "third-party auditors auditing your auditors". (Source: Pt7 p.35)
- Note: the slide distinguishes External Audit (a vendor/contractor *engaged by* the company) from Third-party Audit (*completely unrelated and not previously engaged*). On p.33-34 and the Section Topics list, "independent third-party audit" is one external item; the two slides use "third-party" slightly differently (the p.35 "External Audit" line itself says "(third-party)"). [CONFLICT — terminology only; both readings recorded]

## Penetration Testing (Source: Pt7 p.36)

- **Penetration Test / Ethical Hacking** — uses authorized hacking techniques to discover exploitable weaknesses in the target's security systems; mimics a real-world threat (the phrase "mimics a real-world threat" is underlined on the slide). (Source: Pt7 p.36)
- Advantages of penetration tests (Source: Pt7 p.36):
  - **Verify a threat exists** — use surveillance, social engineering, network scanners, and vulnerability assessment tools to identify a vector by which vulnerabilities could be exploited.
  - **Bypass security controls** — look for easy ways to attack a system.
  - **Actively test security controls** — probe for configuration weaknesses and errors, such as weak passwords or software vulnerabilities.
  - **Exploit vulnerabilities** — prove that a vulnerability is high risk by exploiting it to gain access to data or install backdoors.

### Penetration Test Types (Source: Pt7 p.37)

| Type | Slide definition | Detail |
|---|---|---|
| **Physical** | Assessments of an organization's physical security practices and controls | Simulating real-world attack scenarios to identify vulnerabilities in physical security systems such as access controls, surveillance, and perimeter defenses |
| **Offensive** | Identifies vulnerabilities, weaknesses, and potential attack vectors that malicious actors could exploit | A proactive and controlled approach to simulate real-world cyberattacks on systems, networks, and applications; labeled "Red Teaming" |
| **Defensive** | Evaluates the organization's ability to detect and respond to threats | (no further detail on slide) |
| **Integrated** | A holistic approach that combines different types of penetration testing methodologies and techniques to assess overall security of systems, networks, applications, and physical infrastructure | — |

(Source: Pt7 p.37 for the whole table)

### Penetration Test Environments (Source: Pt7 p.38)

- Types by position (Source: Pt7 p.38):
  - **Internal** — conducted against hosts internal to the client's network.
  - **External** — conducted against the Internet-facing hosts of a client's network.
- Variations (Source: Pt7 p.38; slide shows white, gray, and black box icons beside the list):

| Variation | Slide's "environment" label (underlined) | Slide detail |
|---|---|---|
| **White-Box** Testing | **Known Environment** | Internal details (source code) are considered; full-knowledge |
| **Gray-Box** Testing | **Partially Known Environment** | Commonly available user information is provided; partial-knowledge |
| **Black-Box** Testing | **Unknown Environment** | No internal code details are used; zero-knowledge / public knowledge |

- Black-box sub-variations (Source: Pt7 p.38):
  - **Blind Test (single-blind)** — attacker has no knowledge of the system but the staff are informed that a PenTest will take place.
  - **Double-blind Test** — attacker has no knowledge of the system and the staff are not made aware that a PenTest will take place.

### Penetration Testing Teams (Source: Pt7 p.39-40)

The slides present these on a football-field background ("Home Team"/"Away Team", "Referee", "Cheerleaders" analogies) with colored figure graphics; credit line "Created by an Education Ecosystem Instructor". (Source: Pt7 p.39-40)

| Team | Slide definition | Slide shorthand | Source |
|---|---|---|---|
| **Blue** | Performs the defensive role by operating monitoring and alerting controls to detect and prevent the infiltration | Security professionals; Defenders (Home Team) | Pt7 p.39 |
| **Red** | Performs the offensive role to try to infiltrate the target | Certified ethical hackers; Attackers (Away Team) | Pt7 p.39 |
| **White** | Staff administering, evaluating, and supervising a penetration test or incident response exercise; sets the rules of engagement and monitors the exercise | Referee | Pt7 p.39 |
| **Purple** | Combination of red and blue teams that share information and encourage collaboration throughout the engagement | Not necessarily a separate team; a different way of structuring the exercise; Facilitators, Cheerleaders | Pt7 p.39 |
| **Yellow** | Represents the builders; software developers and security architects responsible for building cybersecurity systems | Focuses on secure coding practices and building systems with security in mind; composed primarily of software developers and system architects; Builders | Pt7 p.40 |
| **Orange** | Combination of red and yellow teams; includes IT personnel who use insights gained from the red team to help the yellow team be more security conscious in development | Educating/informing developers/builders on potential vulnerabilities/threats; provides threat modeling and security awareness training to the yellow team | Pt7 p.40 |
| **Green** | Combination of blue and yellow teams to use the blue team's reporting to improve upon the yellow team's security code | Focus on improving security practices within the development process; may also automate blue team tasks like threat detection; may involve reviewing code and suggesting security enhancements | Pt7 p.40 |

### Reconnaissance

**Passive Reconnaissance** (Source: Pt7 p.41)
- Gathering information about target systems and networks without directly interacting with them, by collecting publicly available data and passively observing network traffic.
  - The computers, servers, or devices are not affected by your scans/tests; no data/traffic is sent to those devices.
  - Aims to gather intelligence on the target environment and identify potential vulnerabilities while generating minimal evidence of their actions.
- Slide examples (underlined terms):
  - **Open-Source Intelligence (OSINT) Gathering** — collecting publicly available information from sources like search engines, social media, public databases, and websites.
  - **Network Traffic Analysis** — monitoring network traffic to identify patterns, devices, IP addresses, and potential vulnerabilities without actively generating traffic.
    - **War Driving** — driving around and mapping the location and type (frequency channel and security method) of wireless networks operated by the target.
    - **Drones/Unmanned Aerial Vehicle (UAV)** — allow the tester to reconnoiter campus premises, and even to perform war driving from the air (**war flying**).
  - **Social Engineering** — gathering information through social engineering techniques, such as deceiving employees and vendors to extract sensitive information or access credentials.
  - [CONFLICT — consistency with Active definition: the slide lists social engineering under *Passive*, although it involves interacting with people; recorded as the slide states it.]

**Active Reconnaissance** (Source: Pt7 p.42)
- Actively probing and interacting with target systems and networks to gather information.
  - Traffic or data is sent to the computers, servers, or devices to solicit information from them based on the responses they provide.
  - Aims to discover and obtain information about the target infrastructure, services, and potential vulnerabilities.
- Slide examples (underlined terms):
  - **Port Scanning** — scanning a target network to identify open ports and the services running on them.
  - **Service Enumeration** — interacting with identified services to gather information about their versions, configurations, and potential vulnerabilities.
  - **OS Fingerprinting** — attempting to identify the operating system running on target machines by analyzing network responses and behavior.
  - **DNS Enumeration** — gathering information about the target's DNS infrastructure, such as domain names, subdomains, and IP addresses.
  - **Web Application Crawling** — exploring web applications to identify pages, directories, and potential vulnerabilities.

## Security Assessment Tools (Source: Pt7 p.43-46)

(These slides are not itemized on the 5.5 Section Topics list; recorded because they sit inside the 5.5 slide range.)

- **Network Mapping / Network Mappers** (Source: Pt7 p.43) — the study of physical and logical connectivity of networks. Allows information/system security professionals to see what devices are connected to their network and understand what the network architecture looks like.
  - Screenshots: a terminal `nmap -A -T4 scanme.nmap.org d0ze` run (Nmap 4.01) listing open ports/services (ssh 22, smtp 25, domain 53, http 80 Apache httpd 2.0.52 (Fedora)) with OS details "Linux 2.6.0 - 2.6.11", and a second host d0ze.internal showing ftp, smtp, http (Microsoft IIS webserver 5.0), pop3, msrpc, netbios-ssn, microsoft-ds, vnc-http ports and "OS details: Microsoft Windows 2000 Professional"; plus a **Zenmap** GUI screenshot (Intense Scan, Nmap Output tab). Credit: "Screenshots taken by an Education Ecosystem Instructor". (Source: Pt7 p.43)
- **Banner Grabbing** (Source: Pt7 p.44) — a technique used to find out information about web servers, FTP servers, mail servers, and other services running on a system.
  - Used by network administrators to inventory systems and the services running on them; this technique is often used by attackers to determine potential attack vectors.
  - Example screenshot: `C:\ nc 192.168.1.20 80` then `HEAD / HTTP/1.0` returns `HTTP/1.1 200 OK`, Date, `Server: Apache/2.0.46 (Unix) (Red Hat/Linux)`, Last-Modified, ETag, Accept-Ranges, Content-Length: 1110, Connection: close, Content-Type: text/html.
  - Tools banner on the slide: "netcat, nmap, telnet, etc."
- **Network Sniffing** (Source: Pt7 p.45) — the process of using a tool to find and investigate communications between computers on the network.
- **Protocol Analyzer** (Source: Pt7 p.45) — a tool that captures packets as they are transmitted across the network (wired or wireless) and analyzes the traffic to determine the type of data being transmitted. Screenshot: Wireshark `capture.pcap` (HTTP/1.1 302 Found packet selected).
- **Protocol Analyzer / Packet Sniffer** (Source: Pt7 p.46) — a software or integrated hardware/software system that can capture and decode network traffic. Uses listed:
  - Detecting network intrusions and undesirable traffic, botnets, trojans, or infected systems
  - Analyzing network problems and debugging client/server communications
  - Detecting misconfigured applications or misbehaving applications
  - Gathering and reporting network usage and traffic statistics
  - Capturing traffic during incident response or incident handling
  - NOTE: sniffing network traffic requires the Network Interface Card (NIC) to be in "promiscuous mode".
- **Promiscuous Mode** — the network adapter listens to ALL network frames transmitted on the network rather than just those addressed for the particular network adapter. **Non-Promiscuous Mode** — the network adapter captures only the packets addressed to it specifically. (Source: Pt7 p.46)

## Official-objective gap check (5.5)

Official sub-bullets compared with the validated note. Status is relative to the slides only — no outside knowledge used.

| Official bullet | Result | Evidence / gap |
|---|---|---|
| Attestation | Covered | Defined with three detail bullets (Pt7 p.31) |
| Internal — Compliance | Covered | Compliance Assessment (Pt7 p.32) |
| Internal — Audit committee | Covered | Pt7 p.32 |
| Internal — Self-assessments | Covered | Pt7 p.32 |
| External — Regulatory | Covered | Pt7 p.33 |
| External — Examinations | Covered | Pt7 p.33 |
| External — Assessment | Covered | Pt7 p.34 |
| External — Independent third-party audit | Covered | Pt7 p.34-35; terminology overlap with "External Audit" noted [CONFLICT] |
| Pen testing — Physical | Covered | Pt7 p.37 |
| Pen testing — Offensive | Covered | Pt7 p.37 (tied to "Red Teaming") |
| Pen testing — Defensive | Weak | One-sentence definition only; no example or method (Pt7 p.37). Blue team role is on Pt7 p.39 but is not linked to "defensive" on the slides |
| Pen testing — Integrated | Weak | One-sentence definition only (Pt7 p.37) |
| Pen testing — Known environment | Covered | White-box (Pt7 p.38) |
| Pen testing — Partially known environment | Covered | Gray-box (Pt7 p.38) |
| Pen testing — Unknown environment | Covered | Black-box, blind and double-blind (Pt7 p.38) |
| Reconnaissance — Passive | Covered | Pt7 p.41 (social engineering listed as passive — see [CONFLICT]) |
| Reconnaissance — Active | Covered | Pt7 p.42 |

**Result: Weakly Covered** under the strict rule (2 Weak bullets: defensive, integrated). All other bullets covered.

Other gaps and observations:
- The slides do not explain *when* to choose internal vs external audits, nor who may perform an attestation beyond "auditor or assessor". Not on the official bullet list; noted only.
- SOC reports / SSAE attestation reporting are in the 5.4 unit (Pt7 p.18), not here — cross-link [[effective-security-compliance]].
- Possible bearing on the open 4.3 bullet "system/process audit" as a vulnerability-identification method: this unit's audit material (Pt7 p.35) is about compliance/governance audits, not vulnerability-identification audits, so that 4.3 gap is **not** closed by this unit.

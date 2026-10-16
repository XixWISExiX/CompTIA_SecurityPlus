---
Unit: Security Alerting and Monitoring Concepts and Tools
Domain: 4.0 Security Operations (sub-objective 4.4 — Explain security alerting and monitoring concepts and tools)
Source: Pt5 p.46-56 (global 446-456; course slides 4-61 to 4-71). Boundaries: Pt5 p.46 = 4.4 roadmap (4-61, confirmed in the 4.3 pass); Pt5 p.57 = 4.5 roadmap (4-72)
Extraction_Status: Fully Extracted (all 11 pages read via vision; boundary confirmed: Pt5 p.57 = 4.5 roadmap)
Pages_Done: Pt5 p.46-56
Pages_Remaining: none
Next_Page: none
Validation_Status: Validated (2026-10-16) — all 11 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt5 p.46-47)

- Pt5 p.46 (4-61) is the Domain 4 roadmap slide with "Security alerting and monitoring concepts and tools" highlighted. (Source: Pt5 p.46)
- Pt5 p.47 (4-62) is the 4.4 Section Topics slide (Source: Pt5 p.47):
  - **Monitoring computing resources:** Systems; Applications; Infrastructure
  - **Activities:** Log aggregation; Alerting; Scanning; Reporting; Archiving; Alert response and remediation/validation (Quarantine, Alert tuning)
  - **Tools:** Security Content Automation Protocol (SCAP); Benchmarks; Agents/agentless; Security information and event management (SIEM); Antivirus; Data loss prevention (DLP); Simple Network Management Protocol (SNMP) traps; NetFlow; Vulnerability scanners

## Monitoring computing resources (Source: Pt5 p.48)

- **System monitor** — software that tracks the health of a computer's subsystems using metrics reported by system hardware or sensors. Provides an alerting service for faults such as high temperature, chassis intrusion, and so on. Implements the same functionality as a network monitor for a computer host. Switches and routers, server hosts can report health status using SNMP traps.
- **Application monitor** — a basic heartbeat test to verify that it is responding. Also: the number of sessions and requests, bandwidth consumption, CPU and memory utilization, and error or security alert conditions.
- **Cloud monitor** — assess different facets of cloud services, such as network bandwidth, virtual machine status, and application health.
- **Infrastructure** — managerial reports can be used for day-to-day monitoring of computer resources and network infrastructure. Not all issues can be identified from alerts and alarms. Running a custom report allows a manager to verify results of logging and monitoring activity to ensure that the network remains in a secure state.

(Source: Pt5 p.48)

## Alerting and monitoring activities (Source: Pt5 p.49)

| Activity | Slide definition |
|---|---|
| Log aggregation | Parsing information from multiple log and security event data sources so that it can be presented in a consistent and searchable format |
| Alerting | Real-time notification of security events |
| Scanning | Actively checking systems and devices |
| Reporting | A managerial control that provides insight into the status of the security system |
| Archiving | A retention policy so that historical log and network traffic data is kept for a defined period |
| Alert response and remediation | Steps will often be guided by a playbook that assists the analyst with applying all incident response processes for a given scenario |
| — Validation | How the analyst decides whether the alert is a true positive and needs to be treated as an incident |
| — Quarantine | The step of isolating the source of indicators, such as a network address, host computer, or file |
| — Alert tuning | The process of adjusting detection and correlation rules to reduce incidence of false positives and low-priority alerts |

(Source: Pt5 p.49)

## Benchmarks and SCAP (Source: Pt5 p.50)

- **Benchmarks** — specific information about best practices in configuring a particular application or security control. (Source: Pt5 p.50)
- **Security Content Automation Protocol (SCAP)** — a NIST framework that outlines various accepted practices for automating vulnerability scanning. (Source: Pt5 p.50)
  - A method for using specific standards to obtain vulnerability feed, maintained by the **National Vulnerability Database (NVD)**.
  - Allows compatible scanners to determine whether a computer meets a configuration baseline.
  - Uses several components:
    - **Open Vulnerability and Assessment Language (OVAL)** — an XML schema for describing system security state and querying vulnerability reports and information.
    - **Extensible Configuration Checklist Description Format (XCCDF)** — an XML schema for developing and auditing best practice configuration checklists and rules. Previously, best practice guides might have been written in prose for systems administrators to apply manually; XCCDF provides a machine-readable format that can be applied and validated using compatible software.

## Agent-based and agentless collection (Source: Pt5 p.51)

- **Agent-based** — installing an agent service on each host. As events occur on the host, logging data is filtered, aggregated, and normalized at the host, then sent to the SIEM server for analysis and storage.
- **Listener/collector** — a network appliance that gathers or receives log and/or state data from other network systems (agentless). Used to collect logs from switches, routers, and firewalls.
- **Sensor** — a monitor that records (or "sniffs") data from frames as they pass over network media, using methods such as a mirror port or TAP device. A sniffer can record network data using either the mirror port functionality of a switch or using some type of TAP on the network media.

(Source: Pt5 p.51)

## SIEM (Source: Pt5 p.52)

- **Security Information and Event Management (SIEM)** — a solution that provides real-time or near-real-time analysis of security alerts generated by network hardware and applications. (Source: Pt5 p.52)
  - **Data aggregation** — combine and correlate data from network devices and applications.
  - **Correlation engines** — look for common attributes of events.
  - **Compliance analysis** — scan for compliance with government laws and regulations.
  - **Forensic analysis** — collect and manage data for forensic analysis.
  - **Time synchronization** — synchronize the time stamps for the data collected surrounding an event.
  - **Event de-duplication** — removing multiple reports of the instance.
  - **WORM (Write Once, Read Many) data** — data that is written once and cannot be modified.
  - **Vulnerability scan output** — reports that identify vulnerabilities (findings) and suggested remediation can be sent to a SIEM for correlation and compliance.
- The slide includes a screenshot of a Splunk "Nessus Vulnerability Severity 2" dashboard (credited "Screenshots taken by an Education Ecosystem Instructor"); not transcribed beyond that description.

## Antivirus and DLP (Source: Pt5 p.53)

- **Antivirus (AV)** — software capable of detecting and removing virus infections and other types of malware. Contains a virus scanning engine and a database of known virus "signatures"; scans the computer's file system and attempts to match known virus patterns/signatures against those files; a match may indicate an infected file and may quarantine or delete it. (Source: Pt5 p.53)
- **Data Loss Prevention (DLP)** — a software solution that detects and prevents sensitive information from being stored on unauthorized systems or transmitted over unauthorized networks. (Source: Pt5 p.53)
  - Block USB interfaces — prevent users from attaching storage devices to the system.
  - Monitor who is using the data — track when users are using/accessing data that has been deemed important.
  - Monitor who is transmitting the data — track when/where users transmit data that has been deemed important.

## SNMP traps (Source: Pt5 p.54)

- **SNMP monitor** — a software program that provides a location from which network activity can be overseen. Monitors all agents by polling them at regular intervals for information from their MIBs and displays the information for review. Displays any trap operations as alerts for the network administrator to assess and act upon as necessary.
- **SNMP agent** — a process (software or firmware) running on a switch, router, server, or other SNMP-compatible network device. Maintains a database (Management Information Base (MIB)) that holds statistics relating to the activity of the device (e.g. the number of frames per second handled by a switch). Capable of initiating a **trap** operation where it informs the management system of a notable event.
- **SNMP trap** — informs the management system of a notable event, such as port failure, chassis overheating, power failure, or excessive CPU utilization.
- Ports: device queries take place over **port 161 (UDP)**; traps are communicated over **port 162 (UDP)**.

(Source: Pt5 p.54)

## Flow data (Source: Pt5 p.55)

- **NetFlow** — a Cisco-developed means of reporting network flow information to a structured database that allows for better understanding of IP traffic flows as used by different network applications and hosts.
- **sFlow** — developed by HP and subsequently adopted as a web standard that uses sampling to measure traffic statistics at any layer of the OSI model for a wider range of protocol types than the IP-based NetFlow.
- **IPFIX (IP Flow Information Export)** — capture data for point-in-time analysis and to diagnose any security or operational issues the network is experiencing. Standards-based version of the NetFlow framework; Internet Engineering Task Force (IETF) standard.
- Diagram on the slide (credited to an Education Ecosystem instructor): PCAP (header + payload for each packet) minus payload equals packet headers, which are summarized into NetFlow records. The NetFlow fields listed in the diagram: Source IP, Destination IP, Source Port, Destination Port, Protocol, TCP Flags, Time Info, Byte Info, Packet Info, ICMP Info.

(Source: Pt5 p.55)

## Vulnerability scanners (Source: Pt5 p.56)

| Type | Slide definition | Slide examples |
|---|---|---|
| Vulnerability scanners (general) | Hardware or software configured with a list of known weaknesses and exploits and that can scan for their presence in a host OS or particular application | — |
| Network | Designed to test network hosts, including client PCs, mobile devices, servers, routers, and switches | Tenable Nessus, Greenbone OpenVAS, Greenbone Vulnerability Management (GVM) |
| Application | Configured with more detailed and specific scripts to test for known attacks, as well as scanning for missing patches and weak configurations | HP Fortify, Grabber, Amazon Inspector |
| Web application | Designed to look for known web exploits, such as SQL injection and cross-site scripting (XSS), and may also analyze source code and database security to detect unsecure programming practices | Nikto, Accunetix |

(Source: Pt5 p.56)

## Boundary (Source: Pt5 p.57)
- Pt5 p.57 (4-72) is the Domain 4 roadmap slide with "Modify enterprise capabilities to enhance security" highlighted, so 4.4 ends at Pt5 p.56. (Source: Pt5 p.57)

## Validation log
- Extraction: 11 pages read at 100 dpi, written in two saves (after p.51, then p.56).
- Validation (separate pass, 2026-10-16): Pt5 p.47-56 re-opened at 130 dpi and compared item by item (definitions, ports 161/162, acronyms, tool names, page citations); p.46 and p.57 were boundary slides already seen at 100 dpi. No omissions, wrong values or wrong citations found; no content changes needed.
- Slide wording kept as printed: "Netflow" (p.55 body) vs "NetFlow" (Section Topics); "Accunetix" (p.56, sic); "Security Information And Event Management" (p.52).
- Not transcribed: the Splunk screenshot content on Pt5 p.52 (illustrative only).

## Official-objective gap check (4.4 bullets as listed on the slides' Section Topics slide, Pt5 p.47)
| Official bullet | Status | Where |
|---|---|---|
| Monitoring: systems | Covered (system monitor) | Pt5 p.48 |
| Monitoring: applications | Covered (application monitor) | Pt5 p.48 |
| Monitoring: infrastructure | Covered (also cloud monitor) | Pt5 p.48 |
| Activities: log aggregation, alerting, scanning, reporting, archiving | Covered | Pt5 p.49 |
| Alert response and remediation/validation; quarantine; alert tuning | Covered | Pt5 p.49 |
| SCAP | Covered (OVAL, XCCDF, NVD) | Pt5 p.50 |
| Benchmarks | Covered (one definition) | Pt5 p.50 |
| Agents/agentless | Covered (agent-based, listener/collector, sensor) | Pt5 p.51 |
| SIEM | Covered | Pt5 p.52 |
| Antivirus | Covered | Pt5 p.53 |
| DLP | Covered | Pt5 p.53 |
| SNMP traps | Covered | Pt5 p.54 |
| NetFlow | Covered (also sFlow, IPFIX) | Pt5 p.55 |
| Vulnerability scanners | Covered | Pt5 p.56 |

All official bullets are present and validated; no gaps. Depth is brief on benchmarks (one definition). Extra slide content: cloud monitor, sFlow/IPFIX, scanner product examples.

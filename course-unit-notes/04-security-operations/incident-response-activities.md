---
Unit: Incident Response Activities
Domain: 4.0 Security Operations (sub-objective 4.8 — Explain appropriate incident response activities)
Source: Pt6 p.23-49 (module slides 4-138 to 4-164)
Extraction_Status: Fully Extracted (every page read directly via vision, in full, in order — not OCR-derived)
Validation_Status: Validated (100% of pages in range individually visually reviewed; no sampling was used for this unit)
---

## Section overview (Source: Pt6 p.24)

Official sub-objective 4.8 topic list, as presented on the course's "Section
Topics" divider slide: Process (Preparation, Detection, Analysis,
Containment, Eradication, Recovery, Lessons learned), Training, Testing
(Tabletop exercise, Simulation), Root cause analysis, Threat hunting, Digital
forensics (Legal hold, Chain of custody, Acquisition, Reporting,
Preservation, E-discovery).

## Core definitions (Source: Pt6 p.25)

- **Event** — any observable occurrence in a system or network.
- **Adverse Event** — an event with a negative consequence.
- **Incident** — a violation or imminent threat of violation of computer
  security policies, acceptable use policies, or standard security practices.
- **Incident Response** — the process of identifying, investigating,
  repairing, documenting, and adjusting procedures to prevent another
  incident.

## Incident Response Phases

The course diagram (Source: Pt6 p.25) groups the phases as: Preparation →
Identification → (Containment, Eradication & Recovery) → Lessons Learned,
with a feedback loop back to Preparation. The individual phase slides treat
Containment, Eradication, and Recovery as three distinct phases, for six
total:

1. **Preparation** (Source: Pt6 p.26) — establishing incident response
   procedures, security posture, and knowledgeable staff *before* an
   incident occurs.
   - Trial runs and tests: security controls, checklists/SOPs.
   - Resources: communications and facilities, hardware/software, incident
     analysis resources, incident mitigation software.
   - Preventing incidents: risk assessments, host security, network
     security, malware prevention, user awareness and training.
2. **Identification** (Source: Pt6 p.30) — recognizing whether an event
   should be classified as an incident. Driven by **information
   criticality** (data classification/quantity involved) and a **business
   decision** (how the breach affects business operations).
3. **Containment** (Source: Pt6 p.37) — isolating a threat to minimize
   overall damage.
   - Short-term solutions: take host(s) offline/quarantine,
     physical/logical isolation, block site/IP/MAC address, disable user
     account(s), disable/update certificate, application blocklist/deny
     list, content/URL filter.
   - Long-term solutions: permanent IP/DNS blocks, patch/fix
     vulnerabilities, update scans/signatures/rules, segmentation-based
     controls, application approved list/MDM/DLP, revoke certificate.
4. **Eradication** (Source: Pt6 p.38) — removal of malware/artifacts from
   impacted systems, removal of the system from the network, or other
   mitigation. An incident is **not** fully eradicated until all machines
   exhibiting known network/host-based indicators have been identified.
   Once eradicated, a thorough analysis can take place if needed — severity
   and complexity determine the depth of analysis (targeted vs. non-targeted).
5. **Recovery** (Source: Pt6 p.39) — retrieving data, repairing systems,
   re-enabling servers/networks, returning impacted systems to operation.
   Full recovery can be slow and should: confirm the threat is completely
   mitigated before systems go back online, implement defensive measures
   against recurrence, and monitor to confirm no further attacks/symptoms.
6. **Lessons Learned** (Source: Pt6 p.40) — reviewing the scenario to define
   what went wrong and why. Document the process, make changes to prevent
   recurrence, calculate damage/loss and share with other departments,
   monitor affected systems for repercussions, update training requirements
   and re-evaluate tools/practices.

**Exam-relevant note (not from slides, general knowledge):** CompTIA's
official phase list in the objectives/common study materials is usually
given as *Preparation, Detection, Analysis, Containment, Eradication,
Recovery, Lessons Learned* (sometimes shown as 7 steps with
Detection+Analysis split out, matching the divider slide's "Process" list on
p.24) — be ready for either a 6-phase or a Detection/Analysis-split framing
in practice questions; the course's own phase-numbered slides (1-6) treat
Identification as the single "detect & analyze" phase.

## Supporting topics within 4.8

### Frameworks (Source: Pt6 p.27)
- **MITRE ATT&CK** — knowledge base of adversary tactics, techniques, and
  procedures (TTPs), referenceable globally.
- **Diamond Model of Intrusion Analysis** — analyzes an intrusion event via
  four core features/vertices: adversary, capability, infrastructure,
  victim.
- **Cyber Kill Chain** (Lockheed Martin) — stages a threat actor progresses
  through during a network intrusion: Reconnaissance → Weaponization →
  Delivery → Exploitation → Installation → Command & Control →
  Actions on Objectives.

### SOAR, Runbooks, and Playbooks (Source: Pt6 p.28)
- **SOAR** (Security Orchestration, Automation, and Response) — automation
  is scripting a *single* activity; orchestration is coordinating *multiple*
  automations for a complex task.
- **Playbook** — a data-driven SOP to assist junior analysts in detecting
  and responding to specific threat scenarios (e.g., phishing, SQL
  injection exfiltration, connection to a blacklisted IP range).
- **Runbook** — an *automated* version of a playbook that still leaves
  clearly defined interaction points for human analysis.

### Incident Response Personnel (Source: Pt6 p.29)
- **CSIRT / CIRT / CERT** — the group that prepares for and responds to
  emergency incidents.
- **First Responder** — first person on scene; responsible for controlling
  damage/loss of evidence (secure physical media, request log copies,
  photograph screens and hardware before removal).
- **Escalation and Notification** — raising incident awareness to other
  groups; response should map to the incident's actual scope/risk level.

### Root Cause Analysis (Source: Pt6 p.42)
Determines the underlying weakness/vulnerability that allowed the incident.
Without it, recovered systems may still contain the exploited weakness —
**the incident could be repeated.** Rebuilding from already-compromised
backups/snapshots is called out as a specific risk.

### Training and Testing (Source: Pt6 p.41)
Validates preparation and organizational readiness. Lessons learned may
surface a need for more training. Incident response often needs
cross-departmental coordination, so cross-departmental training matters.
Test types: **tabletop exercise**, **walkthrough**, **simulation**.

### Threat Hunting (Source: Pt6 p.43)
A proactive assessment technique using threat-intelligence insights to
discover whether TTP evidence already exists in the network/system.
- **Intelligence Fusion and Threat Data** — SIEM + threat analytics used to
  build queries/filters correlating threat data against on-prem network/log
  data.
- **Threat Feeds** — collecting network/log data from multiple sources and
  automating fusion with IoC/threat intelligence data.
- **Advisories and Bulletins** — correlating IoCs against vendor advisories
  to connect a hypothesis of possible threat.
- **Maneuver** — attackers deploying countermeasures to frustrate detection
  and accelerate their goals.

### Digital Forensics (Source: Pt6 p.44, p.45, p.46, p.47, p.48, p.49)

Digital forensics is the practice of collecting evidence from computer
systems to a standard acceptable in a court of law.

- **Legal Hold** — process preserving all relevant information when
  litigation is reasonably expected.
- **Acquisition** — obtaining a forensically clean copy of data from a
  device seized as evidence.
- **Reporting** — summarizes significant contents of digital data and the
  investigator's conclusions.
- **Preservation of Evidence** — host devices/media from the scene labeled,
  bagged, sealed with tamper-evident bags; each item documented via a chain
  of custody form and stored securely.
- **E-Discovery** — discovering electronic data, securing it within legal
  bounds, then analyzing it toward conclusions usable in criminal/civil
  litigation.

**Evidence admissibility criteria** (Source: Pt6 p.45) — for digital
evidence to be considered in court it must be: **Authentic**, **Accurate**,
**Complete**, **Convincing**, **Admissible**.

- **Interviews** — open-ended questions, witness supplies the evidence;
  conducted at office/home/workplace/crime scene.
- **Interrogations** — intent is extracting confessions where police already
  have other concrete evidence; typically in a law-enforcement/correctional
  setting.

**Order of Volatility (OOV)** (Source: Pt6 p.46) — acquire evidence before
it disappears/is overwritten; collect in this priority order:
1. CPU registers and cache memory
2. Routing tables, ARP cache, process tables, kernel statistics
3. Live network connections and data flows
4. Memory (RAM)
5. Temporary file system (swap space/paging files)
6. Data on hard disk/OS (config/apps/files/registry)
7. Remotely logged and monitored data
8. Data stored on archival media/backups/snapshots

**Data Acquisition techniques** (Source: Pt6 p.47): review network traffic
captures/logs (e.g., Wireshark), capture screenshots, capture video (note:
CCTV may record in local time zone), record time offset (difference between
a video timestamp and current local time), capture system images (full hard
drive image, then hashed to verify integrity), forensic copy (bit-by-bit
copy with hashing, typically made using a **write blocker** to prevent
writing to the source drive).

**Chain of Custody (CoC)** (Source: Pt6 p.49) — chronological documentation/
paper trail of seizure, custody, control, transfer, analysis, and
disposition of evidence. Critical steps: record each item collected; record
who collected it plus date/time; write a description; tag containers with
case number/collector name/date-time; record hash values; securely
transport to protected storage; obtain a signature from whoever accepts it
at the storage facility; control access to prevent compromise while stored;
securely transport to court for proceedings. **Goal: preserve the integrity
of evidence.**

**Digital Forensics Software** (Source: Pt6 p.48): **EnCase** (case
management, Guidance Software), **FTK/Forensic Toolkit** (AccessData;
free FTK Imager version exists), **The Sleuth Kit** (open-source
command-line disk imaging/file analysis; **Autopsy** is its GUI front-end),
**WinHex** (X-Ways; binary/memory-dump recovery and analysis), **Volatility**
(RAM forensic framework), **Memdump** (Linux, Coroner's Toolkit, dumps
system memory to a file), **dd** (converts/copies a file) and **dcfldd**
(enhanced `dd` from the DoD Digital Forensic Lab, can hash source-disk data
on the fly).

### Investigation support tooling mentioned in this section
(Note: these command-line/platform tools appear within the 4.8 slide range,
supporting identification/threat-hunting/forensics work. They overlap
conceptually with sub-objective 4.9 "data sources to support an
investigation," which begins immediately after this section at Pt6 p.50 —
flagged here for awareness, not claimed as 4.9 coverage.)

- **Network Discovery Tools** (Source: Pt6 p.31-33): tracert/traceroute,
  nslookup/dig, ping, pathping/mtr, netstat, arp, route, ipconfig/ifconfig,
  hping, nmap, netcat ("Swiss Army Knife" — banner grabbing, port scanning,
  fingerprinting, reverse shell, exfiltration, open listening port),
  ipscanners, cURL, theHarvester (OSINT gathering), sn1per (pentest
  reporting/evidence), scanless (3rd-party-relayed port scans to evade
  detection), dnsenum (DNS record enumeration incl. zone transfer attempts),
  Nessus (commercial vulnerability scanner, Tenable), Cuckoo (sandboxed
  malware analysis).
- **File Manipulation Tools** (Source: Pt6 p.34): head, tail, cat, grep,
  chmod, chown, logger (writes input to local/remote syslog).
- **Logging Platforms** (Source: Pt6 p.35): syslog, rsyslog/syslog-ng
  (TCP + secure comms), journalctl (reads the systemd `journald` binary
  log), NXLog (Windows log normalization to syslog format, XML-based).
- **Shell and Script Environments** (Source: Pt6 p.36): PowerShell, Python,
  Bash, OpenSSL, SSH, Macros (VBA in Office, JavaScript in PDFs), VBA.

## Confidence notes

- High confidence: all definitions, phase content, and forensics/evidence
  material — directly transcribed from clearly legible text slides, each
  individually read via vision.
- The six numbered phase slides (Preparation/Identification/Containment/
  Eradication/Recovery/Lessons Learned) are unambiguous and well-suited to
  ordering-style PBQ questions.
- One judgment call flagged above (not from the slides): whether an exam
  question expects 6 phases or a 7-step Detection/Analysis split — both
  framings are defensible from this course's own material and should be
  cross-checked against an external source (e.g., Professor Messer) before
  being treated as settled.

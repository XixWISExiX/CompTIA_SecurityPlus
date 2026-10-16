# Glossary

Concise cross-domain term reference. Each entry links back to the detailed
`course-unit-notes/` file where the concept is actually explained. This file
is seeded incrementally as units are validated — it is not a restatement of
the full acronym list (see the official objectives document for that); it
exists for terms that benefit from a short, plain-language definition across
domains.

## Incident response & digital forensics

_From [04-security-operations/incident-response-activities.md](../course-unit-notes/04-security-operations/incident-response-activities.md) (sub-objective 4.8, validated)._

- **Incident** — a violation, or imminent threat of violation, of computer
  security policies, acceptable use policies, or standard security
  practices (distinct from an **Event**, which is any observable
  occurrence, or an **Adverse Event**, an event with a negative
  consequence).
- **Incident Response Phases** — Preparation → Identification →
  Containment → Eradication → Recovery → Lessons Learned.
- **Chain of Custody (CoC)** — the chronological documentation/paper trail
  of an evidence item's seizure, custody, control, transfer, analysis, and
  disposition; exists to preserve evidence integrity for legal proceedings.
- **Order of Volatility (OOV)** — the priority order for collecting digital
  evidence before it's lost, from most volatile (CPU registers/cache) to
  least (archival media/backups).
- **SOAR (Security Orchestration, Automation, and Response)** — automation
  scripts a single activity; orchestration coordinates multiple automations
  into one complex task. A **Playbook** is the human-readable SOP; a
  **Runbook** is its automated version with defined human checkpoints.
- **Root Cause Analysis** — determining the underlying vulnerability that
  allowed an incident; skipping it risks recovering systems that still
  contain the weakness that caused the incident in the first place.

## Computing resource security (4.1)

_From [04-security-operations/computing-resource-security-techniques.md](../course-unit-notes/04-security-operations/computing-resource-security-techniques.md) (sub-objective 4.1 — extracted, NOT fully validated; treat as provisional)._

- **Secure baseline** — configuration guides/benchmarks defining the minimum security level a system must meet for its role (Pt4 p.90). **Hardening** — reducing attack surface by changing defaults, disabling unneeded services, patching (Pt4 p.91).
- **MDM / MAM / UEM / EMM** — device-level / app-and-data-level / all-endpoint-types management; EMM is the umbrella class (Pt4 p.96).
- **BYOD / COBO / COPE / CYOD / VDI** — employee-owned / company-owned business-only / company-owned personally enabled / company-owned employee-chosen / VM reachable from any personal device (Pt4 p.100).
- **Site survey / heat map** — measuring signal strength and channel use to build a wireless coverage map (Pt4 p.95).
- **WEP → WPA → WPA2 → WPA3** — RC4 / RC4+TKIP / AES-CCMP / AES-GCMP; WPA3-Personal uses SAE instead of PSK (Pt5 p.7-10).
- **RADIUS vs TACACS+** — RADIUS: connectionless, UDP 1812 (auth) / 1813 (accounting); TACACS+: Cisco, TCP port 49, separates AAA, encrypts the whole packet (Pt5 p.12-13). **Diameter** is RADIUS's successor (Pt5 p.12).
- **PAP / CHAP** — clear-text two-way handshake / challenge-response, one-way (not mutual) (Pt5 p.14).
- **SAST vs DAST** — static (source/binary, non-running, white-box) vs dynamic (running app, black-box) testing (Pt5 p.20).
- **Input validation / output encoding / normalization** — reject bad input / re-encode for context / strip illegal characters (Pt5 p.17).
- **Secure / HttpOnly / SameSite cookie attributes; HSTS; CSP** — Pt5 p.18.
- **Code signing** — digital signature proving code integrity and publisher identity (Pt5 p.21). **Sandboxing** — isolating running processes (Pt5 p.22).

## Asset management (4.2)

_From [04-security-operations/asset-management.md](../course-unit-notes/04-security-operations/asset-management.md) (sub-objective 4.2, validated)._

- **Acquisition/procurement** — policies ensuring purchases and contracts are managed, secure, use authorized vendors (Pt5 p.25).
- **Asset ownership vs. classification** — who is accountable for an asset vs. organizing assets by value/sensitivity/criticality (Pt5 p.26).
- **Enumeration / inventory / CMDB** — ways to find and list assets: manual, network scan, asset software, CMDB, MDM, cloud discovery; tracked with asset tags, RFID, GPS (Pt5 p.27).
- **Sanitization vs. destruction vs. certification** — remove data so it cannot be recovered / physically or electronically eliminate the media / document it with a certificate from a reputable third party (Pt5 p.28).
- **Data retention** — keeping and controlling data to meet policy and legal requirements (Pt5 p.28).
- **Overwriting, degaussing, pulverizing, pulping, incinerating; ATA Secure Erase (SSD)** — media sanitization/destruction methods (Pt5 p.29).

## Vulnerability management (4.3)

_From [04-security-operations/vulnerability-management.md](../course-unit-notes/04-security-operations/vulnerability-management.md) (sub-objective 4.3, validated)._

- **Vulnerability scan vs. penetration test** — a scan reports weaknesses and does not exploit them; a pen test mimics real attacks and actively exploits, with the owner's written consent (Pt5 p.32, p.39).
- **Scan types** — active (intrusive / non-intrusive), credentialed vs. non-credentialed, compliance (Pt5 p.33).
- **Static vs. dynamic analysis; package monitoring** — review code without running it / observe it running / track third-party libraries and the SBOM (Pt5 p.34).
- **True/false positive/negative** — alarm vs. actual event: TP alarm+event, TN neither, FP alarm without event, FN event without alarm (Pt5 p.42).
- **CVE / CVSS** — CVE-YYYY-#### identifier dictionary (Mitre); CVSS 0-10 criticality score maintained by FIRST (Pt5 p.43).
- **IoC, AIS, STIX, TAXII** — evidence of an attack / DHS indicator-sharing service / syntax for describing CTI / protocol for transmitting it (Pt5 p.36).
- **Deep web vs. dark net vs. dark web** — unindexed content / overlay network such as Tor / sites reachable only over a dark net (Pt5 p.38).
- **Responsible disclosure and bug bounty** — safe vulnerability reporting / paid crowdsourced reporting (Pt5 p.40).
- **Exposure factor, environmental variables, risk tolerance** — susceptibility of an asset / local configuration factors that change risk / how much risk the organization accepts (Pt5 p.41).
- **Remediation options** — patching, insurance, segmentation, compensating controls, exceptions/exemptions (Pt5 p.44). **Validation of remediation** — rescanning, audit, verification (Pt5 p.45).

## Alerting and monitoring (4.4)

_From [04-security-operations/alerting-and-monitoring.md](../course-unit-notes/04-security-operations/alerting-and-monitoring.md) (sub-objective 4.4, validated)._

- **Log aggregation / alerting / scanning / reporting / archiving** — consolidate logs / real-time notification / actively check / managerial status view / retain history for a defined period (Pt5 p.49).
- **Alert tuning vs. quarantine vs. validation** — reduce false positives and low-priority alerts / isolate the source of indicators / decide if an alert is a true positive (Pt5 p.49).
- **SCAP, OVAL, XCCDF, NVD** — NIST framework for automated scanning; OVAL describes system state, XCCDF is a machine-readable checklist format; NVD maintains the feed (Pt5 p.50). **Benchmark** — configuration best practices for one app or control (Pt5 p.50).
- **Agent-based vs. agentless (listener/collector, sensor)** — host agent forwards filtered logs to the SIEM / appliance collects logs from switches, routers, firewalls / sniffs frames via mirror port or TAP (Pt5 p.51).
- **SIEM** — real-time analysis of alerts; aggregation, correlation, time sync, de-duplication, WORM storage (Pt5 p.52).
- **DLP** — detects and prevents sensitive data on unauthorized systems or networks (Pt5 p.53).
- **SNMP trap** — agent-initiated notice of a notable event; queries on UDP 161, traps on UDP 162 (Pt5 p.54).
- **NetFlow / sFlow / IPFIX** — flow-record reporting: Cisco / HP sampling at any OSI layer / IETF standard NetFlow-based (Pt5 p.55).
- **Vulnerability scanner types** — network, application, web application (Pt5 p.56).

## Enterprise security capabilities (4.5)

_From [04-security-operations/enterprise-security-capabilities.md](../course-unit-notes/04-security-operations/enterprise-security-capabilities.md) (sub-objective 4.5, validated)._

- **Explicit allow / implicit deny** — a rule that permits specific traffic / deny everything not allowed; the implicit deny is the last rule in a top-down firewall ACL (Pt5 p.59).
- **Port ranges** — well-known 0-1023, registered 1024-49151, private/dynamic 49152-65535 (Pt5 p.60). Common ports table: Pt5 p.61.
- **Secure vs. unsecure pairs** — Telnet/rlogin/rsh/rexec → SSH; HTTP → HTTPS; FTP/TFTP → SFTP/FTPS; SNMPv1/v2 → SNMPv3 (Pt5 p.77). LDAP 389 → LDAPS 636 (Pt5 p.68).
- **DNSSEC / split DNS / zone-transfer blocking** — signed responses (authentication + integrity, no confidentiality) / separate internal and external DNS / block TCP 53 transfers (Pt5 p.64).
- **DMZ (screened subnet)** — semi-trusted buffer zone between the Internet and the internal network; hosts web, email, remote-access servers and honeypots (Pt5 p.69).
- **Behavior-, anomaly-, signature-based detection** — IDS/IPS methods; behavior/anomaly can catch zero-days but may produce false positives; signature is fast and precise but needs accurate signatures (Pt5 p.70-71). Snort, Suricata, Security Onion (Pt5 p.72).
- **Web filter types** — agent-based, centralized proxy, URL scanning, content categorization, block rules, reputation-based (Pt5 p.73). **DNS filtering** — block unapproved sites via DNS (Pt5 p.78).
- **SPF / DKIM / DMARC / SEG** — authorized senders / signed mail via a public key in DNS / policy that applies SPF+DKIM results and reports / inline email control point (Pt5 p.79).
- **FIM, DEP** — detect tampering with system files (Tripwire, OSSEC, SFC) / block code execution from non-executable memory (Pt5 p.80, p.82).
- **DLP types** — endpoint (data in use), network (in motion), storage (at rest), cloud-based (Pt5 p.81).
- **NAC** — host health check before network access; permanent vs. dissolvable agent (Pt5 p.83).
- **EDR / XDR / UEBA** — endpoint agent / extended to network, cloud, email, firewall / behavior analytics (Pt5 p.84).
- **Group Policy, Local Policy, SELinux (MAC) vs. DAC, hardened OS / bastion host** — Pt5 p.76.

## Identity and access management (4.6)

_From [04-security-operations/identity-and-access-management.md](../course-unit-notes/04-security-operations/identity-and-access-management.md) (sub-objective 4.6, validated)._

- **Provisioning / de-provisioning** — deploy an account with identity proofing, credentials, assets, policy awareness and permissions / remove it and revoke privileged access (Pt5 p.87-88).
- **Federation, SSO, FIM** — shared login across organizations / authenticate once for many services / identity attributes shared across systems (Pt5 p.92).
- **LDAP / LDAPS** — plaintext directory protocol (X.500 subset, AD) / over SSL/TLS (Pt5 p.93).
- **OAuth vs. OIDC vs. SAML** — token-based delegated authorization / identity layer on OAuth 2.0 / XML-based SSO between an identity provider and a service provider (Pt5 p.94, p.96). **SOAP vs. REST** — XML-only strict protocol / looser style using HTTP verbs (Pt5 p.95).
- **Attestation** — proving a device or module is a trustworthy platform (root of trust) (Pt5 p.97).
- **MAC / DAC / RBAC / RuBAC / ABAC** — labels and clearances / owner decides / by job role / admin-set if-then rules (ACLs) / policy combining attributes, the most fine-grained (Pt5 p.98-100, Pt6 p.1-2).
- **Context-aware restrictions** — time-of-day, computer, location; **need to know, least privilege, privilege creep** (Pt6 p.3).
- **MFA factors** — know, have, are, somewhere you are, something you do (Pt6 p.4).
- **FAR / FRR / CER (EER)** — false accept / false reject / the crossover point, ideally low (Pt6 p.5).
- **Hard vs. soft token; smart card; security key; TOTP vs. HOTP** — hardware cryptoprocessor token / OTP via app, SMS or email / PKI card with PIN / USB or NFC U2F key using a key pair / time-limited code vs. HMAC-based code (Pt6 p.6-8).
- **Password controls** — length, complexity, age/expiration, reuse, history, threshold/clipping level (Pt6 p.9).
- **Password manager / vault / key** — Pt6 p.10, p.13. **Passwordless SSH** — public key in `~/.ssh/authorized_keys` (Pt6 p.11).
- **JIT access vs. JIT provisioning; ephemeral credentials** — time-limited access / create the account at first SAML login / credentials created when needed and discarded (Pt6 p.12, p.14).
- **chmod/chown** — Linux permission commands; r=4, w=2, x(e)=1; `chmod 760` = rwx / rw- / --- (Pt5 p.91).

## Automation and orchestration (4.7)

_From [04-security-operations/automation-and-orchestration.md](../course-unit-notes/04-security-operations/automation-and-orchestration.md) (sub-objective 4.7, validated)._

- **Automation / scripting** — scripts and APIs that provision and deprovision without manual steps; consistent, compliant, fewer errors (Pt6 p.17).
- **Use cases** — user and resource provisioning, guardrails (prevent or flag risky activity), security groups, automatic ticketing and escalation, enabling/disabling services (Pt6 p.17-18).
- **CI / CD / continuous deployment / continuous monitoring / continuous validation** — rapid tested commits / always releasable / commits to production / constant environment evaluation (CSM) / V&V: verification meets design goals, validation is fit-for-purpose (Pt6 p.19).
- **Workforce multiplier** — automation that lets staff do more tasks to the same standard per unit of time (Pt6 p.20). **Reaction time** — time from incident to response (Pt6 p.20).
- **Enforcing baselines / standard configurations / configuration drift** — configuration management overrides unauthorized changes (Pt6 p.20).
- **Drawbacks** — complexity, cost, single point of failure, technical debt, ongoing support (Pt6 p.21).
- **DevSecOps** — development, security and systems operations integrated; security baked into rapid releases (Pt6 p.22).

## Data sources for investigations (4.9)

_From [04-security-operations/data-sources-for-investigation.md](../course-unit-notes/04-security-operations/data-sources-for-investigation.md) (sub-objective 4.9, validated)._

- **Log data** — automatic event records: troubleshooting, an audit trail, and warning of suspicious activity; logs and their configuration should be tamperproof (Pt6 p.52).
- **Metadata** — properties of an object, system state or transaction; file date/time and security attributes, web request/response headers, email Internet headers (message transfer agents) (Pt6 p.52).
- **Syslog** — protocol and format for sending logs to a central server over UDP 514; PRI (facility + severity), HEADER (timestamp, host, app, process ID, message ID), MSG (Pt6 p.52).
- **Application / endpoint / OS logs** — app-managed logs / events from host malware and intrusion agents / Windows Event Viewer (Application, Security, System), Linux syslog vs journald, macOS Unified Logs (Pt6 p.53).
- **Network, firewall, IPS/IDS logs** — appliance traffic and access events / rule-triggered events with timestamp, interface, ingress/egress, accept/drop / traffic pattern matched to a rule (Pt6 p.54).
- **Vulnerability scans, automated reports, dashboards (analyst vs manager), packet captures** — Pt6 p.55.

## Threat actors and motivations (2.1)

_From [02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md) (sub-objective 2.1, validated)._

- **APT (Advanced Persistent Threat)** — state-sponsored/nation-state actors: advanced = targeted, coordinated, purposeful; persistent = month after month; threat = intent, opportunity, capability (Pt2 p.29).
- **Hacktivist / criminal syndicate / competitor** — hacking for a cause (DoS, defacement, leaks) / organized criminals or terrorist groups, financially driven, cross-jurisdiction (ransomware) / corporate espionage (Pt2 p.29).
- **Insider threat** — current or former employee, contractor or partner who had authorized access and misused it (Pt2 p.29). **Shadow IT** — hardware or software introduced without IT approval or a security analysis (Pt2 p.29).
- **Unskilled attacker (script kiddie)** — little skill; uses code written by others (Pt2 p.29).
- **White / gray / black hat; ethical hacker** — authorized tester / may break the law but tells the admin / malicious and unauthorized; an ethical hacker is a white hat with the owner's permission (Pt2 p.30).
- **TTPs** — tactics (campaign strategy), techniques (generalized attack vectors), procedures (specific tools and methods) (Pt2 p.31).
- **Intent vs. motivation** — what the attacker hopes to achieve vs. the reason behind the attack (greed, curiosity, grievance) (Pt2 p.32).

## Threat vectors and attack surfaces (2.2)

_From [02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md) (sub-objective 2.2, validated)._

- **Threat vector groups (slide)** — vulnerable software; message-based; lure-based (USB, executable, document, image files); network-based (direct access, wired, remote/wireless, cloud, Bluetooth, default credentials, open service port) (Pt2 p.35).
- **WPS** — Wi-Fi Protected Setup; the eight-digit PIN could be brute-forced (Pt2 p.36). **AP isolation** — wireless clients segmented, can't talk to each other (Pt2 p.36). **Ad hoc network** — wireless links without a central WAP/WLAN controller (Pt2 p.36). **War-chalking** — marking a location to signal a vulnerable WAP (Pt2 p.36).
- **Rogue access point** — unauthorized WAP giving access to secure networks; detect with site surveys, NIDS/NIPS, device accountability audits (Pt2 p.37).
- **Bluejacking / bluesnarfing** — unsolicited messages to a Bluetooth device / unauthorized access or theft of its information (Pt2 p.38).
- **Default credentials / misconfiguration** — admin/admin etc.; also unused open ports, HTTP instead of HTTPS, unused running services (Pt2 p.39).
- **Supply chain; MSP; supplier; vendor; business partner** — end-to-end design/manufacture/distribution; outsourced IT provider; bulk seller from manufacturer; sells finished products; closely aligned partner (Pt2 p.40).
- **Social engineering** — manipulation of the natural human tendency to trust; slide: only defense is user training and awareness (Pt2 p.41).
- **SPAM / SPIM / SPIT / SMiShing** — unsolicited email / via IM or chat / via Internet telephony / phishing by SMS (Pt2 p.42).
- **Phishing / spear phishing / whaling / vishing / quishing** — fake legitimate-source email or web notice / targeted users or groups / targets executives ("big fish") / by telephone / via QR codes (Pt2 p.43).
- **Pretexting, authority, intimidation, impersonation, consensus/social proof, scarcity, urgency, familiarity/liking, trust** — the slide's social-engineering principle list (Pt2 p.44).
- **Shoulder surfing; dumpster diving; electronic dumpster diving; Google dorking** — reading a screen over a shoulder / discarded materials / search engines for posted documents / customized Google search strings (Pt2 p.45).
- **Hoax; typosquatting** — fake-virus warning email / malicious content on common-typo domains (slide pairs it with "bit flipping") (Pt2 p.46).
- **Misinformation vs. disinformation** — false claims repeated without intent to deceive / falsifying a normally trusted information resource with purposeful intent (Pt2 p.47).
- **Business email compromise (BEC)** — attacker controls an employee's account to push others into fraud, e.g. a fraudulent wire transfer (Pt2 p.48).
- **Watering hole attack** — infect sites a target group typically visits to reach the organization's network (Pt2 p.49).
- **Brand impersonation (brand spoofing)** — phishing that poses as a legitimate brand using its logos, formatting and tone (Pt2 p.50).

## Types of vulnerabilities (2.3)

_From [02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md) (sub-objective 2.3, validated)._

- **Memory injection** — injecting malicious code into a running application's process memory; includes buffer overflow, format string, code injection; mitigations: secure coding, input/output validation, encoding, type-casting, access controls, static/dynamic testing (Pt2 p.53).
- **Buffer / buffer overflow / object-pointer dereference** — memory the app reserves for expected data / writing more than it can handle, can crash or run arbitrary code with system/root privileges / overwriting the return address to point at shellcode (Pt2 p.54-55).
- **Pivot / lateral movement** — using an exploited machine to attack other systems and their data (Pt2 p.56).
- **Race condition; TOC/TOU** — outcome depends on event order/timing / a resource changes between the check and the use, giving a brief window to manipulate data (Pt2 p.57).
- **Malicious update** — a legitimate-looking update with harmful code via a software repository or supply chain; CCleaner (2017), SolarWinds Orion (2020) (Pt2 p.58).
- **OS-based examples** — MS08-067/Conficker; MS17-010 (SMB) EternalBlue/WannaCry; Shellshock (Bash); Stagefright (MMS); iOS watering hole (2019); Heartbleed (OpenSSL) (Pt2 p.59).
- **OWASP** — web-application security standards; Top 10 list (Pt2 p.60).
- **SQL injection (SQLi)** — server-side attack manipulating back-end databases; a single quote is the test character; `' or 1=1` style input returns every row (Pt2 p.61-63).
- **XSS (cross-site scripting)** — client-side attack injecting script that executes in a victim's browser; stored (persistent) vs. reflected (non-persistent); mitigation shown: replace `<` with `&lt;` and `>` with `&gt;` (Pt2 p.64-69).
- **CSRF/XSRF** — tricks a browser into an unwanted action on a trusted site where the user is authenticated; "session riding", "one-click attack" (Pt2 p.70-71).
- **EOL / EOSL** — manufacturer discontinues sales and support becomes limited / legacy system no longer supported or receiving security updates (Pt2 p.72).
- **VM escape; sandboxing; VM sprawl; resource reuse; intermingled network security controls** — guest malware reaching the hypervisor/host or other guests / restricted memory areas / uncontrolled growth of virtual systems / data recoverable from previously used resources / admin tools lacking network-control granularity (Pt2 p.73).
- **Cloud bursting / spillage** — hybrid cloud lets public-cloud vulnerabilities affect private systems; data migration raises spillage risk (Pt2 p.74).
- **Supply chain: service / hardware / software provider; SBOM** — Software Bill of Materials = inventory of all components and dependencies (names, versions, suppliers) (Pt2 p.75).
- **Cryptographic vulnerabilities** — social engineering of the key holder; deprecated algorithms (DES, SHA-1); improper implementation (weak choices, exposed private keys, MD5/SHA-1 collisions, DES 56-bit, 3DES Sweet32, weak RSA keys/RNG/reuse) (Pt2 p.76).
- **Heartbleed; KRACK; BEAST; POODLE** — OpenSSL memory disclosure (64k chunks) / WPA2 key reinstallation / attacks on SSL and early TLS cipher suites (Pt2 p.77).
- **Sideloading / jailbreaking / rooting** — installing apps without the store signing process; Android = rooting, iOS = jailbreaking (Pt2 p.78).
- **Zero-day** — vulnerability unpatched by the developer, or an attack exploiting it; slide examples EternalBlue/WannaCry and the Stuxnet worm (Pt2 p.79).


## Indicators of malicious activity (2.4)

_From [02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md) (sub-objective 2.4)._

- **Virus vs. worm** — a virus replicates *on* the host by attaching to executable code, usually with human interaction; a worm self-replicates *between* computers with no user interaction.
- **Polymorphic vs. metamorphic virus** — polymorphic rewrites its code every time it executes; metamorphic rewrites its code after it infects a new file.
- **Fileless / Living off the Land (LotL)** — malware that does not write code to disk and abuses a system's own native tools to evade detection.
- **Trojan / RAT** — software that hides malicious functionality; a Remote Access Trojan is the most common type and gives the attacker remote control. A *wrapper/binder* bundles a Trojan with a legitimate application.
- **Backdoor / maintenance hook** — a program that bypasses normal authentication; a maintenance hook is one installed by a developer/vendor.
- **Rootkit** — malware that gains admin-level control without detection; types: firmware, virtual, kernel, library, application.
- **Spyware / keylogger** — spyware tracks users without consent; a keylogger records keystrokes (physical device or software).
- **Grayware / PUP / adware / bloatware** — software between malware and legitimate; adware pushes unwanted ads; bloatware is unwanted pre-installed software.
- **Malvertising / ad fraud (Methbot)** — malware spread via third-party ad networks / robo-browser that spoofs ad auction interactions to redirect ad revenue.
- **Ransomware / scareware / crypto-malware** — ransomware encrypts data until a fee is paid; scareware only claims a threat exists (no encryption); crypto-malware encrypts every reachable file and escalates pressure.
- **Logic bomb** — dormant malware triggered by a pre-determined event; not the same as an Easter egg (benign undocumented feature).
- **RFID cloning / skimming** — copying a card, or capturing its details with a counterfeit reader to program a duplicate. NFC range is about 4 cm.
- **DoS attacks** — Ping of Death (oversized reassembled ICMP), Teardrop (overlapping IP fragments), SYN flood (exhaust open connections).
- **Botnet / bot herder / dead drop C&C** — bots under a herder's control; a dead drop uses unsent email drafts to pass commands.
- **DRDoS / amplification** — reflected DDoS using spoofed source IPs; amplification abuses protocols (DNS, NTP, CLDAP) where a small request yields a large response.
- **Smurf / Fraggle** — spoofed ICMP echo to a broadcast address / same idea using UDP.
- **ARP poisoning / MAC flooding** — corrupting an ARP table for MITM / filling the switch CAM table so it floods traffic like a hub.
- **DNS cache poisoning / pharming** — altering DNS cache (or the Hosts file) to redirect users to a malicious site.
- **Evil twin / jamming / deauthentication** — rogue WAP with the same SSID / radio interference / forced disassociation to capture the WPA handshake.
- **On-path (MITM) / man-in-the-browser / replay / TCP session hijacking** — interception attacks; replay re-sends captured data (credential, token, session ID, cookie replay).
- **SSL stripping / HSTS** — downgrading HTTPS to HTTP; HSTS is the countermeasure.
- **Credential dumping / DCSync / persistence** — taking credentials from SAM or lsass.exe / tricking a DC into replicating credentials / AutoRun keys, scheduled tasks, WMI subscriptions.
- **LDAP / XML / DLL injection** — manipulating directory queries / XPath queries / injecting into DLL calls (shimming, refactoring).
- **Clickjacking** — tricking users into clicking something other than what they see.
- **Vertical vs. horizontal privilege escalation** — to a higher privilege level / to another user at the same level.
- **Directory traversal** — "dot-dot-slash" (`../`) access to unauthorized directories.
- **Downgrade / birthday / collision attacks** — forcing a weaker protocol / exploiting the birthday paradox / two inputs producing the same hash.
- **Cryptanalytic attacks** — known ciphertext, known plaintext, chosen plaintext, chosen ciphertext.
- **Password attacks** — brute force, dictionary, rainbow table (defeated by *salting*), password spraying (one password across many accounts), pass the hash.
- **Indicators of compromise** — account lockout, concurrent session usage, blocked content, impossible travel, resource inaccessibility/consumption, out-of-cycle logging, published/documented (MITRE ATT&CK), missing logs.

## Mitigation techniques (2.5)

_From [02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md) (sub-objective 2.5)._

- **Segmentation / isolation** — dividing systems into segments (VLANs, subnets, enclaves) with distinct controls; isolation removes or severely restricts communication paths to a device.
- **VLAN** — logically separate Layer 2 broadcast domain on a switch; unused ports can go to an isolated empty VLAN.
- **Intranet / extranet / DMZ** — internal-only resources / controlled access for outside organizations / semi-trusted zone between outer and inner firewalls.
- **ACL: whitelist vs. blacklist** — implicit deny/explicit allow vs. explicit deny/implicit allow.
- **Patch categories** — patch, hotfix (urgent), security update, critical update, service pack, Windows Update, driver update.
- **FDE / removable media / VPN / email encryption** — BitLocker/FileVault; SD/USB; secure tunnel; PGP and S/MIME.
- **Sensors and collectors** — sources of monitoring data vs. SIEM/syslog consoles (SIEM correlation engine).
- **Least privilege / least functionality** — minimum access needed / system configured to do only its intended function.
- **Configuration enforcement** — baselines, automated configuration tools, continuous monitoring/compliance checks, change and configuration management.
- **Decommissioning** — secure erase/overwrite, factory reset, update inventory records.
- **System hardening** — configuring for the most secure state: disable unneeded protocols/services/ports (Telnet, NetBIOS, IPX, FTP; ECHO, CHARGEN), remove unneeded software/shares, host firewall/HIPS, secure BIOS/UEFI, manage remote interfaces (SSH over Telnet, secure/disable SNMP).

_More entries will be added as additional units are validated — this is not
yet a complete cross-domain glossary._

## Security governance (Domain 5)

_From [05-security-program-management-and-oversight/effective-security-governance.md](../course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md) (sub-objective 5.1, validated)._

- **Policy / Standard / Procedure / Guideline / Baseline** — slide pyramid: policy, procedure, and standard are Mandatory; guideline is Recommendations; baseline is Discretionary. Policy = high-level strictly enforceable ruleset; standard = expected outcome/method derived from policy; procedure = step-by-step instructions; guideline = flexible best-practice advice.
- **AUP (Acceptable Use Policy)** — defines acceptable user behavior on network/computer systems; employees acknowledge by signature.
- **Mandatory vacations / Job rotation / Separation of duties / Clean desk** — personnel/physical policies used to detect fraud, reduce collusion and single points of failure, prevent one person causing catastrophic damage, and limit exposed data.
- **BCP / CoOP / DRP** — BCP keeps critical processes running through a disruption; CoOP is BCP for a government agency; DRP is recovery/rebuilding after a disaster (protects human life, tested periodically).
- **SDLC phases (slides)** — Development, Test/Integration, Staging (mirror of production), Production.
- **Governance structures** — Board (executives, strategy), Committee (SMEs, specific domain), centralized vs decentralized vs hybrid.
- **Data roles** — Owner (accountable, classification/access), Controller (purposes and means of processing, GDPR), Processor (processes on controller's behalf, often a CSP), Custodian/Data Steward (safe custody, implements controls; usually IT).
- **Frameworks/standards named** — CIS Controls, NIST RMF (Prepare–Monitor), NIST CSF (Identify–Recover), ISO/IEC 27001/27002/27017/27018/27701/31000, NIST SP 800-63, FIPS, PCI-DSS (12 requirements, at least quarterly reviews).

## Risk management (Domain 5)

_From [05-security-program-management-and-oversight/risk-management-process.md](../course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md) (sub-objective 5.2, validated)._

- **Risk assessment types** — ad hoc (as needed, e.g., new zero-day), one-time (point in time), recurring (scheduled), continuous (real-time tools such as agent-based scanning, IDS).
- **Qualitative vs. quantitative analysis** — qualitative = subjective/expert judgment (Delphi = anonymous opinions); quantitative = objective/numeric from historical data and models.
- **SLE / ARO / ALE** — SLE = AV × EF; ALE = SLE × ARO (= AV × EF × ARO). Slide example: $200,000 facility × 50% = $100,000 SLE; ARO 0.10 → $10,000 ALE.
- **Risk register / KRI / risk owner / risk threshold** — document of risks, severity, owners, mitigations; KRI = predictive early-warning indicator; owner = person managing the risk; threshold = limit of acceptable risk.
- **Risk tolerance vs. appetite** — tolerance = acceptable variance around thresholds; appetite = strategic level of residual risk acceptable (expansionary / conservative / neutral).
- **Residual / inherent / control risk** — risk after controls / risk without controls / how much less effective a control has become over time.
- **Risk strategies** — acceptance (exception = short-term, exemption = longer-term per slides), avoidance, transference (insurance, third party, SLA), mitigation, deterrence (log-in banner).
- **BIA metrics** — MTD (= RTO + WRT), RTO (time to recover), RPO (tolerable data loss, measured in time), WRT, MEF, SPoF, MTBF (repairable), MTTF (non-repairable), MTTR (time to repair).

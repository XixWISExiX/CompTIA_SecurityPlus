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

## Security compliance (Domain 5)

_From [05-security-program-management-and-oversight/effective-security-compliance.md](../course-unit-notes/05-security-program-management-and-oversight/effective-security-compliance.md) (sub-objective 5.4, validated)._

- **Internal vs. external compliance reporting** — internal = operational detail for risk managers, executives, security analysts, privacy officers; external = regulatory/high-level summaries for customers, clients, regulators, vendors, partners.
- **SSAE / SOC 1-2-3** — AICPA attestation spec for cloud/hosting providers. SOC 1 = financial reporting controls; SOC 2 = detailed, NDA required, security/availability/confidentiality/processing integrity/privacy; SOC 3 = short, broad, general distribution. Type I = design of controls; Type II = ongoing effectiveness over 6-12 months.
- **Consequences of non-compliance** — fines, legal sanctions, reputational damage, license/usage-rights revocation, lawsuits, extra audits; contractually: breach, termination, indemnification/liability, penalties.
- **Attestation and acknowledgment** — formal signed agreements, policy acknowledgments, training sign-offs confirming understanding of compliance obligations.
- **Due diligence / due care / due process** — diligence = reasonable steps to satisfy legal requirement (assessment); care = mitigation actions on risks found in diligence; process = respecting personnel's rights.
- **GDPR** — EU/EEA personal data; informed consent required; data subjects may withdraw consent and inspect, amend, or erase data.
- **FISMA / HIPAA / SOX / GLBA** — federal agency security (annual reviews) / health information / financial reporting integrity in public companies / financial-institution consumer data.
- **Data subject / data owner / controller / processor** — subject = individual identified by the data; owner = senior executive accountable for CIA of an asset; controller = decides purposes and means; processor = processes only on controller's instructions. Organizations are custodians/stewards, not owners, of personal data.
- **Data inventory / data retention** — classified list of data held (drives retention periods); keep personal data only as long as needed or required by law.
- **Right to be forgotten (RTBF)** — right to erasure; data subject may request deletion (GDPR; also Argentina, Philippines).

## Audits and assessments (Domain 5)

_From [05-security-program-management-and-oversight/audits-and-assessments.md](../course-unit-notes/05-security-program-management-and-oversight/audits-and-assessments.md) (sub-objective 5.5, validated)._

- **Attestation** — formal declaration, by an independent qualified entity, that security controls comply with standards/regulations (Pt7 p.31).
- **Compliance assessment / audit committee / self-assessment** — internal: check practices against laws and policies / independent board members overseeing financial reporting, controls, and the external audit / internal personnel evaluate themselves against predetermined metrics (Pt7 p.32).
- **Regulatory / examination / assessment / independent third-party audit** — external: agency checks of legal compliance / formal evaluation by auditors or regulators / broad review by outside consultants / unbiased audit free of conflicts of interest (Pt7 p.33-34).
- **Internal vs. external vs. third-party audit** — own personnel / vendor or contractor engaged by the company / party unrelated and never engaged by the company (accreditation, auditing your auditors) (Pt7 p.35).
- **Penetration test** — authorized hacking that mimics a real-world threat to find and exploit weaknesses (Pt7 p.36).
- **Physical / offensive / defensive / integrated pen test** — physical controls / red teaming / ability to detect and respond / combined methodologies across systems, apps, and physical (Pt7 p.37).
- **Known / partially known / unknown environment** — white-box (full knowledge) / gray-box (partial) / black-box (zero). Blind (single-blind) = staff informed; double-blind = staff not told (Pt7 p.38).
- **Blue / red / white / purple team** — defenders / attackers / referee setting rules of engagement / red+blue collaboration (Pt7 p.39). **Yellow / orange / green** — builders / red+yellow / blue+yellow (Pt7 p.40).
- **Passive vs. active reconnaissance** — no traffic sent to target (OSINT, traffic analysis, war driving/flying, social engineering) vs. traffic sent to solicit responses (port scan, service enumeration, OS fingerprinting, DNS enumeration, web app crawling) (Pt7 p.41-42).
- **Banner grabbing** — query a service (netcat, nmap, telnet) to learn server software/version (Pt7 p.44).
- **Promiscuous mode** — NIC listens to all frames, not just those addressed to it; required for sniffing (Pt7 p.46).
- **Phishing campaign** — internal training exercise sending simulated phishing messages; users who respond get follow-up training (Pt7 p.49).
- **Anomalous behavior: risky / unexpected / unintentional** — threatens security (weak passwords, untrusted links) / violates policy or bypasses controls / no malicious intent but harmful (human error, falling for social engineering) (Pt7 p.50).
- **"If you see something, say something"** — insider-threat awareness slogan; report suspicious behavior (Pt7 p.51).
- **Role-based training / CBT / CTF / gamification** — training tailored to job role / computer-delivered (simulations, branching scenarios) / flag-capturing challenges, red vs blue / game mechanics (points, badges) applied to awareness (Pt7 p.54).
- **Initial vs. recurring (training) measurement** — immediate effect (pre/post quizzes, surveys) vs. long-term retention and sustained behavior change (Pt7 p.56).

## Security architecture models

_From [03-security-architecture/security-implications-of-architecture-models.md](../course-unit-notes/03-security-architecture/security-implications-of-architecture-models.md) (sub-objective 3.1, validated)._

- **Responsibility Matrix (Shared Responsibility)** — security responsibility split between customer and Cloud Service Provider; the customer manages more layers in IaaS than PaaS, and none of the stack in SaaS (Pt3 p.54-55).
- **IaaS / PaaS / SaaS** — customer manages OS and up / only applications and data / nothing (Pt3 p.54-55).
- **Hybrid / Community / Private / Multi-Cloud** — public+private combined / several organizations sharing costs / owned and operated by one organization / services from multiple CSPs (Pt3 p.56).
- **MSSP vs. SECaaS** — fully outsourced information-assurance responsibility vs. a single security control delivered from the cloud (Pt3 p.57).
- **CASB** — software that mediates access to cloud services; SSO and access control, malware scanning, monitoring, data-exfiltration prevention; deployed as forward proxy, reverse proxy, or API (Pt3 p.59).
- **Infrastructure as Code (IaC) / snowflake system** — scripted automation replacing manual configuration / a build unlike any other system, which IaC aims to eliminate (Pt3 p.60).
- **Serverless (FaaS), SOA, Microservices** — functions in cloud runtime containers with no server management / loosely coupled services / highly decoupled, independently deployable services (Pt3 p.60).
- **Air-gapped** — physically and logically isolated, no wired or wireless interfaces; slide calls it most secure (Pt3 p.61).
- **SDN: control / data / management plane** — decisions about traffic / actual forwarding and access-control enforcement / monitoring traffic and network status (Pt3 p.62).
- **Fog vs. Edge computing** — processing between IoT edge and data center to cut latency / servers and devices near the user or data origin (Pt3 p.63).
- **Port security: static / dynamic / sticky learning** — MAC defined in advance / learned on connect / learned and kept in persistent memory across reboots (Pt3 p.75).
- **Flood guard, STP, BPDU, DHCP snooping** — rate-based traffic limiting / loop-free switch topology / rogue-switch ("evil twin") attack per the slide / checks hosts are not spoofing MAC (Pt3 p.76).
- **Collision vs. broadcast domains** — switches break up collision domains; routers break up broadcast domains (Pt3 p.78).
- **NAT vs. PAT** — internal-to-external IP mapping at the firewall/router / also maps ports so many internal hosts share one external IP (Pt3 p.81).
- **TCP three-way handshake and flags** — SYN, SYN-ACK, ACK; ACK/FIN/PSH/RST/SYN/URG (Pt3 p.84-85).
- **Type I vs. Type II hypervisor** — bare metal on host hardware vs. hosted on top of the host OS (Pt3 p.90).
- **Container vs. VM** — containers share one engine and host OS; VMs each carry a guest OS (Pt3 p.91).
- **OT / ICS / SCADA** — network of embedded controllers vs. ICS that manages them vs. ICS for large, geographically spread sites (Pt3 p.94).
- **Embedded system constraints; PLC, SoC, FPGA, RTOS** — cost, power, compute, weak crypto/authentication, implied trust, range (Pt3 p.95); PLC readymade embedded controller, SoC single-die design, FPGA customer-programmable, RTOS deterministic real-time OS (Pt3 p.96).
- **Active-active vs. active-passive; fault tolerance; five nines** — load balancing / hot-spare failover / sustain operations through a component failure / 99.999% = 00:05:15 annual downtime (Pt3 p.97).
- **Local / regional / geo-redundant replication** — single data center / multiple datacenters in one or two regions (zone-redundant) / distant secondary region (Pt3 p.98).
- **Power events** — fault (momentary loss), blackout (complete loss), sag/dip (momentary low), brownout (prolonged low), spike (momentary high), surge (prolonged high) (Pt3 p.100).

## Securing enterprise infrastructure (3.2)

_From [03-security-architecture/security-principles-to-secure-enterprise-infrastructure.md](../course-unit-notes/03-security-architecture/security-principles-to-secure-enterprise-infrastructure.md) (sub-objective 3.2, validated)._

- **Fail-open (fail safe) vs. fail-closed (fail secure)** — logical: availability kept but data may be exposed / data secure but availability lost; physical: entrances unlocked, humans safe / entrances locked, access blocked (Pt4 p.4).
- **Security zone; attack surface; attack vector** — area with one security configuration for all hosts / points exposed to external input or connections / a specific path to unauthorized access (Pt4 p.3).
- **SPAN (mirror port) vs. TAP** — switch port receiving copies of frames / passive (splitter, physical copy) or active (powered, regenerates signal) test access point (Pt4 p.5).
- **Jump server** — hardened server providing access to other hosts (Pt4 p.6).
- **Forward, reverse, caching, content-filtering, open, anonymizing proxy** — see note; reverse proxy sits on the server side (filtering, SSL decryption, static content, load balancing) (Pt4 p.7-8).
- **Load balancer** — spreads processing across systems; best for stateless; survivors pick up load on failure (Pt4 p.9).
- **IDS vs. IPS; HIDS/HIPS vs. NIDS/NIPS** — detect and report / reactive in-line blocking; host-based can read encrypted traffic, network-based cannot see inside a host (Pt4 p.10-11).
- **802.1X (PNAC) and EAP** — port-based network access control at the data link layer; EAP-MD5 / -TLS / -TTLS / -FAST, PEAP, LEAP (Pt4 p.13-14).
- **Stateless vs. stateful (SPI) firewall; layer 4 vs. layer 7 inspection** — ports/protocols/IPs / dynamic state table of TCP sessions; SPI inspects the TCP handshake (L4) or content (L7) (Pt4 p.15-16).
- **WAF, SWG, UTM** — HTTP/HTTPS content-filtering firewall / on-premises proxy-based filter+IDS/IPS for user Internet access / all-in-one firewall, IDS/IPS, AV, VPN, web filtering (Pt4 p.21-22).
- **VPN: site-to-site, remote access, always-on, split tunnel, full tunnel** — Pt4 p.26-29.
- **PPTP, L2F, L2TP** — obsolete/no-encryption/authentication-only layer 2 tunnels; L2TP with IPsec adds confidentiality (Pt4 p.30).
- **IPsec: SA, IKE, AH, ESP; transport vs. tunnel mode** — AH = integrity/authentication, ESP = plus confidentiality; transport encrypts payload only, tunnel encrypts whole packet in a new IP header; IKE phase 1 secure channel, phase 2 IPsec SA (Pt4 p.31-34).
- **SD-WAN; SASE** — virtual WAN over MPLS/LTE/broadband with microsegmentation / cloud-delivered SWG, CASB, ZTNA, FWaaS plus WAN (Pt4 p.36-37).
- **Defense in depth (the FAN)** — layered perimeter, network, application, and data security around mission-critical assets, spanning technology, process, and people (Pt4 p.39).

## Protecting data (3.3)

_From [03-security-architecture/concepts-and-strategies-to-protect-data.md](../course-unit-notes/03-security-architecture/concepts-and-strategies-to-protect-data.md) (sub-objective 3.3, validated)._

- **Regulated / trade secret / legal / financial data** — compliance-governed by law or industry rules / IP giving advantage but unregistered (no copyright, trademark, patent) / contracts, court and regulatory records / bank, investment, payroll, tax (Pt4 p.42-43).
- **Human- vs. non-human-readable data** — readable with basic viewer software / needs a specialized processor or algorithm (binary, encrypted, encoded) (Pt4 p.43).
- **Classification labels** — Public (Unclassified), Confidential (Secret, NDA third parties), Critical (Top Secret), Proprietary/IP, Private/Personal (PII), Sensitive (personal-data context; GDPR list), Restricted (stringent controls) (Pt4 p.44-45).
- **Data at rest / in motion (in transit) / in use; data replication** — in storage / across a network / in an application or memory / backup or copy and its protection (Pt4 p.46).
- **Data sovereignty; geographical considerations** — jurisdiction restricts processing/storage to systems inside it / pick storage locations and set access controls by client location (Pt4 p.47).
- **Masking vs. tokenization** — replace with fictional/partial values keeping format and length / replace with a random token, original stored separately (Pt4 p.48).
- **Hashing; obfuscation; segmentation; permission restrictions; geographic restrictions** — fixed-length output / harder to understand or reverse engineer, same function / isolated components limit breach impact / access by user permissions / access by location (Pt4 p.48).
- **Data minimization; deidentification; anonymization; pseudo-anonymization; reidentification attack; k-anonymity** — Pt4 p.49.

## Resilience and recovery (3.4)

_From [03-security-architecture/resilience-and-recovery-in-security-architecture.md](../course-unit-notes/03-security-architecture/resilience-and-recovery-in-security-architecture.md)_

- **Failover (high availability) cluster vs. load balancing cluster** — secondary server takes over if primary fails (DNS, domain controllers) / servers share load and replicate data so each holds the same information (Pt4 p.52).
- **NIC teaming / adapter teaming** — multiple NICs or ports give load balancing at the adapter level; clustering works at the service level (Pt4 p.53).
- **Cold / warm / hot / mobile site; geographic dispersion; CoOP site** — empty or near-empty, up in days to a week ($) / peripherals and software, backups days or weeks old, up in hours to 3 days ($$) / fully configured, up in minutes to an hour ($$$) / portable / replicated between distant sites / recovery, alternate, or backup site (Pt4 p.54).
- **Platform, technology, control, vendor, crypto, software diversity** — mix of OSes and hardware / mix of OSes, apps, languages, virtualization / mix of control classes and functions / multiple suppliers / varied algorithms and implementations / different binary per build (Pt4 p.55-56).
- **Multi-cloud** — spreads risk across providers; primary on one, backup and DR on another (Pt4 p.57).
- **COOP (Continuity of Operations Plan)** — keeps critical functions running or quickly resumed; government term similar to business continuity planning; alternate site for up to 30 days (Pt4 p.58).
- **Capacity planning** — forecast people, technology, and infrastructure needs (Pt4 p.59).
- **Tabletop / failover / simulation / parallel processing tests** — discuss the scenario / intentionally fail the primary (full-interruption, live) / teams carry out recovery in a realistic drill / run primary and backup together, duplicating transactions (Pt4 p.60-63).
- **Three factors of data risk** — time, quantity, access (Pt4 p.64).
- **Backup media; NAS vs. SAN** — disk, tape, NAS, SAN, cloud / NAS = file-level over SMB or FTP; SAN = block-level over Fibre Channel, SCSI, SAS, or InfiniBand (Pt4 p.68).
- **Non-persistence; snapshot; rollback; live boot media; master image; template build** — static instance with data separated / saved state / restore baseline (e.g., Windows System Restore) / boots read-only to memory / gold disk / build from instructions (Pt4 p.69).
- **Tape rotation: GFS, Tower of Hanoi, FIFO** — daily, weekly, monthly cycles / recursive, even wear / oldest media overwritten (Pt4 p.70).
- **Database replication; shadow database; remote journaling (log shipping); JFS** — live mirror serving clients / one-way mirror clients do not access / transactions shipped to another site, recover from checkpoint plus journal / file system with a change log (Pt4 p.71).
- **Full / incremental / differential backup** — all data, clears archive bit / changes since last backup, clears bit, restore = full + all incrementals / changes since last full, does not clear bit, restore = full + latest differential (Pt4 p.72-73).
- **RAID 0, 1, 3, 4, 5, 6, 10 (0+1); multipath** — striping, no redundancy (2 drives) / mirroring (2) / byte stripe, dedicated parity (3) / block stripe, dedicated parity (3) / distributed parity, one disk can fail (3) / double parity, two can fail (4) / mirrors then striped (4) / extra controllers and cabling for failover to storage (Pt4 p.74-81).
- **Dual PSU; managed PDU; UPS; backup generators** — hot-plug redundant supplies / strip socket with filtered voltage and remote administration / surge suppressor plus battery (surges, spikes, sags, brownouts, blackouts) / portable gas, permanently installed (natural gas or propane, auto-start), battery-inverter (Pt4 p.82).

## Security controls (1.1)

- **Security control categories: Managerial (Administrative), Physical, Operational, Technical (Logical)** — policy/procedure oversight / physical assets against in-person intrusion / implemented primarily by people / software, hardware, or firmware restricting logical access (Pt1 p.19). Technical and Physical controls should be supported with Administrative controls (Pt1 p.19).
- **Security control types: Directive, Deterrent, Detective, Preventive, Compensating/Alternative, Corrective/Recovery** — instruct on rules of behavior / discourage violations / warn after unwanted activity is discovered / proactively stop it / make up for deficiencies in other controls / fix a problem or restore the baseline after an incident (Pt1 p.20).

## Fundamental security concepts (1.2)

- **CIA triad** — Confidentiality (vs. disclosure; only shared among persons or organizations), Integrity (vs. alteration; accurate, trustworthy, reliable), Availability (vs. destruction; accessible when needed) (Pt1 p.23). Slide base labels it "5 Pillars of Information Security" with three drawn.
- **Confidentiality concepts** — sensitivity, discretion, criticality, concealment ("security through obscurity"), secrecy, privacy, seclusion, isolation (Pt1 p.24).
- **Integrity concepts** — accuracy, truthfulness, authenticity, validity, non-repudiation, accountability, responsibility, completeness, comprehensiveness (Pt1 p.25). **Availability concepts** — usability, accessibility, timeliness (Pt1 p.26).
- **Non-repudiation** — a subject cannot deny doing something; proof of origin, authenticity and integrity (digital signatures) (Pt1 p.25).
- **Identification / authentication / authorization / auditing / accounting** — claiming to be someone / proving it / allowing resource access / recording and reviewing logs / holding subjects accountable (Pt1 p.27). **Mutual authentication** — client and server verify each other, reducing MiTM probability (Pt1 p.27).
- **Least privilege vs. need to know** — minimum access to do the job / more granular: must need that specific information (Pt1 p.28).
- **X.500; LDAP; LDAPS** — ISO directory standard, inverted-tree hierarchy (used by AD, UNIX/Linux) / subset of X.500, port 389 (TCP or UDP per slide), can be plaintext, TLS supported / LDAP Secure, port 636 (Pt1 p.29).
- **Kerberos; KDC; AS; TGS; TGT; service server** — ticket-based, mostly symmetric keys, UDP 88, prevents eavesdropping/replay/MiTM / holds AS + TGS + database / handles user authentication / issues TGT and session key / holds session key, expiry, IP, used to get service tickets / grants access on valid ticket (Pt1 p.30-31).
- **Gap analysis** — review of the difference between current and desired (or industry-required) security state; done when adopting a framework or meeting a new requirement (Pt1 p.32).
- **Zero trust; microsegmentation; east-west vs. north-south traffic** — no implicit trust, continuous authentication/authorization/posture validation / policies applied to a single node (single-host zone) / server-to-server inside the data center vs. client-to/from the data center (Pt1 p.33).
- **Adaptive identity; threat scope reduction; policy-driven access control; implicit trust zone** — continuous, context-based verification / need-to-know, task-limited access shrinks attack surface / policies based on identity, device posture, network context / data pathway between the PEP and the resource (Pt1 p.34).
- **Control plane; data plane (forwarding plane); management plane** — policies, routing decisions (OSPF, BGP, MPLS) / forwards packets as directed (implicit trust zones) / configures and monitors devices (SNMP, SSH, Telnet) (Pt1 p.36).
- **PDP, Policy Engine, Policy Administrator, PEP** — makes access decisions (control plane) / grant, deny, revoke / issues tokens, sets up/tears down sessions, tells PEP allow or disallow / gatekeeper enforcing decisions, allows/monitors/terminates connections (data plane) (Pt1 p.35, p.37-38).
- **Bollard; access control vestibule (mantrap)** — post/planter stopping vehicles / two interlocked doors, each with separate authentication, prevents tailgating and piggybacking (Pt1 p.39-40).
- **Tailgating vs. piggybacking** — following an approved person without their knowledge / convincing an authorized person to let you in (e.g., "forgot my badge") (Pt1 p.41).
- **Fencing heights** — 3-4 ft deters casual trespassers; 6-7 ft too high to climb easily; 8 ft (with wire) deters determined intruders (Pt1 p.42).
- **CCTV; IP camera** — detective device aiding guards; analog CRT vs. digital CCD; IP-based cameras on a separate network (Pt1 p.43).
- **Proximity reader; smart card; CAC; PIV** — contactless card (PIN = two-factor) / card with embedded memory, chip, RFID/NFC/magstripe / DoD smart card / U.S. federal employee and contractor smart card (Pt1 p.45).
- **Lighting** — both detective and deterrent (Pt1 p.46).
- **Sensors** — alarm; infrared-based motion detection; pressure (force/weight); ultrasonic and microwave (Doppler-like echo); photoelectric (broken beam) (Pt1 p.47).
- **Hot/cold aisles; fire classes A, B, C, D, K** — cold aisle = intake, hot = exhaust / common combustibles (water, soda acid), liquids (halon, argon, FM-200, CO2, soda acid), electrical (halon, argon, FM-200, CO2), combustible metals (dry powder, halon), kitchen (wet chemicals, foam) (Pt1 p.48-49). **Halon** banned in 1994 (Pt1 p.49).
- **Locks; key control; signs; logon banner** — resist picking/drilling/bypass / records of key holders / mark restricted areas and escort-required zones / pop-up stating only authorized users allowed; must accept AUP (Pt1 p.50).
- **Honeypot; honeynet; honeyfile / honeytoken; fake telemetry; DNS sinkhole** — fake attractive system / fake network segment (can include fake wireless) / bait file (honeyfile = bait, honeytoken = tracking) / spoofed data returned to scans / routes suspicious traffic to e.g. a honeynet for analysis (Pt1 p.51).

## Change management

_From [01-general-security-concepts/change-management-processes.md](../course-unit-notes/01-general-security-concepts/change-management-processes.md) (sub-objective 1.3, validated)._

- **Request for change (RFC)** — the submission that starts the change approval process; outlines the change's purpose, scope, and potential impact.
- **Change owner** — the individual or group primarily responsible for implementing a specific change and accountable for it going as planned.
- **Impact analysis** — identifying the potential implications of a proposed change for users, business processes, and interconnected systems.
- **Backout plan** — contingency plan to reverse a failed change and return systems to their original state.
- **Maintenance window** — predefined, recurring time frame, usually low-activity, for implementing changes.
- **Standard operating procedure (SOP)** — detailed written instructions for routine operations or changes; developed during testing.
- **Allow list / deny list (change management)** — pre-approved software, hardware, and change types that skip the full process, versus explicitly blocked ones.
- **Restricted activities** — changes needing extra scrutiny or higher approval due to impact on critical systems, sensitive data, or compliance.
- **Version control** — an ID system for each iteration of a software product (customer version ID, developer build ID; e.g., 1.0 major, 1.0.2 minor).

## Cryptographic solutions (1.4)

Note: [cryptographic-solutions.md](../course-unit-notes/01-general-security-concepts/cryptographic-solutions.md)

- **PKI** — third party that creates, issues and manages keys/certificates; not an encryption algorithm; CA, RA, VA.
- **CA / RA / VA** — CA issues certificates; RA verifies identity and processes requests; VA validates certificates via OCSP.
- **Key escrow** — private key stored (split in two halves) with a trusted third party for authorized recovery.
- **M-of-N control** — key backup distributed across several people/devices; separation of duties.
- **Symmetric vs asymmetric** — one shared key (fast, bulk) vs public/private pair (slower, non-repudiation); k = n(n-1)/2 shared keys.
- **RSA / ElGamal / ECC / Diffie-Hellman** — asymmetric algorithms; DH is key exchange only (table); ECC small keys, low power.
- **DES / 3DES / AES / Blowfish / Twofish / IDEA / RC4** — symmetric ciphers; AES 128/192/256, 128-bit block.
- **Block vs stream cipher** — fixed-size blocks vs one bit at a time.
- **One-time pad / XOR** — unbreakable if key is random, as long as the message, and never reused.
- **TPM / HSM / secure enclave** — motherboard crypto chip / key-storage-and-acceleration device / CPU-protected memory.
- **FDE / SED / EFS / PGP / GPG** — full-disk, self-encrypting drive, Windows file encryption, email/file encryption.
- **Perfect forward secrecy / DHE** — session keys survive later compromise of the server private key; ephemeral DH.
- **Steganography / tokenization / data masking** — hide data in another medium / replace with vault-stored token / irreversible redaction.
- **Hashing / HMAC / MD5 / SHA-1 / SHA-2** — one-way fixed-length digest for integrity; MD5 128-bit, SHA-1 160-bit.
- **Salt / key stretching (PBKDF2, bcrypt)** — random value added before hashing / extra rounds to resist brute force.
- **Digital signature** — sender signs a hash with own private key; receiver verifies with sender's public key.
- **Blockchain / open public ledger** — decentralized, cryptographically secured transaction record.
- **X.509 certificate** — binds identity to public key; signed by CA.
- **CRL / OCSP / OCSP stapling** — revoked-serial list / real-time status lookup / server-supplied time-stamped response.
- **Root of trust / root certificate** — self-signed CA certificate that anchors trust.
- **CSR** — Base64 request to a CA containing subject details and public key.
- **Wildcard / SAN / EV certificate** — domain + subdomains / multiple host names / extended business verification.
- **PKCS #7 / #12, DER / PEM / CER / PFX** — certificate import-export and file formats (.p7b; .pfx/.p12).

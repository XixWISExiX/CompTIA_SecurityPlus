---
Unit: Fundamental Security Concepts
Domain: 1.0 General Security Concepts (sub-objective 1.2 — Summarize fundamental security concepts)
Source: Pt1 p.21-51 (global 21-51; course slides 1-7 to 1-37). Boundaries: Pt1 p.21 = 1.2 roadmap (1-7); Pt1 p.52 = 1.3 roadmap (change management).
Extraction_Status: Fully Extracted (all 31 pages read via vision at 80 dpi)
Pages_Done: Pt1 p.21-51
Pages_Remaining: none
Next_Page: none
Validation_Status: Validated (2026-10-16) — same-session re-check; p.35 (NIST SP 800-207 diagram) and p.49 (fire-class table) re-rendered at 130 dpi and compared with the note; not an independent second reader. See Validation log.
---

## Roadmap and Section Topics (Source: Pt1 p.21-22)

- Pt1 p.21 (1-7) is the Domain 1 roadmap with "Fundamental security concepts" highlighted. (Source: Pt1 p.21)
- Pt1 p.22 (1-8) is the 1.2 Section Topics slide. (Source: Pt1 p.22)
  - Confidentiality, Integrity, and Availability (CIA); Non-repudiation
  - Authentication, Authorization, and Accounting (AAA): Authenticating people; Authenticating systems; Authorization models
  - Gap analysis
  - Zero trust: Control plane (Adaptive identity, Threat scope reduction, Policy-driven access control, Policy Administrator); Data plane (Implicit trust zones, Subject/System, Policy enforcement point)
  - Physical security: Bollards; Access control vestibule; Fencing; Video surveillance; Security guard; Access badge; Lighting; Sensors (Infrared, Pressure, Microwave, Ultrasonic)
  - Deception and disruption technology: Honeypot; Honeynet; Honeyfile; Honeytoken
- [GAP] "Authenticating people", "Authenticating systems", and "Authorization models" are listed as Section Topics but no slide in p.23-51 is titled or devoted to them (see Gaps).

## CIA triad (Source: Pt1 p.23-26)

- Pt1 p.23 (1-9): "INFOSEC" with three pillars; the base is labelled "5 Pillars of Information Security" although only three pillars are drawn. [CONFLICT: label vs. three pillars shown] (Source: Pt1 p.23)

| Pillar | Opposes | Slide definition |
|---|---|---|
| Confidentiality | Disclosure | Only shared among persons or organizations (Source: Pt1 p.23) |
| Integrity | Alteration | Accurate, trustworthy and reliable (Source: Pt1 p.23) |
| Availability | Destruction | Accessible when needed by those who need it (Source: Pt1 p.23) |

### Confidentiality concepts (Source: Pt1 p.24)

- **Sensitivity** — quality of information which could cause harm if disclosed
- **Discretion** — an operator's act or decision to control disclosure to minimize harm
- **Criticality** — the level to which information is mission critical; highly critical information is essential to the operation or function of an organization
- **Concealment** — hiding or preventing disclosure; a means of cover, obfuscation, or distraction; "security through obscurity"
- **Secrecy** — keeping something secret; preventing disclosure
- **Privacy** — keeping information confidential that is personally identifiable or that might cause harm, embarrassment, or disgrace
- **Seclusion** — storing something in an out-of-the-way location
- **Isolation** — keeping something separated from others

### Integrity concepts (Source: Pt1 p.25)

- **Accuracy** — being correct and precise; integrity makes sure information alteration should not occur while the object is in storage, in transit or in process
- **Truthfulness** — being a true reflection of reality
- **Authenticity** — being authentic or genuine; assurance that a message, transaction, or other exchange of information is from its source
- **Validity** — being factually or logically sound
- **Non-repudiation** — a subject cannot deny doing something, such as creating, modifying, or sending a resource; provides proof of the origin, authenticity and integrity of data; prevents entities from denying that they took an action (Digital Signatures)
- **Accountability** — being responsible for actions and results
- **Responsibility** — being in charge or having control over something
- **Completeness** — having all needed parts
- **Comprehensiveness** — being complete in scope
- Slide-wording note: non-repudiation is listed under Integrity concepts, not as a separate pillar. (Source: Pt1 p.25)

### Availability concepts (Source: Pt1 p.26)

- **Usability** — the state of being easy to use or learn or being able to be understood and controlled
- **Accessibility** — assurance that the widest range of subjects can interact with a resource regardless of their capabilities
- **Timeliness** — being prompt, on time, or within a reasonable timeframe

## AAA and related terms (Source: Pt1 p.27-28)

- Pt1 p.27 (1-13) "AAA" (Source: Pt1 p.27):
  - **Identification** — claiming to be someone
  - **Authentication** — proving that you are that person (ID verification)
  - **Mutual authentication** — the client and server verify the authenticity of each other; ensures you are communicating with the correct server, reducing the probability of a man-in-the-middle attack
  - **Authorization** — allowing you to access resources
  - **Auditing** — recording and reviewing log files of what you do
  - **Accounting** — holding subjects accountable for their actions
  - Pictured: a VPN-client window, a lanyard badge, a Windows Event Viewer security log (illustrative screenshots; no detail extracted).
- Pt1 p.28 (1-14) "Identification and Authentication": username field = Identification; password field = Authentication. (Source: Pt1 p.28)
  - **Least privilege** — users should be granted the minimum amount of access (authorization) required to do their jobs, but no more
  - **Need to know** — more granular than least privilege; the user must need to know that specific piece of information before accessing it

### Central directory management (Source: Pt1 p.29)

- **X.500 standard**: published by the International Standards Organization (ISO); hierarchical database is an inverted tree structure; concepts used by Windows Active Directory (AD) and UNIX/Linux. (Source: Pt1 p.29)
- **LDAP (Lightweight Directory Access Protocol)**: a subset of the X.500 protocol; used by most internal identity services; interfaces with Active Directory; uses TCP or UDP 389; LDAPS (LDAP Secure) uses 636; can use plaintext transmission; supports authenticated connection and secure transmissions with TLS. (Source: Pt1 p.29)

### Kerberos (Source: Pt1 p.30-31)

- **Kerberos** — client-server-based authentication system that uses "tickets" to securely authenticate nodes on a network. Primarily uses symmetric key cryptography and mutual authentication; may use public-key cryptography in some authentication phases. Uses UDP port 88. Prevents eavesdropping, replay and MiTM attacks. Third-party authentication service developed at MIT. (Source: Pt1 p.30)
- **Key Distribution Center (KDC)** — components implemented as a single daemon: Kerberos Database (stores user account information); **Authentication Server (AS)** (handles user authentication); **Ticket Granting Server (TGS)** (issues a Ticket-Granting Ticket (TGT) and a ticket session key to the authenticated user). (Source: Pt1 p.30)
- **Ticket Granting Ticket (TGT)** — contains the session key, expiration date/time, user's IP address; used to obtain access to network services. (Source: Pt1 p.30)
- **Service Server** — grants access to users upon presentation of a valid ticket, and verification of access to services. (Source: Pt1 p.30)
- Side note on slide: in Greek mythology, Cerberus is the "Hound of Hades". (Source: Pt1 p.30)

Kerberos authentication process, example with principal Alice and a printer (Source: Pt1 p.31):

| Step | What happens | Message in diagram |
|---|---|---|
| 1 | Alice contacts the KDC, which acts as an AS, requesting authentication | "Alice wishes to authenticate" |
| 2 | KDC sends Alice a session key encrypted with Alice's secret key; also sends a TGT encrypted with the TGS's secret key | {Session Key} Alice's Key; {TGT} TGS's Key |
| 3 | Alice decrypts the session key and uses it to request permission to print from the TGS | "Alice wishes to print": {TGT} TGS's Key, {Auth1} Session Key |
| 4 | Seeing Alice has a valid session key (so she has proven her identity claim), the TGS sends a C/S session key (second session key); also sends a service ticket encrypted with the printer's key | {C/S Session Key} Session Key; {Service Ticket} Printer's Key |
| 5 | Alice connects to the printer; the printer, seeing a valid C/S session key, knows Alice has permission to print and that she is authentic | "Service: print": {Service Ticket} Printer's Key, {Auth2} C/S Session Key |

## Gap analysis (Source: Pt1 p.32)

- **Information Security Gap Analysis** — an in-depth review that helps organizations determine the difference between the current state of their information security and specific industry requirements. Also called IT Security Gap Analysis.
- Conducted to understand the status of your cybersecurity risks and vulnerabilities; performed when first adopting a framework or when meeting a new industry or legal compliance requirement.
- Allows organizations to identify areas of weakness within their network security controls.
- Notable security gaps include weak credentials, insider threats, outdated software, and malware.
- Slide callout: "The difference between the current and desired states". (Source: Pt1 p.32)

## Zero trust (Source: Pt1 p.33-38)

### Definition and microsegmentation (Source: Pt1 p.33)

- **Zero Trust (ZT)** — requires all users, even those inside the organization's enterprise network, to be authenticated, authorized, and continuously validating security configuration and posture, before being granted or keeping access to applications and data.
- Assumes all devices, users, and services are not inherently trusted (**no implicit trust**), regardless of whether inside or outside a network's perimeter; requires all users and devices to be authenticated and authorized before accessing network resources.
- A zero-trust technique is to apply **microsegmentation**: a security process capable of applying policies to a single node, as though it were in a zone of its own (single host zones). Like east-west traffic, this requires a new generation of virtualized security appliances to implement.
- **East-west traffic** — traffic mostly between servers within the data center where cloud and other Internet services are being serviced.
- **North-south traffic** — traffic that goes to and from a data center where traffic represents clients outside the data center making requests and receiving responses; a problem for security inspection and filtering. Example begun on slide: a client uploading a photograph as part of a social media post. (Source: Pt1 p.33)

### Zero trust security concepts (Source: Pt1 p.34)

- **Adaptive identity** — user identities are not static; identity verification must be continuous and based on a user's current context and the resources they are attempting to access.
- **Threat scope reduction** — access to network resources is granted on a need-to-know basis and limited to only those resources required to complete a specific task; reduces the network's attack surface and limits the damage a successful attack can cause.
- **Policy-driven access control** — how access control policies are used to enforce access restrictions based on user identity, device posture, and network context.
- **Implicit trust zone** — the data pathway established between the policy enforcement point and the resource.

### NIST SP 800-207 core logical components (Source: Pt1 p.35)

Diagram "Figure 2: Core Zero Trust Logical Components" (source credited on slide to nvlpubs.nist.gov NIST.SP.800-207.pdf):

- **Control plane** (top): Policy Decision Point = Policy Engine + Policy Administrator.
- **Data plane** (bottom): Subject → System → (untrusted) → Policy Enforcement Point → (trusted) → Enterprise Resource.
- Dashed arrows connect the Policy Administrator and the Policy Enforcement Point (control-to-data-plane interface).
- Left inputs to the control plane: CDM System, Industry Compliance, Threat Intelligence, Activity Logs. Right inputs: Data Access Policy, PKI, ID Management, SIEM System.
- Slide callout: "ZTA components use the control plane to communicate, while application data is sent on a data plane". (Source: Pt1 p.35)

### Control, data, and management planes (Source: Pt1 p.36)

| Plane | Responsibility | Slide details |
|---|---|---|
| Control plane | Managing network routing protocols, which enable communication between devices; defines policies and rules | Manages the actions of the data plane; determines the optimal path for data packets (how packets should be forwarded); uses OSPF, BGP, and MPLS to exchange information between network devices; routing tables, session tables, NAT tables |
| Data plane (forwarding plane) | Forwarding data packets between devices in the network | Transfers/forwards packets based on direction from the control plane; processes frames, packets, and network data; implicit trust zones; "Root of Trust"; "Boarding area at the airport"; uses Ethernet, TCP/IP, and UDP; processing, forwarding, trunking, encrypting, NAT |
| Management plane | Managing and monitoring the network's operations | Configuring and monitoring network devices; uses SNMP, SSH, and Telnet |

### Policy Decision Point (PDP) (Source: Pt1 p.37)

- Responsible for **making access control decisions** based on predefined access policies and rules; evaluates access requests; makes authentication decisions; a control plane component.
- Slide also says the PDP "determines the optimal path for data packets; how packets should be forwarded" (identical wording to the control-plane bullet on p.36). [CONFLICT/oddity: routing-path language attached to an access-decision component]
- Two logical PDP components:
  - **Policy Engine (PE)** — evaluates each access decision based on policy and other information sources; grant, deny, or revoke.
  - **Policy Administrator (PA)** — communicates with the PEP; generates/issues access tokens or credentials; establishes or tears down sessions; implements an interface between the control plane and the data plane; tells the PEP to allow or disallow access.

### Policy Enforcement Point (PEP) (Source: Pt1 p.38)

- Responsible for **enforcing** the access control decisions made by the PDP; acts as a gatekeeper; a data plane component.
- Transfers/forwards packets across the network based on the direction from the control plane; allow, monitor, and terminate connections; can consist of multiple components working together.
- Applies to subjects and systems: end users, applications, non-human entities.

## Physical security (Source: Pt1 p.39-49)

### Bollards / barricades (Source: Pt1 p.39)

- A traffic **bollard** is a strong post designed to stop a vehicle from entering a facility; derives from mooring bollards used to tie ships to piers.
- Can be decorations and **prevent** vehicles from entering restricted areas; often installed in front of convenience stores to prevent a confused driver (accelerator/brake mix-up) from driving into the store.
- Used in secure facilities to prevent cars from entering (intentionally or not); many secure facilities use large concrete planters for the same effect.

### Access control vestibule (Source: Pt1 p.40)

- **Access Control Vestibule (Mantrap)** — an arrangement of two doors (only one opens at a time) to prevent unauthorized people from following authorized users through an access-controlled door.
- A preventive physical control with two doors; the first door must close and lock before the second may be opened; each door typically requires a separate form of authentication (e.g., PIN and biometrics); an intruder is trapped between the doors after entering; prevents tailgating and piggybacking.

### Tailgating vs. piggybacking (Source: Pt1 p.41)

| Term | Slide definition |
|---|---|
| Tailgating | Following an approved individual into a secure facility without the appropriate access credentials, without the approved person's knowledge. Example: a tailgater waits outside until an employee exits, slips behind them and grabs the door before it closes |
| Piggybacking | Convincing an authorized person to let the attacker into a secure facility, typically under the guise of having "forgotten one's badge" |

### Fencing (Source: Pt1 p.42)

- Physical barrier around property to keep unauthorized personnel from accessing restricted areas; often seen as a first layer of defense; used to separate security zones, provide safe areas, and maintain traffic separation; ranges from simple deterrents to sophisticated deterrence devices.
- Three to four feet high only deter casual trespassers; six to seven feet are considered too high to climb easily; eight feet (possibly with barbed or razor wire at the top) means you are serious about protecting your property and often deters the more determined intruder.

### Video surveillance (Source: Pt1 p.43)

- **CCTV (Closed Circuit Television)** — a detective device used to aid guards in detecting the presence of intruders in restricted areas.
  - Normal light spectrum requires sufficient visibility to illuminate the field of view; infrared devices can see in the dark by displaying heat.
  - Older "tube cameras" CRT (Cathode Ray Tube) are analog; modern cameras use CCD ("Charged Couple Discharge" as written on the slide), which are digital.
- **Cameras** — provide surveillance and monitoring over large areas; monitoring from a central or remote location; can be combined with facial recognition technology to track individuals; can be CCTV or IP-based; IP-based cameras should be on a separate network to protect against attacks.

### Security guards (Source: Pt1 p.44)

- Provide a visible presence with direct responsibility for security; monitor entrances and exits and maintain visitor logs.
- Pros: one of the best mechanisms to monitor a facility's grounds; more flexible than other mechanisms; good response to suspicious activities; great deterrent.
- Cons: costly (salary, benefits, time off); people sometimes unreliable (social engineering).

### Access badges (Source: Pt1 p.45)

- **Proximity readers** — control access through doors using contactless access cards; with a PIN provides two-factor authentication.
- **Smart card** — small card with embedded integrated memory that can store permissions and access information; cryptographic chip and connector; contact/contactless proximity card circuit (magnetic strips, RFID chips, NFC technology); standards for printed photo and name on front; biometric data storage.
- **Common Access Card (CAC)** — smart card used by the DoD as a general identification/authentication card for military personnel, contractors, and non-DoD employees.
- **Personal Identity Verification (PIV) card** — smart card for U.S. federal employees and contractors, similar to DoD CAC; contains information to access federal institutions and systems.

### Lighting (Source: Pt1 p.46)

- Proper lighting is often a critical component in ensuring physical security is maintained.
- Poor lighting can let individuals sneak in through doors, bypassing a checkpoint or facial recognition systems; bright lights in access ways, parking lots and storage areas deter would-be attackers.
- Can act as both a **detective** and **deterrent** control: lets a guard see an intruder (detective); criminals favor a poorly lit target over a visible one (deterrent). Should be bright enough to illuminate the desired field of vision.

### Sensors (Source: Pt1 p.47)

- **Alarms** — a device used to draw attention to a breach, or suspected breach, of a security zone when it occurs.
- **Motion detection** — detects the motion of a living being within the sensor's footprint; typically infrared (heat) based; can be tuned to ignore smaller heat signatures (animals); often tied to video surveillance that records once motion is sensed.
- **Pressure** — detects a change in force; floor and window sensors activated by weight.
- **Ultrasonic and microwave motion detectors** — work like Doppler radar; send out a signal and measure the reflected signal ("echo").
- **Photoelectric motion sensor** — sends a beam across a monitored space; detects when the beam is broken.

### Environmental controls (Source: Pt1 p.48-49)

- **Environmental controls** — protect information systems from the effects of the physical world: heating and cooling (HVAC); hot and cold aisles; fire suppression; temperature and humidity controls; EMI and RF protection. (Source: Pt1 p.48)
- **Hot and cold aisles** — controlling airflow in a data center so cold aisles are used for air intake and hot aisles for air exhaust, to improve efficiency. (Source: Pt1 p.48)
- Fire suppression (Source: Pt1 p.49):
  - **Water-based** — primary tool to control and suppress structural fires but can damage electrical equipment.
  - **Halon-based** — chemical system; Halon mixes quickly with room air to extinguish a fire; banned in 1994 due to its danger to humans.
  - **Clean-agent** — protect the contents of the room including people, documents, and electronic equipment; carbon dioxide, argon, Inergen, FM-200 (heptafluoropropane), FE-13 (trifluoromethane).
  - **Hand-held extinguishers** — based on the type of fire.

| Fire class | Type of fire | Elements of fire | Suppression method |
|---|---|---|---|
| Class A | Common combustibles | Ashes, paper, wood, cloth, etc. | Water, soda acid |
| Class B | Liquid | Barrels of oils, petroleum, tars, solvents, alcohol, gases | Halon, argon, FM-200, CO2, soda acid |
| Class C | Electrical | Circuits, electrical equipment, and wires | Halon, argon, FM-200, CO2 |
| Class D | Dry chemical | Combustible metals, and chemical | Dry powder, halon |
| Class K | Commercial kitchen | Food, grease | Wet chemicals, foam |

(Source for table: Pt1 p.49)

### Other security controls: locks, signs, banner (Source: Pt1 p.50)

- **Physical — Locks**: traditional locks to secure devices or doors; high-security models resist lock picking, drilling or bypass. **Key control** — keeping records of the authorized users of keys and controlling access to them.
- **Physical — Signs**: informational devices; identify restricted areas or delineate where visitors are allowed versus areas where escorts are required.
- **Technical (Logical) — Logon/pop-up banner**: window at logon informing the user only authorized users are allowed and others will be prosecuted; users must accept or agree to the terms (AUP) in the banner before continuing. A screenshot of a Northrop Grumman network banner is shown (illustrative).

## Deception and disruption technology (Source: Pt1 p.51)

- **Honeypot** — a separate system that appears to be an attractive target for attackers; records and files are fake and legitimate users never have access, so no actual organization data is on it; the attacker may spend time investigating the honeypot rather than your real network.
- **Honeynet** — a fake network segment that appears enticing to the attacker; can include fake wireless networks.
- **Honeyfile** — also known as honeytoken; can be made trackable so that when an attacker exfiltrates it, attempts to reuse or exploit it can be traced. Slide sub-bullets: Honeyfile = **bait**; Honeytoken = **tracking**.
- **Fake telemetry** — deception strategy that returns spoofed data in response to network scanning activity.
- **DNS sinkhole** — routes suspicious traffic to a different network such as a honeynet, where it can be analyzed.

## Gaps, conflicts, and slide quirks

- [GAP] No dedicated slides for "Authenticating people", "Authenticating systems", or "Authorization models" (the latter would normally cover MAC/DAC/RBAC/ABAC); the Section Topics list them but p.27-31 only cover AAA terms, X.500/LDAP, and Kerberos. Authentication factors, biometrics, and access-control models must be sourced elsewhere or may appear in a Domain 4 unit (4.6 IAM); not checked here.
- [GAP] Honeypot-family and sinkhole content is definition-level only; no operational detail.
- [CONFLICT] p.23 base label "5 Pillars of Information Security" with three pillars drawn.
- [CONFLICT/oddity] p.37 PDP bullet repeats the routing-path wording of the control plane.
- Slide quirks (recorded as written, not corrected): "Charged Couple Discharge" (p.43; CCD is normally "charge-coupled device"); LDAP "uses TCP or UDP 389" (p.29); non-repudiation filed under Integrity (p.25).

## Official-objective bullet check (1.2)

| Official 1.2 bullet | Slide support |
|---|---|
| CIA | Yes (p.23-26) |
| Non-repudiation | Yes (p.25) |
| AAA — authenticating people / systems / authorization models | Partial: AAA terms, mutual authentication, Kerberos, LDAP; no people/systems/authorization-model slides (gap) |
| Gap analysis | Yes (p.32) |
| Zero trust — control plane (adaptive identity, threat scope reduction, policy-driven access control, policy administrator, policy engine) | Yes (p.34-37) |
| Zero trust — data plane (implicit trust zones, subject/system, policy enforcement point) | Yes (p.36, p.38) |
| Physical security (bollards, access control vestibule, fencing, video surveillance, security guard, access badge, lighting, sensors) | Yes (p.39-47) |
| Deception and disruption technology (honeypot, honeynet, honeyfile, honeytoken) | Yes (p.51) |

(Coverage status for this unit is recorded in `source_coverage/objective_mapping.md`, not here.)

## Validation log

- 2026-10-16: All 31 pages (p.21-51) read at 80 dpi and compared with this note. p.35 (NIST SP 800-207 diagram) and p.49 (fire suppression table) re-rendered at 130 dpi; box labels, plane membership, and every table cell matched. No transcription errors found. Same-session check, not an independent reader.

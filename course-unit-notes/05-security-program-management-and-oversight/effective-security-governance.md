---
Unit: Effective Security Governance
Domain: 5.0 Security Program Management and Oversight (sub-objective 5.1 — Summarize elements of effective security governance)
Source: Pt6 p.61-85 (global 561-585; course slides 5-3 to 5-27). Boundaries: Pt6 p.60 = Domain 5 "Domain Topics" (5-2); Pt6 p.61 = 5.1 roadmap (5-3); Pt6 p.86 = 5.2 roadmap (5-28)
Extraction_Status: Fully Extracted (all 25 pages read via vision at 110 dpi)
Pages_Done: Pt6 p.61-85
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — all 25 pages (Pt6 p.61-85) re-rendered at 100 dpi and visually compared against the note (see Validation log)
---

## Roadmap and Section Topics (Source: Pt6 p.60-62)

- Pt6 p.60 (5-2) is the Domain 5 "Domain Topics" slide listing 5.1-5.6 (5.1 governance; 5.2 risk management process; 5.3 third-party risk assessment and management; 5.4 security compliance; 5.5 audits and assessments; 5.6 security awareness practices). (Source: Pt6 p.60)
- Pt6 p.61 (5-3) is the roadmap slide with "Effective security governance" highlighted. (Source: Pt6 p.61)
- Pt6 p.62 (5-4) is the 5.1 Section Topics slide (Source: Pt6 p.62):
  - Guidelines
  - Policies: AUP; information security policies; business continuity; disaster recovery; incident response; SDLC; change management
  - Standards: password; access control; physical security; encryption
  - Procedures: change management; onboarding/offboarding; playbooks
  - External considerations: regulatory; legal; industry; local/regional; national; global
  - Monitoring and revision
  - Types of governance structures: boards; committees; government entities; centralized/decentralized
  - Roles and responsibilities for systems and data: owners; controllers; processors; custodians/stewards

## Policies, Procedures, Standards, Guidelines, and Baselines — pyramid (Source: Pt6 p.63)

| Layer (top to bottom) | Label on slide |
|---|---|
| Policy | Mandatory |
| Procedure | Mandatory |
| Standard | Mandatory |
| Guideline | Recommendations |
| Baseline | Discretionary |

(Source: Pt6 p.63) Baseline appears only on this pyramid; no other slide in 5.1 defines it. [GAP]

## Policy (Source: Pt6 p.64)

- **Policy** — a strictly enforceable ruleset that determines how a task should be completed. (Source: Pt6 p.64)
  - High-level; outputs of governance.
  - Authoritative documents defining the organization's security commitment.
  - Form the framework for operations, decision-making, and behaviors, setting the rules for a compliant and ethical corporate culture.

## Policies (Source: Pt6 p.65-67)

- **Acceptable Use Policy (AUP)** — outlines the acceptable ways in which network and computer systems may be used by defining what constitutes acceptable behavior by users. (Source: Pt6 p.65)
  - Addresses browsing behavior, appropriate content, software downloads, handling sensitive information.
  - Goal: users do not engage in activities that could harm the organization or its resources.
  - Covers consequences for noncompliance, how compliance is monitored, and requires employees to acknowledge comprehension of the AUP's rules via signature.
- **Information Security Policies** — ensure all IT users comply with rules and guidelines related to the security of information stored within the environment or the organization's sphere of authority. (Source: Pt6 p.65)
- **Business Continuity & Continuity of Operations Plans (COOP)** — focus on the critical processes that must remain operational during and after a substantial disruption, like a natural disaster or a cyber-attack. (Source: Pt6 p.65)
- **Disaster Recovery** — details the steps required to recover from a catastrophic event such as a natural disaster, major hardware failure, or significant security breach; goal is to restore operations as quickly and efficiently as possible. (Source: Pt6 p.65)
- **Incident Response** — outlines the processes followed after a security breach or cyberattack occurs. (Source: Pt6 p.66)
  - Details steps for identifying, investigating, controlling, and mitigating the impact of incidents, including communicating about the incident to internal and external sources.
  - Overall goal: control the **cost and damage** associated with incidents and make recovery of impacted systems **quicker** (bold on slide).
- **Software Development Life Cycle (SDLC)** — governs software development within an organization. (Source: Pt6 p.66)
  - Structured plan detailing the stages from initial requirement analysis to maintenance after deployment.
  - Ensures all software meets the organization's efficiency, reliability, and security standards.
- **Change Management** — outlines how changes to IT systems and software are requested, reviewed, approved, and implemented, including all documentation requirements. (Source: Pt6 p.66)
- **Mandatory Vacations** — a policy directing employees to take vacations. (Source: Pt6 p.67)
  - Used to uncover fraudulent/nefarious behavior or activity.
  - See what they do; detect or prevent fraud; irregularities.
- **Job Rotation** — rotating employees through security positions to provide a wider understanding of security issues within the organization. (Source: Pt6 p.67)
  - Provides redundancy within the organizational structure.
  - Reduced attack vector for disgruntled employees.
  - Reduces fraud and single point of failure; reduces the risk of collusion.
- **Separation of Duties** — a process that requires more than one person to complete critical functions. (Source: Pt6 p.67)
  - Prevents one person from being able to cause catastrophic damage to the organization.
  - Avoids fraud; employees don't have access to all steps of a business process.
- **Clean Desk Policy** — requires employees to limit what is on their desks to what they are working on at the present time, and secure anything not presently needed. (Source: Pt6 p.67)
  - Helps increase physical security by limiting what data is exposed.
  - "Due Care" is printed as the last sub-bullet, with no explanation. [GAP]

## Business Continuity concepts (Source: Pt6 p.68)

- **Business Continuity Plan (BCP)** — identifies controls and processes that enable an organization to maintain critical workflows sustaining mission/business processes during and after a disruption. Part of the Organizational Security Policy. (Source: Pt6 p.68)
- **Continuity of Operations Plan (CoOP)** — same as BCP when undertaken by a government agency, rather than a business. (Source: Pt6 p.68)
- **Disaster Recovery Plan (DRP)** — a plan focused on the recovery and rebuilding of the organization after a disaster (system/network failure, infrastructure failure, or natural disaster) has occurred. (Source: Pt6 p.68)
  - Part of the Business Continuity Plan.
  - Focused on the protection of human life.
  - Includes evacuation plans and system shutdown plans.
  - Long-term recovery of the organization.
  - Should be tested/exercised periodically.

## Software Development Life Cycle (SDLC) phases (Source: Pt6 p.69)

- **SDLC** — divides the creation and maintenance of software into discrete phases. (Source: Pt6 p.69)
- **Development** — code is hosted on a secure server throughout the development cycle. Each developer checks out a portion of code for editing on their local machine; the local machine is normally configured with a sandbox for local testing, ensuring other local processes do not interfere with or compromise the application being developed.
- **Test/Integration** — code from multiple developers is merged to a single master copy and subjected to basic unit and functional tests to ensure the code builds correctly and fulfills the functions required by the design.
- **Staging** — creating a secure development environment (**mirror of the production**, underlined on slide) for the different phases of a software development project.
- **Production** — the application is released to end users.

## Procedures (Source: Pt6 p.70)

- **Procedures** — detailed, step-by-step instructions and checklists for ensuring a task is completed in a way that complies with policy (pyramid label: Mandatory). (Source: Pt6 p.70)
- **Change Management** — implementation of changes should be carefully planned, considering how the change will affect dependent components. Every change should come with a rollback, backout, or remediation plan so it can be reversed if it has harmful or unforeseen consequences.
- **Onboarding** — bringing in a new employee, contractor, or supplier.
- **Offboarding (Exit Interview)** — ensuring an employee leaves a company gracefully; also used when a project using contractors or third parties ends.
- **Playbooks** — a central repository of well-defined, standardized strategies and tactics; guide personnel to ensure consistency in operations and improve quality and effectiveness.

## Standards (Source: Pt6 p.71-75)

- **Standards** — explain how specific business activities should be performed (pyramid label: Mandatory). (Source: Pt6 p.71)
  - Derived directly from the organization's policies and should provide enough detail to determine whether the standard is being met.
  - Define the expected outcome of a task, such as a particular configuration state for a server or a performance baseline for a service.
  - More specific than policies and specify the methods used to implement technical and procedural requirements.
- **Password standards** (Source: Pt6 p.72):
  - Hashing algorithms — requirements for hash functions used to store passwords.
  - Password salting — methods used to protect password hashes from rainbow table attacks.
  - Secure password transmission — methods incl. appropriate cipher suites.
  - Password reset — identity verification methods to protect reset requests from exploitation.
  - Password managers — requirements for password managers an organization may incorporate.
- **Access control standards** (Source: Pt6 p.73):
  - Access control models — appropriate models for different use cases.
  - User identity verification — acceptable methods to verify identities before granting access.
  - Privilege management — methods for managing privileges so users have the minimum required access.
  - Authentication protocols — specific acceptable protocols (Kerberos, OAuth, or SAML).
  - Session management — allowable practices incl. session timeouts, secure generation and transmission of session cookies.
  - Audit trails — mandatory audit capabilities to help identify and investigate security incidents.
- **Physical security standards** (Source: Pt6 p.74):
  - Building security — card access systems, CCTV surveillance, security personnel.
  - Workstation security — physically securing laptops or other portable devices.
  - Datacenter and server room security — card access, biometric scans, sign-in/sign-out logs, escorted visitor access.
  - Equipment disposal — securely disposing of or repurposing equipment so sensitive data is irrecoverable.
  - Visitor management — sign-in/sign-out, visitor badges, escorted access.
- **Encryption standards** (Source: Pt6 p.75):
  - Encryption algorithms — allowable algorithms: AES (Advanced Encryption Standard) for symmetric; ECC (Elliptic Curve Cryptosystem) for asymmetric.
  - Key length — minimum allowable key lengths for different types of encryption.
  - Key management — how keys are generated, distributed, stored, and changed: requirements for secure key management systems; procedures for regularly changing keys; procedures for revoking them if compromised.

## Frameworks (Source: Pt6 p.76)

- **Center for Internet Security (CIS)** — not-for-profit organization that publishes the Control, Risk Assessment Method, and benchmarks for different aspects of cybersecurity, IT frameworks, and compliance programs. (Source: Pt6 p.76)
  - "The 20 CIS Controls" — now The 18 CIS Critical Security Controls (as printed).
  - CIS-RAM (Risk Assessment Method).
- **NIST Risk Management Framework (RMF)** — integrates security, privacy, and cyber supply chain risk management activities into the system development life cycle. Steps: Prepare – Categorize – Select – Implement – Assess – Authorize – Monitor. (Source: Pt6 p.76)
- **NIST Cybersecurity Framework (CSF)** — voluntary guidance, based on existing standards, guidelines, and practices, for organizations to better manage and reduce cybersecurity risk. Functions: Identify – Protect – Detect – Respond – Recover. (Source: Pt6 p.76)

## Industry standards (Source: Pt6 p.77-78)

| Standard | Slide description | Source |
|---|---|---|
| ISO/IEC 27001 | International standard providing an information security management system (ISMS) framework to ensure adequate and proportionate security controls are in place | Pt6 p.77 |
| ISO/IEC 27002 | Detailed guidance on specific controls | Pt6 p.77 |
| ISO/IEC 27017 | Specific to cloud services | Pt6 p.77 |
| ISO/IEC 27018 | Specific to protecting PII in public clouds | Pt6 p.77 |
| ISO/IEC 27701 | Focuses on personal data and privacy | Pt6 p.77 |
| ISO/IEC 21000 (21K) | "cybersecurity framework" (as printed) | Pt6 p.77 |
| ISO/IEC 31000 (31K) | Overall framework for Enterprise Risk Management (ERM) | Pt6 p.77 |
| NIST SP 800-63 | US government standard for digital identity guidelines, including password and access control requirements | Pt6 p.77 |
| FIPS | Standards and guidelines developed by NIST for US federal computer systems specifying cryptography requirements | Pt6 p.77 |

- [CONFLICT/ODD] The slide labels ISO/IEC 21000 as a "cybersecurity framework"; recorded as printed, not corrected from outside knowledge. (Source: Pt6 p.77)
- **PCI-DSS (Payment Card Industry Digital Security Standard)** — standard for organizations that handle credit cards from major card providers, including requirements for protecting cardholder data. (Source: Pt6 p.78) [Slide text reads "Digital Security Standard" in the definition and the title/heading is "PCI-DSS"; Pt6 p.81 prints "Data Security Standard" — the two slides differ, recorded as printed.]
  - Lists the security controls and objectives for companies that store, process, and/or transmit cardholder data.
  - Requires security auditing and penetration testing to ensure controls are implemented and objectives met.
  - Callout box: "Conduct at least quarterly reviews."
  - Requirements table (Source: Pt6 p.78):

| Assessment procedure (goal) | Requirements |
|---|---|
| Build and Maintain a Secure Network | 1: install and maintain a firewall configuration to protect cardholder data; 2: do not use vendor-supplied defaults for system passwords and other security parameters |
| Protect Cardholder Data | 3: protect stored cardholder data; 4: encrypt transmission of cardholder data across open, public networks |
| Maintain a Vulnerability Management Program | 5: use and regularly update anti-virus software or programs; 6: develop and maintain secure systems and applications |
| Implement Strong Access Control Measures | 7: restrict access to cardholder data by business need-to-know; 8: assign a unique ID to each person with computer access; 9: restrict physical access to cardholder data |
| Regularly Monitor and Test Networks | 10: track and monitor all access to network resources and cardholder data; 11: regular test security systems and processes (as printed) |
| Maintain an Information Security Policy | 12: maintain a policy that addresses information security for all personnel |

## Guidelines (Source: Pt6 p.79)

- **Guidelines** — best-practice recommendations and advice for configuration items where detailed, strictly enforceable policies and standards are impractical (pyramid label: Recommendations). (Source: Pt6 p.79)
  - Recommendations that steer actions in a particular job role or department.
  - More flexible than policies; allow greater discretion for the individuals implementing them.
  - Provide best practices and suggestions on achieving goals and completing tasks effectively.
  - Help individuals understand the required steps to comply with a policy or improve effectiveness.

## External considerations (Source: Pt6 p.80-81)

- Organizations must comply with the laws in all jurisdictions where they operate. (Source: Pt6 p.80)

| Region | Laws listed (Source: Pt6 p.80) |
|---|---|
| United States | HIPAA; Gramm-Leach-Bliley Act (GLBA); Federal Information Security Management Act (FISMA); California Consumer Privacy Act (CCPA); Cybersecurity Maturity Model Certification (CMMC) |
| United Kingdom | Data Protection Act 2018; Network and Information Systems (NIS) Regulations 2018 |
| Canada | PIPEDA (Personal Information Protection and Electronic Documents Act) |
| India | The Information Technology Act 2000 |
| Australia | The Privacy Act 1988 |
| Global | General Data Protection Regulation (GDPR) |

- **Industry-specific** (Source: Pt6 p.81):

| Industry | Laws listed |
|---|---|
| Healthcare | HIPAA (United States); GDPR (European Union) |
| Financial services | GLBA (United States); PCI DSS (contractual obligation) |
| Telecommunications | Communications Assistance for Law Enforcement Act (CALEA) (United States) |
| Energy | North American Electric Reliability Corporation (NERC) (United States and Canada) |
| Education & children | FERPA (US); Children's Internet Protection Act (CIPA) (US); Children's Online Privacy Protection Act (COPPA) (US) |
| Government | Federal Information Security Modernization Act (FISMA) (US); Criminal Justice Information Services Security Policy (CJIS) (US); Government Security Classifications (GSC) (UK) |

- [CONFLICT/ODD] FISMA expands as "Federal Information Security Management Act" on Pt6 p.80 and "Federal Information Security Modernization Act" on Pt6 p.81. Recorded as printed.
- The slides give names only, no explanation of what each law requires. [GAP]

## Monitoring and revision (Source: Pt6 p.82)

- The cybersecurity landscape is continually evolving; organizations must ensure policies, procedures, standards, and legal compliance practices associated with legal and regulatory compliance are regularly monitored, evaluated, and updated. (Source: Pt6 p.82)
  - Routine audits, inspections, and assessments are commonly used to measure compliance levels and identify new risks.
  - Regular training sessions inform employees of policy changes and ensure continued compliance.
  - **Ongoing continuous monitoring** (underlined; sub-bullets printed as fragments): conducted at least annually; updates occur; new regulations are introduced; interdependencies change.

## Types of governance structures (Source: Pt6 p.83-84)

- **Governance Board** — typically executives with ultimate decision-making authority; responsible for setting strategic direction and policies. Senior executives and external stakeholders responsible for setting strategy and ensuring compliance. (Source: Pt6 p.83)
- **Governance Committee** — subject matter experts, stakeholders, and representatives from relevant departments focused on specific issues such as security, risk management, audit, or compliance. Leaders and SMEs responsible for defining policies, procedures, and standards within a particular domain or scope. (Source: Pt6 p.83)
- **Government Entities and Groups** — regulatory agencies; intelligence agencies; law enforcement agencies; defense and military organizations; data protection authorities; national cybersecurity agencies. (Source: Pt6 p.83)
- **Centralized vs. decentralized security governance** (Source: Pt6 p.84):
  - Both aim to achieve security goals, protect assets, mitigate risks, and ensure regulatory compliance. The choice depends on organization's size, structure, culture, and risk appetite; the goal is a model that supports the organization's needs while balancing security risks.
  - **Centralized** — decision-making authority primarily rests with a single core group or department that establishes policies, procedures, and guidelines and makes important security decisions. Includes resource allocation (budget and personnel); promotes consistency and standardization across the entire organization.
  - **Decentralized** — distributes decision-making authority to different groups or departments for decisions based on localized needs and priorities. Each unit has greater control over allocation of security resources; allows greater adaptability and tailoring of security capabilities.
  - **Hybrid** — balances centralized oversight and decentralized implementation. Specific processes/decisions are centralized, others delegated to business units; enables standardized enterprise-level policies with flexibility and local control as warranted.

## Roles and responsibilities for systems and data (Source: Pt6 p.85)

| Role | Slide description |
|---|---|
| **Owner** | High-ranking employee (director or VP) typically holds the role and is ultimately responsible for ensuring data is appropriately protected. Identifies classification and sensitivity level, decides who should have access and what level of security applies; provides strategic guidance so security policies align with business objectives |
| **Controller** | Identifies the purposes, conditions, and means of processing personal data (GDPR). An individual, public authority, agency, or other body can fill the role. Ensures processing adheres to all legal requirements; helps maintain legal and regulatory compliance |
| **Processor** | Responsible for processing personal data on behalf of the controller; often represents cloud service providers (CSP) but could also be vendors and business partners. Must maintain records of processing activities, cooperate with supervisory authorities, implement appropriate security measures. Ensures data is handled securely and per the rules established by the owner and controller roles |
| **Custodian (Data Steward)** | Responsible for the safe custody, transport, and storage of the data, and implementation of business rules. The IT department typically represents the custodian role. Implements and enforces the security controls established by the data owner and controller |

(Source: Pt6 p.85)

## Validation log
- Extraction: all 25 pages (Pt6 p.61-85) read at 110 dpi; Pt6 p.60 and p.86 read as the Domain Topics and next-section roadmap slides (boundary confirmation).
- Validation pass (2026-10-16): all 25 pages (Pt6 p.61-85) re-rendered at 100 dpi and each re-opened and compared line by line against the note. Pt6 p.61-62 roadmap/Section Topics, p.63 pyramid, p.64-79 definitions/tables, p.80-81 law lists, p.82-85 monitoring, governance structures, and roles all confirmed.
- Corrections made (3, all wording/fidelity): (1) PCI-DSS requirement 11 now recorded as printed ("regular test security systems and processes"); (2) Guidelines sub-bullet restored to "required steps"; (3) Monitoring slide wording restored ("legal compliance practices associated with legal and regulatory compliance") and continuous-monitoring sub-bullets recorded as the printed fragments. No omissions, wrong values, or mis-cited pages found.
- Not independently checked: nothing in range skipped. Section Topics lists "Regulatory/Legal/National" as separate bullets, but the slides give only region/industry law lists (p.80-81).

## Official-objective gap check (5.1 bullets from the slides' Section Topics slide, Pt6 p.62)
*Finalized after validation, 2026-10-16. Note: these are the slides' Section Topics bullets; the official CompTIA bullet list should be cross-checked in `objective_mapping.md`.*

| Official bullet | Status | Where |
|---|---|---|
| Guidelines | Covered | Pt6 p.79 |
| Policies: AUP, information security, BC, DR, IR, SDLC, change management | Covered | Pt6 p.65-69 |
| Standards: password, access control, physical security, encryption | Covered | Pt6 p.71-75 |
| Procedures: change management, onboarding/offboarding, playbooks | Covered (one slide, brief) | Pt6 p.70 |
| External considerations: regulatory, legal, industry, local/regional, national, global | Weak — laws are listed by name/region only; no explanation of requirements; "regulatory" vs "legal" is not distinguished | Pt6 p.80-81 |
| Monitoring and revision | Covered | Pt6 p.82 |
| Governance structures: boards, committees, government entities, centralized/decentralized | Covered | Pt6 p.83-84 |
| Roles: owners, controllers, processors, custodians/stewards | Covered | Pt6 p.85 |

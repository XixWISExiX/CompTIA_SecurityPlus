---
Unit: Change Management Processes and the Impact to Security
Domain: 1.0 General Security Concepts (sub-objective 1.3 — Explain the importance of change management processes and the impact to security)
Source: Pt1 p.52-59 (global 52-59; course slides 1-38 to 1-45). Boundaries: Pt1 p.52 = 1.3 roadmap (1-38); Pt1 p.60 = 1.4 roadmap (Cryptographic solutions).
Extraction_Status: Fully Extracted (all 8 pages read via vision at 80 dpi)
Pages_Done: Pt1 p.52-59
Pages_Remaining: none
Next_Page: none
Validation_Status: Validated (2026-10-16) — p.54-59 re-opened at 130 dpi and compared with the note; p.52-53 confirmed at 80 dpi only; see Validation log
---

## Roadmap and Section Topics (Source: Pt1 p.52-53)

- Pt1 p.52 (1-38) is the Domain 1 roadmap slide with "Change management processes and the impact to security" highlighted; the other items are Types of security controls, Fundamental security concepts, and Cryptographic solutions. (Source: Pt1 p.52)
- Pt1 p.53 (1-39) is the 1.3 Section Topics slide (Source: Pt1 p.53):
  - **Business processes impacting security operation:** Approval process; Ownership; Stakeholders; Impact analysis; Test results; Backout plan; Maintenance window; Standard operating procedure
  - **Technical implications:** Allow lists/deny lists; Restricted activities; Downtime; Service restart; Application restart; Legacy applications; Dependencies
  - **Documentation:** Updating diagrams; Updating policies/procedures
  - **Version control**

## Approval process, stakeholders, ownership (Source: Pt1 p.54)

- The change management **approval process** involves several stages designed to ensure proper assessment and approval of change proposals. (Source: Pt1 p.54)
  1. Change requests usually begin with submitting a **request for change (RFC)**, which outlines the details of the proposed change, including its purpose, scope, and potential impact. (Source: Pt1 p.54)
  2. The change request is reviewed by a designated **change manager or committee**, who assess feasibility, risks, alignment with organizational objectives, and policy compliance. (Source: Pt1 p.54)
  3. After initial review, the request undergoes a formal approval process involving relevant **stakeholders** to ensure consensus and authorization before the change is implemented. Stakeholders listed: management, IT teams, and any impacted departments. (Source: Pt1 p.54)
  4. Throughout the process, documentation and communication are crucial in tracking the status and outcome of approved changes. (Source: Pt1 p.54)
- **Ownership** — individuals or groups primarily responsible for implementing a specific change; examples: project managers, team leaders, or anyone responsible for the change. (Source: Pt1 p.54)
  - Owners are accountable for: ensuring the change is implemented as planned; risks are managed effectively; a clear plan for communication and training associated with the change. (Source: Pt1 p.54)

## Change management concepts (Source: Pt1 p.55)

| Concept | Slide definition | Slide sub-points |
|---|---|---|
| Impact Analysis | The process of identifying and assessing the potential implications of a proposed change, including how it will impact individual users, business processes, or interconnected systems | — |
| Test Results | Before implementation, changes must first be evaluated in a test environment to ensure they work as intended and do not cause issues | Provide valuable insight into the likelihood of success and help identify potential issues without impacting business operations |
| Backout Plans | A contingency plan for reversing changes and returning systems and software to their original state if the implementation plan fails | Helps minimize downtime; reduces the risk of data loss or other severe impacts |
| Maintenance Window | A predefined, recurring time frame for implementing changes | Typically scheduled during periods of low activity to minimize business disruptions |
| Standard Operating Procedure (SOP) | Detailed, written instructions that describe how to carry out routine operations or changes | Ensure changes are implemented consistently and effectively; developed during testing phases |

(Source: Pt1 p.55)

## Technical implications (Source: Pt1 p.56-57)

### Allow lists and deny lists (Source: Pt1 p.56)

- Allow and block lists describe software restriction approaches designed to control computer software. (Source: Pt1 p.56)
- **Allow list** — a list of approved software, hardware, and specific change types (such as routine or low-risk changes) that are not required to go through the entire change management process. (Source: Pt1 p.56)
  - May include specific individuals with change management approval authority. (Source: Pt1 p.56)
  - Helps streamline change management by reducing the time and effort required for trusted or preauthorized changes. (Source: Pt1 p.56)
  - Must be updated via regular reviews to stay current with changing organizational needs. (Source: Pt1 p.56)
- **Deny list** — explicitly blocked software, hardware, and specific change types. (Source: Pt1 p.56)
  - Software and hardware with known security or compatibility issues. (Source: Pt1 p.56)
  - High-risk or high-impact changes. (Source: Pt1 p.56)
  - Might include individuals who are not authorized to implement or approve changes. (Source: Pt1 p.56)
  - Helps prevent unauthorized or risky changes from being implemented. (Source: Pt1 p.56)
- Screenshot on the slide (caption "Source: Screenshot taken by an Education Ecosystem Instructor"): a Carbon Black Protect (Bit9) Security Notification – Unapproved Executable. Text: "An execution was blocked because the file is not pre-approved." Target `sec+_simulation_questions.exe`, process `dfsvc.exe`, file publisher "No Publisher (Valid[No] Trusted[Ineligible:No Cert])", with computer ITE00457669, timestamp 7/28/2020 3:39:33 PM, and a link "Click here to open a self-service App Whitelisting request"; below it a table of numbered Process / Target / Path rows (rows 3-5 marked with a red X: dfsvc.exe and explorer.exe/setup.exe; row 6 a yellow warning icon) and a "Northrop Grumman Corporation – Application Whitelisting" footer. It illustrates an application allow list (whitelist) blocking an unapproved executable. (Source: Pt1 p.56)
  - [Interpretation note] The slide does not caption the screenshot beyond its source line; the "illustrates an allow list" reading is inferred from the dialog's own "pre-approved" and "Whitelisting" wording.

### Restricted activities, restarts, dependencies, legacy applications (Source: Pt1 p.57)

- **Restricted activities** — actions or changes that require additional scrutiny, strict controls, or higher levels of approval/authorization due to their potential impact on critical systems, sensitive data, or regulatory compliance. (Source: Pt1 p.57)
- **Downtime / service restart / application restart** — reconfigurations and patching often require restarting services or applications, leading to downtime. (Source: Pt1 p.57)
- **Dependencies** — services and applications often depend on other software, interfaces, and services to function correctly. (Source: Pt1 p.57)
  - May complicate changes because a service restart in one area may significantly impact another. (Source: Pt1 p.57)
  - Example: if a database server is restarted, all applications that rely on the database will likely experience issues or downtime. (Source: Pt1 p.57)
- **Legacy applications** — legacy applications and systems are often critical to business operations and are difficult to manage. (Source: Pt1 p.57)
  - Many are built using outdated technology. (Source: Pt1 p.57)
  - New software or security updates may be incompatible with legacy systems. (Source: Pt1 p.57)

## Documentation (Source: Pt1 p.58)

Possible documentation impacted by change management (Source: Pt1 p.58):

- **Change Requests** — reviewed and updated to reflect the details and status of the change, including any modifications or approvals during the process.
- **Policies and Procedures** — reviewed and updated to ensure they align with the new processes, guidelines, or controls introduced through the change.
- **System or Process Documentation** — should reflect any changes to systems, applications, or processes. May involve updating system architecture, **diagrams**, process flows, standard operating procedures (SOPs), or user manuals to represent the current state and functionality of the changed system.
- **Configuration Management Documentation** — tracked and documented to maintain an accurate record of the configuration such as servers, networks, or databases.
- **Training Materials** — must be reviewed and updated as warranted.
- **Incident Response and Recovery Plans** — ensure they account for the revised configurations, new dependencies, or recovery procedures resulting from the change.

## Version control (Source: Pt1 p.59)

- **Version Control** — an ID system for each iteration of a software product. (Source: Pt1 p.59)
  - Customer version ID — known to the customer or end user. (Source: Pt1 p.59)
  - Developer build ID — internal build numbers for use in the development process. (Source: Pt1 p.59)
  - Code commits and backups. (Source: Pt1 p.59)
  - Software control management. (Source: Pt1 p.59)
  - Labeling/numbering systems — internal build numbers for use in the development process; made known to the customer or end user. (Source: Pt1 p.59)
  - Differentiates between configurations: major updates (version 1.0); minor updates (version 1.0.2). (Source: Pt1 p.59)
- Slide-wording note: "Code commits and backups" and "Software control management" are bare bullets with no sub-explanation. The slide says "Software control management" (not "source control management"); the note keeps the slide's wording. (Source: Pt1 p.59)

## Validation log
- Extraction: 8 pages read at 80 dpi (p.52-59).
- Validation (separate pass, 2026-10-16): Pt1 p.54-59 re-opened at 130 dpi and compared bullet by bullet (RFC/approval stages, ownership duties, five concept definitions and sub-points, allow/deny list bullets, restricted-activities/restart/dependency/legacy bullets, six documentation items, version-control bullets, page citations). Pt1 p.52-53 (roadmap, Section Topics) confirmed at 80 dpi only.
- Validation corrections (3): added "valuable" to the Test Results sub-point; added computer name and timestamp and the row/icon details of the p.56 screenshot. No wrong values or wrong citations found.
- Not on the slides: no diagrams; one screenshot (p.56). Not an independent second reader.

## Official-objective gap check (1.3 bullets as listed on the slides' Section Topics slide, Pt1 p.53)
| Official bullet | Status | Where |
|---|---|---|
| Business processes: Approval process | Covered | Pt1 p.54 |
| Business processes: Ownership | Covered | Pt1 p.54 |
| Business processes: Stakeholders | Covered (named: management, IT teams, impacted departments) | Pt1 p.54 |
| Business processes: Impact analysis | Covered | Pt1 p.55 |
| Business processes: Test results | Covered | Pt1 p.55 |
| Business processes: Backout plan | Covered | Pt1 p.55 |
| Business processes: Maintenance window | Covered | Pt1 p.55 |
| Business processes: Standard operating procedure | Covered | Pt1 p.55 |
| Technical: Allow lists/deny lists | Covered (with screenshot) | Pt1 p.56 |
| Technical: Restricted activities | Covered (definition only, no examples) | Pt1 p.57 |
| Technical: Downtime | Covered (one sentence, shared with restarts) | Pt1 p.57 |
| Technical: Service restart | Covered (one sentence, shared with downtime) | Pt1 p.57 |
| Technical: Application restart | Covered (one sentence, shared with downtime) | Pt1 p.57 |
| Technical: Legacy applications | Covered | Pt1 p.57 |
| Technical: Dependencies | Covered (database-restart example) | Pt1 p.57 |
| Documentation: Updating diagrams | Covered (named as one item under System or Process Documentation) | Pt1 p.58 |
| Documentation: Updating policies/procedures | Covered | Pt1 p.58 |
| Version control | Covered (bullets only: customer ID, build ID, commits, 1.0 vs 1.0.2) | Pt1 p.59 |

All 18 Section Topics bullets are present. Weak spots, none rising to a gap: restricted activities has no examples; downtime/service restart/application restart share one sentence; version control bullets are unexplained ("Code commits and backups", "Software control management"); no worked change-request scenario. The allow/deny list slide is about change types and software restriction together, a likely exam trap with application allow lists in 2.5/4.5. No outside knowledge added.

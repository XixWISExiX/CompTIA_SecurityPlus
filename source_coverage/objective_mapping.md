# Objective Mapping

Maps every official SY0-701 sub-objective (CompTIA Exam Objectives Version
5.0, 2023) to this repo's notes and source slides. This is **Stage 5**
(Objective Coverage) and is kept strictly separate from OCR extraction, visual
review, note extraction, and validation (Stages 1-4, tracked in
`coverage_tracker.md`). A row's Coverage Status changes only as a direct
consequence of evidence recorded there — never inferred, never defaulted.

## Coverage Status definitions

| Status | Meaning |
|---|---|
| **Not Assessed** | Source material has not yet been sufficiently examined for this sub-objective. Default for every row below. |
| **Absent** | Material *was* reviewed (OCR-scanned and/or visually sampled) and no supporting content was found. |
| **Weakly Covered** | Topic is mentioned but insufficiently explained (incidental bullet, no dedicated treatment). |
| **Unverified** | Candidate coverage identified (OCR guess or written note) but not yet validated against the source render. Do not build practice questions from Unverified content without flagging it. |
| **Well Covered** | Note extracted, **validated** (Stage 4 complete) over its whole range, **and** the official bullets are adequately addressed. A note can be an accurate copy of the slides and still miss official bullets — list those in the Gaps column; do not mark Well Covered while they remain. |

## 1.0 General Security Concepts (12%)

| Sub-Objective | Course Unit Notes | Source Slides | Coverage Status | Confidence | Last Reviewed | Gaps |
|---|---|---|---|---|---|---|
| 1.1 Compare and contrast various types of security controls | — | — | Not Assessed | — | 2026-10-16 | — |
| 1.2 Summarize fundamental security concepts | — | — | Not Assessed | — | 2026-10-16 | — |
| 1.3 Explain the importance of change management processes and the impact to security | — | — | Not Assessed | — | 2026-10-16 | — |
| 1.4 Explain the importance of using appropriate cryptographic solutions | — | — | Not Assessed | — | 2026-10-16 | — |

## 2.0 Threats, Vulnerabilities, and Mitigations (22%)

| Sub-Objective | Course Unit Notes | Source Slides | Coverage Status | Confidence | Last Reviewed | Gaps |
|---|---|---|---|---|---|---|
| 2.1 Compare and contrast common threat actors and motivations | [threat-actors-and-motivations.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md) | Pt2 p.26-32 | Weakly Covered | High (note accuracy) | 2026-10-16 | Motivations (10 terms) and the resources/funding attribute are list-only; no slide maps actors to motivations or capability levels. All six actor types are defined. Held below Well Covered by the strict rule. |
| 2.2 Explain common threat vectors and attack surfaces | [threat-vectors-and-attack-surfaces.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md) | Pt2 p.33-50 | Weakly Covered | High (note accuracy) | 2026-10-16 | Non-human vectors are list-only (image-based, file-based, removable device, client-based vs. agentless, unsupported systems, wired network, open service ports); "attack surface" is never defined in the slides. Wireless, Bluetooth, default credentials, supply chain and all human/social-engineering vectors are well supported. Typosquatting is paired with "bit flipping" on the slide. |
| 2.3 Explain various types of vulnerabilities | [types-of-vulnerabilities.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md) | Pt2 p.51-79 | Weakly Covered | High (note accuracy) | 2026-10-16 | Firmware, legacy and cloud-specific vulnerabilities are thin (a phrase or two each). OS-based and misconfiguration are covered through examples only (OS incident table; Heartbleed/KRACK/BEAST/POODLE). Application, web-based (SQLi, XSS, CSRF), virtualization, supply chain, cryptographic, mobile and zero-day are well supported. OWASP Top 10 table has no edition stated. |
| 2.4 Given a scenario, analyze indicators of malicious activity | [indicators-of-malicious-activity.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md) | Pt2 p.80-100; Pt3 p.1-30 | Weakly Covered | High (note accuracy) | 2026-10-16 | Application attack "forgery" (CSRF/SSRF) is absent from the slides. Credential replay is a single underlined sub-bullet; "resource consumption" is only a phrase inside resource inaccessibility. Malware, physical, network, cryptographic, password attacks and the other indicators are well supported. Slide oddities kept as printed (DRDoS wording, known-ciphertext 'active attack'). |
| 2.5 Explain the purpose of mitigation techniques used to secure the enterprise | [mitigation-techniques-to-secure-the-enterprise.md](../course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md) | Pt3 p.31-45 | Weakly Covered | High (note accuracy) | 2026-10-16 | "Permissions" has no slide. Application allow list is only whitelisting inside the ACL slide. Configuration enforcement is a method list; host-based firewall and HIPS are list-only; default password changes are not stated (only "password management"). Segmentation, ACL, patching, encryption, monitoring, least privilege, decommissioning, port/protocol disabling are covered. |

## 3.0 Security Architecture (18%)

| Sub-Objective | Course Unit Notes | Source Slides | Coverage Status | Confidence | Last Reviewed | Gaps |
|---|---|---|---|---|---|---|
| 3.1 Compare and contrast security implications of different architecture models | — | — | Not Assessed | — | 2026-10-16 | — |
| 3.2 Given a scenario, apply security principles to secure enterprise infrastructure | — | — | Not Assessed | — | 2026-10-16 | — |
| 3.3 Compare and contrast concepts and strategies to protect data | — | — | Not Assessed | — | 2026-10-16 | — |
| 3.4 Explain the importance of resilience and recovery in security architecture | — | — | Not Assessed | — | 2026-10-16 | — |

## 4.0 Security Operations (28%)

| Sub-Objective | Course Unit Notes | Source Slides | Coverage Status | Confidence | Last Reviewed | Gaps |
|---|---|---|---|---|---|---|
| 4.1 Given a scenario, apply common security techniques to computing resources | [computing-resource-security-techniques.md](../course-unit-notes/04-security-operations/computing-resource-security-techniques.md) | Pt4 p.88-100; Pt5 p.1-22 | Weakly Covered | High (note accuracy) | 2026-10-16 | Note validated against all 35 slides. Coverage of the official bullets is partial, hence not Well Covered. Gaps: workstation, cloud, ICS/SCADA, embedded, RTOS, IoT hardening; baseline establish/deploy/maintain; EAP; monitoring is thin. Possible coverage elsewhere (OCR only, unread): g232-245 (2.5), g292-296 (3.1). See note's gap check. |
| 4.2 Explain the security implications of proper hardware, software, and data asset management | [asset-management.md](../course-unit-notes/04-security-operations/asset-management.md) | Pt5 p.23-29 | Well Covered | High | 2026-10-16 | None against the official bullets. Acquisition/procurement and data retention are one definition each (thin but present). |
| 4.3 Explain various activities associated with vulnerability management | [vulnerability-management.md](../course-unit-notes/04-security-operations/vulnerability-management.md) | Pt5 p.30-45 | Weakly Covered | High (note accuracy) | 2026-10-16 | Near-complete: 1 official bullet missing — system/process audit as an identification method (check 5.5). All other bullets covered. Held below Well Covered by the strict rule. |
| 4.4 Explain security alerting and monitoring concepts and tools | [alerting-and-monitoring.md](../course-unit-notes/04-security-operations/alerting-and-monitoring.md) | Pt5 p.46-56 | Well Covered | High | 2026-10-16 | None against the official bullets. Benchmarks is one definition (thin but present). |
| 4.5 Given a scenario, modify enterprise capabilities to enhance security | [enterprise-security-capabilities.md](../course-unit-notes/04-security-operations/enterprise-security-capabilities.md) | Pt5 p.57-84 | Weakly Covered | High (note accuracy) | 2026-10-16 | 1 weak bullet: secure-protocol "transport method" has no dedicated explanation. All other bullets covered. Held below Well Covered by the strict rule. |
| 4.6 Given a scenario, implement and maintain identity and access management | [identity-and-access-management.md](../course-unit-notes/04-security-operations/identity-and-access-management.md) | Pt5 p.85-100; Pt6 p.1-14 | Weakly Covered | High (note accuracy) | 2026-10-16 | 1 weak bullet: "passwordless" (only a passwordless SSH key-login slide). All other bullets covered. Held below Well Covered by the strict rule. |
| 4.7 Explain the importance of automation and orchestration related to secure operations | [automation-and-orchestration.md](../course-unit-notes/04-security-operations/automation-and-orchestration.md) | Pt6 p.15-22 | Well Covered | High | 2026-10-16 | None against the official bullets. "Orchestration" itself is defined only in the 4.8 unit; "integrations" is covered only through the API bullet. |
| 4.8 Explain appropriate incident response activities | [incident-response-activities.md](../course-unit-notes/04-security-operations/incident-response-activities.md) | Pt6 p.23-49 | Well Covered | High | 2026-10-16 | Official-bullet gap check not recorded (note predates that requirement); re-check against the official bullets. |
| 4.9 Given a scenario, use data sources to support an investigation | [data-sources-for-investigation.md](../course-unit-notes/04-security-operations/data-sources-for-investigation.md) | Pt6 p.50-55 | Weakly Covered | High (note accuracy) | 2026-10-16 | 1 weak bullet: OS-specific security logs (Linux and macOS lines are heading-only; Windows only briefly). All other bullets covered. Held below Well Covered by the strict rule. |

## 5.0 Security Program Management and Oversight (20%)

| Sub-Objective | Course Unit Notes | Source Slides | Coverage Status | Confidence | Last Reviewed | Gaps |
|---|---|---|---|---|---|---|
| 5.1 Summarize elements of effective security governance | [effective-security-governance.md](../course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md) | Pt6 p.61-85 | Weakly Covered | High (note accuracy) | 2026-10-16 | External considerations weak: laws listed by name/region/industry only, no requirements; regulatory vs legal not distinguished. "Baseline" appears only on the pyramid; "Due Care" is an unexplained sub-bullet. All other Section Topics bullets covered. |
| 5.2 Explain elements of the risk management process | [risk-management-process.md](../course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md) | Pt6 p.86-100; Pt7 p.1-5 | Weakly Covered | High (note accuracy) | 2026-10-16 | 1 weak bullet: "probability" is never defined separately (only inside qualitative analysis); "likelihood" has a bold label with no definition. All other Section Topics bullets covered, incl. SLE/ALE/ARO formulas with worked examples. Held below Well Covered by the strict rule. |
| 5.3 Explain the processes associated with third-party risk assessment and management | [third-party-risk-assessment-and-management.md](../course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md) | Pt7 p.6-14 | Weakly Covered | High (note accuracy) | 2026-10-16 | Held below Well Covered by the strict rule: supply chain analysis is only described, not explained as a process; MOA/MOU share one definition with no distinction; ISA appears on the slides but not on the Section Topics list. All other Section Topics bullets covered. |
| 5.4 Summarize elements of effective security compliance | — | — | Not Assessed | — | 2026-10-16 | — |
| 5.5 Explain types and purposes of audits and assessments | — | — | Not Assessed | — | 2026-10-16 | — |
| 5.6 Given a scenario, implement security awareness practices | — | — | Not Assessed | — | 2026-10-16 | — |

---
Source: CompTIA Security+ SY0-701 Certification Exam: Exam Objectives Version
5.0, Copyright © 2023 CompTIA, Inc. Fetched and verified directly from
CompTIA's published objectives PDF on 2026-10-16.

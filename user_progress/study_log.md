# Study Log

## 2026-10-16 — Session 1: Repo bootstrap + first validated unit

**Scope completed:**
- Scaffolded the full repo structure (`course-unit-notes/` with the 5
  official domain folders, `glossary/`, `user_progress/`, `source_coverage/`,
  `CLAUDE.md`, `AGENTS.md`, `README.md`).
- Verified official SY0-701 Exam Objectives Version 5.0 (CompTIA, 2023)
  directly from CompTIA's own published PDF; recorded all 28 sub-objectives
  across the 5 domains into `source_coverage/objective_mapping.md`
  (all starting "Not Assessed").
- User installed `tesseract-ocr` themselves mid-session; ran a full bulk OCR
  pass across all 659 source pages in the background (hybrid extraction
  approach).
- Initial vision sampling across all 7 source PDF parts suggested a rough
  structural map, but the completed OCR pass revealed something more
  precise: every domain has an exact "Domain Topics N.0 &lt;name&gt;" divider
  slide (appearing once at the domain's start, once as an end-of-domain
  recap). Grepping the OCR output for these pinned all 5 domain boundaries
  exactly (High confidence): global pages 1-15 are course
  overview/logistics (pre-Domain 1 content); **1.0** = 16-124; **2.0** =
  125-249; **3.0** = 250-386; **4.0** = 387-549; **5.0** = 550-659. Notably,
  Domain 1.0 (General Security Concepts, 12% weight) runs much deeper into
  Pt2 than the initial sampling pass suggested, because its cryptography
  sub-objective (1.4) is slide-heavy.
- Fully extracted and validated **sub-objective 4.8 (Incident Response
  Activities)** — every one of its 27 source pages (Pt6 p.23-49) was
  individually read via vision, not sampled or OCR-only. Written to
  `course-unit-notes/04-security-operations/incident-response-activities.md`
  with inline page citations. `objective_mapping.md` row updated to
  **Well Covered / High confidence**.
- Seeded `glossary/README.md` with real terms from the validated unit.
- Wrote 10 original practice questions (scenario/ordering/term-ID style)
  covering only the validated unit; delivered to the user, answers pending.
- Built `source_coverage/coverage_tracker.md` with all 659 page rows:
  domain-zone guesses from this session's structural evidence, OCR topic
  guesses where the background OCR pass completed in time, and accurate
  Visual_Reviewed/Note_Extracted/Validated flags (true only for pages
  actually reviewed/extracted this session).

**Explicitly not done this session:** extraction of the other 27
sub-objectives; full-domain validation; Day 6 mock exam; resolving the two
Low-confidence domain-boundary zones; grading the practice batch (pending
user response).

**Next session should start with:** grading Practice Batch 1 if not already
done, then either (a) continuing extraction into an adjacent high-value unit
(4.9 Data sources, or circling back to 2.0/4.0 given their exam weight), or
(b) following whatever the bootcamp has covered most recently, per the
standing rule in `CLAUDE.md`.

---

## Session 2026-10-16 (extraction batch 1)

- Plan agreed with the user: extraction in exam-weight order (Domain 4 → 2 → 5 → 3 → 1), one sub-objective per batch, every page read inline by vision.
- Fixed a boundary overlap: g523 belongs to 4.8 (it is the 4.8 roadmap slide). Section rule: roadmap slide to the page before the next roadmap slide. 4.7 = g515-522.
- Extracted **4.1** (Pt4 p.88-100 + Pt5 p.1-22, 35 pages, all read) into `course-unit-notes/04-security-operations/computing-resource-security-techniques.md`.
  - Validation is partial: only Pt4 p.94 and Pt5 p.18 were re-checked at higher resolution. The full independent re-comparison is still to do.
  - `objective_mapping.md` row 4.1 = **Unverified**. Official-bullet gaps recorded (workstation, cloud, ICS/SCADA, embedded, RTOS, IoT hardening; baseline lifecycle detail; EAP).
- `objective_mapping.md` gained a Gaps column. The 4.8 row is flagged: its official-bullet gap check was never recorded.
- Noted: CLAUDE.md lists `prompts/01-extract-course-material.md`, which is not in `prompts/`.
- **Next:** full validation pass of 4.1, then 4.2 (g423-429), 4.3, 4.4, 4.5, 4.6, 4.7, 4.9. Resume state is at the top of `coverage_tracker.md`.

- **4.1 validated** (all 35 pages re-opened and compared). Status Weakly Covered: the slides skip workstation/cloud/ICS/SCADA/embedded/RTOS/IoT hardening and the baseline establish-deploy-maintain steps. Possible coverage elsewhere (OCR only): g232-245, g292-296.
- **4.2 extracted and validated** end to end (Pt5 p.23-29, 7 pages) → `course-unit-notes/04-security-operations/asset-management.md`. Well Covered; all official bullets present. Glossary updated.
- Workflow change from the user: each sub-objective now runs end to end (extract → validate against every page → gap check → tracking files) before the next one starts. Progress is saved about every 5 pages.
- **Next:** 4.3 Vulnerability management (g430-445 = Pt5 p.30-45).
- **4.3 extracted and validated** end to end (Pt5 p.30-45, 16 pages) → `course-unit-notes/04-security-operations/vulnerability-management.md`. Weakly Covered under the strict rule: one official bullet (system/process audit as an identification method) has no slide; everything else covered. Glossary updated.
- **Next:** 4.4 Security alerting and monitoring (g446-456 = Pt5 p.46-56).
- **4.4 extracted and validated** end to end (Pt5 p.46-56, 11 pages) → `course-unit-notes/04-security-operations/alerting-and-monitoring.md`. Well Covered; no official-bullet gaps. Glossary updated.
- **Next:** 4.5 Modify enterprise capabilities to enhance security (g457-484 = Pt5 p.57-84).
- **4.5 extracted and validated** end to end (Pt5 p.57-84, 28 pages) → `course-unit-notes/04-security-operations/enterprise-security-capabilities.md`. Weakly Covered under the strict rule: one official bullet (secure-protocol "transport method") has no dedicated slide. Glossary updated.
- **Next:** 4.6 Identity and access management (g485-514 = Pt5 p.85-100 and Pt6 p.1-14).
- **4.6 extracted and validated** end to end (Pt5 p.85-100 + Pt6 p.1-14, 30 pages) → `course-unit-notes/04-security-operations/identity-and-access-management.md`. Weakly Covered under the strict rule: one official bullet ("passwordless") has only a passwordless-SSH slide. Glossary updated.
- **Next:** 4.7 Automation and orchestration (g515-522 = Pt6 p.15-22), then 4.9 (g550-560), then Domain 2.
- **4.7 extracted and validated** end to end (Pt6 p.15-22, 8 pages) → `course-unit-notes/04-security-operations/automation-and-orchestration.md`. Well Covered; no official-bullet gaps. Glossary updated.
- **Next:** 4.9 Data sources to support an investigation (g550-560 = Pt6 p.50-60). Then Domain 2 (2.1-2.5).
- **4.9 extracted and validated** end to end (Pt6 p.50-55, 6 pages; p.56-60 read as non-objective Domain 4 recap / logo / Module 5 title slides) → `course-unit-notes/04-security-operations/data-sources-for-investigation.md`. Weakly Covered under the strict rule: OS-specific security logs are thin (Linux and macOS lines are headings only). Glossary updated.
- **Domain 4 extraction is complete** (4.1-4.9). Statuses: Well Covered — 4.2, 4.4, 4.7, 4.8 (4.8's official-bullet gap check is still to be recorded); Weakly Covered — 4.1, 4.3, 4.5, 4.6, 4.9 (each with listed gaps).
- **Next:** Domain 2 in order: 2.1 (g126-132 = Pt2 p.26-32), then 2.2-2.5. First step is to confirm the 2.1 boundary visually.
- **2.1 extracted and validated** end to end (Pt2 p.26-32, 7 pages) → `course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md`. Weakly Covered under the strict rule: motivations and resources/funding are list-only; no actor-to-motivation mapping. Glossary updated. Boundary confirmed: Pt2 p.33 is the 2.2 roadmap.
- **Next:** 2.2 Threat vectors and attack surfaces (g133-150 = Pt2 p.33-50).

- **2.2 extracted and validated** end to end (Pt2 p.33-50, 18 pages; Pt2 p.51 confirmed as the 2.3 roadmap) → `course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md`. Weakly Covered under the strict rule: non-human vectors (image-based, file-based, removable device, client-based vs. agentless, unsupported systems, wired, open ports) are list-only, and "attack surface" is never defined. Human-vector/social-engineering, wireless, Bluetooth, default-credential and supply-chain bullets are covered. Validation found no transcription errors; one diagram label on Pt2 p.44 stays flagged as unconfirmed. Glossary updated.
- **Next:** 2.3 Types of vulnerabilities (g151-180 provisional = Pt2 p.51-80; confirm the end against the 2.4 roadmap, OCR suggests g181). Then 2.4 and 2.5, Domain 5 (g561-659), Domain 3 (g251-385), Domain 1 (g17-123).

- **2.3 extracted and validated** end to end (Pt2 p.51-79, 29 pages; Pt2 p.80 confirmed as the 2.4 roadmap) → `course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md`. Weakly Covered under the strict rule: firmware, legacy and cloud-specific vulnerabilities are thin; OS-based and misconfiguration covered through examples only. Validation corrected one wrong diagram description (p.56 pivoting) and added missing screenshot detail (p.71). Two [CONFLICT] items kept as printed (p.54 memory-leak bullet; p.72 "EOS" used for both End of Sale and End of Support). Glossary updated.
- **Next:** 2.4 Indicators of malicious activity (starts at g180 = Pt2 p.80; Section Topics at Pt2 p.81). Then 2.5, Domain 5 (g561-659), Domain 3 (g251-385), Domain 1 (g17-123).

- **2.4 extracted and validated** end to end (Pt2 p.80-100 + Pt3 p.1-30, 51 pages; Pt3 p.31 confirmed as the 2.5 roadmap) → `course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md`. Weakly Covered under the strict rule: "forgery" is absent; credential replay and resource consumption are thin. Validation (independent subagent pass at 130 dpi) corrected a "complied" [CONFLICT] marker, one omitted Ad Fraud bullet, and two diagram descriptions. Glossary updated.
- **2.5 extracted and validated** end to end (Pt3 p.31-45, 15 pages; p.46-47 recap/logo, no unit content) → `course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md`. Weakly Covered under the strict rule: "permissions" has no slide; application allow list, configuration enforcement, host firewall/HIPS and default password changes are thin. Validation filled in the exact CIDR table values and fixed several diagram descriptions. Glossary updated.
- **Domain 2 extraction is complete** (2.1-2.5, all Weakly Covered).
- **Next:** ask which of Domain 5 (g561-659, exam-weight order) or the bootcamp's current topic to take next; then Domain 3 (g251-385), Domain 1 (g17-123).

- **5.1 extracted (validation pending)** (Pt6 p.61-85, 25 pages; Pt6 p.86 confirmed as the 5.2 roadmap) -> `course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md`. Not validated, no coverage status assigned yet.
- **Next:** validate 5.1 (re-open every page against the note), then 5.2 Risk management process (g586-605).

- **5.1 validated** (2026-10-16): all 25 pages (Pt6 p.61-85) re-rendered at 100 dpi and visually compared; 3 minor wording-fidelity corrections (PCI-DSS req. 11, Guidelines "required steps", Monitoring slide wording). Weakly Covered under the strict rule: laws in External considerations are names only; "baseline" defined only on the pyramid; "Due Care" unexplained. Glossary updated.
- **Next:** 5.2 Risk management process (g586-605 = Pt6 p.86-Pt7 p.5; 5.3 roadmap at g606).

- **5.2 extracted and validated** (2026-10-16): Pt6 p.86-100 + Pt7 p.1-5 (20 pages; Pt7 p.6 confirmed as the 5.3 roadmap) -> `course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md`. Weakly Covered under the strict rule: "probability" is never defined separately. Dense pages re-rendered at 140 dpi; SLE/ALE table recomputed; no corrections needed. Validation was a same-session re-check, not an independent reader. Flagged as printed: garbled RCA definition; Exception = short-term / Exemption = longer-term; Deterrence listed as a fifth strategy.
- **Next:** 5.3 Third-party risk assessment and management (roadmap Pt7 p.6 = g606).

- **5.3 recorded retroactively** (2026-10-16): the 5.3 session (Pt7 p.6-14, 9 pages) -> `third-party-risk-assessment-and-management.md`, validated and Weakly Covered per `objective_mapping.md`, had no study-log entry; added here. Glossary has no 5.3 section yet.
- **5.4 extracted and validated** (2026-10-16): Pt7 p.16-28 (13 pages; Pt7 p.15 and p.29 confirmed as the 5.4 and 5.5 roadmaps) -> `course-unit-notes/05-security-program-management-and-oversight/effective-security-compliance.md`. Weakly Covered under the strict rule: "loss of license" is software-licensing only; local/national/global legal implications are not itemized. Validation was a same-session re-check at 100 dpi (SOC table cells re-checked), not an independent reader; no corrections needed. Glossary updated.
- **Next:** 5.5 Audits and assessments (roadmap Pt7 p.29 = g629; Section Topics Pt7 p.30), then 5.6, Domain 3 (g251-385), Domain 1 (g17-123).

- **5.5 extracted and validated** (2026-10-16): Pt7 p.29-46 (18 pages; Pt7 p.29 = 5.5 roadmap, Pt7 p.47 = 5.6 roadmap) -> `course-unit-notes/05-security-program-management-and-oversight/audits-and-assessments.md`. Weakly Covered under the strict rule: pen-test "defensive" and "integrated" are one-sentence definitions only. Validation was a same-session re-check against the renders, not an independent reader. Flagged as printed: External Audit vs Third-party Audit wording (p.35 vs p.34); social engineering listed under passive reconnaissance (p.41). Glossary updated.
- **Next:** 5.6 Security awareness practices (roadmap Pt7 p.47 = g647; Section Topics Pt7 p.48), then Domain 3 (g251-385), Domain 1 (g17-123).

- **5.6 extracted and validated** (2026-10-16): Pt7 p.47-56 (10 pages; Pt7 p.57 = Domain 5 recap, no unit content) -> `course-unit-notes/05-security-program-management-and-oversight/security-awareness-practices.md`. Weakly Covered under the strict rule: "recognizing a phishing attempt" and "responding to reported suspicious messages" are named but not itemized. Validation was a same-session re-check against the 80 dpi renders, not an independent reader; no source errors found. Glossary updated.
- **Domain 5 extraction is complete** (5.1-5.6, all Weakly Covered).
- **Next:** Domain 3 (g251-385) — ask which section the bootcamp is on; then Domain 1 (g17-123).

## 2026-10-16 — Domain 3 extraction begins (3.1)

- User confirmed the bootcamp is on 3.1 Architecture models.
- **3.1 extracted and validated**: Pt3 p.51-100 (50 pages; g251-300; Pt3 p.50 = Domain 3 recap, Pt4 p.1 = 3.2 roadmap) -> `course-unit-notes/03-security-architecture/security-implications-of-architecture-models.md`. Weakly Covered: on-premises, hybrid considerations, third-party vendors, logical segmentation, and the considerations list are thin. Source conflict recorded (Pt3 p.97 availability footnote vs. table). Validation was a same-session re-check against the renders, not an independent second reader.
- Files updated: coverage_tracker.md (g250-300 flags and resume state), objective_mapping.md (3.1 row), glossary/README.md.
- **Next:** 3.2 (Pt4 p.1 = 3.2 roadmap, slide 3-53) after confirming bootcamp pace; then 3.3, 3.4, then Domain 1 (g17-123). A 10-15 question practice batch on 3.1 is available on request.

## 2026-10-16 — Domain 3 extraction continues (3.2)

- User confirmed the bootcamp is on 3.2.
- **3.2 extracted and validated**: Pt4 p.1-39 (39 pages; g301-339; Pt4 p.1 = 3.2 roadmap, Pt4 p.40 = 3.3 roadmap) -> `course-unit-notes/03-security-architecture/security-principles-to-secure-enterprise-infrastructure.md`. Weakly Covered: Connectivity is named but never discussed; security zones, jump server, sensors, NGFW, TLS tunneling, SASE components, and active/passive and inline/tap are thin. Validation was a same-session re-check against the renders (Pt4 p.39 FAN diagram re-read at 150 dpi), not an independent second reader; no transcription errors found. Source quirks recorded in the note (NIDS "inline" vs TAP/SPAN; IPTables/IPChains as application firewalls).
- Files updated: coverage_tracker.md (g301-339 flags, resume state), objective_mapping.md (3.2 row), glossary/README.md.
- **Next:** 3.3 Concepts and strategies to protect data (Pt4 p.40 = roadmap, Section Topics p.41) after confirming bootcamp pace; then 3.4, then Domain 1 (g17-123). A 10-15 question practice batch on 3.2 is available on request.

## 2026-10-16 — Domain 3 extraction continues (3.3)

- User confirmed the bootcamp is on 3.3.
- **3.3 extracted and validated**: Pt4 p.40-49 (10 pages; g340-349; Pt4 p.40 = 3.3 roadmap, Pt4 p.50 = 3.4 roadmap) -> `course-unit-notes/03-security-architecture/concepts-and-strategies-to-protect-data.md`. Weakly Covered: geolocation is not defined; geographic restrictions, encryption, hashing, obfuscation, segmentation, and permission restrictions are one-line definitions. Validation was a same-session re-check (p.43, p.45, p.49 re-rendered at 110 dpi; others at 80 dpi), not an independent second reader; no transcription errors found. Source quirks recorded in the note (labels with Secret/Top Secret aliases, "Data in Motion" vs "in transit", sovereignty grammar slip).
- Files updated: coverage_tracker.md (g340-349 flags, resume state), objective_mapping.md (3.3 row), glossary/README.md.
- **Next:** 3.4 Resilience and recovery (Pt4 p.50 = roadmap, Section Topics p.51) after confirming bootcamp pace; then Domain 1 (g17-123). A 10-15 question practice batch on 3.3 is available on request.

## 2026-10-16 — Domain 3 extraction completes (3.4)

- User confirmed 3.4 as the next unit (tracker's recommended next).
- **3.4 extracted and validated**: Pt4 p.50-82 (33 pages; g350-382; Pt4 p.50 = 3.4 roadmap, p.83 = Domain 3 recap, p.84-85 logos, p.86 = Module 4 title) -> `course-unit-notes/03-security-architecture/resilience-and-recovery-in-security-architecture.md`. Weakly Covered: snapshots (one line under non-persistence) and recovery (no dedicated slide; RTO/RPO not in range) are thin. Validation was a same-session re-check (p.71, p.73, p.81 re-rendered at 110 dpi; others at 80 dpi), not an independent second reader; one correction (RAID summary "Ø" marker on level 0). Source quirks recorded (Fail over = full-interruption/live testing; three COOP descriptions; RAID 4 and 0+1 only on the summary slide; backup/restore time column order unstated).
- **Domain 3 extraction is complete** (3.1-3.4, all Weakly Covered).
- Files updated: coverage_tracker.md (g350-382 flags, resume state), objective_mapping.md (3.4 row), glossary/README.md.
- **Next:** Domain 1 (g17-123) — ask which sub-objective the bootcamp is on. A 10-15 question practice batch on 3.4 is available on request.

## 2026-10-16 — Domain 1 extraction begins (1.1)

- User asked to "collect the next unit"; the tracker's queue put Domain 1 (g17-123) next, 1.1 first by page order. The bootcamp-pace question was not asked this session; that choice followed the tracker queue.
- **1.1 extracted and validated**: Pt1 p.17-20 (4 pages; Pt1 p.16 = Domain 1 "Domain Topics", Pt1 p.17 = 1.1 roadmap, Pt1 p.21 = 1.2 roadmap) -> `course-unit-notes/01-general-security-concepts/types-of-security-controls.md`. Well Covered: all ten official bullets present. Validation was a same-session re-check (p.18-20 at 130 dpi, p.17 at 80 dpi), not an independent second reader; no transcription errors found.
- Also visually reviewed (80 dpi) but **not yet extracted or validated**: Pt1 p.21-52 (1.2 range, p.21-51; p.52 = 1.3 roadmap). Tracker marks these Visual_Reviewed only.
- Files updated: coverage_tracker.md (g16-20, g21-52 visual flags), objective_mapping.md (1.1 row), glossary/README.md.
- **Next:** 1.2 Fundamental security concepts (Pt1 p.21-51), then 1.3 (Pt1 p.52-59), 1.4. A 10-15 question practice batch on 1.1 is available on request.

## 2026-10-16 — Domain 1 extraction continues (1.2)

- User asked to "collect the next unit"; the tracker's queue put 1.2 next. The bootcamp-pace question was not asked (only Domain 1 remains, so the order follows page order).
- **1.2 extracted and validated**: Pt1 p.21-51 (31 pages; g21-51; Pt1 p.21 = 1.2 roadmap, p.52 = 1.3 roadmap) -> `course-unit-notes/01-general-security-concepts/fundamental-security-concepts.md`. Weakly Covered: "Authenticating people", "Authenticating systems" and "Authorization models" are Section Topics with no dedicated slides; deception content is definition-level. Validation was a same-session re-check (p.35 and p.49 re-rendered at 130 dpi; others at 80 dpi), not an independent second reader; no transcription errors found. Source quirks recorded in the note (p.23 "5 Pillars" over three pillars; p.37 PDP routing wording; "Charged Couple Discharge"; LDAP "TCP or UDP 389").
- Files updated: coverage_tracker.md (g21-51 flags, resume state), objective_mapping.md (1.2 row), glossary/README.md.
- **Next:** 1.3 Change management (Pt1 p.52-59), then 1.4 Cryptographic solutions (Pt1 p.60 - Pt2 p.24, provisional). A 10-15 question practice batch on 1.2 is available on request.

## 2026-10-16 — Domain 1 extraction continues (1.3)

- User asked to "collect the next unit"; the tracker's queue put 1.3 next. The bootcamp-pace question was not asked (only Domain 1 remains, so the order follows page order).
- **1.3 extracted and validated**: Pt1 p.52-59 (8 pages; g52-59; Pt1 p.52 = 1.3 roadmap, p.53 = Section Topics, p.60 = 1.4 roadmap) -> `course-unit-notes/01-general-security-concepts/change-management-processes.md`. Well Covered: all 18 Section Topics bullets present, though several are brief. Validation was a same-session re-check (p.54-59 re-rendered at 130 dpi; p.52-53 at 80 dpi only), not an independent second reader; three small corrections (a missing word and screenshot details). Source quirk recorded: "Software control management" wording on p.59.
- Files updated: coverage_tracker.md (g53-59 flags, resume state), objective_mapping.md (1.3 row), glossary/README.md.
- **Next:** 1.4 Cryptographic solutions (Pt1 p.60 - Pt2 p.23, provisional boundaries). A 10-15 question practice batch on 1.3 is available on request.

## 2026-10-16 — Domain 1 extraction completes (1.4)

- User asked to "collect the next unit"; the tracker's queue put 1.4 next. The bootcamp-pace question was not asked (only Domain 1 remained).
- **1.4 extracted and validated**: Pt1 p.60 - Pt2 p.20 (61 pages; g60-120; Pt2 p.21 = Domain 1 recap, p.22-23 logos, p.24 = Module 2 title; the provisional end g123 was corrected) -> `course-unit-notes/01-general-security-concepts/cryptographic-solutions.md`. Weakly Covered: encryption levels beyond FDE/file/SED, key exchange, "key management system", and self-signed vs third-party certificates are thin. Validation was a same-session re-check (number- and table-heavy pages at 130 dpi, others 80 dpi), not an independent second reader; no transcription corrections. Source conflicts recorded (DH signatures/non-repudiation; 3DES 112 vs 168 bit; SHA-2 vs SHA-3 wording).
- The session hit a usage limit mid-validation and resumed; no work was repeated.
- Files updated: coverage_tracker.md (g60-123 flags, resume state), objective_mapping.md (1.4 row), glossary/README.md.
- **Domain 1 extraction is complete; all five domains (28 units) are extracted and validated.**
- **Next:** practice batches (10-15 questions) on validated units; ask which bootcamp topic is current. A batch on 1.4 is available on request.

## 2026-10-16 — Extraction resumed: closing the 4.8 gap check

- User asked to resume extraction. The tracker showed all 28 units extracted and validated; the only open extraction item was the missing 4.8 official-bullet gap check.
- Recorded the 4.8 gap check in `incident-response-activities.md` (retroactive, from the validated note; slides not re-rendered). 4.8 changed from Well Covered to **Weakly Covered** (Detection/Analysis not split; tabletop/simulation are one-liners). Updated objective_mapping.md and coverage_tracker.md accordingly.
- No slide extraction remains. Pt1 p.1-15 (course overview/logistics) is non-exam content and intentionally has no unit.
- **Next:** practice batches (10-15 questions) on validated units; ask which bootcamp topic is current.

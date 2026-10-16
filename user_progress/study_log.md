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

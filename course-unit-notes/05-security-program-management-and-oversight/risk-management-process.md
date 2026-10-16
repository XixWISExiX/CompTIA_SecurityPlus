---
Unit: Risk Management Process
Domain: 5.0 Security Program Management and Oversight (sub-objective 5.2 — Explain elements of the risk management process)
Source: Pt6 p.86-100 + Pt7 p.1-5 (global 586-605; course slides 5-28 to 5-47). Boundaries: Pt6 p.86 = 5.2 roadmap (5-28); Pt7 p.6 = 5.3 roadmap (5-48, "Third-party risk assessment and management" highlighted)
Extraction_Status: Fully Extracted (all 20 pages read via vision at 100 dpi)
Pages_Done: Pt6 p.86-100, Pt7 p.1-5
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — all 20 pages compared against renders; dense pages re-rendered at 140 dpi (see Validation log)
---

## Roadmap and Section Topics (Source: Pt6 p.86-87)

- Pt6 p.86 (5-28) is the roadmap slide with "Risk management process" highlighted. (Source: Pt6 p.86)
- Pt6 p.87 (5-29) is the 5.2 Section Topics slide (Source: Pt6 p.87):
  - Risk identification
  - Risk assessment: ad hoc; recurring; one-time; continuous
  - Risk analysis: qualitative; quantitative; single loss expectancy (SLE); annualized loss expectancy (ALE); annualized rate of occurrence (ARO); probability; likelihood; exposure factor; impact
  - Risk register: key risk indicators; risk owners; risk threshold
  - Risk tolerance
  - Risk appetite: expansionary; conservative; neutral
  - Risk management strategies: transfer; accept (exemption, exception); avoid; mitigate
  - Risk reporting
  - Business impact analysis: recovery time objective (RTO); recovery point objective (RPO); mean time to repair (MTTR); mean time between failures (MTBF)

## Risk Management Process — 5-step flow (Source: Pt6 p.88)

Diagram: five rounded boxes in a left-to-right arrow (Source: Pt6 p.88):

1. Step 1: Identify Mission Essential Functions
2. Step 2: Identify Vulnerabilities
3. Step 3: Identify Threats and Threat Likelihood
4. Step 4: Analyze Business Impacts
5. Step 5: Identify Risk Response

## Risk Identification (Source: Pt6 p.89)

- **Risk Identification** — the specific process of listing sources of risk due to threats and vulnerabilities. (Source: Pt6 p.89)
  - The foundation for risk assessment and management practices.
  - Allows organizations to make informed decisions regarding resource allocation, risk mitigation strategies, and overall risk management practices.
- **Risk identification methods**: vulnerability assessments; penetration testing; security audits; threat intelligence, and other methods. (Source: Pt6 p.89)
- **Recognizing risks**: malware attacks; phishing attempts; insider threats; equipment failures; software vulnerabilities; nontechnical risks (inadequate policies or training). (Source: Pt6 p.89)

## Security/Risk Definitions (Source: Pt6 p.90)

| Term | Slide definition |
|---|---|
| **Asset** | Valuable resource to protect |
| **Threat** | Circumstance or event with the potential to adversely impact an organization |
| **Risk** | A measure of the **likelihood** of occurrence and potential impact of a threat; sub-bullets: **Likelihood**; Impact — severity of the damage in dollars |
| **Vulnerability** | A **weakness** in a target that can potentially be exploited by a threat source (lack of safeguard) |
| **Exploit** | Leveraging a vulnerability to complete the attack mission |

(Source: Pt6 p.90) Callout bar: "The key to effective security is management of organizational risk." (Source: Pt6 p.90) The "Likelihood" sub-bullet has no definition text beyond its bold label. [GAP]

## Risk Awareness, RCA, RCSA (Source: Pt6 p.91)

- **Risk Awareness** — ensures business stakeholders understand each risk scenario and articulate it such that the cause and effect can clearly be understood by the owner of the asset. (Source: Pt6 p.91)
- **Risk and Control Assessment (RCA)** — an **external process led by third-party** (underlined) to lead to conduct risk assessment for an organization (wording as printed). (Source: Pt6 p.91)
- **Risk and Control Self-Assessment (RCSA)** — an **internal process** (underlined) in the Enterprise Risk Management (ERM) to identify, assess and prioritize risks and the effectiveness with which controls mitigate those risks, based on RMF or ISO 31000 (31K). (Source: Pt6 p.91)

## Threat Sources (Source: Pt6 p.92)

- **Environmental** — earthquakes; floods; tornados & tsunamis; wildfires. (Source: Pt6 p.92)
- **Man-Made** — power failures; system crashes/failures; intentional actions (setting off smoke detectors; pulling fire alarms). (Source: Pt6 p.92)
- **External** — introduced from the outside of an organization. (Source: Pt6 p.92)
- **Internal** — introduced from the inside of an organization, often from disgruntled employees, insider threat/malicious insider, accidental non-malicious or intentional malicious, and can include contractors granted temporary access. (Source: Pt6 p.92)
- Slide images: a tornado photo and a city skyline photo (decorative). (Source: Pt6 p.92)

## Risk Assessment (Source: Pt6 p.93)

- **Risk Assessment** — the process of identifying risks, analyzing them, developing a response strategy for them, and mitigating their future impact. (Source: Pt6 p.93)
  - Evaluates previously identified risks to determine their potential impact on the organization.
  - **Ad hoc** — conducted as needed, often in response to specific incidents: news of a new, actively exploited zero-day vulnerability; environmental changes; system upgrades.
  - **One-time** — carried out at a particular point in time: during the implementation of a new system (or process); an independent assessment of an organization's operational maturity.
  - **Recurring** — scheduled at regular intervals: annually, quarterly, or monthly; audits, compliance checks, or vulnerability scans.
  - **Continuous** — constantly evaluate risks; supported by specialized tools that produce real-time data: agent-based vulnerability scanning platforms; Intrusion Detection Systems (IDS).

## Risk Analysis (Source: Pt6 p.94)

- **Risk Analysis** — the process for qualifying or quantifying the likelihood and impact of a factor. (Source: Pt6 p.94)
  - Describes the process of identifying and evaluating potential risks and the characteristics that define them.
  - Aims to understand the nature and scope of risks by examining their causes, consequences, and concerns.
- **Qualitative** — a process of subjective (non-numerical) assessment of a project, program, or business. (Source: Pt6 p.94)
  - Involves the use of expert judgment, experience, or group consensus to compare the impact of the threat with the probability of occurrence.
  - **Delphi** — a method that allows people to express their opinions, thoughts, and ideas **anonymously** (underlined; "suggestion box").
- **Quantitative Risk** — a process of objective (numeric) assessment of a project, program or business. (Source: Pt6 p.94)
  - Relies on historical data/trends, models, metrics to measure risk levels and predict future outcomes.
- **Two matrix images** (right side of slide) (Source: Pt6 p.94):
  - Top: 5×5 color grid, Likelihood on the vertical axis (5 Near Certainty, 4 Highly Likely, 3 Possible, 2 Unlikely, 1 Remote) and Consequence on the horizontal axis (1 Minimal, 2 Moderate, 3 Significant, 4 Extensive, 5 Severe). Colors by row (left→right): likelihood 5 = green, yellow, yellow, red, red; 4 = green, green, yellow, red, red; 3 = green, green, green, yellow, yellow; 2 = green, green, green, green, yellow; 1 = all green.
  - Bottom: 5×5 numeric matrix, Likelihood (vertical, 1-5) × Impact (horizontal, 1-5), each cell = likelihood × impact (e.g., 5×5 = 25 red; 4×4 = 16 orange; 3×3 = 9 yellow; 1×1 = 1 dark green; 5×1 = 5 blue, 1×5 = 5 blue).

## Risk Calculations (Source: Pt6 p.95)

| Term | Unit | Slide definition |
|---|---|---|
| Asset Value (AV) | $ | value of a given asset |
| Exposure Factor (EF) | % | measure of magnitude of a loss of an asset |
| Single Loss Expectancy (SLE) | $ | how much is lost in a single event |
| Annual Rate of Occurrence (ARO) | # | how often an event happens per year |
| Annual Loss Expectancy (ALE) | $ | yearly cost due to risk (printed in red) |

- **SLE = Asset Value (AV) × Exposure Factor (EF%)** (Source: Pt6 p.95)
- **ALE = SLE × ARO** (Source: Pt6 p.95)
- Slide spells out "Annual Loss Expectancy" here; the Section Topics slide says "annualized loss expectancy" and "annualized rate of occurrence." Recorded as printed. (Source: Pt6 p.87, p.95)

## Risk Calculations — Examples (Source: Pt6 p.96)

- Worked tornado example (Source: Pt6 p.96):
  1. A tornado is estimated to damage 50% (.50) of a facility if it hits the facility.
  2. The value of the facility is $200,000.
  3. The probability is one tornado in ten (.10) years.
  - SLE = AV × EF → $200,000 × .50 = **$100,000**
  - ALE = SLE × ARO → $100,000 × .10 = **$10,000** ("Averaged over ten years the ALE is $10,000")
  4. "Management should not spend over $10,000 per year in countermeasures trying to protect against this risk."
- Formula chips at bottom: SLE = AV × EF; ALE = SLE × ARO; **ALE = AV × EF × ARO**. (Source: Pt6 p.96)
- Table (Source: Pt6 p.96):

| Asset | Threat | AV | EF (%) | SLE | ARO | ALE |
|---|---|---|---|---|---|---|
| Facility | Fire | $560,000 | 40% | $224,000 | 0.25 | $56,000 |
| Trade Secret | Stolen | $43,500 | 92% | $40,020 | 0.75 | $30,015 |
| File Server | Failed | $11,500 | 100% | $11,500 | 0.50 | $5,750 |
| Data | Virus | $8,900 | 70% | $6,230 | 0.80 | $4,984 |
| Customer Credit Card Info | Stolen | $325,500 | 83% | $270,165 | 0.60 | $162,099 |

(Arithmetic checked against the printed formulas: all five rows are consistent.)

## Risk Register (Source: Pt6 p.97-98)

- **Risk Register** — a document highlighting the results of risk assessments in an easily comprehensible format. (Source: Pt6 p.97)
  - Includes information regarding risks, their severity, the associated **owner of the risk** (underlined), and all identified mitigation strategies.
  - A "traffic light" grid; a "heat map" matrix.
  - Columns: impact ratings; likelihood ratings; date of identification; description; countermeasures; **owner** (bold); route for escalation; status.
- Image on slide: "Simple Safety Risk Register Template" screenshot (smartsheet.com/risk-register-templates) with columns Risk Description, Impact Description, Impact Level, Probability Level, Priority Level (Impact × Probability; "Address highest first"), Mitigation Notes, Owner; two example rows (slippery floor leaks — priority 15; shortage of eye protection — priority 5), and an inset 5×5 probability × impact heat map. (Source: Pt6 p.97)
- **Key Risk Indicators (KRI)** — critical predictive indicators organizations use to monitor and predict potential risks. (Source: Pt6 p.98)
  - Provide an early indication of increasing risk exposures.
  - Assess the potential impact and likelihood of various risks.
- **Risk Owner** — the individual responsible for managing a particular risk, including identifying and assessing the risk, implementing measures to mitigate it, monitoring the effectiveness of the measures, and taking corrective actions as warranted. (Source: Pt6 p.98)
  - Has a comprehensive understanding of the risk and its potential impacts.
  - Has a thorough understanding of the measures needed to manage the risk.
- **Risk Threshold** — the limits or levels of acceptable risk an organization is willing to tolerate. (Source: Pt6 p.98)
  - Represents the boundaries within which risks are considered to be acceptable and manageable.

## Risk Tolerance and Risk Appetite (Source: Pt6 p.99)

- **Risk Tolerance** — determines the thresholds that separate different levels of risk. (Source: Pt6 p.99)
  - Describes the specific amount of variance an organization is willing to accept regarding measured risk levels and the established risk appetite.
- **Risk Appetite** — a strategic assessment of what level of residual risk is acceptable for an organization. (Source: Pt6 p.99)
  - Describes the level of risk that an organization is willing to accept.
  - **Expansionary** — willing to take on higher levels of risk in the pursuit of high returns or aggressive growth; typically operate in rapidly evolving markets or industries and must take risks to remain competitive; e.g., launching new products, entering new markets, or making major corporate acquisitions.
  - **Conservative** — prioritizes risk avoidance; takes a cautious approach and prioritizes preserving cash, maintaining a good reputation, or ensuring regulatory compliance over pursuing aggressive growth.
  - **Neutral** — balances expansionary and conservative approaches; willing to take on risks if they align with strategic objectives and can be managed effectively.

## Other Risk Management Terms (Source: Pt6 p.100)

- **Residual Risk** — the likelihood and impact after specific mitigation, transference, or acceptance measures have been applied. (Source: Pt6 p.100)
- **Inherent Risk** — the amount of risk that exists, without taking into account the existence of controls. (Source: Pt6 p.100)
- **Control Risk** — a measure of how much less effective a security control has become over time. (Source: Pt6 p.100)

## Risk Management Strategies (Source: Pt7 p.1)

| Strategy | Slide description | Slide examples / notes |
|---|---|---|
| **Acceptance** | Deciding to accept the risk | Allowing remote access to employees; "Do nothing – cost too much"; "Cost vs Benefit" |
| **Avoidance** | Deciding the benefit is not worth the risk | BYOD policy, access to Facebook from within enterprise; "Buy something new / Alternate action" |
| **Transference** | Sharing the risk with another | Insurance – cost; cybersecurity insurance (underlined); "Someone else, 3rd Party, or SLA"; "Pass off risk / Risk Assignment" (underlined) |
| **Mitigation** | Taking steps to reduce the risk | Securing remote access with VPN, training employees, implementing firewalls; "Repair – fix it / Reduce risk" |
| **Deterrence** | Warning of the consequences | Placing a statement of conduct/misuse on a log-in banner |

(Source: Pt7 p.1) Callout: "Ignoring risk is not a valid option, the risk is not going away!" Image: a dial labeled Risk with positions Transfer, Accept, Avoid, Mitigate (Mitigate lit). (Source: Pt7 p.1) Note: the slide table lists five strategies (adds Deterrence), while the Section Topics slide lists four (transfer, accept, avoid, mitigate). (Source: Pt6 p.87; Pt7 p.1)

## Risk Acceptance, Assignment, and Reporting (Source: Pt7 p.2)

- **Risk Acceptance** — the result after a cost/benefit analysis shows countermeasure costs would outweigh the possible cost of loss due to a risk. (Source: Pt7 p.2)
  - **Exception** — a request considered to be a **short-term solution** (underlined) to issues related to the security controls and policies.
  - **Exemption** — a request considered to be a **longer-term solution** (underlined) to issues related to the security controls and policies.
- **Risk Assignment (Pass off risk)** — assigning risk or transferring risk is the placement of the responsibility of loss due to a risk onto another entity or organization. (Source: Pt7 p.2)
  - Senior Management's delegation and are ultimately responsible (wording as printed).
  - Risk Transference (underlined).
  - Cybersecurity Insurance, Cyber Liability Insurance or Cyber Insurance.
- **Risk Reporting** — a periodic summary of relevant information about a project's current risks. (Source: Pt7 p.2)
  - Provides a summarized overview of known risks, realized risks, and their impact on the organization.

## Business Impact Analysis (BIA) (Source: Pt7 p.3-5)

- **Business Impact Analysis (BIA)** — the process of assessing what losses might occur for a range of threat scenario (**identifies risk**, underlined). (Source: Pt7 p.3)
  - Assesses potential impact of a disruption.
  - Identifies critical assets/processes and interdependencies.
  - Establishes value of each organizational area/core resource.
  - Results provide direction on business continuity resource allocation.
- **Questions answered** (Source: Pt7 p.3): What system, if rendered unavailable, would prevent the enterprise from doing business? What are the system independencies (as printed)? What are the critical assets, prioritized from highest to lowest?
- **Identifies** (Source: Pt7 p.3): critical organizational resources; potential threats against these resources; the likelihood that identified threats will occur; impact the threats may have on the business, should they occur.
- **Maximum Tolerable Downtime (MTD)** — the longest period of time that a business function outage may occur for without causing irrecoverable business failure. (Source: Pt7 p.4)
  - "Without this resource – cutoff – drop dead – (MTD = RTO+WRT)".
- **Recovery Point Objective (RPO)** — the amount of data loss that a system can sustain, measured in time; if a database is destroyed by a virus, an RPO of 24 hours means that the data can be recovered (from a backup copy) to a point not more than 24 hours before the database was infected. (Source: Pt7 p.4)
  - "Maximum tolerable data loss – backup time – set/fixed time".
- **Recovery Time Objective (RTO)** — represents the amount of time it takes to identify a problem and then perform recovery. (Source: Pt7 p.4)
  - "How quick can we recover – restore/recovery".
- **Work Recovery Time (WRT)** — following systems recovery, there may be additional work to reintegrate different systems, test overall functionality, and brief system users on any changes or different working practices so that the business function is again fully supported. (Source: Pt7 p.4)
  - The time required to configure a recovered system.
- **Mission Essential Function (MEF)** — the organization must be able to perform the function as close to continually as possible, and if there is any service disruption, these functions must be restored first; functions that cannot be deferred. (Source: Pt7 p.5)
- **Single Point of Failure (SPoF)** — an asset that causes the entire workflow to fail if it is damaged or otherwise not available. (Source: Pt7 p.5)
- **Mean Time Between Failures (MTBF)** — quantifies how long a new or repaired system will run before failing. (Source: Pt7 p.5)
  - The average time to failure for a system that is repairable.
  - Approximated lifetime of when a piece of equipment will work before it needs to be replaced/repaired.
- **Mean Time To Failure (MTTF)** — similar to MTBF but refers to a system that is non-repairable; if the system is able to be repaired, then MTBF should be used. (Source: Pt7 p.5)
  - The average time that an item will function before it fails and cannot be repaired.
- **Mean Time to Repair (MTTR)** — a measure of the time taken to correct a fault so that the system is restored to full operation; can also be described as mean time to "replace" or "recover". (Source: Pt7 p.5)
  - The amount of time to fix a system before it can be used again in production.

## Slide-quality flags

- [CONFLICT/ODD] RCA definition on Pt6 p.91 is grammatically garbled ("An external process led by third-party to lead to conduct risk assessment"); recorded as printed.
- [CONFLICT/ODD] Exception = short-term and Exemption = longer-term on Pt7 p.2, recorded as printed; no other slide in this range gives different definitions.
- [GAP] "Probability" (a Section Topics bullet) is never defined separately; it appears only inside the qualitative-analysis definition ("probability of occurrence", Pt6 p.94). "Likelihood" is bolded on Pt6 p.90 without its own definition.

## Validation log
- Extraction: all 20 pages (Pt6 p.86-100, Pt7 p.1-5) read at 100 dpi; Pt7 p.6 read as the 5.3 roadmap slide (boundary confirmation).
- Validation pass (2026-10-16): note compared against all 20 pages. The densest pages (Pt6 p.94 matrices, p.96 calculations table, p.97 risk-register screenshot; Pt7 p.1 strategies table) were re-rendered at 140 dpi and re-read; matrix cell colors/values, all 15 table values, and the register template columns were confirmed. Text-only pages (Pt6 p.86-93, 95, 98-100; Pt7 p.2-5) were re-checked line by line against the 100 dpi renders. All five worked-example/table ALE and SLE values were also recomputed (AV×EF, SLE×ARO) and match.
- Corrections made: none required. Limitation: this was a same-session re-check by the extracting reviewer, not an independent second reader (4.x/2.4 notes used a subagent pass for some units).

## Official-objective gap check (5.2 bullets from the slides' Section Topics slide, Pt6 p.87)
*Finalized after validation, 2026-10-16.*

| Official bullet | Status | Where |
|---|---|---|
| Risk identification | Covered | Pt6 p.89-90 |
| Risk assessment: ad hoc, recurring, one-time, continuous | Covered | Pt6 p.93 |
| Risk analysis: qualitative, quantitative | Covered | Pt6 p.94 |
| SLE, ALE, ARO, exposure factor | Covered (formulas + worked examples) | Pt6 p.95-96 |
| Probability, likelihood, impact | Weak — likelihood/impact appear in the Risk definition (p.90) and risk analysis (p.94); "probability" is never separately defined | Pt6 p.90, p.94 |
| Risk register: KRI, risk owners, risk threshold | Covered | Pt6 p.97-98 |
| Risk tolerance | Covered | Pt6 p.99 |
| Risk appetite: expansionary, conservative, neutral | Covered | Pt6 p.99 |
| Risk management strategies: transfer, accept (exemption, exception), avoid, mitigate | Covered | Pt7 p.1-2 |
| Risk reporting | Covered | Pt7 p.2 |
| BIA: RTO, RPO, MTTR, MTBF | Covered | Pt7 p.3-5 |

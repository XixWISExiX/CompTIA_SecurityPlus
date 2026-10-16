# Coverage Tracker

One row per source slide page across all 659 pages of `CompTIA_SecurityPlus_Slides/`. Tracks four independent stages — OCR extraction, visual review, note extraction, and validation — per `CLAUDE.md`'s five-stage separation. **No field implies a later stage happened.**

- OCR pass completed for **659 / 659** pages as of this session (bulk `tesseract` pass, run in background; see `OCR_Topic_Guess`).
- `Domain_Guess` is derived from exact-text matches of each domain's "Domain Topics N.0 (domain name)" divider slide in the OCR output (confirmed by reading the full OCR text at each divider, not just a heuristic guess) — see zone table below. All five domain boundaries are High confidence. This is still page-range-level, not sub-objective-level, except where a unit has been individually extracted (see below).
- Twelve units have been extracted and validated so far (Domain 4: 4.1-4.9; Domain 2: 2.1-2.3) — see the Resume state and `objective_mapping.md` for statuses and note links.

## Resume state (update every session)

| Item | State |
|---|---|
| Order | Domain 4 → 2 → 5 → 3 → 1 (exam weight), one sub-objective per batch |
| Boundary rule | A section starts at its roadmap slide (the slide before "Section Topics") and ends before the next roadmap slide. 4.7 = g515-522, 4.8 = g523-549 (no overlap) |
| Done | 4.8 (g523-549): extracted + validated (official-bullet gap check still to record). 4.1 (g388-422): extracted + validated; Weakly Covered (official-bullet gaps). 4.2 (g423-429): extracted + validated; Well Covered. 4.3 (g430-445): extracted + validated; Weakly Covered (1 bullet gap: system/process audit). 4.4 (g446-456): extracted + validated; Well Covered. 4.5 (g457-484): extracted + validated; Weakly Covered (1 weak bullet: transport method). 4.6 (g485-514): extracted + validated; Weakly Covered (1 weak bullet: passwordless). 4.7 (g515-522): extracted + validated; Well Covered. 4.9 (g550-555): extracted + validated; Weakly Covered (OS-specific logs thin). 5.1 (g561-585 = Pt6 p.61-85): extracted + validated 2026-10-16; Weakly Covered (external-consideration laws are names only; baseline and due care undefined). 5.2 (g586-605 = Pt6 p.86-100 + Pt7 p.1-5): extracted + validated 2026-10-16; Weakly Covered ("probability" never defined separately). 5.3 (g606-614 = Pt7 p.6-14): extracted + validated 2026-10-16; Covered on all Section Topics bullets (MOA/MOU share one definition; supply chain analysis descriptive only). g556-560 are Domain 4 recap / logo / Module 5 title slides (read, no objective content). **Domain 4 extraction is complete (4.1-4.9).** Domain 2: 2.1 (g126-132): extracted + validated; Weakly Covered (motivations list-only). 2.2 (g133-150): extracted + validated; Weakly Covered (non-human vectors list-only; "attack surface" not defined). 2.3 (g151-179): extracted + validated; Weakly Covered (firmware, legacy, cloud-specific thin). 2.4 (g180-230 = Pt2 p.80-100 + Pt3 p.1-30): extracted + validated; Weakly Covered (forgery absent; credential replay, resource consumption thin). 2.5 (g231-245 = Pt3 p.31-45): extracted + validated; Weakly Covered (permissions absent; app allow list, config enforcement, host firewall/HIPS, default passwords thin). g246-247 are the Domain 2 recap / logo (viewed, no unit). **Domain 2 extraction is complete (2.1-2.5).** g125 is the Domain 2 "Domain Topics" recap slide (titles only; not marked, no unit). |
| In progress | none — 5.3 complete; 5.4 next |
| Next | 5.4 Effective security compliance (roadmap g615 = Pt7 p.15 viewed; content starts g616 = Pt7 p.16; end TBD at 5.5 roadmap g629) |
| Then | Domain 3 (g251-385), Domain 1 (g17-123); Domain 2 is complete — boundaries provisional, confirm visually |
| Do not run | `.render_cache/build_tracker.py` — it regenerates the whole tracker and would erase per-page flags |

## Domain zone basis (OCR divider-slide evidence)

| Global page range | Domain | Confidence |
|---|---|---|
| 1-15 | 0.0 Course overview/logistics (non-exam-objective content) | High |
| 16-124 | 1.0 General Security Concepts | High |
| 125-249 | 2.0 Threats, Vulnerabilities, and Mitigations | High |
| 250-386 | 3.0 Security Architecture | High |
| 387-549 | 4.0 Security Operations | High |
| 550-659 | 5.0 Security Program Management and Oversight | High |

## Page-level tracker

| Part | Page | Global# | OCR_Topic_Guess | Domain_Guess | Guess_Confidence | Visual_Reviewed | Note_Extracted | Validated | Notes_File |
|---|---|---|---|---|---|---|---|---|---|
| 1 | 1 | 1 | § 1. Use this coversheet as the front cover to the 1. Folow all applic | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 2 | 2 | Security+ { | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 3 | 3 | * This course is UNCLASSIFIED | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 4 | 4 | «Is this your first time attending a Boot Camp? | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 5 | 5 | Infrastructure ES nsomocke cealuye Eas roatinen | 0.0 Course overview/logistics (non-exam-objective content) | High | Y | N | N |  |
| 1 | 6 | 6 | * Domain 2 — Threats, Vulnerabilities, and Mitigations J o | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 7 | 7 | The CompTIA Security+ certification exam will verify the successful ca | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 8 | 8 | 1. Threats, Attacks and Vulnerabilities 21% 1.0 Attacks, Threats, and  | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 9 | 9 | — Objectives focus more on a conceptual and analytical understanding o | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 10 | 10 | * Scroll down to Featured Providers and search their websites for cont | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 11 | 11 | —https:/Awww.professormesser.com/security-plus/sy0-701/sy0-701-video/s | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 12 | 12 | * Actively participate, collaborate, share, learn, ask | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 13 | 13 | _(blank/unreadable)_ | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 14 | 14 | SS RULART All | 0.0 Course overview/logistics (non-exam-objective content) | High | N | N | N |  |
| 1 | 15 | 15 | General Security Concepts | 0.0 Course overview/logistics (non-exam-objective content) | High | Y | N | N |  |
| 1 | 16 | 16 | — 1.3 Explain the importance of change management processes and the im | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 17 | 17 | Fundamental security concepts | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 18 | 18 | 1.1 Compare and contrast various types of security controls. | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 19 | 19 | * Managerial (Administrative) — Implemented by creating and following  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 20 | 20 | - Detective — Send a warning after discovering unwanted activities dur | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 21 | 21 | Fundamental security concepts | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 22 | 22 | — Authentication, Authorization, and Accounting (AAA) + Access control | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 23 | 23 | Confidentiality, Integrity, And Availability (CIA) | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 24 | 24 | ¢ Discretion — An operator's act or decision to control disclosure to  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 25 | 25 | — Integrity makes sure information alteration should not occur while t | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 26 | 26 | * Accessibility - Assurance that the widest range of subjects can inte | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 27 | 27 | — Mutual Authentication — the client and server verify the authenticit | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 28 | 28 | rna me be granted the minimum amount of | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 29 | 29 | — International Standards Organization (ISO) published | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 30 | 30 | + Kerberos — A client-server-based authentication system that uses “ti | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 31 | 31 | 1. Kerberos Principal Alice contacts to the KDC Kerberos kpc | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 32 | 32 | — Conducted to understand the status of your cybersecurity risks and | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 33 | 33 | validating security configuration and posture, before being granted or | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 34 | 34 | - Adaptive identity — User identities are not static, and that identit | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 35 | 35 | ‘CDM System Policy Policy | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 36 | 36 | * Control Plane — Responsible for managing network routing protocols,  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 37 | 37 | * Policy Decision Point (PDP) — Responsible for making access control  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 38 | 38 | * Transfers/forwards packets across the network based on the direction | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 39 | 39 | ¢ Atraffic bollard is a strong post designed to stop == | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 40 | 40 | (only one opens at a time) to prevent unauthorized people from followi | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 41 | 41 | facility without the appropriate access credentials, without 7 (ee } | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 42 | 42 | — Used to separate security zones, provide safe areas, and maintain tr | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 43 | 43 | —Normal light spectrum require sufficient visibility to illuminate ea | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 44 | 44 | — One of the best security mechanisms to monitor a facility's grounds | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 45 | 45 | + Proximity Readers — method of controlling access through Key card | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 46 | 46 | —Poor lighting can lead to individuals sneaking in through doors, allo | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 47 | 47 | * Motion Detection — Used to detect the motion of a living being withi | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 48 | 48 | that cold aisles are used for air intake, and hot aisle are used for a | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 49 | 49 | mixes quickly with the air in the room to extinguish a fire; Banned in | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 50 | 50 | « High-security models are resistant to lock picking, drilling or bypa | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 51 | 51 | — Records and files are fake, and legitimate users never have access t | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 52 | 52 | Change management processes | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 53 | 53 | 1.3 Explain the importance of change management processes and the impa | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 54 | 54 | * Outlines the details of the proposed change, including its purpose,  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 55 | 55 | + Impact Analysis — The process of identifying and assessing the poten | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 56 | 56 | + Allow and block lists describe software restriction approaches desig | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 57 | 57 | * Restricted activities — Actions or changes that require additional s | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 58 | 58 | — Change Requests should be reviewed and updated to reflect the detail | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 59 | 59 | ¢ Version Control — An ID system for each iteration of a software prod | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 60 | 60 | Fundamental security concepts | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 61 | 61 | + Private key + Hardware security module (HSM) * Certificate revocatio | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 62 | 62 | - Public Key Infrastructure (PKI) Ceireacerastntcy @vl | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 63 | 63 | —CAis at the top of the system, and performs the following functions:  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 64 | 64 | —Local Registration Authorities could be used by systems to off-load r | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 65 | 65 | * Online Certificate Status Protocol (OCSP) — a “request-response prot | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 66 | 66 | * Key — mathematical value entered into a cryptographic algorithm to p | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 67 | 67 | ¢ Key Escrow -— The storing of private keys so that the key can be obt | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 68 | 68 | — Cryptography is a critical element in protecting the Confidentiality | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 69 | 69 | + Cleartext — readable (unencrypted) data that is transmitted or store | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 70 | 70 | + Initialization Vector (IV) — used in some symmetric ciphers to ensur | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 71 | 71 | ¢ Substitution Cipher — substitutes one character for another | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 72 | 72 | * Vigenere — uses multiple alphabets to help combat against japabponun | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 73 | 73 | * Basic Input/Output System (BIOS) — an older method for handling boot | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 74 | 74 | Client Fokenibased Operating System i  Ay | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 75 | 75 | ¢ Hard Drive Security — both permanent and portable hard drives should | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 76 | 76 | — Data/Media Encryption Key (DEK/MEK) — the key used to encrypt the da | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 77 | 77 | ¢ File and File System Encryption — encryption software can be used to | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 78 | 78 | — Internet Protocol Security (IPsec) — securing traffic sent between t | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 79 | 79 | + When the value of a qubit is read, it collapses to either 1 or 0, an | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 80 | 80 | + Uses a “public key” to encrypt a message, and a “private key” to dec | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 81 | 81 | El-Gamal Yes Yes Yes Does not use prime number factoring but | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 82 | 82 | * RSA Algorithm — Named for its inventors Ron Rivest, Adi Shamir, Leon | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 83 | 83 | ¢ ElGamal — A public key algorithm that can be used for digital signat | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 84 | 84 | —Leverages one-way function that is based on the idea of using truly r | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 85 | 85 | —Allows 2 parties that have no prior knowledge of each other to jointl | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 86 | 86 | - A“shared key” is used by both the sender and receiver to encrypt and | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 87 | 87 | 3DES 56, 112, or 168 Block (64 bit) Effective strength is 112 bits | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 88 | 88 | —Commornly use substitution or transposition ciphers | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 89 | 89 | ¢ Data Encryption Standard (DES) — Based on a 56-bit cipher key and 8- | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 90 | 90 | versions of block cipher keys: 128, 192, 256 each with the same cipher | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 91 | 91 | key and is similar in speed and capability to DES, but has more securi | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 92 | 92 | * Contains several vulnerabilities and therefore avoided for newer app | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 93 | 93 | ¢ Blowfish — Block cipher with a 64-bit block size with a key size ran | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 94 | 94 | — Data is encrypted using modular addition (y+c=b) or XOR with shared  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 95 | 95 | ¢ Shared keys present a vulnerability when they are transmitted across | 1.0 General Security Concepts | High | Y | N | N |  |
| 1 | 96 | 96 | ¢ Key size — the security of a cipher is strongly related to the size  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 97 | 97 | —Trusted Platform Module (TPM) — A microchip or a co-processor on a co | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 98 | 98 | ¢ Key Generation — Creates an asymmetric key pair or symmetric secret  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 99 | 99 | « An account or combination of accounts that can copy a cryptographic  | 1.0 General Security Concepts | High | N | N | N |  |
| 1 | 100 | 100 | —Most common files used are pictures, but can be done with audio and v | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 1 | 101 | — Techniques to preserve the original format of the field | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 2 | 102 | * Hashing — a ONE-WAY mathematical function that produces a fixed leng | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 3 | 103 | —Version 5 (MD5) — a generic version of several algorithms used to has | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 4 | 104 | ¢ Secure Hash Algorithm (SHA) — designed by the National Security Agen | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 5 | 105 | * NTLM — uses MD4 and MD5 hashing algorithms, and is primarily | 1.0 General Security Concepts | High | Y | N | N |  |
| 2 | 6 | 106 | —Also ensures unique password hashes are stored, F — | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 7 | 107 | — Digital Signature Algorithm (DSA) and FIPS 186-2 are used in the gen | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 8 | 108 | ¢ Key Stretching — a process of protecting weak keys from brute-forcin | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 9 | 109 | expanding list of transactional records record of transactions that un | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 10 | 110 | to associate a user’s identity to a public key that has been “digitall | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 11 | 111 | — Third-party trust — two individuals trust each other because each tr | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 12 | 112 | —A tiered system of CAs, Root CA signs all digital certificates with a | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 13 | 113 | * Certificate Revocation List (CRL) — CAs maintain an online CRL | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 14 | 114 | * OCSP Stapling — variation of OCSP that attempts to reduce traffic by | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 15 | 115 | —PKCS #7 — typically used to import and export certificates and privat | 1.0 General Security Concepts | High | Y | N | N |  |
| 2 | 16 | 116 | techniques to provide confidentiality, sender authentication, and mess | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 17 | 117 | + Root Digital Certificate — generated and self-signed by the Root CA  | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 18 | 118 | ¢ Root of Trust (RoT) — Defines how users and different CAs can trust  | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 19 | 119 | Common name Fully qualified domain name (FQDN) of the server www.abcco | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 20 | 120 | * Subject Alternative Name (SAN) Digital Certificate — Allows the addi | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 21 | 121 | — 1.3 Explain the importance of change management processes and the im | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 22 | 122 | _(blank/unreadable)_ | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 23 | 123 | SS RULART All | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 24 | 124 | Threats, Vulnerabilities, and Mitigations a ! | 1.0 General Security Concepts | High | N | N | N |  |
| 2 | 25 | 125 | —2.4 Given a scenario, analyze indicators of malicious activity. | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 2 | 26 | 126 | Mitigation techniques used to secure | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 27 | 127 | 2.1 Compare and contrast common threat actors and motivations. | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 28 | 128 | something to someone ) \\ ihe = | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 29 | 129 | + Hacktivist — might attempt to obtain and release confidential inform | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 30 | 130 | owner to conduct system attacks, penetration testing, and intrusion te | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 31 | 131 | —Internal threats are even more dangerous given the level of legitimat | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 32 | 132 | —Intent describes what an attacker hopes to achieve from the attack | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-actors-and-motivations.md |
| 2 | 33 | 133 | Mitigation techniques used to secure | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 34 | 134 | — Message-based — Unsecure networks — Human vectors/social | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 35 | 135 | — Unsupported Systems and Applications — Removable Device (USB) | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 36 | 136 | ¢ Weak Encryption — the use of weak encryption opens up the network to | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 37 | 137 | + Administrators sometimes reduce the power level to restrict access t | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 38 | 138 | * Bluesnarfing — Unauthorized access, theft, or stealing | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 39 | 139 | ¢ Misconfigurations result from improperly configured operating system | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 40 | 140 | to infiltrate it via companies in its supply chain (Target data breach | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 41 | 141 | * Social Engineering — the clever manipulation of the natural human te | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 42 | 142 | « SPIM — unwanted message delivered via an Instant Messaging or chat a | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 43 | 143 | —Whaling — a type of spear phishing that targets the | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 44 | 144 | a victim through a convincing story or subliminal conditioning Lorn | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 45 | 145 | ¢ Shoulder Surfing — looking over someone's “shoulder” to read | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 46 | 146 | Internet and that the recipient should erase specific files, ' sc T | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 47 | 147 | —Persuade users to install a “must-have” app that is actually a Trojan | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 48 | 148 | — Financial motivation, where the objective is to persuade a budget | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 49 | 149 | they typically visit and luring them to a malicious site, with an end  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 50 | 150 | aims to solicit sensitive information from victims by posing as a legi | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/threat-vectors-and-attack-surfaces.md |
| 2 | 51 | 151 | Mitigation techniques used to secure | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 52 | 152 | * Memory injection * Virtual machine (VM) escape | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 53 | 153 | — Used to install malware, exfiltrate sensitive data, or create a back | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 54 | 154 | — Inserting/injecting more information into an application than it is  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 55 | 155 | [- [ Unallocated Memory Space | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 56 | 156 | ¢ Pivot/Lateral Movement — using an exploited machine to attack | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 57 | 157 | is directly dependent on the order and timing of certain events, and t | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 58 | 158 | —The update may claim to fix software bugs or offer new features but i | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 59 | 159 | - 2017 MS17-010 — vulnerability with Server Message Block (SMB) protoc | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 60 | 160 | —The OWASP Top 10 list of security controls for web application develo | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 61 | 161 | —Asingle quote (') — the one single character used to check for a SQL  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 62 | 162 | SELECT User from LOGON where ID=bob1 and PASS=12345 —- —- — — — > | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 63 | 163 | SELECT User from LOGON where ID=admin and PASS=anything ‘or'1'="1 res | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 64 | 164 | * Cross-Site Scripting (XSS) — Injection of malicious code into a vuln | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 65 | 165 | \\ . Ke hele g & Poul “ | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 66 | 166 | * The web site does not properly sanitize input and code is added via  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 67 | 167 | Cross-Site Script — Persistent (Stored) — Example | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 68 | 168 | — Uses reflected input to trick a user’s browser into executing untrus | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 69 | 169 | Cross-Site Script — Non-Persistent (Reflected) — Example | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 70 | 170 | into executing a malicious action on a trusted site for which the user | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 71 | 171 | Cross Site Request Forgery (XSRF)(CSRF) — continued | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 72 | 172 | —End of Life (EOL) —A manufacturer ceva woalysupoe End.ofiSate(FOS) | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 73 | 173 | — Sandboxing — running apps in restricted memory areas to protect from | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 74 | 174 | —When data migrates to and from private and public clouds, the risk of | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 75 | 175 | * Offering development, testing, and deployment platforms or directly  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 76 | 176 | * Social Engineering — If the human can be persuaded to reveal the key | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 77 | 177 | an attacker to retrieve private memory of an application in chunks | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 78 | 178 | * Mobile device challenges include: | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 79 | 179 | —A vulnerability that is exploited before the developer knows about it | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/types-of-vulnerabilities.md |
| 2 | 80 | 180 | Mitigation techniques used to secure | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 81 | 181 | 2.4 Given a scenario, analyze indicators of malicious activity. | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 82 | 182 | — Several classifications exist to help categorize | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 83 | 183 | — Just like a biological virus it infects the host and then replicates | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 84 | 184 | + Boot — loads into the boot sector or the partition table of the i | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 85 | 185 | — Fileless — does not write its code to disk instead uses lightweight  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 2 | 86 | 186 | user interaction and can quickly travel across networks € <4 7 | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 87 | 187 | * Trojans — software that appears to do one thing but hides other, mal | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 88 | 188 | — After initial system compromise an attacker can return later bypassi | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 89 | 189 | — Secretly monitors users by collecting information without their appr | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 90 | 190 | + Grayware — A category of software that sits in the ‘gray area’ — a s | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 91 | 191 | * Online advertising has become very profitable for websites | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 92 | 192 | to retrieve the ad banners, pop-up ads, video/picture files which are  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 93 | 193 | —Methbot — spoofs the interactions between the browser coos, ._) | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 94 | 194 | it cannot be bypassed and prevents the computer from properly | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 95 | 195 | — Exploited a security vulnerability in the SMB and encrypted the user | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 2 | 96 | 196 | « Encrypted files start to be deleted after a set time and can only be | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 97 | 197 | benign features inserted by developers (for recreation or notoriety) d | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 98 | 198 | attached to objects that respond to specific radio frequencies | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 99 | 199 | ¢ Aphysical attack is one directed against cabling infrastructure, har | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 2 | 100 | 200 | than it can handle; though the traffic is often “legitimate”, the serv | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 1 | 201 | malicious activity, such as distributed denial-of-service (DDoS) attac | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 2 | 202 | ¢ Website — the bot automatically signs into a website that | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 3 | 203 | + Distributed Reflected DoS (DRDoS) — A malicious request to a legitim | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 4 | 204 | Distributed Denial-of-Service (DDoS) — continued | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 5 | 205 | ¢ Smurf Attack — Attacker sends an ICMP ECHO Request (Ping) to a netwo | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 6 | 206 | * Cache — Stored information on servers and hosts that can be accessed | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 7 | 207 | canonical names (i.e. google.com) to IP addresses; like a phone book | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 8 | 208 | DNS Cache Poisoning / Pharming | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 9 | 209 | —DNS query requests are typically much smaller in size than the DNS re | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 10 | 210 | « Initialization Vector (IV) Attacks — a related key attack in which t | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 11 | 211 | ¢ Interception Attacks — rely on the attacker being able to insert the | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 12 | 212 | * Replay Attack — the attacker makes of copy of the data and then send | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 13 | 213 | ¢ SSL Stripping — a technique where a website is downgraded | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 14 | 214 | + Shellcode — A minimal program designed to exploit a vulnerability in | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 15 | 215 | — Lightweight Directory Access Protocol (LDAP) — protocol used in @ 7) | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 16 | 216 | —E-Mail spoofing — sent with a “From” address different from the actua | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 17 | 217 | — Typically implemented as a concealed link or embedded code/script | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 18 | 218 | —Code runs with higher privileges and can allow an end user to have | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 19 | 219 | — Because a web server is simply a set of directories and files which  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 20 | 220 | — Algorithm Attacks — attacks that target weaknesses in the algorithms | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 21 | 221 | ¢ Brute Force — trying every possible key; will always be successful,  | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 22 | 222 | —When two variable inputs result in the same fixed length output (hash | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 23 | 223 | — Most common type of active attack because it is very easy to get cip | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 24 | 224 | - Brute-force Attack — involves using every possible combination of ch | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 25 | 225 | Password: apple apple () [A90BC322 A90BC322 | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 26 | 226 | Brute Force Plaintext Entered Hash Stored Hash | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 27 | 227 | A90 BC322 Hash Algorithm (MD5, SHA, etc.) | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 28 | 228 | A90 BC322 Hash Algorithm (MD5, SHA, etc.) | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 29 | 229 | — Account lockout — Policy that prevents access to an account under ce | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 30 | 230 | « Host and network gateways might be unavailable due to excessive reso | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/indicators-of-malicious-activity.md |
| 3 | 31 | 231 | Mitigation techniques used to secure | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 32 | 232 | 2.5 Explain the purpose of mitigation techniques used to secure the en | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 33 | 233 | or subnets, each with distinct security controls and access permission | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 34 | 234 | —Compartmentalizes portions of the network, thereby increasing securit | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 35 | 235 | CIDR Mask Classful IPv4-Addresses CIDR Mask Classful IPv4-Addresses | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 36 | 236 | ¢ Virtual Local Area Network (VLAN) — a logically separate network, cr | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 37 | 237 | systems, networks and websites Telscommulcis | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 38 | 238 | + Implicit Deny/Explicit Allow — if you are not on the list to be allo | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 39 | 239 | + Patch/Update Management - the planning, testing, implementing, and a | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 40 | 240 | —Ensures that all data, including the operating system and user files, | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 41 | 241 | —Once devices are hardened, monitoring helps to ensure these condition | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 42 | 242 | — Reduces the exposure and harm that can be done by accessing property | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 43 | 243 | * Configuration Enforcement — Methods used to ensure that systems | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 44 | 244 | — Resetting devices to their factory settings eliminating any residual | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | Y | Y | course-unit-notes/02-threats-vulnerabilities-and-mitigations/mitigation-techniques-to-secure-the-enterprise.md |
| 3 | 45 | 245 | * System Hardening — The process of configuring systems and networks | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 46 | 246 | —2.4 Given a scenario, analyze indicators of malicious activity. | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 47 | 247 | _(blank/unreadable)_ | 2.0 Threats, Vulnerabilities, and Mitigations | High | Y | N | N |  |
| 3 | 48 | 248 | SS RULART All | 2.0 Threats, Vulnerabilities, and Mitigations | High | N | N | N |  |
| 3 | 49 | 249 | Module 3 —~& Bi | 2.0 Threats, Vulnerabilities, and Mitigations | High | N | N | N |  |
| 3 | 50 | 250 | —3.2 Given a scenario, apply security principles to secure enterprise  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 51 | 251 | Security implications of different | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 52 | 252 | — Architecture and infrastructure concepts + Industrial control system | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 53 | 253 | * Cloud Computing — Computing, storage, application and other services | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 54 | 254 | ¢ Responsibility Matrix (Shared Responsibility) — Identifies that resp | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 55 | 255 | (On-Premises) (as a Service) (as a Service) (as a Service) | 3.0 Security Architecture | High | Y | N | N |  |
| 3 | 56 | 256 | —Multi-Cloud — Architectures are where an organization uses services f | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 57 | 257 | or for more specific or product-focused projects (pen testing, SIEM ro | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 58 | 258 | up and delivering secure cloud platforms for evaluating and selecting  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 59 | 259 | — Provides security, manageability, and visibility into how clients Pa | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 60 | 260 | * Serverless — a software architecture that runs functions within virt | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 61 | 261 | — Physically Isolating a host or group of hosts improves security but  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 62 | 262 | — Control plane — makes decisions about how traffic should be prioriti | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 63 | 263 | —Prioritize data for analysis and alert conditions See | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 64 | 264 | 7 Application Network process to application (FTP, HTTP, and SMTP) | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 65 | 265 | Protocol Data Units (PDUs) | 3.0 Security Architecture | High | Y | N | N |  |
| 3 | 66 | 266 | 7 Application OHCP, DNS, FTP, TFTP, SSH, LDAP, IMAP, | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 67 | 267 | — Communication protocol for local area networks and the Internet | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 68 | 268 | with four pairs of wires (eight total) each of which is = | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 69 | 269 | — Still used today as the primary standard transmission method for fib | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 70 | 270 | ¢ Electromagnetic Interference (EMI) — Interference on network cables | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 71 | 271 | * Cable Locks — A sturdy cable with either a built-in lock, or eyelet  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 72 | 272 | * Switch — Intelligent hub; knows the system addresses connected | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 73 | 273 | ¢ Switch — a typical layer 2 device that forwards frames based on hard | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 74 | 274 | + Every Network Interface Card (NIC) has a 6 byte (48 bits) Ethernet a | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 75 | 275 | —MAC Filtering — manually defining which MAC addresses are allowed to  | 3.0 Security Architecture | High | Y | N | N |  |
| 3 | 76 | 276 | + Flood Guards — manage traffic flows by monitoring traffic rate and p | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 77 | 277 | ¢ Router — connects two or more networks together to form an internetw | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 78 | 278 | * Switches — break up Layer 2 — Switch 2 Broadcast Domains Layer 1 — H | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 79 | 279 | * IPv4 — Uses a 32-bit address notation expressed in dotted-quad (dott | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 80 | 280 | reserved for internal networks and are not routed by Internet (public) | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 81 | 281 | sets of IP addresses (internal & external) for mapping 192.168.1.2 QR | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 82 | 282 | + IPv6 — replacement for IPv4 that uses 128-bit address notation expre | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 83 | 283 | « ARecommendation for IPv6 Address Text Representation | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 84 | 284 | number, which is also used to make sure that the data is delivered to  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 85 | 285 | field is valid and contains the next sequence number that is expected  | 3.0 Security Architecture | High | Y | N | N |  |
| 3 | 86 | 286 | ¢ Faster and more efficient for many lightweight or time-sensitive | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 87 | 287 | —All users and devices rely on the central server to access and proces | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 88 | 288 | — Often used in situations where resilience and flexibility are more i | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 89 | 289 | —The virtual OS is often referred to as a virtual desktop environment  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 90 | 290 | — Thin client — a computer only be powerful enough to display the scre | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 91 | 291 | — Docker - container image is a lightweight, standalone, Bins/ Bins/ B | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 92 | 292 | * Internet of Things (loT) — used to describe a global network of appl | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 93 | 293 | * Enterprise management tools are usually lacking | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 94 | 294 | Industrial Control System (ICS), embedded systems, devices and their c | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 95 | 295 | designed for fairly predictable processing workloads, cost per unit ca | 3.0 Security Architecture | High | Y | N | N |  |
| 3 | 96 | 296 | are provided on a single processor die (or chip), a type of packaging  | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 97 | 297 | * High Availability (HA) — Decrease the recovery time of a system or n | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 98 | 298 | ¢ Local Replication — Replicates data within a single data center in t | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 99 | 299 | + Availability —- Minimizes downtime or maximizes uptime | 3.0 Security Architecture | High | N | N | N |  |
| 3 | 100 | 300 | ¢ Aprimary concerns during a disaster or incident is to ensure the org | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 1 | 301 | Security principles to secure | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 2 | 302 | 3.2 Given a scenario, apply security principles to secure enterprise i | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 3 | 303 | ¢ Device Placement — Considerations for positioning security controls  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 4 | 304 | ¢ Fail Securely —A component, application, or device is configured to  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 5 | 305 | to a specially configured port on a Cisco switch that receives copies  | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 6 | 306 | * Server — a computer system that stores, transfers, archives, and all | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 7 | 307 | — Often used to protect personal information being transferred across  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 8 | 308 | preventing packets from traversing the firewall, but instead flows the | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 9 | 309 | ¢ Load Balancing — a fault tolerance technique designed to distribute  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 10 | 310 | — Goal is to identify intrusion attempts, while minimizing . . ‘ | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 11 | 311 | * Host-Based (HIDS/HIPS) — loaded onto an individual system (host / en | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 12 | 312 | ¢ Traffic collector (or sensor) — placed at various locations across t | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 13 | 313 | -Asecurity control that ties physical ports to end-device (client) | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 14 | 314 | - Extensible Authentication Protocol — a framework for negotiating aut | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 15 | 315 | — Principle of least access/privilege — allow only the necessary acces | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 16 | 316 | — Application (layer 7) — can inspect the contents of packets at the a | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 17 | 317 | * Appliance Firewall — a stand-alone hardware firewall deployed to mon | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 18 | 318 | ¢ Application Firewall — operates on the Application Layer (Layer 7) t | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 19 | 319 | —Hypervisor-Based — filtering functionality is built into the hypervis | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 20 | 320 | — Mostly Proprietary — developed from a Linux kernel, but with proprie | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 21 | 321 | — Detects and blocks disclosure of critical data (account numbers, SSN | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 22 | 322 | ¢ Unified Threat Management (UTM)-~ an “all-in-one” device that combin | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 23 | 323 | — Involves the use of modems, traditional Plain Old Telephone Service  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 24 | 324 | analog voice to digital signals for transmission over the network, and | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 25 | 325 | — Secure Real-time Transport Protocol (SRTP) | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 26 | 326 | —VPN Concentrator — the device at which VPN connections terminate with | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 27 | 327 | — Establishes a trust relationship between the gateways and sets up a | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 28 | 328 | —Example: Telecommuter model allowing home-workers and employees worki | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 29 | 329 | connection over a trusted network is detected, using the user's cached | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 30 | 330 | — It provides encapsulation for IP traffic plus IP address assignment  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 31 | 331 | — For bi-directional protection (two-way traffic) two Security Associa | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 32 | 332 | ¢ Internet Key Exchange (IKE) — protocol handles authentication and ke | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 33 | 333 | « Support for EAP authentication methods, allowing, for example, user  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 34 | 334 | — Encrypts only the payload of the packet (source and destination IP a | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 35 | 335 | Connects two systems (such as file servers) to each other Used to conn | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 36 | 336 | — Simplifies the management and operation of a WAN by decoupling the n | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 37 | 337 | (SWG, CASB, ZTNA, and FWaaS) together with wide area network (WAN) | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 38 | 338 | and placement of security controls to ensure the goals of the CIA tria | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 39 | 339 | - Defense-In-Depth — A security principle by which multiple, differing | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 40 | 340 | Security implications of different | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 41 | 341 | 3.3 Compare and contrast concepts and strategies to protect data. | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 42 | 342 | requirements defined by national and state legislation and/or industry | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 43 | 343 | — Financial activities, performance, and transactions, including finan | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 44 | 344 | — Public information presents no risk to an organization if it is disc | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 45 | 345 | numbers, financial information, and sensitive data like health records | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 46 | 346 | * Data in Use: Data being used by an application or resident in memory | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 47 | 347 | — Jurisdiction preventing or restricting processing and storage from t | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 48 | 348 | * Hashing — Converting data into a fixed-length string of characters u | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 49 | 349 | ¢ Data Minimization — Limiting data collection to only what is require | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 50 | 350 | in security architecture | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 51 | 351 | 3.4 Explain the importance of resilience and recovery in security arch | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 52 | 352 | secondary server can take over in the case that the primary one fails, | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 53 | 353 | be considered in order to ensure the organization is able to continue | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 54 | 354 | — Asurviving site includes two geographically dispersed buildings that | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 55 | 355 | ¢ Control Diversity — The layers of controls should combine different  | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 56 | 356 | —Also refers to the obfuscation technique to make code difficult for u | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 57 | 357 | —Enhances cybersecurity by diversifying the risk associated with a sin | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 58 | 358 | should deal with both minor and disaster-level disruption by ensuring  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 59 | 359 | « Evaluating and forecasting the necessary resources in terms of peopl | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 60 | 360 | * Tabletop Exercises — involve teams discussing and working through hy | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 61 | 361 | ¢ Failover Tests — involve intentionally causing the failure of a prim | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 62 | 362 | —Can reveal potential bottlenecks, inefficiencies, or vulnerabilities  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 63 | 363 | — Ensure their backup systems can handle the same workload as primary | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 64 | 364 | — Short-term — Files that change frequently might need retaining for v | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 65 | 365 | ¢ Onsite Storage — Storing of information (tapes, cartridges, or other | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 66 | 366 | * Businesses with relatively stable data or less stringent regulatory | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 67 | 367 | + Ensuring sensitive data remains unreadable without the appropriate d | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 68 | 368 | * Tape — a popular choice for organizations with multi-terabyte storag | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 69 | 369 | — Snapshot/Revert to Known State — a saved system state that can be re | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 70 | 370 | in which there are three or more backup cycles, such as daily, weekly, | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 71 | 371 | — Mirrors a live database allowing simultaneous reads and writes to mu | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 72 | 372 | Data Selection Backup/Restore Time  Archive Attributes | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 73 | 373 | nine CHOMED TOA CraNET FIED Coane FICC craNea FIED | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 74 | 374 | data normally stored on a single disk across a series of disks to prev | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 75 | 375 | Loss of a single disk will result in the loss of all data | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 76 | 376 | (Mirrored Disks) _ f one disk fails, the other continues to operate | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 77 | 377 | Dedicated Parity) Should one drive fail, it can be replaced, and the n | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 78 | 378 | FD Stripes data at block level and spreads parit: | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 79 | 379 | (Block-striped with there are two stripes of parity information Yes 4 | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 80 | 380 | (Raid 1+0) Contains two RAID 1 mirrors which are then striped | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 81 | 381 | 0 Block Striping or Spanning Speed —- No Redundancy 17) | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 82 | 382 | — Managed Power Distribution Units (PDUs) — An advanced strip socket t | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 83 | 383 | —3.2 Given a scenario, apply security principles to secure enterprise  | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 84 | 384 | _(blank/unreadable)_ | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 85 | 385 | SS RULART All | 3.0 Security Architecture | High | Y | N | N |  |
| 4 | 86 | 386 | Module 4 2 ao | 3.0 Security Architecture | High | N | N | N |  |
| 4 | 87 | 387 | —4.2 Explain the security implications of proper hardware, software, a | 4.0 Security Operations | High | N | N | N |  |
| 4 | 88 | 388 | Common security techniques to computing resources I | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 89 | 389 | 4.1 Given a scenario, apply common security techniques to computing re | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 90 | 390 | practices for deploying and maintaining a network device or applicatio | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 91 | 391 | installing monitoring software to protect against malware and intrusio | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 92 | 392 | - Examples of changes designed to improve the security of switches and | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 93 | 393 | « Examples of changes designed to improve the security of servers from | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 94 | 394 | y MEANS! Oh aip ysica ‘Opo ogy 802.119 2.4 GHz 54 Mbps 450 ft. | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 95 | 395 | ¢ Site Survey — The process of developing a wireless coverage map | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 96 | 396 | + Sets device policies for authentication, feature use (camera and mic | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 97 | 397 | — Apps must be submitted to and approved by Apple before they are rele | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 98 | 398 | ¢ Screen Lock — the display is configured to automatically time out af | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 99 | 399 | * Geo-location — use of network attributes to identify the physical lo | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 4 | 100 | 400 | — Mobile device is owned by the company and used | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 1 | 401 | of a mobile device when an employee exits in accordance with the polic | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 2 | 402 | ¢ Architecture/Infrastructure — securely connecting a BOYD to the exis | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 3 | 403 | + Z-Wave — low-power wireless communications protocol used primarily | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 4 | 404 | * Subscriber Identity Module (SIM) — a small chip card that identifies | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 5 | 405 | —Can be used by small low-power devices such as cell phones to transmi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 6 | 406 | —Each WAP is identified by its MAC address, aka Basic Service Set Iden | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 7 | 407 | * MAC Address Filtering (Open System Authentication) | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 8 | 408 | — Uses Temporal Key Integrity Protocol (TKIP), a 128-bit key for integ | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 9 | 409 | — Key derivation uses 384-bit Hashed Message Authentication Mode (HMAC | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 10 | 410 | ‘Authentication WEP-Open WPA-PSK WPA2-Personal WPA3-Personal | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 11 | 411 | — Uses a series remote access protocols for Authentication and Authori | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 12 | 412 | — Designed for use on dial-up connections, but has evolved and is now | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 13 | 413 | proprietary remote access authentication protocol using client/server | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 14 | 414 | + Challenge Handshake Authentication Protocol (CHAP) — used to provide | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 15 | 415 | access to specific application from a client computer on the LAN or ac | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 16 | 416 | pictures which the user must properly identify prior to being granted | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 17 | 417 | a field or variable in an application is handled appropriately by that | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 18 | 418 | — Secure Cookies — an HTTP cookie (web cookie, browser cookie) is a sm | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 19 | 419 | ¢ Data Exposure — a fault that allows privileged information (such as | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 20 | 420 | application source code, byte code and binaries for coding and design | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 21 | 421 | * Code Signing Digital Certificate — certificate used to verify that t | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 22 | 422 | virtualization vendor identifying security vulnerabilities | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/computing-resource-security-techniques.md |
| 5 | 23 | 423 | Security alerting and monitoring concepts and tools | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 24 | 424 | 4.2 Explain the security implications of proper hardware, software, an | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 25 | 425 | ¢ Acquisition/Procurement — Policies and processes that ensure asset | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 26 | 426 | establish a clear chain of accountability for asset security, maintena | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 27 | 427 | baselines, and have not been tampered with or suffered other unauthori | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 28 | 428 | — The process of removing sensitive information from storage media to | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 29 | 429 | + Necessary upon any removal of equipment with data storage (lost, tra | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/asset-management.md |
| 5 | 30 | 430 | Common security techniques to computing cesources, I | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 31 | 431 | 4.3 Explain various activities associated with vulnerability managemen | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 32 | 432 | ¢ Vulnerability Assessment/Testing/Scanning/Auditing involves | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 33 | 433 | —Intrusive Scan — a measure of how much the scanner interacts with the | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 34 | 434 | ¢ Dynamic Analysis — Software testing that examines code behavior duri | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 35 | 435 | + Reputational Threat Intelligence — lists of IP addresses and domains | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 36 | 436 | + Vulnerability Databases and Feeds — security researchers look for vu | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 37 | 437 | profit trade bodies and associations, such as the IEEE, are published | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 38 | 438 | — Includes pages that require registration, pages that block search in | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 39 | 439 | — Often involves launching real attacks on real systems and data that | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 40 | 440 | * Notifications of Breach — the organization policy should indicate wh | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 41 | 441 | * Prioritize — Identifying the most critical vulnerabilities that pose | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 42 | 442 | —An actual vulnerability, attack or intrusion occurred, and an alarm w | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 43 | 443 | vulnerabilities in published operating systems and applications softwa | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 44 | 444 | ¢ Patching — Applying updates and patches to software or systems to fi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 45 | 445 | + Determine if the vulnerabilities identified in the initial scan have | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/vulnerability-management.md |
| 5 | 46 | 446 | Security alerting and monitoring concepts and tools | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 47 | 447 | 4.4 Explain security alerting and monitoring concepts and tools. | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 48 | 448 | — Provides an alerting service for faults such as high temperature, ch | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 49 | 449 | ¢ Reporting — A managerial control that provides insight into the stat | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 50 | 450 | * Benchmarks - Specific information about best practices in configurin | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 51 | 451 | —As events occur on the host, logging data is filtered, aggregated, an | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 52 | 452 | — Data Aggregation — combine and correlate data from network devices a | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 53 | 453 | ¢ Antivirus (AV) — Software capable of detecting and removing virus in | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 54 | 454 | — Monitors all agents by polling them at regular intervals for informa | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 55 | 455 | a structured database that allows for better understanding of IP traff | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 56 | 456 | « Network — Designed to test network hosts, including client PCs, mobi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/alerting-and-monitoring.md |
| 5 | 57 | 457 | Security alerting and monitoring concepts and tools | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 58 | 458 | 4.5 Given a scenario, modify enterprise capabilities to enhance securi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 59 | 459 | — As each packet reaches the device, the rules are applied and interpr | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 60 | 460 | — Outbound Port — used when your computer wants to connect with a serv | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 61 | 461 | 20/21 FIP TCP 989/990 20 data / 24 control 110 POP3 TCP SSL/TLS 995 Re | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 62 | 462 | - Hyper-Text Transfer Protocol (HTTP) — Port 80/TCP — an application p | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 63 | 463 | — Somewhat like a directory assistance or a phone SS 207 25.71.29" | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 64 | 464 | — Adds authentication and integrity to DNS responses jai as, | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 65 | 465 | —If an entry for an Internet Protocol (IP) address is not found in the | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 66 | 466 | — Used to manage and monitor computers, network devices and other devi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 67 | 467 | ¢ File Transfer Protocol (FTP) — Ports 20&21/TCP — unsecure, plaintext | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 68 | 468 | access protocol that is used to access, query, and modify directory se | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 69 | 469 | —Forces outside users to make at least one hop before accessing the tr | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 70 | 470 | — Anomalies can be defined and implemented by an artificial intelligen | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 71 | 471 | —Relies on a set of patterns, trends, signatures, or strings to determ | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 72 | 472 | * Snort — An open-source rule-driven language, which combines the bene | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 73 | 473 | known to host malicious or inappropriate content, or violates the comp | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 74 | 474 | ¢ SPAM Filter — Used to filter unsolicited or undesired bulk electroni | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 75 | 475 | is done at the SMTP level in order to have a centralized solution | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 76 | 476 | —GPOs are able to update settings related to security (user credential | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 77 | 477 | —Unsecure: HTTP (Hypertext Transport Protocol) | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 78 | 478 | (DNS) to block Internet users from accessing unapproved websites on a | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 79 | 479 | + Secure Email Gateway (SEG) - An email security solution that sits in | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 80 | 480 | ¢ FIM (File Integrity Monitoring) — A type of software that reviews sy | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 81 | 481 | - Data Loss Prevention — Systems designed to prevent the loss/leak of | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 82 | 482 | ¢ Data Execution Prevention (DEP) — Attempts EE ee ee eee es | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 83 | 483 | — The client that is connecting will have one of two types of agents r | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 84 | 484 | incorporating data from the network, cloud platforms, email gateway, f | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/enterprise-security-capabilities.md |
| 5 | 85 | 485 | Common security techniques to computing cesources, I | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 86 | 486 | 4.6 Given a scenario, implement and maintain identity and access manag | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 87 | 487 | — The process of setting up a service according to a standard procedur | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 88 | 488 | — Requires revoking any privileged access that had been assigned to th | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 89 | 489 | + Use logs to compare login times for users accessing the systems and | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 90 | 490 | * Permission Inheritance — sub-folders inherit the permissions of the | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 91 | 491 | — chown (change owner) — used to change the owner of file system files | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 92 | 492 | « Federated Identity — Linking a user’s identity with their privileges | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 93 | 493 | network directory databases, which store information about authorized | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 94 | 494 | — Allows third-party applications to verify the identity of the end us | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 95 | 495 | —Allows an application to communicate with another application, operat | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 96 | 496 | * Security Assertion Markup Language (SAML) — Defines standards for ex | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 97 | 497 | ¢ Interoperability — The ability of computer systems or software to ex | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 98 | 498 | + Subjects (users) — label/clearance determines security level and lev | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 99 | 499 | — Supports Boolean logic, in which rules contain "IF, THEN" statements | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 5 | 100 | 500 | — Users cannot make changes to rules, administrators are required for | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 1 | 501 | —An employee’s “role” is determined by their job function or position | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 2 | 502 | ¢ Discretionary Access Control (DAC) — The owner of a file specifies | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 3 | 503 | + Context-aware Authentication — Authenticating users based on criteri | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 4 | 504 | ¢ Multifactor Authentication (MFA) — An authentication scheme that req | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 5 | 505 | ¢ Biometrics — The use of measurements of biological | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 6 | 506 | ¢ Hard Authentication Token — An authentication token generated | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 7 | 507 | — Type of hardware token that does not need an interface to connect wi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 8 | 508 | — Time-based One-Time Password (TOTP) —A PIN is issued with a finite p | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 9 | 509 | knowledge factor authentication secrets, such as length, complexity, a | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 10 | 510 | - Password Manager — Software that can suggest and store site and app | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 11 | 511 | —To set up a passwordless SSH login in Linux all you need to do is to | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 12 | 512 | + Just In Time (JIT) — Enables organizations to grant access to applic | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 13 | 513 | —Credentials are kept in an encrypted database and protected by a mast | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 14 | 514 | —The system generates or enables an account to use to perform the admi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/identity-and-access-management.md |
| 6 | 15 | 515 | Security alerting and monitoring concepts and tools | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 16 | 516 | 4.7 Explain the importance of automation and orchestration related to | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 17 | 517 | — Scripting these tasks helps organizations provide consistent impleme | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 18 | 518 | — Freeing up time to focus on more strategic or complicated analytical | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 19 | 519 | * Continuous Integration (Cl) — A software development method in which | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 20 | 520 | + Efficiency/Time Saving — Enabling repetitive tasks to be performed q | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 21 | 521 | — Apoorly planned or executed automation strategy can add complexity, | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 22 | 522 | —A culture shift in the software industry that aims to bake security i | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/automation-and-orchestration.md |
| 6 | 23 | 523 | Common security techniques to computing cesources, I | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 24 | 524 | 4.8 Explain appropriate incident response activities. | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 25 | 525 | ¢ Incident — A violation or imminent threat of violation of computer s | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 26 | 526 | security posture, and knowledgeable security staff prior to an inciden | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 27 | 527 | (contains methods and techniques used in real-world attacks and can be | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 28 | 528 | action of scripting a single activity, while orchestration is the acti | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 29 | 529 | who prepare for and respond to an emergency incident, such as a natura | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 30 | 530 | — Information Criticality — Primary determinant, based on the data | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 31 | 531 | * nslookup/dig — query name records for a given domain using a particu | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 32 | 532 | * ipconfig/ifconfig — show the configuration assigned to network inter | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 33 | 533 | * scanless — a utility that runs port scans through third-party websit | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 34 | 534 | * grep — searches the input files for lines containing a match to a gi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 35 | 535 | - A protocol enabling different appliances and software applications t | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 36 | 536 | ¢ Bash —A shell interpreter that takes commands in plain text format a | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 37 | 537 | * Containment — The isolation of a threat to minimize the overall dama | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 38 | 538 | —An incident is not fully eradicated until all machines that exhibit t | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 39 | 539 | « Ensure threat is completely mitigated before systems are put back on | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 40 | 540 | —Calculate damage and loss and share information with other department | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 41 | 541 | —Lessons learned might identify a need for additional testing and trai | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 42 | 542 | —Attempts to determine the underlying weakness or vulnerability that a | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 43 | 543 | —Intelligence Fusion and Threat Data — using Security Information and  | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 44 | 544 | — Legal Hold —A process designed to preserve all relevant information  | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 45 | 545 | — Complete — absolute; total; whole; perfect; all the necessary parts | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 46 | 546 | —The goal is to create a snapshot of the environment as it existed at  | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 47 | 547 | * Review Network Traffic Captures/Logs — Review the information captur | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 48 | 548 | * The Forensic Toolkit (FTK) — commercial investigation suite created  | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 49 | 549 | showing the seizure, custody, control, transfer, analysis, and disposi | 4.0 Security Operations | High | Y | Y | Y | course-unit-notes/04-security-operations/incident-response-activities.md |
| 6 | 50 | 550 | Common security techniques to computing cesources, I | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 51 | 551 | 4.9 Given a scenario, use data sources to support an investigation. | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 52 | 552 | — Security logs provide an audit trail of actions performed on the sys | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 53 | 553 | might write log files to its own application directories in whatever f | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 54 | 554 | — Generated by appliances such as routers, firewalls, switches, and ac | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 55 | 555 | — Can include missing patches and noncompliance with a baseline securi | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 56 | 556 | —4.2 Explain the security implications of proper hardware, software, a | 5.0 Security Program Management and Oversight | High | Y | N (non-objective page, recorded in note) | N | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 57 | 557 | _(blank/unreadable)_ | 5.0 Security Program Management and Oversight | High | Y | N (non-objective page, recorded in note) | N | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 58 | 558 | SS RULART All | 5.0 Security Program Management and Oversight | High | Y | N (non-objective page, recorded in note) | N | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 59 | 559 | Management and Oversight | 5.0 Security Program Management and Oversight | High | Y | N (non-objective page, recorded in note) | N | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 60 | 560 | —5.3 Explain the processes associated with third-party risk assessment | 5.0 Security Program Management and Oversight | High | Y | N (non-objective page, recorded in note) | N | course-unit-notes/04-security-operations/data-sources-for-investigation.md |
| 6 | 61 | 561 | * Effective security governance | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 62 | 562 | + Acceptable use policy (AUP) + Onboarding/offboarding + Committees | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 63 | 563 | Guidelines, and Baselines | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 64 | 564 | — Authoritative documents defining the organization’s security commitm | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 65 | 565 | — The goal is to ensure that users do not engage in activities that co | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 66 | 566 | — The overall goal of the incident response plan is to allow the organ | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 67 | 567 | + Job Rotation — Rotating employees through security positions to prov | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 68 | 568 | ¢ Business Continuity Plan (BCP) — Identifies controls and processes t | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 69 | 569 | + Each developer checks out a portion of code for editing on their loc | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 70 | 570 | planned, with consideration for how the change will affect dependent c | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 71 | 571 | — Define the expected outcome of a task, such as a particular configur | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 72 | 572 | ¢ Hashing Algorithms — Defines requirements for the hash functions use | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 73 | 573 | ¢ User Identity Verification — Defines acceptable methods to verify id | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 74 | 574 | « Datacenter and Server Room Security — Defines requirements for card  | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 75 | 575 | « Key Length — Defines the minimum allowable key lengths for different | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 76 | 576 | ¢ Center for Internet Security (CIS) — A not-for-profit organization t | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 77 | 577 | + ISO/MEC 27001 — An international standard that provides an informati | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 78 | 578 | organizations that handle credit cards from major card providers, incl | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 79 | 579 | —More flexible than policies and allow greater discretion for the indi | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 80 | 580 | — Health Insurance Portability and Accountability — Personal Informati | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 81 | 581 | — Health Insurance Portability and Accountability — Family Educational | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 82 | 582 | — Routine audits, inspections, and assessments are commonly used to me | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 83 | 583 | authority and is responsible for setting the strategic direction and p | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 84 | 584 | — The goal is to create a security governance model that effectively s | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 85 | 585 | — Identifies what level of classification and sensitivity the data has | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/effective-security-governance.md |
| 6 | 86 | 586 | Effective security governance | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 87 | 587 | — Risk assessment = Key risk indicators — Business impact analysis | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 88 | 588 | Mission Vulnerabilities Threats and Business Response , | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 89 | 589 | — Allows organizations to make informed decisions regarding resource a | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 90 | 590 | - Circumstance or event with the potential | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 91 | 591 | risk scenario and articulate it such that the cause and effect can cle | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 92 | 592 | - Tornados & Tsunamis = = | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 93 | 593 | — Evaluates previously identified risks to determine their potential i | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 94 | 594 | — Describes the process of identifying and evaluating potential risks  | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 95 | 595 | Annual Rate of Occurrence (ARO) # — how often an event happens per yea | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 96 | 596 | 1. A tornado is estimated to damage 50% (.50) of a facility if it hits | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 97 | 597 | — Includes information regarding risks, their severity, the associated | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 98 | 598 | ¢ Key Risk Indicators (KRI) — Critical predictive indicators organizat | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 99 | 599 | — Describes the specific amount of variance an organization is willing | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 6 | 100 | 600 | ¢ Inherent Risk — the amount of risk that exists, without taking into  | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 7 | 1 | 601 | ; Deciding the benefit is not BYOD policy, access to Facebook from | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 7 | 2 | 602 | + Risk Acceptance — The result after a cost/benefit analysis shows cou | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 7 | 3 | 603 | - Business Impact Analysis (BIA) — The process of assessing what losse | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 7 | 4 | 604 | measured in time, if a database is destroyed by a virus, an RPO of 24  | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 7 | 5 | 605 | + Single Point of Failure (SPoF) — An asset that causes the entire wor | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/risk-management-process.md |
| 7 | 6 | 606 | Third-party risk assessment | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 7 | 607 | 5.3 Explain the processes associated with third-party risk assessment  | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 8 | 608 | —Plays a pivotal role in maintaining the security of IT and business o | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 9 | 609 | * Vendor Selection — Systematically evaluate and assess potential vend | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 10 | 610 | commits the agency and supplier to implementing security controls; any | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 11 | 611 | agreement to express an intent to work together; expressing the intend | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 12 | 612 | ¢ Vendor Monitoring — Continuously overseeing and evaluating vendors t | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 13 | 613 | * Questionnaires — Structured means of obtaining consistent informatio | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 14 | 614 | —A definition of how a pen test will be executed and what constraints  | 5.0 Security Program Management and Oversight | High | Y | Y | Y | course-unit-notes/05-security-program-management-and-oversight/third-party-risk-assessment-and-management.md |
| 7 | 15 | 615 | Effective security governance | 5.0 Security Program Management and Oversight | High | Y | N | N |  |
| 7 | 16 | 616 | 5.4 Summarize elements of effective security compliance. | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 17 | 617 | ¢ Internal — Focuses on operational details, and supports internal dec | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 18 | 618 | specification developed by the American Institute of Certified Public  | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 19 | 619 | — Software licensing requirements can result in the revocation of usag | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 20 | 620 | * Termination of Contracts — Clauses allowing termination if the other | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 21 | 621 | * Compliance with legal and regulatory requirements, industry standard | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 22 | 622 | ¢ Due Diligence — Taking reasonable steps to satisfy a legal requireme | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 23 | 623 | — Protecting privacy data carries significant local, national, and glo | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 24 | 624 | and the head of each agency to conduct annual reviews of information s | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 25 | 625 | —GDPR, the emphasis is placed on the rights and protections of the dat | 5.0 Security Program Management and Oversight | High | Y | N | N |  |
| 7 | 26 | 626 | — Exercise decision-making authority, define the purposes of data proc | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 27 | 627 | — Helps organizations determine appropriate retention periods for diff | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 28 | 628 | —The concept has been discussed and put into practice in several juris | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 29 | 629 | Effective security governance | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 30 | 630 | 5.5 Explain types and purposes of audits and assessments. | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 31 | 631 | —Verifying and validating the accuracy, reliability, and effectiveness | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 32 | 632 | — Evaluate the effectiveness of internal controls, identify noncomplia | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 33 | 633 | * Regulatory authorities or agencies — Perform assessments to ensure c | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 34 | 634 | assess an organization’s overall performance, practices, capabilities, | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 35 | 635 | — External Audit — Carried out by a vendor or contractor that is engag | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 36 | 636 | * Verify a threat exists — use surveillance, social engineering, netwo | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 37 | 637 | — Involves simulating real-world attack scenarios to identify vulnerab | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 38 | 638 | — External — Conducted against the Internet facing hosts of a client's | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 39 | 639 | ¢ Blue Team — Performs the defensive role by operating monitoring and  | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 40 | 640 | + Focuses on secure coding practices and building systems with securit | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 41 | 641 | without directly interacting with them by focusing on collecting publi | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 42 | 642 | — Traffic or data is sent to the computers, servers, or devices to sol | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 43 | 643 | — Allow information/system security professionals to see what devices  | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 44 | 644 | them, this technique is often used by attackers to determine potential | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 45 | 645 | « Network Sniffi ng — The process Tis E6t Vew Go Coptire Anais Satstes | 5.0 Security Program Management and Oversight | High | Y | N | N |  |
| 7 | 46 | 646 | — Detecting network intrusions and undesirable traffic, botnets, troja | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 47 | 647 | Effective security governance | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 48 | 648 | — Phishing — User guidance and training — Reporting and monitoring | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 49 | 649 | — Raises awareness and educates employees about the risks and conseque | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 50 | 650 | — Unusual network traffic, user account activity anomalies, insider th | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 51 | 651 | and confidentiality and emphasize the importance of adhering to these  | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 52 | 652 | — Guides users on the risks associated with malicious charging cables  | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 53 | 653 | * Content development focuses on creating engaging and informative | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 54 | 654 | — Simulations — Recreating system interfaces or using emulators so par | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 55 | 655 | * Successfully executing security training means effectively providing | 5.0 Security Program Management and Oversight | High | Y | N | N |  |
| 7 | 56 | 656 | + Measures the knowledge gained, awareness raised, and behavioral chan | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 57 | 657 | —5.3 Explain the processes associated with third-party risk assessment | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 58 | 658 | _(blank/unreadable)_ | 5.0 Security Program Management and Oversight | High | N | N | N |  |
| 7 | 59 | 659 | SS RULART All | 5.0 Security Program Management and Oversight | High | N | N | N |  |

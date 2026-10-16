---
Unit: Concepts and Strategies to Protect Data
Domain: 3.0 Security Architecture (sub-objective 3.3 — Compare and contrast concepts and strategies to protect data)
Source: Pt4 p.40-49 (global 340-349; course slides 3-92 to 3-101). Boundaries: Pt4 p.40 = 3.3 roadmap (3-92, "Concepts and strategies to protect data" highlighted); Pt4 p.50 = 3.4 roadmap (3-102, next section, not part of this unit); Pt4 p.39 = last 3.2 page
Extraction_Status: Fully Extracted (all 10 pages Pt4 p.40-49 read via vision at 80 dpi)
Pages_Done: Pt4 p.40-49
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — same-session re-check of the note against the renders (see Validation record at the end); not an independent second reader
---

## Roadmap and Section Topics (Source: Pt4 p.40-41)

- Pt4 p.40 is the section roadmap: the four Domain 3 sections are listed with "Concepts and strategies to protect data" highlighted (Source: Pt4 p.40).
- Section Topics slide, "3.3 Compare and contrast concepts and strategies to protect data" (Source: Pt4 p.41):
  - **Data types**: Regulated; Trade secret; Intellectual property; Legal information; Financial information; Human- and non-human-readable
  - **Data classifications**: Sensitive; Confidential; Public; Restricted; Private; Critical
  - **General data considerations**: Data states (Data at rest; Data in transit; Data in use); Data sovereignty; Geolocation
  - **Methods to secure data**: Geographic restrictions; Encryption; Hashing; Masking; Tokenization; Obfuscation; Segmentation; Permission restrictions

## Data Types (Source: Pt4 p.42-43)

| Data type | Definition as printed | Examples / detail as printed |
|---|---|---|
| Regulated | Information that has storage and handling compliance requirements defined by national and state legislation and/or industry regulations (Source: Pt4 p.42) | Information subject to legal or regulatory requirements regarding their handling, storage, and protection (Source: Pt4 p.42) |
| Trade Secret | Intellectual property that gives a company a competitive advantage but hasn't been registered with a copyright, trademark, or patent (Source: Pt4 p.42) | Formulas, processes, methods, techniques, customer lists, pricing information, marketing strategies, and other business-critical data (Source: Pt4 p.42) |
| Legal Information | Documents and records that relate to matters of law, such as contracts, property, court cases, and regulatory filings (Source: Pt4 p.42) | Documents, contracts, legal agreements, court records, litigation information, intellectual property filings, regulatory filings, and other legal documents (Source: Pt4 p.42) |
| Financial Information | Data regarding bank and investment accounts, plus information such as payroll and tax returns (Source: Pt4 p.43) | Financial activities, performance, and transactions, including financial statements, balance sheets, income statements, cash flow statements, audit reports, tax records, financial projections, budgets, and other financial reports (Source: Pt4 p.43) |
| Human-readable Data | Information stored in a file type that human beings can access and understand using basic viewer software, such as documents, images, video, and audio (Source: Pt4 p.43) | Information that humans can easily understand and interpret without additional processing or translation (Source: Pt4 p.43) |
| Non-human-readable Data | Information stored in a file that human beings cannot read without a specialized processor to decode the binary or complex structure (Source: Pt4 p.43) | Not easily understood or interpreted by humans in its raw form; may be in a machine-readable format such as binary code, encrypted data, or data represented in a complex structure or encoding that requires specialized software or algorithms to decipher and interpret (Source: Pt4 p.43) |

- Intellectual property as a data type is not on a Data Types slide; it appears on the Data Classification slide as "Proprietary or Intellectual Property (IP)" (see below) (Source: Pt4 p.44).

## Data Classification (Source: Pt4 p.44-45)

| Classification (label as printed) | Definition as printed | Detail as printed |
|---|---|---|
| Public (Unclassified) | No restrictions on viewing the data (Source: Pt4 p.44) | Presents no risk to an organization if disclosed but does present a risk if it is modified or not available (Source: Pt4 p.44) |
| Confidential (Secret) | Information is highly sensitive, for viewing only by approved persons within the owner organization, and possibly by trusted third parties under NDA (Source: Pt4 p.44) | — |
| Critical (Top Secret) | Information is too valuable to allow any risk of its capture (Source: Pt4 p.44) | Viewing is severely restricted (Source: Pt4 p.44) |
| Proprietary or Intellectual Property (IP) | Information created and owned by the company, typically about the products or services that they make or perform (Source: Pt4 p.44) | An obvious target for competitors; IP in some industries (such as defense or energy) is of interest to foreign governments; may also represent a counterfeiting opportunity (movies, music, books) (Source: Pt4 p.44) |
| Private/Personal Data | Information that relates to an individual identity (Source: Pt4 p.45) | PII such as names, addresses, social security numbers, financial information, and sensitive data like health records, login credentials, biometric data, and confidential business information (Source: Pt4 p.45) |
| Sensitive | Usually used in the context of personal data (Source: Pt4 p.45) | Privacy-sensitive information about a person could harm them if made public and could prejudice decisions made about them if referred to by internal procedures; under the EU's GDPR, sensitive personal data includes religious beliefs, political opinions, trade union membership, gender, sexual orientation, racial or ethnic origin, genetic data, and health information (Source: Pt4 p.45) |
| Restricted | Sensitive information that requires stringent controls and limited access due to its highly confidential nature (Source: Pt4 p.45) | Unauthorized disclosure could cause significant harm to individuals, organizations, or national security (Source: Pt4 p.45) |

- The slides give no ranking or ordering of these labels; they are listed as separate definitions across two slides (Source: Pt4 p.44-45).

## General Data Considerations

### Data states / Protection of data (Source: Pt4 p.46)

- **Data at Rest** — all data in computer storage (Source: Pt4 p.46)
- **Data in Motion** — data in transit across a network infrastructure (Source: Pt4 p.46). (The Section Topics slide calls this "Data in transit" (Source: Pt4 p.41).)
- **Data in Use** — data being used by an application or resident in memory (Source: Pt4 p.46)
- **Data Replication** — where that data is replicated (backup or copy) and the implemented controls for the protection of the replicated data (Source: Pt4 p.46)
- Diagram: a hard-disk platter showing hex-like characters with an arrow to a second, empty platter (replication/copy); callout "You can't protect your data if you don't know where it is at all times" (Source: Pt4 p.46)

### Data sovereignty and geolocation (Source: Pt4 p.47)

- **Data Sovereignty** — jurisdiction preventing or restricting processing and storage from taking place on systems [that] do not physically reside within that jurisdiction (wording as printed, verb "do" sic) (Source: Pt4 p.47)
- **Geographical Considerations** (the slide title is "Data Sovereignty and Geolocation"; the term "geolocation" itself is not defined) (Source: Pt4 p.47):
  - Select storage locations to mitigate data sovereignty issues
  - Define access controls on the basis of client location

## Methods to Secure Data (Source: Pt4 p.48)

| Method | Definition as printed |
|---|---|
| Geographic Restrictions | Limiting access to data based on specific geographic locations (Source: Pt4 p.48) |
| Encryption | Converting data into a coded format that can only be accessed or deciphered with an encryption key or password (Source: Pt4 p.48) |
| Hashing | Converting data into a fixed-length string of characters using a hashing algorithm (Source: Pt4 p.48) |
| Masking | Replacing sensitive data with fictional or partially concealed values while preserving the format and length of the original data (Source: Pt4 p.48) |
| Tokenization | Replacing sensitive data with a randomly generated token while securely storing the original data in a separate location (Source: Pt4 p.48) |
| Obfuscation | Modifying data to make it difficult to understand or reverse engineer without altering functionality (Source: Pt4 p.48) |
| Segmentation | Securing data by dividing networks, data, and applications into isolated components to improve sensitive data protection, limit the impact of a breach, and improve network security (Source: Pt4 p.48) |
| Permission Restrictions | Controlling access to data based on user permissions (Source: Pt4 p.48) |

## Privacy Enhancing Technologies (Source: Pt4 p.49)

Not an official 3.3 bullet, but it is the last slide in the section as delivered.

- **Data Minimization** — limiting data collection to only what is required to fulfill a specific purpose (Source: Pt4 p.49)
- **Deidentification** — removing personal information from shared data sets (Source: Pt4 p.49)
- **Anonymization** — individual subjects can no longer be identified, even if the data set is combined with other data sources (Source: Pt4 p.49)
- **Pseudo-anonymization** — modifies or replaces identifying information so that reidentification depends on an alternate data source which must be kept separate (Source: Pt4 p.49)
- **Reidentification Attacks** — combines a deidentified data set with other data sources, such as public voter records, to discover how secure the deidentification method that was used (Source: Pt4 p.49)
  - **K-anonymous information** — "data that can be linked to two or more individuals" (as printed); this means the data does not unambiguously reidentify a specific individual, but there is a significant risk of reidentification, given the value of K (Source: Pt4 p.49)
  - Example: if k=5, any group that can be identified within the data set contains at least five individuals (Source: Pt4 p.49)

## Source quirks (kept as printed)

- Classification labels carry government-style aliases: Public (Unclassified), Confidential (Secret), Critical (Top Secret) (Source: Pt4 p.44).
- "Data in Motion" (p.46) vs. "Data in transit" (p.41) for the same state.
- Data sovereignty sentence has a grammar slip ("systems do not physically reside") (Source: Pt4 p.47).
- Masking is defined as keeping the format and length of the original data; tokenization keeps the original in a separate location; these two definitions are the only contrast the slides draw between methods (Source: Pt4 p.48).

## Official-objective gap check (3.3)

Official sub-bullets as listed on Pt4 p.41 and in `source_coverage/objective_mapping.md`:

| Official bullet | Result | Support / gap |
|---|---|---|
| Data types: Regulated | Covered | Pt4 p.42 |
| Data types: Trade secret | Covered | Pt4 p.42 |
| Data types: Intellectual property | Covered | Defined under classification as Proprietary/IP (Pt4 p.44); trade secret also described as IP (Pt4 p.42) |
| Data types: Legal information | Covered | Pt4 p.42 |
| Data types: Financial information | Covered | Pt4 p.43 |
| Data types: Human- and non-human-readable | Covered | Pt4 p.43 |
| Classifications: Sensitive | Covered | Pt4 p.45 |
| Classifications: Confidential | Covered | Pt4 p.44 |
| Classifications: Public | Covered | Pt4 p.44 |
| Classifications: Restricted | Covered | Pt4 p.45 |
| Classifications: Private | Covered | Pt4 p.45 (Private/Personal Data) |
| Classifications: Critical | Covered | Pt4 p.44 |
| Data states: at rest, in transit, in use | Covered | Pt4 p.46; one-line definitions, no protection examples per state |
| Data sovereignty | Covered | Pt4 p.47; one definition |
| Geolocation | Weak | Only "Geographical Considerations" (two bullets); the term is not defined (Pt4 p.47) |
| Methods: Geographic restrictions | Weak | One-line definition (Pt4 p.48); linked only loosely to access-control-by-location (Pt4 p.47) |
| Methods: Encryption | Weak | One-line definition; no algorithms, key types, or per-state use on these slides (Pt4 p.48) |
| Methods: Hashing | Weak | One-line definition; one-way/integrity purpose not stated (Pt4 p.48) |
| Methods: Masking | Covered | Definition with format/length preservation (Pt4 p.48) |
| Methods: Tokenization | Covered | Definition with separate storage of the original (Pt4 p.48) |
| Methods: Obfuscation | Weak | One-line definition (Pt4 p.48) |
| Methods: Segmentation | Weak | One-line definition (Pt4 p.48) |
| Methods: Permission restrictions | Weak | One-line definition (Pt4 p.48) |

Overall under the strict rule: **Weakly Covered** (all bullets are present, but geolocation and five of the eight methods are one-line definitions with no comparison, example, or scenario). Slides also cover Privacy Enhancing Technologies and data replication (Pt4 p.46, p.49), which are not official 3.3 bullets.

## Validation record

- Date: 2026-10-16. Scope: all 10 pages Pt4 p.40-49 re-compared against the note after writing (see corrections below).
- Same-session re-check against the renders; not an independent second reader.
- Pt4 p.43, p.45, p.49 re-rendered at 110 dpi and compared line by line; all other pages compared against the 80 dpi renders (text legible; no table-cell ambiguity).
- Corrections: none; no transcription errors found.

---
Unit: Hardware, Software, and Data Asset Management
Domain: 4.0 Security Operations (sub-objective 4.2 — Explain the security implications of proper hardware, software, and data asset management)
Source: Pt5 p.23-29 (global 423-429; course slides 4-38 to 4-44). Boundaries: Pt5 p.23 = 4.2 roadmap (4-38); Pt5 p.30 = 4.3 roadmap (4-45)
Extraction_Status: Fully Extracted (all 7 pages read via vision)
Pages_Done: Pt5 p.23-29
Pages_Remaining: none
Validation_Status: Validated (2026-10-16) — all 7 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt5 p.23-24)

- Pt5 p.23 (4-38) is the Domain 4 roadmap slide with "Hardware, software, and data asset management" highlighted. (Source: Pt5 p.23)
- Pt5 p.24 (4-39) is the 4.2 Section Topics slide: Acquisition/procurement process; Assignment/accounting (Ownership, Classification); Monitoring/asset tracking (Inventory, Enumeration); Disposal/decommissioning (Sanitization, Destruction, Certification, Data retention). (Source: Pt5 p.24)

## Acquisition/procurement (Source: Pt5 p.25)

- **Acquisition/Procurement** — policies and processes that ensure asset and service purchases and contracts are fully managed, secure, use authorized suppliers/vendors, and meet business goals. (Source: Pt5 p.25)
- This is the only content on the slide; no further detail (e.g. examples of vendor vetting) is given.

## Assignment/accounting (Source: Pt5 p.26)

- **Assigning asset ownership** — designating specific individuals or teams within the organization as responsible for particular assets to establish a clear chain of accountability for asset security, maintenance, and ongoing management. (Source: Pt5 p.26)
- **Asset classification** — organizing assets based on their value, sensitivity, or criticality to the organization. Enables the consistent and repeatable application of required security controls, effective prioritization for maintenance and updates, and appropriate budget allocation. (Source: Pt5 p.26)

## Monitoring/asset tracking (Source: Pt5 p.27)

- **Monitoring/asset tracking** — enumeration and inventory processes and software that ensure physical and data assets comply with configuration and performance baselines, and have not been tampered with or suffered other unauthorized access. (Source: Pt5 p.27)
- There are several ways to perform asset enumeration, depending on the size and complexity of the organization and the types of assets involved (Source: Pt5 p.27):
  - Manual inventory
  - Network scanning
  - Asset management software
  - Configuration Management Database (CMDB)
  - Mobile Device Management (MDM) solutions
  - Cloud asset discovery
- **Tracking** methods (Source: Pt5 p.27): asset tags (bold on the slide); databases (inventory); Radio Frequency Identifier (RFID); GPS.
- The slide does not separately define "inventory" and "enumeration"; it uses them together in the first definition.

## Disposal/decommissioning (Source: Pt5 p.28)

| Term | Slide definition |
|---|---|
| Disposal/decommissioning | The policies and procedures that govern the removal of devices and software from production networks, and their subsequent disposal through sale, donation, or as waste |
| Sanitization | The process of thoroughly and completely removing data from a storage medium so that file remnants cannot be recovered. Also: removing sensitive information from storage media to prevent unauthorized access or data breaches; uses specialized techniques (data wiping, degaussing, or encryption) to ensure the data becomes irretrievable |
| Destruction | The physical or electronic elimination of information stored on media, rendering it inaccessible and irrecoverable. Methods include shredding, crushing, or incinerating storage devices. Electronic destruction involves overwriting data multiple times or using degaussing techniques to eliminate magnetic fields on storage media |
| Certification | The documentation and verification of the data sanitization or destruction process. Often involves obtaining a certificate of destruction or sanitization from a reputable third-party provider, attesting that the data has been securely removed or destroyed in accordance with industry standards and regulations |
| Data retention | The process an organization uses to maintain the existence of and control over certain data in order to comply with business policies and/or applicable laws and regulations |

(Source: Pt5 p.28)

## Data sanitization/destruction methods (Source: Pt5 p.29)

- Necessary upon any removal of equipment with data storage (lost, transferred, disposed): PCs, laptops, servers, mobile devices; printers, copy machines, routers, switches. (Source: Pt5 p.29)
- **Magnetic media** (Source: Pt5 p.29):
  - **Overwriting** (also called purging, shredding, wiping, zeroization on the slide). Write over the data seven times (BCWipe) — marked *high level*. Deleting a file does not erase its contents.
  - **Degaussing** — expose the media to a strong magnetic field — marked *low level*.
  - **Destruction** — damage or destroy the media itself: shredding (hard copies, floppy or optical disks, and tape media); pulverizing (reducing media to dust); incinerating (burning media); pulping (chemically altering media); bathing metal components in acid.
- **Solid State Drives (SSDs)** (Source: Pt5 p.29):
  - **ATA Secure Erase** — marked as empty, restoring it to factory default. Turn on encryption before the drive is ever used.
  - **Destruction** — the slide's final line is a bare "– Destruction" at the bottom edge of the slide; no sub-bullets are visible. [POSSIBLE CLIPPING] Do not assume content was lost: the page image ends at the footer.
- [CONFLICT/ODD] The slide groups "purging, shredding, wiping, zeroization" under overwriting; the term "shredding" is also used under destruction on the same slide. Recorded as printed.
- [CONFLICT/ODD] Overwriting is marked "high level" and degaussing "low level" on the slide. This appears to describe sanitization effort/level as the slide's own label; the slide does not explain the levels.
- Two photos (a burning hard drive, a person buried in shredded paper) are decorative.
- The note's terms "inventory" and "enumeration" are used together on Pt5 p.27; the three overwriting-related labels in the SSD/magnetic lists are as printed.

## Validation log
- Extraction: all 7 pages read at 100 dpi and written to this note.
- Validation (separate pass, 2026-10-16): all 7 pages (Pt5 p.23-29) re-opened at 130 dpi and compared item by item (lists, terms, numbers, page citations). No omissions or wrong citations found; no changes were needed to the extracted content.
- Slide oddities kept as printed: "seven times (BCWipe)", "high level"/"low level" labels, the bare "– Destruction" line at the foot of Pt5 p.29, and "Radio Frequency Identifier" (Pt5 p.27, sic).

## Official-objective gap check (4.2 bullets as listed on the slides' Section Topics slide, Pt5 p.24)
| Official bullet | Status | Where |
|---|---|---|
| Acquisition/procurement process | Covered — one definition only; no detail | Pt5 p.25 |
| Assignment/accounting: ownership | Covered | Pt5 p.26 |
| Assignment/accounting: classification | Covered | Pt5 p.26 |
| Monitoring/asset tracking: inventory | Covered (no separate definition; tracking methods listed) | Pt5 p.27 |
| Monitoring/asset tracking: enumeration | Covered (six enumeration methods listed) | Pt5 p.27 |
| Disposal/decommissioning: sanitization | Covered | Pt5 p.28-29 |
| Disposal/decommissioning: destruction | Covered | Pt5 p.28-29 |
| Disposal/decommissioning: certification | Covered | Pt5 p.28 |
| Disposal/decommissioning: data retention | Covered — one definition only | Pt5 p.28 |

All official bullets are present and defined. Depth is shallow for acquisition/procurement and data retention (one definition each); the exam question style for 4.2 is definitional, so this is judged adequate. Extra slide content: asset tags/RFID/GPS tracking, overwrite/degauss/destruction methods, SSD handling.
No gaps requiring outside material.

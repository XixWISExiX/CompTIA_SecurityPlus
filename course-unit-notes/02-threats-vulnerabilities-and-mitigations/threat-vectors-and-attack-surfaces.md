---
Unit: Threat Vectors and Attack Surfaces
Domain: 2.0 Threats, Vulnerabilities, and Mitigations (sub-objective 2.2 — Explain common threat vectors and attack surfaces)
Source: Pt2 p.33-50 (global 133-150; course slides 2-10 to 2-27). Boundaries: Pt2 p.33 = 2.2 roadmap (2-10); Pt2 p.51 = 2.3 roadmap (2-28, "Types of vulnerabilities" highlighted), so 2.2 ends at Pt2 p.50
Extraction_Status: Fully Extracted (all 18 pages read via vision at 100 dpi; two small-text diagrams re-read at 250 dpi)
Pages_Done: Pt2 p.33-50
Pages_Remaining: none
Validation_Status: Validated (2026-10-16) — all 18 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt2 p.33-34)

- Pt2 p.33 (2-10) is the Domain 2 roadmap slide with "Threat vectors and attack surfaces" highlighted. Other entries: Threat actors and motivations; Types of vulnerabilities; Indicators of malicious activity; Mitigation techniques used to secure the enterprise. (Source: Pt2 p.33)
- Pt2 p.34 (2-11) is the 2.2 Section Topics slide, "2.2 Explain common threat vectors and attack surfaces." (Source: Pt2 p.34)
  - **Message-based:** Email; Short Message Service (SMS); Instant messaging (IM)
  - **Image-based**
  - **File-based**
  - **Voice call**
  - **Removable device**
  - **Vulnerable software:** Client-based vs. agentless
  - **Unsupported systems and applications**
  - **Unsecure networks:** Wireless; Wired; Bluetooth
  - **Open service ports**
  - **Default credentials**
  - **Supply chain:** Managed service providers (MSPs); Vendors; Suppliers
  - **Human vectors/social engineering:** Phishing; Vishing; Smishing; Misinformation/disinformation; Impersonation; Business email compromise; Pretexting; Watering hole; Brand impersonation; Typosquatting
- [GAP] The phrase "attack surface" appears only in the section title; no slide in Pt2 p.33-50 defines or discusses "attack surface".

## Threat vectors overview (Source: Pt2 p.35)

Slide title "Threat Vectors" — a four-group outline, terms only (no definitions):

| Group | Items on the slide |
|---|---|
| Vulnerable Software Vectors | Unsupported Systems and Applications; Client-Based; Agentless |
| Message-Based Vectors | Email; Short Message Service (SMS); Instant Messaging (IM); Telephony (VoIP); Web and Social Media |
| Lure-Based Vectors | Removable Device (USB); Executable File; Document Files; Image Files |
| Network-Based Vectors | Direct Access; Wired Network; Remote and Wireless Network; Cloud Access; Bluetooth Network; Default Credentials; Open service port |

(Source: Pt2 p.35)

## Wireless vulnerabilities (Source: Pt2 p.36-37)

Slide title "Wireless Vulnerabilities" (p.36) and "– continued" (p.37).

- **Weak Encryption** — the use of weak encryption opens up the network to potential attack, sniffing, spoofing, and data loss. (Source: Pt2 p.36)
- **Wi-Fi Protected Setup (WPS)** — designed to enable easy connectivity and configuration with WAPs, however due to problems with how it is implemented the eight-digit pin could be brute-forced. (Source: Pt2 p.36)
- **AP Isolation** — wireless clients connected to the WAP are segmented and unable to communicate with each other. (Source: Pt2 p.36)
- **Ad Hoc Networks** — allow for wireless connections between devices without a centralized WAP or WLAN controller. (Source: Pt2 p.36)
- **War-Chalking** — attacker marks a location to indicate a vulnerable WAP for other attackers. (Source: Pt2 p.36)
  - Diagram (credited "Source: CEH All-in-One Exam Guide"): five war-chalking symbols, each a pair of facing arcs. (Source: Pt2 p.36)
    - Free Wi-Fi — plain arcs. 
    - Free Wi-Fi — the word "Anything" above; caption: "Anything can be the SSID or the administrative password".
    - Restricted Wi-Fi — circle with a key-like line through the arcs; caption: "May also have words or codes around it indicating hacks".
    - Pay-for-access — circle containing "$"; caption: "May also have words or codes around it indicating hacks".
    - MAC filtered — circle containing a padlock; caption: "Sometimes lists of MACs will be written nearby".
- **Antenna Power and Signal Strength** (Source: Pt2 p.37)
  - Cannot modify the gain of an antenna without changing its physical properties.
  - Many wireless access points include a **power setting** that you can manipulate to increase or decrease the transmit power.
    - Administrators sometimes *reduce the power level* to restrict access to a small area such as a conference room, or to prevent wireless users from connecting from the parking lot or somewhere else outside the building.
    - Administrators sometimes *increase the power level* to increase the range of the AP.
- **Rogue Access Point** — unauthorized wireless access points (WAPs) that allows access to secure networks. (Source: Pt2 p.37)
  - Can also include laptop computers and/or mobile devices as these devices can contain applications that allow the device to function as a WAP.
  - Site surveys, NIDS/NIPS and device accountability audits should be done regularly to help detect these devices.

## Bluetooth vulnerabilities (Source: Pt2 p.38)

- **Bluejacking** — sending unsolicited messages (SPAM) to and from a Bluetooth enabled device.
- **Bluesnarfing** — unauthorized access, theft, or stealing of information from a Bluetooth enabled device.
- Picture only (Bluetooth speaker, laptop, phone); decorative.

(Source: Pt2 p.38)

## Default credentials and misconfigurations (Source: Pt2 p.39)

- **Misconfigurations** result from improperly configured operating systems, applications, and networks. They can provide easy ways to gain unauthorized access. (Source: Pt2 p.39)
- Examples of misconfigurations listed (Source: Pt2 p.39):
  - **Default credentials:** admin/admin; administrator/administrator; user/password
  - Unused ports left open
  - HTTP instead of HTTPS
  - Unused, running services
  - Default "administrator" privileges
  - A link to https://www.routerpasswords.com (a source of default router passwords — the slide gives only the link, no explanation)
- Picture: hand touching a login box (Username: Administrator, Password masked, Login/Cancel); decorative. (Source: Pt2 p.39)
- Note: the slide has no separate definition of "open service ports"; it appears only as "Unused ports left open" (here) and "Open service port" in the network-based vectors list (Pt2 p.35).

## Supply chain (Source: Pt2 p.40)

- **Supply Chain** — the end-to-end process of designing, manufacturing, and distributing goods and services to a customer.
  - Rather than attack the target directly, a threat actor may seek ways to infiltrate it via companies in its supply chain (Target data breach).
- **Managed Service Provider (MSP)** — provisions and supports IT resources such as networks, security, or web infrastructure.
  - Useful when an organization finds it cheaper or more reliable to outsource all or part of IT provision rather than try to manage it directly.
- **Supplier** — obtains products directly from a manufacturer to sell in bulk to other businesses.
- **Vendor** — an entity (supplier) that directly sells finished products or services to consumers or businesses.
- **Business Partner** — implies a closer relationship where two companies share quite closely aligned goals and marketing opportunities.

(Source: Pt2 p.40)

## Social engineering overview (Source: Pt2 p.41)

- **Social Engineering** — the clever manipulation of the natural human tendency to trust.
- Callout (orange box): "The only defense against Social Engineering is User Training and Awareness".
- Footer bar: "Social Engineering is a no-tech or low-tech method that uses the human mind to bypass security controls". Small tag: "Trickery".
- **Human-based:** Dumpster Diving; Impersonation / Spoofing / Masquerading; Technical Support / Help Desk Fraud; Shoulder Surfing; Tailgating / Piggybacking; Eavesdropping (listening).
- **Computer-based:** Sniffing / Eavesdropping (Network, VoIP); Phishing / Whaling / Spear Phishing / SPAM; Pop-up Windows Attacks; Chat / Messenger Attacks.
- Picture of three people at a table; decorative.

(Source: Pt2 p.41)

## SPAM / SPIM / SPIT / SMiShing (Source: Pt2 p.42)

- **SPAM** — unsolicited email that is sent to many recipients.
- **SPIM** — unwanted message delivered via an Instant Messaging or chat applications.
- **SPIT** — unwanted message delivered via Internet Telephony.
- **SMiShing** — a form of phishing using SMS text messages.
- Picture of an email folder list (Inbox 68, Draft, Sent Mail, Spam 221, Trash); decorative.

(Source: Pt2 p.42)

## Phishing / Vishing / Quishing (Source: Pt2 p.43)

- **Phishing** — sending an email or displaying a web announcement that falsely claims to be from a legitimate business/site.
  - **Spear Phishing** — targeting specific users/groups.
  - **Whaling** — a type of spear phishing that targets the "big fish" (CEO, senior executives, board members).
- **Vishing (voice phishing)** — the attacker uses the telephone to contact the victim rather than email.
- **Quishing (QR Code phishing)** — Quick Response (QR) Codes are used by an attacker to redirect traffic to a malicious site.
- Pictures: hacker with fishing rod and laptop, a whale, a hacker with phone and open padlock, a phone scanning a QR code on a hook; decorative.

(Source: Pt2 p.43)

## Social engineering attacks (principles) (Source: Pt2 p.44)

Slide title "Social Engineering Attacks":

| Term | Slide definition |
|---|---|
| Pretexting | an attacker tries to convince/persuade a victim through a convincing story or subliminal conditioning |
| Authority | convincing a target that the attacker comes from a position of authority |
| Intimidation | bullying or intimidating a user from a position of perceived authority |
| Impersonation | impersonate someone in a position of authority, or who is otherwise authorized to receive information from the target and convince them to act in a certain way (help desk/tech support) |
| Consensus/social proof | gaining the support of a group |
| Scarcity | ensuring the attacker can offer the target something that is valuable |
| Urgency | forcing the target to make a quick or hasty decision |
| Familiarity/liking | building a connection with a target through a common interest |
| Trust | building trust with a target by providing favors or spending time with them |

(Source: Pt2 p.44)

- Picture: hooded figure behind a hexagon diagram with "Social engineering" in the centre. Hexagon labels (re-read at 250 dpi): Baiting; Spear phishing; Pretexting; Shoulder surfing; Quid pro quo; Phishing; Tailgating; Dumpster diving; and one label that reads "Waling" at that resolution (probably "Whaling" — [ILLEGIBLE]/unconfirmed). Baiting and quid pro quo appear only in this picture, with no definition on any slide in this unit. (Source: Pt2 p.44)

## Social engineering methods (Source: Pt2 p.45)

- **Shoulder Surfing** — looking over someone's "shoulder" to read information on a computer screen without their knowledge.
  - Attackers use webcams and smartphone cameras to "shoulder surf" users at ATM terminals.
- **Dumpster Diving** — sifting through discarded materials in a dumpster or garbage bin.
  - Post-it notes with passwords
  - Printed files
  - Personally Identifiable Information (PII)
- **Electronic Dumpster Diving** — using search engines to look for documents previously posted online.
- **Google Dorking/Hacking** — using customized search strings within Google.
  - `intext:"SSN" filetype:xlsx` — find Excel documents that contain the term "SSN".
  - `allintitle: "passwords" filetype:docx` — find Word documents that contain the term "passwords".
- Pictures: shoulder surfer with magnifying glass, dumpster; decorative.

(Source: Pt2 p.45)

## Hoax / Typosquatting (Source: Pt2 p.46)

- **Hoaxes** — an email that attempts to spread fake news or information throughout an organization.
  - The hoax claims a "deadly virus" circulating through the Internet and that the recipient should erase specific files, change security configurations, or forward the message to other users.
- **Typo Squatting/Bit Flipping** — placing malicious information on domains arrived at through common typos (gogle.com, fscebook.com, yahooo.com).
  - Slide groups "Typo Squatting" and "Bit Flipping" under one definition; the examples given are all typo-style domains. Bit flipping is not separately explained.
- Pictures: "SCAM ALERT" key; "TYPO" weightlifter; decorative.

(Source: Pt2 p.46)

## Misinformation / Disinformation (Source: Pt2 p.47)

- Disinformation/misinformation tactics could be used to create fake social media posts or referrers to boost search ranking.
  - Persuade users to install a "must-have" app that is actually a Trojan.
- **Misinformation** — repeating false claims or rumors without the intention to deceive.
- **Disinformation** — a type of attack that falsifies an information resource that is normally trusted by others.
  - A purposeful motivation to deceive
  - Changing the content of a website
  - Manipulating search engines to inject fake sites
  - Using bots to post false information to social media sites

(Source: Pt2 p.47)

## Business Email Compromise (BEC) (Source: Pt2 p.48)

- **Business Email Compromise (BEC)** — an impersonation attack in which the attacker gains control of an employee's account and uses it to convince other employees to perform fraudulent actions.
  - Financial motivation, where the objective is to persuade a budget holder to authorize a fraudulent payment or wire transfer.
  - Typically, an executive or senior manager.
    - The threat actor poses as a colleague, business partner, or vendor.
    - The threat actor is likely to perform reconnaissance to obtain a detailed understanding of the target and the best psychological approach and pretexts to trick them.

(Source: Pt2 p.48)

## Watering hole attack (Source: Pt2 p.49)

- **Watering Hole Attack** — a targeted attack designed to compromise users within a specific industry or group of users by infecting websites they typically visit and luring them to a malicious site, with an end goal of gaining access to the organization's network.
- Picture: a cartoon pond in a forest; decorative.

(Source: Pt2 p.49)

## Brand impersonation (Source: Pt2 p.50)

- **Brand impersonation (brand spoofing)** — a form of phishing cyber-attack that aims to solicit sensitive information from victims by posing as a legitimate brand.
  - Duplicating a company's logos and formatting
  - Mimic the style or tone of email communications or website copy

(Source: Pt2 p.50)

## Boundary (Source: Pt2 p.51)
- Pt2 p.51 (2-28) is the Domain 2 roadmap slide with "Types of vulnerabilities" highlighted, so 2.2 ends at Pt2 p.50. (Source: Pt2 p.51)

## Slide wording kept as printed (not corrected)
- "Unsecure networks" (p.34); "Typo Squatting/Bit Flipping" (p.46); "SMiShing" (p.42) vs "Smishing" (p.34); "War-Chalking" (p.36); "Impersonation" appears both as a human-based method (p.41) and as a defined attack (p.44); BEC's definition itself calls BEC an "impersonation attack" (p.48).
- Slide content beyond the Section Topics list (kept): wireless vulnerabilities such as WPS, AP isolation, ad hoc networks, war-chalking, antenna power, rogue AP; SPIT; quishing; the social-engineering principles table (authority … trust); dumpster diving, electronic dumpster diving, Google dorking; hoaxes; business partner.

## Validation log
- Extraction: 18 pages read at 100 dpi (Pt2 p.33-50) plus boundary p.51; hexagon diagram (p.44) and war-chalking diagram (p.36) re-read at 250 dpi.
- Validation (separate pass, 2026-10-16): Pt2 p.33-50 all re-opened at 130 dpi and compared item by item (section-topic list, the four-group threat-vector table, every wireless/Bluetooth/supply-chain/social-engineering definition, the nine principle definitions, Google-dork strings, BEC sub-bullets, example domains, page citations). Pt2 p.51 is the 2.3 roadmap (boundary, seen at 100 dpi). Result: no transcription errors, omissions, or wrong citations found; no corrections were needed. The one unresolved item is the tenth hexagon label on p.44, which stays flagged as unconfirmed ("Waling", probably "Whaling").
- Slide wording kept as printed: see "Slide wording kept as printed" above.

## Official-objective gap check (2.2 bullets as listed on the slides' Section Topics slide, Pt2 p.34)
| Official bullet | Status | Where / note |
|---|---|---|
| Message-based: email | Covered | SPAM = unsolicited email (p.42); phishing by email (p.43); listed p.35 |
| Message-based: SMS | Covered | SMiShing (p.42) |
| Message-based: instant messaging | Covered | SPIM (p.42); chat/messenger attacks (p.41) |
| Image-based | **Weak** — "Image Files" is a bare list item under Lure-Based Vectors; no explanation | p.35 |
| File-based | **Weak** — "Executable File" and "Document Files" are bare list items | p.35 |
| Voice call | Covered | Vishing (p.43); SPIT (p.42); "Telephony (VoIP)" listed (p.35) |
| Removable device | **Weak** — "Removable Device (USB)" is a bare list item | p.35 |
| Vulnerable software: client-based vs. agentless | **Weak** — both terms listed under Vulnerable Software Vectors, never defined or contrasted | p.35 |
| Unsupported systems and applications | **Weak** — listed only in this unit (p.35). A possible later treatment elsewhere in Domain 2 is unverified (OCR hint only) and will be checked when 2.3 is extracted | p.35 |
| Unsecure networks: wireless | Covered | p.36-37 |
| Unsecure networks: wired | **Weak** — "Wired Network" is a bare list item; no wired-specific vulnerability discussed | p.35 |
| Unsecure networks: Bluetooth | Covered (bluejacking, bluesnarfing) | p.38 |
| Open service ports | **Weak** — "Open service port" listed (p.35) and "Unused ports left open" as a misconfiguration example (p.39); no definition or explanation | p.35, p.39 |
| Default credentials | Covered | p.39 |
| Supply chain: MSPs, vendors, suppliers | Covered (also business partner) | p.40 |
| Human vectors: phishing | Covered | p.43 |
| Human vectors: vishing | Covered | p.43 |
| Human vectors: smishing | Covered | p.42 |
| Human vectors: misinformation/disinformation | Covered | p.47 |
| Human vectors: impersonation | Covered | p.44 (also p.41) |
| Human vectors: business email compromise | Covered | p.48 |
| Human vectors: pretexting | Covered | p.44 |
| Human vectors: watering hole | Covered | p.49 |
| Human vectors: brand impersonation | Covered | p.50 |
| Human vectors: typosquatting | Covered, with caveat — slide pairs it with "Bit Flipping" and gives typo-domain examples only | p.46 |
| "Attack surface" (in the objective title) | **Not in slides** — the term is never defined or discussed on Pt2 p.33-50 | — |

**Gaps against the official objective:** the non-human vectors are mostly list-only (image-based, file-based, removable device, client-based vs. agentless, unsupported systems, wired network, open service ports), and the "attack surface" concept is not in the slides. The human-vector/social-engineering bullets and the wireless, Bluetooth, default-credential and supply-chain bullets are well supported. Under the strict status rule this objective is **Weakly Covered**; gaps are to be closed only with clearly labeled [OUTSIDE-SLIDES] material, none of which has been added here.

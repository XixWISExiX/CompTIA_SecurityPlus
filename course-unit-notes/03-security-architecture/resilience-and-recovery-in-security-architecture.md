---
Unit: Resilience and Recovery in Security Architecture
Domain: 3.0 Security Architecture (sub-objective 3.4 — Explain the importance of resilience and recovery in security architecture)
Source: Pt4 p.50-82 (global 350-382; course slides 3-102 to 3-134). Boundaries: Pt4 p.50 = 3.4 roadmap (3-102, "Resilience and recovery in security architecture" highlighted); Pt4 p.82 = last content slide (Power Redundancy, 3-134); Pt4 p.83 = Domain 3 recap (3-135), Pt4 p.84-85 = logo slides, Pt4 p.86 = Module 4 title (4-1), not part of this unit
Extraction_Status: Fully Extracted (all 33 pages Pt4 p.50-82 read via vision at 80 dpi)
Pages_Done: Pt4 p.50-82
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — same-session re-check of the note against the renders (see Validation record at the end); not an independent second reader
---

## Roadmap and Section Topics (Source: Pt4 p.50-51)

- Pt4 p.50 is the section roadmap: the four Domain 3 sections are listed with "Resilience and recovery in security architecture" highlighted (Source: Pt4 p.50).
- Section Topics slide, "3.4 Explain the importance of resilience and recovery in security architecture" (Source: Pt4 p.51):
  - **High availability**: Load balancing vs. clustering
  - **Site considerations**: Hot; Cold; Warm; Geographic dispersion
  - **Platform diversity**
  - **Multi-cloud systems**
  - **Continuity of operations**
  - **Capacity planning**: People; Technology; Infrastructure
  - **Testing**: Tabletop exercises; Fail over; Simulation; Parallel processing
  - **Backups**: Onsite/offsite; Frequency; Encryption; Snapshots; Recovery; Replication; Journaling
  - **Power**: Generators; Uninterruptible power supply (UPS)

## High Availability: Server Clusters (Source: Pt4 p.52)

| Cluster type | Definition as printed | Example as printed |
|---|---|---|
| Failover Clusters (High Availability Clusters) | Designed so that a secondary server can take over in the case that the primary one fails, with limited or no downtime (Source: Pt4 p.52) | DNS servers or Microsoft domain controllers (Source: Pt4 p.52) |
| Load Balancing Clusters | Multiple servers connected together to share resources (CPU, RAM, storage, etc.) to help balance the load between all of the servers and keep resource usage at a manageable level; data is often replicated between these servers so that each server contains the exact same information as the others (Source: Pt4 p.52) | Web servers, FTP servers, IRC servers, DNS servers, Netflix, Amazon video servers (Source: Pt4 p.52) |

## Redundant Networks and Servers (Source: Pt4 p.53)

- **Redundant Networks** — devices and access to the Internet should be considered in order to ensure the organization is able to continue operating should an issue arise (Source: Pt4 p.53).
- **Redundant Servers** — cluster servers act as a single entity in order to provide the necessary level of service/security should the primary server fail or become overwhelmed with traffic (Source: Pt4 p.53).
- **Network Interface Card (NIC) Teaming / Adapter Teaming** — the server is installed with multiple NICs or NICs with multiple ports, which provides load balancing at the adapter level, whereas clustering can be provisioned at a service level (Source: Pt4 p.53).

## Site Considerations: Sites Resiliency (Source: Pt4 p.54)

- **Continuity of Operations (CoOP) Sites** — often referred to as *recovery site, alternate site, or backup site*; used to provide the restoration of business functions should there be a large-scale loss of service at the primary location (Source: Pt4 p.54).
  - A surviving site includes two geographically dispersed buildings that are fully equipped and staffed (Source: Pt4 p.54).

| Site type | Definition as printed | Readiness as printed |
|---|---|---|
| Geographic Dispersion | A resiliency mechanism where processing and data storage resources are replicated between physically distant sites (Source: Pt4 p.54) | — |
| Cold Site ($) | Basic environmental controls in place, but very few, if any, computing or networking resources are available and takes longer to set up; may be an empty building with a lease agreement in place to install whatever equipment is required when necessary (Source: Pt4 p.54) | Up in Days to a week; computers often not present (Source: Pt4 p.54) |
| Warm Site ($$) | Partially configured with peripherals and software but not the main processing systems; stores backups that are days or weeks old (Source: Pt4 p.54) | Up in Hours to 3 days; computers are there but are off (Source: Pt4 p.54) |
| Hot Site ($$$) | A fully configured environment that can be fully operational very quickly; stores duplicate data or near-ready backups (Source: Pt4 p.54) | Up in Minutes to Hour; computers on (Source: Pt4 p.54) |
| Mobile Site | A portable site that can be driven and used anywhere (Source: Pt4 p.54) | — |

## Diversity (Source: Pt4 p.55-56)

| Term | Definition as printed |
|---|---|
| Platform Diversity | Using multiple technologies, operating systems, and hardware or software components within an organization's infrastructure (Source: Pt4 p.55) |
| Technology Diversity | Environments that are a mix of operating systems, applications, coding languages, virtualization solutions, and so on (Source: Pt4 p.55) |
| Control Diversity | The layers of controls should combine different classes of technical and administrative controls with the range of control functions: prevent, detect, correct and deter (Source: Pt4 p.55) |
| Vendor Diversity | Security controls are sourced from multiple suppliers (Source: Pt4 p.55) |
| Crypto Diversity | Concept that can be extended to the selection of algorithms and implementations of cryptography (Source: Pt4 p.55) |

- **Software Diversity** — Windows environment presents predictable attack surface with plenty of commodity malware tools available to exploit misconfigurations (Source: Pt4 p.56).
  - Also refers to the obfuscation technique to make code difficult for unauthorized access (Source: Pt4 p.56).
  - Alternative compiler paths would result in a different binary each time; each compiled application would result in a different build; overall functionality remains the same (Source: Pt4 p.56).
  - An attack against different binaries would only be successful on a fraction of the users; an attacker wouldn't know what exploit to use; essentially creating an environment that makes attacks against an application more difficult; attacks are harder to develop against non-standard environments (Source: Pt4 p.56).

## Multi-Cloud Systems (Source: Pt4 p.57)

- A multi-cloud strategy offers several benefits for both cybersecurity operations and business needs by leveraging the strengths of multiple cloud service providers (Source: Pt4 p.57).
  - Enhances cybersecurity by diversifying the risk associated with a single point of failure, as vulnerabilities or breaches in one cloud provider's environment are less likely to compromise the entire infrastructure (Source: Pt4 p.57).
  - Can distribute workloads across multiple cloud providers to address high availability, data security, performance optimization, and cost efficiency (Source: Pt4 p.57).
  - Can provide continuous operation even during outages: host the primary application infrastructure on one cloud provider; use another for backup and disaster recovery (Source: Pt4 p.57).

## Continuity of Operations Plan (COOP) (Source: Pt4 p.58)

- **COOP** — identifies how business processes should deal with both minor and disaster-level disruption by ensuring that there is processing redundancy supporting the workflow (Source: Pt4 p.58).
  - Refers to the process of ensuring that an organization can maintain or quickly resume its critical functions in the event of a disruption, disaster, or crisis (Source: Pt4 p.58).
  - Terminology is used for government facilities, but is functionally similar to business continuity planning (Source: Pt4 p.58).
  - Refers specifically to backup methods of performing mission functions without IT support (Source: Pt4 p.58).
  - Relocation to an alternate site to resume operations after a disaster for up to 30 days (underlined on the slide) (Source: Pt4 p.58).

## Capacity Planning (Source: Pt4 p.59)

- **Capacity Planning** — a critical process in which organizations assess their current and future resource requirements to ensure they can efficiently meet their business objectives (Source: Pt4 p.59).
- Evaluating and forecasting the necessary resources in terms of people, technology, and infrastructure to support anticipated growth, changes in demand, or other factors that may impact operations (Source: Pt4 p.59).

| Factor | Definition as printed |
|---|---|
| People | Considers the number of employees, their skill sets, and the potential need for additional training or hiring to meet future demands (Source: Pt4 p.59) |
| Technology | Encompasses the assessment of hardware, software, and network resources required to support business operations, taking into account factors such as performance, scalability, and reliability (Source: Pt4 p.59) |
| Infrastructure | Involves evaluating physical facilities, such as datacenters and office spaces, to determine whether they can accommodate projected growth and maintain business continuity (Source: Pt4 p.59) |

## Testing (Source: Pt4 p.60-63)

| Test | Definition as printed | Example as printed | Callout boxes on the slide |
|---|---|---|---|
| Tabletop Exercises (Source: Pt4 p.60) | Teams discussing and working through hypothetical scenarios to assess their response plans and decision-making processes; help identify knowledge, communication, and coordination gaps, ultimately strengthening the organization's incident response capabilities | Simulate a ransomware attack to test how well the organization's IT and management teams collaborate to mitigate the threat and restore operations | "Let's get in a room and talk about this"; "Walkthrough / Tabletop — Talk through steps" |
| Failover Tests (Source: Pt4 p.61) | Intentionally causing the failure of a primary system or component to evaluate the automatic transfer of operations to a secondary, redundant system; ensure backup systems can seamlessly take over during an actual incident, minimizing downtime and data loss | Simulate the failure of a primary database server to verify that a standby server can successfully assume its role and maintain service continuity | "Shut down and move out!"; "Full-interruption testing / Live testing — Partial and Full Business Interruption — Stop normal systems — Can cause a disaster" |
| Simulation (Source: Pt4 p.62) | Controlled experiments replicating real-world scenarios, allowing organizations to assess their incident response processes and system resilience under realistic conditions; can reveal potential bottlenecks, inefficiencies, or vulnerabilities that might not be apparent in less complex tests | A cyberattack targeting the organization's network infrastructure to evaluate the effectiveness of security measures and the ability to detect, contain, and remediate the threat | "Simulation Test/Walkthrough Drill — Teams actually carry out the recovery process"; "Everyone take your places…Okay, action!" |
| Parallel Processing Tests (Source: Pt4 p.63) | Running primary and backup systems simultaneously to validate the functionality and performance of backup systems without disrupting normal operations; ensure their backup systems can handle the same workload as primary systems during an incident | To verify that a backup datacenter can manage the same traffic and processing demand as the primary datacenter in an outage | "Parallel Processing — Duplicate real business transactions on backup systems"; "Let's do a little processing here and a little processing there" |

## Backups (Source: Pt4 p.64-71)

### Data Backup and Retention; Three Factors of Risk (Source: Pt4 p.64)

- **Short-term** — files that change frequently might need retaining for version control; also important in recovering from malware infection (Source: Pt4 p.64).
- **Long-term** — data may need to be stored to meet legal requirements or to comply with company policies or industry standards; version past the oldest sets must be moved to archive storage (Source: Pt4 p.64).
- **Three Factors of Risk (Data)** (Source: Pt4 p.64):
  - **Time** — the longer data is kept in storage the more likely it is to be attacked and the greater the risk
  - **Quantity** — data in storage is at a much greater risk of breach or compromise than data in transit or data being processed
  - **Access** — various authentication/authorization mechanisms in place directly affect the risks associated with a breach or compromise

### Onsite vs. Offsite (On-Premises vs Cloud) (Source: Pt4 p.65)

- **Onsite Storage** — storing of information (tapes, cartridges, or other backup media) in a protected storage container/environment at the local site; high cost to maintain storage devices and high-bandwidth, low-latency WAN links between two geographically dispersed hot sites (Source: Pt4 p.65).
- **Cloud/Offsite Storage** — cost is one of the big drivers of cloud services, where local and geographic redundancy are built into the system, if you trust the Cloud Service Provider (CSP) to operate the cloud effectively (Source: Pt4 p.65).
  - Geo-redundancy replicates data or services between data centers physically located in two different regions (Source: Pt4 p.65).
  - Disasters that occur at the regional level, like earthquakes, hurricanes, or floods, should not impact availability across multiple zones (Source: Pt4 p.65).

### Frequency (Source: Pt4 p.66)

- Organizations with highly dynamic data or stringent regulatory mandates may opt for more frequent backups: minimize the risk of data loss; ensure compliance (Source: Pt4 p.66).
- Businesses with relatively stable data or less stringent regulatory oversight might choose less frequent backups: data protection; data backup costs; maintenance overhead (Source: Pt4 p.66).
- The optimal data backup frequency is determined by: regulatory requirements; unique needs; risk tolerance; system performance; operational needs; resources (Source: Pt4 p.66).

### Encryption (Source: Pt4 p.67)

- Encryption of backups is essential for various reasons, primarily data security, privacy, and compliance (Source: Pt4 p.67).
  - Adds an extra layer of protection against unauthorized access or theft; ensuring sensitive data remains unreadable without the appropriate decryption key (Source: Pt4 p.67).
  - Crucial for businesses dealing with sensitive customer data, intellectual property, or trade secrets; unauthorized access could lead to severe reputational damage, financial loss, or legal consequences (Source: Pt4 p.67).
  - Copies of sensitive data stored in backup sets are often overlooked; many industries and jurisdictions have regulations that mandate the protection of sensitive data stored in backups (Source: Pt4 p.67).
  - Helps organizations meet regulatory requirements and avoid fines, penalties, or legal actions resulting from noncompliance (Source: Pt4 p.67).

### Backup Media Type (Source: Pt4 p.68)

| Media | Definition as printed |
|---|---|
| Disk | Hard drives (internal/external) are an excellent low-cost option for backups (Source: Pt4 p.68) |
| Tape | A popular choice for organizations with multi-terabyte storage requirements; tape are cost effective and portable (Source: Pt4 p.68) |
| Network Attached Storage (NAS) | Appliance that is specially configured type of server that makes RAID storage available over common network protocols (SMB or FTP) that is also accessible via an IP address; backup takes place at file-level (Source: Pt4 p.68) |
| Storage Area Network (SAN) | A high-speed fiber optic network of storage devices built from technologies such as Fibre Channel, Small Computer System Interface (SCSI), Serial Attached SCSI (SAS), or InfiniBand; backup takes place at block-level (Source: Pt4 p.68) |
| InfiniBand (IB) | A computer networking communications standard used in high-performance computing that features very high throughput and very low latency (Source: Pt4 p.68) |
| Cloud Backup | A service in which data and applications on a business servers are backed up and stored on a remote server (Source: Pt4 p.68) |

### Non-persistence and Mastering Instructions (Source: Pt4 p.69)

- **Non-persistence** — any given instance is completely static in terms of processing function; data is separated from the instance so that it can be swapped out "as a new" copy without suffering any configuration problems (Source: Pt4 p.69).
  - **Snapshot/Revert to Known State** — a saved system state that can be reapplied to the instance (Source: Pt4 p.69).
  - **Rollback to Known Configuration** — a physical instance might not support snapshots but has an "internal" mechanism for restoring the baseline system configuration, such as Windows System Restore (Source: Pt4 p.69).
  - **Live Boot Media** — an instance that boots from read-only storage to memory rather than being installed on a local read/write hard disk (Source: Pt4 p.69).
- When provisioning a new or replacing an instance automatically, the automation system may use one of the following mastering instructions (Source: Pt4 p.69):
  - **Master Image** — the "gold disk" copy of a server instance, with the OS, applications, and patches all installed and configured
  - **Automated Build From a Template** — similar to a master image, this is the build instructions for an instance; rather than storing a master image, the software may build and provision an instance according to the template instructions

### Tape Rotation Schemes (Source: Pt4 p.70)

- **Tape Rotation Scheme** — a system of backing up data to computer media that minimizes the number of media used (Source: Pt4 p.70).
  - **Grandfather-Father-Son (GFS)** — a common rotation scheme for backup media in which there are three or more backup cycles, such as daily, weekly, and monthly (Source: Pt4 p.70).
  - **Tower of Hanoi** — based on the mathematics of the Tower of Hanoi puzzle, using a recursive method to optimize the back up cycle ensuring even wear and tear across different disks (Source: Pt4 p.70).
  - **First In, First Out (FIFO)** — saves new or modified files onto the oldest media in the set (14 media per set); idea that it retains the longest possible tail of daily backups (Source: Pt4 p.70).

### Database Replication and Shadowing (Source: Pt4 p.71)

- **Database Replication** — mirrors a live database allowing simultaneous reads and writes to multiple replicated databases by clients; a two-phase commit can be used to assure integrity before committing (vote); original and copy are in use, serving clients (Source: Pt4 p.71).
- **Working Copies** — also referred to as *shadow copies*; generally the most recent partial or full backups of a system that are stored locally for immediate recovery should a failure occur (Source: Pt4 p.71).
  - *Journaled File System (JFS)* — a file system that includes a log of all changes/transactions that have occurred within a set period of time (Source: Pt4 p.71).
- **Shadow Database** — mirrors all changes made to a primary database, but clients do not access the shadow; one-way (data flows from primary to shadow) (Source: Pt4 p.71).
- **Remote Journaling (log shipping)** — a technique of backing up transactions (changes) to another site allowing rollback or restore (Source: Pt4 p.71).
  - Contains a log of all database transactions; journals may be used to recover from a database failure (Source: Pt4 p.71).
  - A database may be recovered by reverting to the checkpoint, and then applying all subsequent transactions described by the database journal (Source: Pt4 p.71).
  - Saves database checkpoints periodically to a remote site (Source: Pt4 p.71).

### Backup Types (Source: Pt4 p.72-73)

| Type | Data selection | Backup/Restore time | Archive attribute |
|---|---|---|---|
| Full | All selected data regardless of when it was previously backed up | High/Low (one tape set) | Cleared |
| Incremental | New files, as well as files modified since the last backup | Low/High (multiple tape sets) | Cleared |
| Differential | All new and modified files since the last full backup | Moderate/Moderate (no more than two sets) | Not Cleared |

(Source: Pt4 p.72 for the table.)

- Slide note: the difference between an incremental backup and a differential backup is that the Archive file attribute is not reset after the differential backup is completed, therefore the changed file is backed up every time the differential backup is run (Source: Pt4 p.72).
- **Restoration diagram** (Source: Pt4 p.73): a Sunday full backup followed by daily backups Monday-Thursday (changed files A, B, C, D on the labels).
  - Incremental: "Full backup + all subsequent incremental" — Monday-Thursday each hold only that day's change (Changed File A, B, C, D); Recovery stacks the Full plus all four incrementals (Source: Pt4 p.73).
  - Differential: "Full backup + most recent differential" — Monday = file A, Tuesday = A & B, Wednesday = A, B & C, Thursday = A, B, C & D; Recovery stacks the Full plus Thursday's differential only (Source: Pt4 p.73).
  - Graphic credit as printed: "Graphics created by an Education Ecosystem Instructor" (Source: Pt4 p.73).

## RAID and Multipath (Source: Pt4 p.74-81)

- **RAID (Redundant Array of Inexpensive/Independent Disks)** — spreads the data normally stored on a single disk across a series of disks to prevent a single point of failure should a disk fail; provides redundancy for the storage devices (Source: Pt4 p.74).
- **Multipath** — overprovisioning controllers and cabling so that a host has failover connections to storage media; focused on the bus between the server and the storage devices or RAID array (Source: Pt4 p.74).

| RAID level | Description as printed | Fault tolerant | Min. drives |
|---|---|---|---|
| RAID 0 (Striped Disks) | Spreads data across several disks to improve performance but does not provide redundancy; reduced data retrieval time; loss of a single disk will result in the loss of all data. Callout: Striping — focused on increasing the read and write performance by spreading data across multiple hard disks (Source: Pt4 p.75) | No | Two |
| RAID 1 (Mirrored Disks) | Data is copied to two identical disks; if one disk fails, the other continues to operate. Callout: Mirroring — used to achieve full data redundancy by writing the same data to multiple hard disks (Source: Pt4 p.76) | Yes | Two |
| RAID 3 (Byte-striped with Dedicated Parity) | Spreads data across the drives at byte level with one drive for parity bits; should one drive fail, it can be replaced, and the new drive will be regenerated using the parity information. Callout: Parity — achieves data redundancy without incurring the same degree of cost as that of mirroring in terms of disk usage and write performance (Source: Pt4 p.77) | Yes | 3 |
| RAID 5 (Block-striped with Distributed Parity) | Most common RAID type; stripes data at block level and spreads parity across all drives; improved reliability and performance (Source: Pt4 p.78) | Yes | 3 |
| RAID 6 (Block-striped with Double Distributed Parity) | Data is striped across multiple drives but there are two stripes of parity information; can operate with 2 failed drives (Source: Pt4 p.79) | Yes | 4 |
| RAID 10 (Raid 1+0) | Combines advantages of RAID 1 and RAID 0; contains two RAID 1 mirrors which are then striped. Callout: Nested (0+1, 1+0, or 5+0) (Source: Pt4 p.80) | Yes | 4 |

- **RAID 10 diagram** (Source: Pt4 p.80): RAID 1+0 shows a RAID 0 stripe over two RAID 1 mirrors (Disks 0-1 and Disks 2-3); RAID 0+1 shows a RAID 1 mirror over two RAID 0 stripes.
- **RAID summary slide** (Source: Pt4 p.81):

| Level | Description | Notes | Min. drives |
|---|---|---|---|
| 0 | Block striping or spanning | Speed — no redundancy (marked "Ø") | 2 |
| 1 | Mirroring | Redundancy (marked "1 = 1") | 2 |
| 3 | Byte level striping with dedicated parity | — | 3 |
| 4 | Block level striping with dedicated parity | — | 3 |
| 5 | Block level striping with distributed parity | One disk can fail | 3 |
| 6 | Block level striping with double distributed parity | Two disks can fail | 4 |
| 0+1 | Stripe then mirror; mirror of stripes | Mirrored array with segments that are RAID 0 arrays (marked "0 + 1") | 4 |
| 10 | Mirror then stripe; stripe of mirrors; "Oracle — (SAME) Stripe and Mirror Everything" | Mirroring of RAID 1 with the striping of RAID 0; 2 drive redundancy (marked "1 + 0") | 4 |

  - Footer row: "Nested (0+1, 1+0, or 5+0)" (Source: Pt4 p.81). Orange boxes on the slide group the min-drive column as 2 / 3 / 4 (Source: Pt4 p.81).

## Power Redundancy (Source: Pt4 p.82)

- **Dual Power supplies** — a server or appliance enclosure is likely to feature two or more power supply units (PSUs) for redundancy in a way that a hot plug PSU can be replaced in the event of failure without powering down the system (Source: Pt4 p.82).
  - **Managed Power Distribution Units (PDUs)** — an advanced strip socket that provides filtered output voltage; a managed unit supports remote administration for PDUs (Source: Pt4 p.82).
  - **Uninterruptible Power Supplies (UPSs)** — combines a surge suppressor with a battery back-up providing protection against surges, spikes, sags, brownouts and blackouts (Source: Pt4 p.82).
  - **Backup Generators** — part of the emergency power system that takes over when power from the electric power grid fails and are typically designed to start automatically once a loss of power is detected (Source: Pt4 p.82).
    - **Portable gas engine generator** — least expensive; runs on regular gasoline but must be started by hand and only generate enough power for small or mobile operations; requires fuel storage/gas on hand (Source: Pt4 p.82)
    - **Permanently installed generator** — more expensive; run on either natural gas or propane, connected directly to the organization's electrical panel/service and designed to start automatically (Source: Pt4 p.82)
    - **Battery-inverter generator** — rely on lead-acid batteries similar to UPSs and can supply low watt power to systems for a short period of time (Source: Pt4 p.82)

## Source quirks (kept as printed)

- Section Topics lists "Fail over" under Testing; the testing slide is titled "Failover Tests" and its callout equates it with full-interruption / live testing that "can cause a disaster" (Source: Pt4 p.51, p.61).
- The Simulation callout reads "Simulation Test/Walkthrough Drill — Teams actually carry out the recovery process", while the Tabletop callout is labelled "Walkthrough / Tabletop" (Source: Pt4 p.60, p.62).
- COOP is described three ways: processing redundancy, a government-facilities term similar to business continuity planning, and relocation to an alternate site for up to 30 days (Source: Pt4 p.58).
- The slide heading "Sites Resiliency" calls Geographic Dispersion, Cold, Warm, Hot, and Mobile sites all items under CoOP sites; the Mobile Site is not a Section Topics bullet (Source: Pt4 p.51, p.54).
- RAID 4 and RAID 0+1 appear only on the summary slide, not on individual RAID slides; the summary labels RAID 1 as "1 = 1" and nested levels "0 + 1" and "1 + 0" (Source: Pt4 p.81).
- RAID 5 diagram labels parity as "Parity C / Parity A / Parity B" under drives A / B / C (Source: Pt4 p.78).
- "Data Backup and Retention" slide lists "Three Factors of Risk (Data)" which is not a Section Topics bullet (Source: Pt4 p.64).
- Backup Types table header is "Backup/Restore Time" with values written as "High/Low", "Low/High", "Moderate/Moderate"; the slide does not say which half is backup and which is restore (Source: Pt4 p.72).
- The Non-persistence, tape rotation, RAID, multipath, and diversity slides are not Section Topics bullets (Source: Pt4 p.51, p.55-56, p.69-70, p.74-81).

## Official-objective gap check (3.4)

Official sub-bullets as listed on Pt4 p.51 and in `source_coverage/objective_mapping.md`:

| Official bullet | Result | Support / gap |
|---|---|---|
| High availability: load balancing vs. clustering | Covered | Failover (HA) clusters vs. load balancing clusters with examples (Pt4 p.52); NIC teaming contrast (Pt4 p.53). No direct side-by-side "vs." slide |
| Site considerations: hot | Covered | Pt4 p.54 |
| Site considerations: cold | Covered | Pt4 p.54 |
| Site considerations: warm | Covered | Pt4 p.54 |
| Site considerations: geographic dispersion | Covered | Pt4 p.54 (one definition) |
| Platform diversity | Covered | Pt4 p.55 (one definition; software diversity on p.56) |
| Multi-cloud systems | Covered | Pt4 p.57 |
| Continuity of operations | Covered | Pt4 p.58; also CoOP sites (Pt4 p.54). Three overlapping descriptions |
| Capacity planning: people, technology, infrastructure | Covered | Pt4 p.59 |
| Testing: tabletop exercises | Covered | Pt4 p.60 |
| Testing: fail over | Covered | Pt4 p.61 |
| Testing: simulation | Covered | Pt4 p.62 |
| Testing: parallel processing | Covered | Pt4 p.63 |
| Backups: onsite/offsite | Covered | Pt4 p.65 |
| Backups: frequency | Covered | Pt4 p.66 (factors listed, no schedules or RPO link) |
| Backups: encryption | Covered | Pt4 p.67 |
| Backups: snapshots | Weak | Only "Snapshot/Revert to Known State" under non-persistence, one line (Pt4 p.69); no backup-snapshot discussion |
| Backups: recovery | Weak | No dedicated recovery slide; recovery appears only in backup-type restoration diagram (Pt4 p.73) and remote journaling (Pt4 p.71). RTO/RPO not mentioned in this range |
| Backups: replication | Covered | Database replication (Pt4 p.71); geo-redundancy (Pt4 p.65) |
| Backups: journaling | Covered | JFS and remote journaling (Pt4 p.71) |
| Power: generators | Covered | Three generator types (Pt4 p.82) |
| Power: UPS | Covered | Pt4 p.82 (one definition) |

Overall under the strict rule: **Weakly Covered** (two bullets, snapshots and recovery, are thin; all other bullets are covered). The slides also include RAID, multipath, tape rotation, non-persistence, backup types, and the diversity variants, which are not official 3.4 bullets.

## Validation record

- Date: 2026-10-16. Scope: all 33 pages Pt4 p.50-82 re-compared against the note after writing (see corrections below).
- Same-session re-check against the renders; not an independent second reader.
- Dense pages (Pt4 p.71, p.73, p.81) re-rendered at 110 dpi and compared line by line; all other pages compared against the 80 dpi renders (text legible; no table-cell ambiguity).
- Corrections: one. The RAID summary row for level 0 was missing the right-hand "Ø" marker (Pt4 p.81); added. Re-check of p.71 and p.73 found no errors. The orange-box grouping on p.81 (2 / 3 / 4 drives) was re-verified.

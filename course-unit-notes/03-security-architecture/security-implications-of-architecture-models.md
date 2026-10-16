---
Unit: Security Implications of Different Architecture Models
Domain: 3.0 Security Architecture (sub-objective 3.1 — Compare and contrast security implications of different architecture models)
Source: Pt3 p.51-100 (global 251-300; course slides 3-3 to 3-52). Boundaries: Pt3 p.50 = Domain 3 "Domain Topics" recap (3-2, titles only, no unit content); Pt3 p.51 = 3.1 roadmap (3-3, "Security implications of different architecture models" highlighted); Pt4 p.1 = 3.2 roadmap (3-53, next section, not part of this unit)
Extraction_Status: Fully Extracted (all 50 pages Pt3 p.51-100 read via vision at 80 dpi)
Pages_Done: Pt3 p.51-100
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — same-session re-check of the note against the 80 dpi renders (dense pages p.76, p.79, p.97, p.99 re-opened); not an independent second reader
---

> Structure note: the slides never start a new roadmap inside this range, so the networking primer (OSI, cabling, switches, IP, TCP/UDP; Pt3 p.64-86) sits inside 3.1 by slide order. It supports "network infrastructure" but most of it is not named in the official 3.1 bullets.

## Section Topics (Source: Pt3 p.52)

Official-style list shown on the slide:

- **Architecture and infrastructure concepts**: Cloud (responsibility matrix; hybrid considerations; third-party vendors); Infrastructure as code (IaC); Serverless; Microservices; Network infrastructure (physical isolation — air-gapped; logical segmentation; software-defined networking (SDN)); On-premises; Centralized vs. decentralized; Containerization; Virtualization; IoT; Industrial control systems (ICS)/supervisory control and data acquisition (SCADA); Real-time operating system (RTOS); Embedded systems; High availability
- **Considerations**: Availability; Resilience; Cost; Responsiveness; Scalability; Ease of deployment; Risk transference; Ease of recovery; Patch availability; Inability to patch; Power; Compute

(Source: Pt3 p.52)

## Cloud Computing (Source: Pt3 p.53)

- **Cloud Computing** — computing, storage, application and other services provided over a network via the Internet Protocol (Source: Pt3 p.53)
  - Scalable, flexible and reliable; transparent to the end user; encryption is critical to maintain security (Source: Pt3 p.53)
- **Frameworks and Templates** — used to summarize and document the results of threat source identification, characterization, vulnerabilities and impacts; a template ensures all documentation and assessment uses the same guidelines (Source: Pt3 p.53)
- **Elasticity** — the system's ability to handle changes on demand in real time; a system with high elasticity will not lose service or performance if demand suddenly increases rapidly (Source: Pt3 p.53)
- **Scalability** — the capacity to increase system resources to meet demand within similar cost ratios (Source: Pt3 p.53)
  - **Scale out** — add more resources in parallel with existing resources (Source: Pt3 p.53)
  - **Scale up** — increase the power of existing resources (Source: Pt3 p.53)

## Responsibility Matrix and Cloud Service Models (Source: Pt3 p.54-55)

- **Responsibility Matrix (Shared Responsibility)** — responsibility for implementing security is shared between the customer and the Cloud Service Provider (CSP) as applications, data, and workloads move into a cloud platform (Source: Pt3 p.54)
- **SaaS** (Software as a Service) — offloads application management to a third party while still leveraging the features (Source: Pt3 p.54)
- **PaaS** (Platform as a Service) — targeted mostly at developers; the provider manages OS's, servers, storage, networking, deployment, virtualization while developers manage the application (Source: Pt3 p.54)
- **IaaS** (Infrastructure as a Service) — self-service models for accessing, monitoring, and managing remote datacenter infrastructure such as computing, storage, networking, and networking services (Source: Pt3 p.54)

Layer stack diagram ("You manage" vs. "Managed by vendor"); layers listed top to bottom: Applications, Data, Runtime, Middleware, O/S, Virtualization, Servers, Storage, Networking (Source: Pt3 p.55):

| Model | You manage | Managed by vendor |
|---|---|---|
| On-Premises | all nine layers | none |
| IaaS | Applications, Data, Runtime, Middleware, O/S | Virtualization, Servers, Storage, Networking |
| PaaS | Applications, Data | Runtime, Middleware, O/S, Virtualization, Servers, Storage, Networking |
| SaaS | none | all nine layers |

(Source: Pt3 p.55)

## Cloud Deployment Models (Source: Pt3 p.56)

- **Public (or Multi-Tenant) Providers** — businesses can offer subscriptions or pay-as-you-go financing (Source: Pt3 p.56)
  - **Multi-Cloud** — an organization uses services from multiple CSPs (Source: Pt3 p.56)
- **Private Cloud** — completely hosted, owned and operated by the organization (Source: Pt3 p.56)
  - **Hosted Private** — hosted by a third party for the organization's exclusive use (Source: Pt3 p.56)
- **Community Cloud** — several organizations share the costs of either a hosted private or fully private cloud, usually to pool resources for a common concern like standardization and security policies (Source: Pt3 p.56)
- **Hybrid Cloud** — combines public and private clouds (sensitive data on the private cloud, while scaling up space and services on the public cloud) (Source: Pt3 p.56)

## Other Cloud Service Models / Third-Party Vendors (Source: Pt3 p.57)

- **Anything as a Service (XaaS)** — most types of IT requirements can be deployed as a cloud service model (Source: Pt3 p.57)
  - **Consultants** — could be used for "big picture" framework analysis and alignment or for specific, product-focused projects (pen testing, SIEM rollout, etc.) (Source: Pt3 p.57)
  - **Managed Security Services Provider (MSSP)** — fully outsources responsibility for information assurance to a third party; expensive, but can be a good fit for an SME that has experienced rapid growth and has no in-house security capability (Source: Pt3 p.57)
  - **Security as a Service (SECaaS)** — can mean many things, but is typically distinguished from an MSSP as implementing a particular security control, such as virus scanning or SIEM-like functionality, in the cloud (Source: Pt3 p.57)

## Cloud Security Alliance (CSA) (Source: Pt3 p.58)

- **CSA** — dedicated to defining and raising awareness of best practices for a secure cloud computing environment; produces resources to assist CSPs in setting up and delivering secure cloud platforms and for evaluating and selecting cloud services (Source: Pt3 p.58)
  - **Security Guidance** — best-practice summary analyzing the unique challenges of cloud environments and how on-premises controls can be adapted to them (Source: Pt3 p.58)
  - **Enterprise Reference Architecture** — best-practice methodology and tools for CSPs to use in architecting cloud solutions (Source: Pt3 p.58)
  - **Cloud Controls Matrix** — lists specific controls and assessment guidelines CSPs should implement; a starting point for cloud contracts and agreements because it provides a baseline level of security competency the CSP should meet (Source: Pt3 p.58)

## Cloud Access Security Broker (CASB) (Source: Pt3 p.59)

- **CASB** — enterprise management software designed to mediate access to cloud services by users across all types of devices; provides security, manageability, and visibility into how clients and other network nodes use cloud services (Source: Pt3 p.59)
- Functions (Source: Pt3 p.59):
  - Enable single sign-on authentication and enforce access controls and authorizations from the enterprise network to the cloud provider
  - Scan for malware and rogue or non-compliant device access
  - Monitor and audit user and resource activity
  - Mitigate data exfiltration by preventing access to unauthorized cloud services from managed devices
- Implementations: forward proxy; reverse proxy; Application Programming Interface (API) (Source: Pt3 p.59)
- Diagram: IaaS / PaaS / SaaS clouds above the CASB layer (Control and Monitoring, Compliance Management, Data Security, Threat Protection), reached through "Reverse Proxy • Forward Proxy • API Mode", from Off-Premises (mobile, regional offices, home offices) and On-Premises (corporate office) clients (Source: Pt3 p.59)

## Other Architecture and Infrastructure Concepts (Source: Pt3 p.60)

- **Infrastructure as Code (IaC)** — a provisioning architecture where deployment of resources is performed by scripted automation and orchestration, fully replacing manual configuration (Source: Pt3 p.60)
  - One goal is to eliminate snowflake systems; **snowflake** — a configuration or build that is different from any other system (Source: Pt3 p.60)
- **Serverless** — a software architecture that runs functions within virtualized runtime containers in a cloud rather than on dedicated server instances (Source: Pt3 p.60)
  - **Serverless Computing or Function as a Service (FaaS)** (Source: Pt3 p.60)
  - Applications are hosted by a third-party service, eliminating the need to manage physical or virtual server instances (Source: Pt3 p.60)
  - Applications are broken into individual functions and microservices that can be invoked and scaled individually (AWS Lambda and Microsoft Azure Functions) (Source: Pt3 p.60)
- **Service-Oriented Architecture (SOA)** — components conceived as loosely coupled services not dependent on a single platform type or technology (Source: Pt3 p.60)
- **Microservices** — components conceived as highly decoupled services not dependent on a single platform type or technology; should be capable of being developed, tested, and deployed independently (Source: Pt3 p.60)

## Network Infrastructure Segmentation (Source: Pt3 p.61)

- **Physical Isolation** — segregating individual devices within a network to limit their interaction with other devices and systems; removing or severely restricting communication paths to a device or system (Source: Pt3 p.61)
  - Improves security but incurs significant management challenges: device administration has to be performed at a local terminal; any updates or installs have to be performed using USB or optical media (Source: Pt3 p.61)
- **Air-gapped** — a type of network isolation that physically separates a host from other hosts, or a network from all other networks; slide marks it "Most secure" (underlined) (Source: Pt3 p.61)
  - Extreme form of segmentation where one segment is completely isolated from all others physically and logically; no network interfaces, wired or wireless, connected to outside networks (Source: Pt3 p.61)
- **Logical Segmentation** — network topology enforced by switch, router, and firewall configuration, where hosts on one segment are prevented from or restricted in communicating with hosts on other segments (Source: Pt3 p.61)
- **Software-Defined Networking (SDN)** — APIs and compatible hardware/virtual appliances allowing programmable network appliances and systems (Source: Pt3 p.61)

## Software-Defined Concepts (Source: Pt3 p.62)

- **SDN** — separates the control plane management of network devices from the underlying data plane that forwards network traffic; separates a router's control plane from the data (forwarding) plane (Source: Pt3 p.62)
  - **Control plane** — makes decisions about how traffic should be prioritized and secured, and where it should be switched (Source: Pt3 p.62)
  - **Data plane** — handles the actual switching and routing of traffic and imposition of security access controls (Source: Pt3 p.62)
  - **Management plane** — monitors traffic conditions and network status (Source: Pt3 p.62)
- **Software-Defined Visibility (SDV)** — supports assessment and incident response functions in near-real-time collection, aggregation, and reporting of network traffic (Source: Pt3 p.62)

## Fog and Edge Computing (Source: Pt3 p.63)

- **Fog Computing** — provisioning processing resource between the network edge of IoT devices and the data center to reduce latency (Source: Pt3 p.63)
  - Prioritize data for analysis and alert conditions; analyze data before committing it to the cloud (Source: Pt3 p.63)
- **Edge Computing** — offloads computing by placing edge servers and devices close to the user and origin of data, or as the last mile, to provide location-aware, bandwidth-sufficient, real-time, and low-cost services (Source: Pt3 p.63)
  - Components listed: edge device zone; edge gateways; "fog notes" (slide wording as shown); data center (Source: Pt3 p.63)
- Diagram: IoT device → edge servers → fog → cloud (Source: Pt3 p.63)

## Networking Primer — OSI and TCP/IP (Source: Pt3 p.64-67)

**OSI Reference Model** (Source: Pt3 p.64):

| Layer | Name | Function | PDU |
|---|---|---|---|
| 7 | Application | Network process to application (FTP, HTTP, SMTP) | Data |
| 6 | Presentation | Translates data format sender to receiver; encryption/decryption, compression, code conversion | Data |
| 5 | Session | Manages sessions within the OS over the network and between hosts | Data |
| 4 | Transport | End-to-end communications and reliability flow control | Segments |
| 3 | Network | Routing and switching information between hosts, networks and internetworks | Packet/Datagram |
| 2 | Data Link | Establishes, maintains, and decides how data transfer is accomplished over the physical layer | Frame |
| 1 | Physical | Physical and electrical medium for data transfer | Bit |

- The slide table groups layers 4-7 as "Host Layer" and layers 1-3 as "Media Layer" (Source: Pt3 p.64)
- PDU mnemonic "SPF10": Segment, Packet, Frame, One and Zero (Bits) (Source: Pt3 p.65)
- Layer mnemonic: "Please Do Not Tell Secret Passwords Anytime" (layers 1-7 in order); alternates shown include "Please Do Not Throw Sausage Pizza Away" and "Please Do Not Throw Sun Protection Away" (Source: Pt3 p.65)

**OSI relevance to protocols** (Source: Pt3 p.66):

| Layer | Protocols |
|---|---|
| 7 Application | DHCP, DNS, FTP, TFTP, SSH, LDAP, IMAP, POP3, HTTP, NTP, SMTP, SNMP, Telnet… |
| 6 Presentation | MIME, Encoding, SSL, TLS |
| 5 Session | Named Pipes, NetBIOS, SIP, RTP |
| 4 Transport | TCP, UDP, SSL, TLS |
| 3 Network | IP (v4, v6), ICMP, IPsec |
| 2 Data Link | ARP, L2TP, PPP, PPTP |
| 1 Physical | IEEE 802.15 (Bluetooth), IEEE 802.3 (Ethernet), IEEE 802.11 (Wireless), USB |

- **TCP/IP** — communication protocol for LANs and the Internet (Source: Pt3 p.67)
  - **TCP** — Transport Layer (Layer 4) protocol responsible for establishing the connection and ensuring reliable data transport between devices (Source: Pt3 p.67)
  - **IP** — Network Layer (Layer 3) protocol enabling internetworking and used to relay datagrams between networks (Source: Pt3 p.67)
  - 4 layers: Application, Transport, Internet, Network Access. Diagram maps OSI 5-7 → Application; Transport → Transport; Network → Internet; Data Link + Physical → Network Access ("Link Layer") (Source: Pt3 p.67)

## Cabling, Cable Vulnerabilities, Physical Controls (Source: Pt3 p.68-71)

- **Twisted-Pair** — most common type; copper-based cable with four pairs of wires (eight total), each pair twisted together (UTP = Unshielded Twisted Pair pictured) (Source: Pt3 p.68)
- **Fiber-optic** — glass/plastic cable with thin strands carrying light pulses (photons) instead of electricity (Source: Pt3 p.68)
  - Single-mode — long distances; Multi-mode — short distances that are longer than twisted-pair (Source: Pt3 p.68)
- **Coaxial** — copper-based cable with a single copper core (Source: Pt3 p.68)
- **SONET** (Synchronous Optical Networking) — contains multiple T-carrier circuits via fiber optic cabling; still the primary standard transmission method for high-speed, long-distance fiber; ring topology for redundancy (Source: Pt3 p.69)
  - **SONET ring** — optical-fiber backbone connecting nodes in a ring or point-to-point configuration; "self-healing rings" because they keep transmitting if part of the network fails (cut cable) (Source: Pt3 p.69)
- Cable media vulnerabilities (Source: Pt3 p.70):
  - **EMI** — interference on network cables from motors, lights, other electromechanical objects (TVs, microwaves, air-conditioning units, unshielded electrical lines)
  - **RFI** — interference on cables (and wireless systems) from radio frequency projected across the spectrum by electrical processes (AM/FM stations, cell towers)
  - **Crosstalk** — a signal on one copper wire creates an undesired effect on another wire
  - **Data Emanation (signal emanation)** — electromagnetic field from a cable or device can be manipulated to listen to or capture data
  - **Faraday Cage** — shielding a room/container to prevent the electromagnetic field from escaping and being detected
- Media and cable physical security controls (Source: Pt3 p.71):
  - **Safe or Locking Cabinet** — secure location for hard copies, data, backup media; can protect against fire, burglary, robbery, internal theft
  - **Cable Locks** — sturdy cable with built-in lock or eyelet to attach laptop/computer/monitor to a desk or fixture to prevent carry-away
  - **Protected Distribution System (PDS)** — allows transmission of classified information in unencrypted format
  - **Protected Cable Distribution** — protecting cabling from physical tapping with locking wiring closets, locked spare jacks, conduit and cable trays; a hardened PDS routes all cabling through sealed metal conduit with periodic visual inspection

## Network Devices and Switch Security (Source: Pt3 p.72-78)

- **Device definitions** (Source: Pt3 p.72):
  - **Hub** — connects multiple systems; repeats inbound traffic over all outbound ports; Layer 1
  - **Switch** — "intelligent hub"; knows the system addresses on each outbound port; repeats traffic only out of the port where the destination is known; can be programmed to examine/manage traffic; resolves MAC addresses to ports (CAM table); Layer 2
  - **Router** — controls traffic flow between networks; often connects similar networks; connects two networks and routes data between them; static routing tables or dynamic routing; Access Control Lists (ACLs); Layer 3 ("Layer 3 switches")
- **Switch** — typical layer 2 device forwarding frames based on hardware/MAC address between nodes in a cabled network (Source: Pt3 p.73)
  - Layer 2 type uses only the MAC address; Layer 3 type uses MAC plus IP address (Source: Pt3 p.73)
- **MAC addressing** — every NIC has a 6-byte (48-bit) Ethernet/MAC address burned in at the factory (wired, wireless, Bluetooth); typically assigned by the manufacturer; example `ipconfig /all` shows Physical Address 00-1F-E1-CE-6D-CF (Source: Pt3 p.74)
- **Port Security** — controls which devices may connect via each switch port based on MAC address (Source: Pt3 p.75)
  - **MAC Filtering** — manually defining which MAC addresses may connect to a port; guard against MAC flooding attacks
  - **Static Learning** — MAC assigned to a specific port; must be known and defined in advance; not good for visiting connections
  - **Dynamic Learning** — switch learns MACs when they connect; good for a small, limited number of connections
  - **Sticky Learning** — stores MACs in persistent memory; multiple devices allowed per port; persists through reboots
- **Switch security configuration** (Source: Pt3 p.76):
  - **Flood Guards** — manage traffic by monitoring rate and percentage of bandwidth used by broadcast, multicast, and unicast traffic; firewalls can act as flood guards in DoS/DDoS; effective against port floods, SYN floods, ping floods
  - **Spanning Tree Protocol (STP)** — data link layer mechanism in switches that builds a logical loop-free topology and can recognize and bypass improper connections
    - **Network Loops** — switches connected to each other multiple times, traffic circles and overwhelms them
    - **Broadcast Storm** — switches forward broadcast, multicast, and unknown unicast traffic out of all ports
    - **Bridge Protocol Data Unit (BPDU)** — slide: "occurs when an attacker uses rogue switch to imitate a switch (switch evil twin)"
    - **DHCP Snooping** — inspects traffic on access ports to ensure a host is not spoofing its MAC address; Cisco: `ip dhcp snooping binding`
- **Router** — connects two or more networks into an internetwork and routes data using IP addresses; Layer 3; static or dynamic routing; ACLs decide whether a packet may enter a network; remote management via Telnet, SNMP, TFTP, SSH (Source: Pt3 p.77)
- **Collision domains** — Hub: its own collision domain; Switches break up collision domains; Routers break up broadcast domains. Diagram: Layer 1 hub = 1 collision domain; Layer 2 switch = 3 collision domains; Layer 3 router = 2 broadcast domains (Source: Pt3 p.78)

## IPv4, NAT, IPv6 (Source: Pt3 p.79-83)

- **IPv4** — 32-bit dotted-quad notation; format X.X.X.X, X from 0 to 255; slide lists 127.0.0.0 – 127.255.255.255; first octet = class; max octet 255; subnet mask divides an IP address into network and host (Source: Pt3 p.79)

| Class | Range | Network/Host split | Hosts | CIDR |
|---|---|---|---|---|
| A | 1-127 | Net 255.x.x.x | 16,777,216 | /8 |
| B | 128-191 | Net 255.255.x.x | 65,536 | /16 |
| C | 192-223 | Net 255.255.255.x | 256 | /24 |
| D | 224-239 | Multicast | | |
| E | 240-255 | Reserved / Invalid Experimental | | |

(Source: Pt3 p.79) Also shown: subnet-mask bit values 128, 64, 32, 16, 8, 4, 2, 1 with cumulative 128, 192, 224, 240, 248, 252, 254, 255 (Source: Pt3 p.79)

- **Non-routable (private) addresses** — reserved for internal networks, not routed by Internet routers but routable by internal routers; usually translated with NAT (Source: Pt3 p.80). RFC 1918:
  - Class A: 10.0.0.0 – 10.255.255.255
  - Class B: 172.16.0.0 – 172.31.255.255
  - Class C: 192.168.0.0 – 192.168.255.255
  - Example: 192.168.1.0 whole subnet; 192.168.1.1 router/gateway (usually first IP); .2-.254 valid hosts; .255 broadcast (Source: Pt3 p.80)
- **NAT** — uses two sets of IP addresses (internal & external) for mapping of resources; done at firewall or router (Source: Pt3 p.81)
  - Translates between routable and non-routable schemes; one-to-many or one-to-one mapping; reduces the number of public IPs needed; forces users through defined pathways through firewall and routers (Source: Pt3 p.81)
- **PAT** (Port Address Translation) — TCP/UDP ports as well as IPs mapped so a single IP can serve several services (ports); used because NAT one-to-one mapping has high overhead ("NAT Overload"); unique port numbers per conversation let many internal addresses share one external IP (Source: Pt3 p.81)
- **IPv6** — replacement for IPv4; 128-bit address as eight groups of four hex digits separated by colons; 3.4 x 10^38 addresses (Source: Pt3 p.82)
  - Adjacent 0's can be replaced with `::` but only once (Source: Pt3 p.82)
  - Benefits: increased address space; auto-configuration; enhance security; IPsec support; enhanced multicast support (Source: Pt3 p.82)
  - Challenges: not interoperable with IPv4; designed for host-to-host communications making NAT obsolete; IPv4 security tools/techniques do not function properly; requires certain ICMP messages to get through; "IPv6 over IPv4 Tunneling" (Source: Pt3 p.82)
- **RFC 5952** — recommendation for IPv6 text representation; hex digits 0-9, a-f; `::` only used once; example 2001:0db8:0000:0000:0001:0000:0000:0001 shown in several shortened forms (Source: Pt3 p.83)

## TCP and UDP (Source: Pt3 p.84-86)

- **TCP** — guarantees reliable, in-order delivery; sequence numbers detect loss and order data; three-way handshake: client SYN → server SYN-ACK → client ACK establishes the connection (Source: Pt3 p.84)
- **TCP flags** (Source: Pt3 p.85):
  - **ACK** — acknowledgement number field valid; contains next sequence number expected
  - **FIN** — no more data, close the connection
  - **PSH** — push data to the Application Layer immediately; do not wait for buffer to fill
  - **RST** — a problem; sender wants to abort the connection
  - **SYN** — request to synchronize sequence numbers and establish a connection; carries sender's initial sequence number
  - **URG** — urgent; prioritized, will not wait for the whole byte stream
- **UDP** — faster and more efficient for lightweight or time-sensitive uses; depends on the application for reliability; common uses DNS, TFTP, VoIP, streaming audio/video; best effort, unreliable, "fire and forget", "send and pray" (Source: Pt3 p.86)

## Centralized vs. Decentralized Computing (Source: Pt3 p.87-88)

- **Centralized Computing Architecture** — all data processing and storage in a single location, typically a central server (Source: Pt3 p.87)
  - All users and devices rely on the central server; security and privacy depend on the server administrator's and controlling organization's trustworthiness; often large organizations needing strict control and management; examples mainframes and client-server architectures (Source: Pt3 p.87)
- **Decentralized Computing Architecture** — processing and storage distributed across multiple locations or devices; no single device or location responsible for all of it (Source: Pt3 p.88)
  - Used where resilience and flexibility matter more than central control; growing popularity for improved fault tolerance, scalability, unique security features (Source: Pt3 p.88)
  - Examples (Source: Pt3 p.88): Blockchain (distributed ledger for secure, transparent, decentralized transactions); Peer-to-peer (P2P) networks; Content Delivery Networks (CDNs); Internet of Things (decentralized networks sharing data and processing power); Distributed databases (data available even if one server goes down); TOR (The Onion Router) — anonymous communication/browsing by routing through volunteer-operated nodes to hide location and activity

## Virtualization and Containerization (Source: Pt3 p.89-91)

- **Virtualization** — creation of virtual machines (VMs) running within the real OS and operating as if physical; virtual OS often called a virtual desktop environment (VDE) (Source: Pt3 p.89)
  - **Snapshot** — point-in-time image allowing return to a previous point; move images between hardware platforms; faster backups/recoveries; copy entire systems (Source: Pt3 p.89)
  - **Clone** — a copy or replication of a VM (Source: Pt3 p.89)
- **Virtual Desktop Infrastructure (VDI)** — using a VM to provision corporate desktops as thin clients (Source: Pt3 p.90)
  - **Thin client** — only powerful enough to display screen image, play audio, and transfer mouse/key/video/audio over the network to access the OS and applications stored on a central server instead of a local hard drive (Source: Pt3 p.90)
  - **VDE** — desktop and applications provisioned as an instance under VDI; all processing and storage performed by the server; examples Horizon, Citrix, Workspace, VMware ESXi (Source: Pt3 p.90)
- **Hypervisor (Virtual Machine Manager)** — core of most virtualization; manages VMs on a system (Source: Pt3 p.90)
  - **Type I Native (bare metal)** — runs directly on host hardware; ESXi, VMware vCenter and vSphere, Citrix XenServer, MS Hyper-V
  - **Type II Hosted (application)** — runs on top of the host's operating system with VMs inside it; VirtualBox, Windows Virtual PC (Windows 7), MS Hyper-V (Windows 8+), VMware Workstation Pro, VMware Workstation Player
- **Containers/Containerization** — standard unit of software packaging code and all dependencies so the application runs quickly and reliably across computing environments (Source: Pt3 p.91)
  - **Docker** — container image is a lightweight, standalone, executable package with code, runtime, system tools, system libraries, settings (Source: Pt3 p.91)
  - Diagram: containers share a Docker Engine on a Host OS on a Server; VMs each carry a Guest OS (with Bins/Libs) on a Type 2 hypervisor on a Host OS (Source: Pt3 p.91)

## Internet of Things (Source: Pt3 p.92-93)

- **IoT** — global network of appliances and personal devices equipped with sensors, software, and network connectivity (Source: Pt3 p.92)
  - **Hub/control system** — devices usually need a communications hub for Z-Wave or Zigbee networking
  - **Smart devices** — endpoints implement the function (smart lightbulb)
  - **Wearables** — personal accessories (smart watches, fitness monitors)
  - **Sensors** — temperature, light levels, humidity, pressure, proximity, motion
  - **Facility Automation** — specialized system of embedded systems and/or IoT devices; Building Automation System (BAS), smart meters, surveillance systems, specialized systems for vehicles, drones, medical devices, IT
- **IoT issues** (Source: Pt3 p.93): credit card companies partnering with IoT developers to add payment capability; default credentials are common; enterprise management tools usually lacking; patching can be difficult if not impossible; vendors often release base OS patches slowly; end of support for devices still in widespread use

## OT, ICS, SCADA (Source: Pt3 p.94)

- **Operational Technology (OT)** — communications network designed to implement an ICS, embedded systems, devices and their controllers rather than data networking (Source: Pt3 p.94)
  - **ICS** — a network managing embedded devices (systems designed to perform a specific, dedicated function)
  - **SCADA** — a type of ICS that manages large-scale, multiple-site devices and equipment spread over geographically large areas
- ICS/SCADA sectors (Source: Pt3 p.94): Energy (power generation/distribution, utilities incl. water/sewage and transportation networks); Industrial (mining and refining raw materials; hazardous high heat and pressure furnaces, presses, centrifuges, pumps); Fabrication and manufacturing (forges, mills, assembly lines); Logistics; Facilities (building management: HVAC, lighting, security systems)

## Embedded Systems, PLC, SoC, FPGA, RTOS (Source: Pt3 p.95-96)

- **Embedded System** — a complete computer system designed to perform a specific, dedicated function (Source: Pt3 p.95). Constraints listed (Source: Pt3 p.95):
  - **Cost** — large numbers and predictable workloads, so cost per unit driven low
  - **Power** — many battery-powered, may need to run for years
  - **Compute Constraints** — result of battery power; processing kept minimal
  - **Crypto and Authentication** — lacks the cryptographic identification and authentication widely used on computers
  - **Implied Trust Constraints** — every device added to the network is trusted, assuming it was added and continues to be operated by a legitimate administrator
  - **Network and Range Constraints** — minimized compute affects choices for network connectivity over longer distance
- **PLC** (Programmable Logic Controller) — readymade embedded system deployable with little engineering overhead; all PLCs are embedded systems, but not all embedded systems are PLCs (Source: Pt3 p.96)
- **SoC** (System on Chip) — all processors, controllers, and devices on a single die; saves space, power efficient, common with embedded systems (Source: Pt3 p.96)
  - **Raspberry Pi and Arduino** — initially educational tools, now widely used for industrial applications and hacking (Source: Pt3 p.96)
- **FPGA** (Field Programmable Gate Array) — processor programmed by the customer to perform a specific function rather than at manufacture (Source: Pt3 p.96)
- **RTOS** (Real-Time Operating System) — prioritizes deterministic execution of operations to ensure consistent response for time-critical tasks since embedded systems cannot tolerate reboots or crashes (Source: Pt3 p.96)

## High Availability (Source: Pt3 p.97-98)

- **High Availability (HA)** — decrease recovery time of a system or network device; effectively zero downtime (MTD of zero); goal is key services available 99.999% (five nines) of the time (Source: Pt3 p.97)
  - **Active-Active Cluster** — multiple systems all online and actively processing; also called load balancing
  - **Active-Passive Cluster** — devices already in place, configured, and powered on; ready to process if the primary fails; backups come up when main device goes down; also called hot spare, standby, or failover cluster configuration
  - **Fault Tolerance** — ability to sustain operations during a component failure; higher availability need means higher fault tolerance; a device may fail, that is a fault; ensure a fault does not lead to a failure
- Availability table (Source: Pt3 p.97):

| Availability | Annual downtime (hh:mm:ss) |
|---|---|
| 99.9999% | 00:00:32 |
| 99.999% | 00:05:15 |
| 99.99% | 00:52:34 |
| 99.9% | 08:45:36 |
| 99% | 87:36:00 |

  - Slide footnote: "99% availability means that for every hour there is one minute of downtime" (Source: Pt3 p.97) — [CONFLICT] 87:36:00 per year is about 1% of a year, which is about 36 seconds per hour, not one minute; recorded as shown
- **HA service levels** (Source: Pt3 p.98):
  - **Local Replication** — within a single data center in the region of the storage account; replicas often in separate fault domains and upgrade domains
  - **Regional Replication** — across multiple datacenters within one or two regions; safeguards data/access if a single datacenter is destroyed or offline; also called zone-redundant storage
  - **Geo-Redundant Storage (GRS)** — replicates to a secondary region distant from the primary; safeguards against a regional outage or disaster

## Architecture Considerations (Source: Pt3 p.99)

- **Availability** — minimizes downtime or maximizes uptime
- **Cost** — value of the investment: architecture changes; acquisition and upgrade of appliances; software requiring up-front capital; ongoing maintenance and support liabilities
- **Compute and Responsiveness** — minimize processing time for workloads; each network device needs sufficient CPU, memory, storage, and bandwidth for acceptable response time
- **Scalability and Ease of deployment** — quickly or automatically add or remove computing resources without excessive costs
- **Resilience and Ease of recovery** — reduce the time to recover from a failure
- **Inability to patch** — unsupported legacy systems; replacement of the product; software product no longer supported by its vendor
- **Power** — ensures the facility can meet the energy demands of its devices and workloads
- **Patch Availability** — ensures firmware and software code is protected against exploits for known vulnerabilities
- **Risk Transference** — a contract that uses a third party to manage the network infrastructure

(Source: Pt3 p.99)

## Power Failures (Source: Pt3 p.100)

A primary concern during a disaster or incident is ensuring the organization can power critical systems and maintain operations (Source: Pt3 p.100).

| Term | Description |
|---|---|
| Fault | Momentary loss of power |
| Blackout | Complete loss of power |
| Sag/Dip | Momentary low voltage |
| Brownout/Burnout | Prolonged low voltage |
| Spike | Momentary high voltage |
| Surge | Prolonged high voltage |

(Source: Pt3 p.100)

## Source Issues Flagged

- Pt3 p.97: availability footnote ("99% = one minute of downtime per hour") does not match the table's 87:36:00/year [CONFLICT, recorded as shown].
- Pt3 p.79: slide lists 127.0.0.0 – 127.255.255.255 in the format bullets and Class A range as 1-127; recorded as shown (no outside correction).
- Pt3 p.63: "Fog notes" appears to be the slide's wording for fog nodes; recorded as shown.
- Pt3 p.76: BPDU bullet is worded as an attack ("rogue switch to imitate a switch / switch evil twin") rather than defining the BPDU itself; recorded as shown.

## Official-objective gap check (3.1)

| Official bullet | Result | Evidence / gap |
|---|---|---|
| Cloud — responsibility matrix | Covered | Pt3 p.54-55 (definition + IaaS/PaaS/SaaS layer diagram) |
| Cloud — hybrid considerations | Weak | Hybrid cloud defined only (Pt3 p.56); security considerations of hybrid are not itemized |
| Cloud — third-party vendors | Weak | XaaS, consultants, MSSP, SECaaS, CSA, CASB (Pt3 p.57-59); no explicit vendor-risk discussion in this section (supply chain covered in 5.3) |
| Infrastructure as code | Covered | Pt3 p.60 |
| Serverless | Covered | Pt3 p.60 |
| Microservices | Covered | Pt3 p.60 (plus SOA) |
| Network infrastructure — physical isolation / air-gapped | Covered | Pt3 p.61 |
| Network infrastructure — logical segmentation | Weak | One-sentence definition only (Pt3 p.61); VLAN/zone design not covered in this range |
| Network infrastructure — SDN | Covered | Pt3 p.61-62 |
| On-premises | Weak | Appears only as a column in the layer diagram (Pt3 p.55); never defined or discussed as an architecture model |
| Centralized vs. decentralized | Covered | Pt3 p.87-88 |
| Containerization | Covered | Pt3 p.91 |
| Virtualization | Covered | Pt3 p.89-90 |
| IoT | Covered | Pt3 p.92-93 |
| ICS/SCADA | Covered | Pt3 p.94 (definitions and sectors; security implications not discussed) |
| RTOS | Covered | Pt3 p.96 (one definition) |
| Embedded systems | Covered | Pt3 p.95-96 |
| High availability | Covered | Pt3 p.97-98 |
| Considerations — availability, cost, responsiveness (compute), scalability, ease of deployment, power | Covered | Pt3 p.99-100 |
| Considerations — resilience / ease of recovery | Weak | One-line definition only (Pt3 p.99) |
| Considerations — risk transference | Weak | One-line definition only (Pt3 p.99) |
| Considerations — patch availability / inability to patch | Weak | Short definitions only (Pt3 p.99); IoT patch issues add context (Pt3 p.93) |

Overall: all named 3.1 topics have slide support, but several bullets are one-line definitions. Proposed status: **Weakly Covered** (on-premises, hybrid considerations, third-party vendors, logical segmentation, and the "considerations" list are thin; most slide effort went to a networking primer that is not an official 3.1 bullet).

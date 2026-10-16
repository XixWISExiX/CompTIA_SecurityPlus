---
Unit: Security Principles to Secure Enterprise Infrastructure
Domain: 3.0 Security Architecture (sub-objective 3.2 — Given a scenario, apply security principles to secure enterprise infrastructure)
Source: Pt4 p.1-39 (global 301-339; course slides 3-53 to 3-91). Boundaries: Pt4 p.1 = 3.2 roadmap (3-53, "Security principles to secure enterprise infrastructure" highlighted); Pt4 p.40 = 3.3 roadmap (3-92, next section, not part of this unit); Pt3 p.100 = last 3.1 page
Extraction_Status: Fully Extracted (all 39 pages Pt4 p.1-39 read via vision at 80 dpi; the Pt4 p.39 diagram re-read at 150 dpi)
Pages_Done: Pt4 p.1-39
Pages_Remaining: none
Validation_Status: Validated 2026-10-16 — same-session re-check of the note against the renders (see Validation record at the end); not an independent second reader
---

## Section Topics (Source: Pt4 p.2)

Official-style list shown on the slide (3.2 "Given a scenario, apply security principles to secure enterprise infrastructure"):

- **Infrastructure considerations**: Device placement; Security zones; Attack surface; Connectivity; Failure modes (Fail-open, Fail-closed); Device attribute (Active vs. passive; Inline vs. tap/monitor); Network appliances (Jump server; Proxy server; Intrusion prevention system (IPS) / Intrusion detection system (IDS); Load balancer; Sensors)
- **Port security**: 802.1X; Extensible Authentication Protocol (EAP)
- **Firewall types**: Web application firewall (WAF); Unified threat management (UTM); Next-generation firewall (NGFW); Layer 4/Layer 7
- **Secure communication/access**: Virtual private network (VPN); Remote access; Tunneling (Transport Layer Security (TLS), Internet protocol security (IPSec)); Software defined wide area network (SD WAN); Secure access service edge (SASE)
- **Selection of effective controls**

(Source: Pt4 p.2)

## Infrastructure Considerations (Source: Pt4 p.3)

- **Device Placement** — considerations for positioning security controls to protect network zones and individual hosts to implement a defense in depth strategy and to meet overall security goals (Source: Pt4 p.3)
- **Security Zone** — an area of the network (or of a connected network) where the security configuration is the same for all hosts within it (Source: Pt4 p.3)
  - Physical security: an area separated by barriers that control entry and exit points (Source: Pt4 p.3)
- **Attack Surface** — the points at which a network or application receive external connections or inputs/outputs that are potential vectors to be exploited by a threat actor (Source: Pt4 p.3)
- **Attack Vector** — a specific path by which a threat actor gains unauthorized access to a system (Source: Pt4 p.3)

## Failure Modes (Source: Pt4 p.4)

- **Fail Securely** — a component, application, or device is configured to fail in a controlled manner that prevents exploitation while the component, application, or device is in an inconsistent state (Source: Pt4 p.4)

| Category | Mode | Meaning as printed |
|---|---|---|
| Technical (Logical) | Fail Safe / Open / Soft | Availability is preserved, but data may not be secure (Source: Pt4 p.4) |
| Technical (Logical) | Fail Secure / Closed | Data is secure, but availability is not preserved (Source: Pt4 p.4) |
| Physical (Operational) | Fail Safe / Open | System will continue functioning even if one or more parts of the system fail; entrances unlocked — humans are safe; ensures continued access to the resource in the event of failure (Source: Pt4 p.4) |
| Physical (Operational) | Fail Secure / Closed | Systems are shut down; entrances are locked; blocks access to a resource in the event of failure (Source: Pt4 p.4) |

## TAPs and Mirror Ports — Device Attribute (Source: Pt4 p.5)

- **Switched Port Analyzer (SPAN) / Mirror Port** — the sensor is attached to a specially configured port on a Cisco switch that receives copies of frames addressed to nominated access ports (or all the other ports) (Source: Pt4 p.5)
- **Test Access Point (TAP)** (Source: Pt4 p.5)
  - **Passive** — a box with ports for incoming and outgoing network cabling and an inductor or optical splitter that physically copies the signal from the cabling to a monitor port (Source: Pt4 p.5)
  - **Active** — a powered device that performs signal regeneration (Source: Pt4 p.5)

## Network Appliances

### Servers (Source: Pt4 p.6)

- **Server** — a computer system that stores, transfers, archives, and allows/disallows access to the data and the services the network and its users rely on (Source: Pt4 p.6)
  - **File** — central storage and management of data files (Source: Pt4 p.6)
  - **FTP** — software on a computer that uses File Transfer Protocol to store and share files (Source: Pt4 p.6)
  - **E-mail** — an application or computer in a network whose sole purpose is to act as a virtual post office (Source: Pt4 p.6)
  - **Web** — stores and delivers website content (text, images, video, application data) to clients that request it (Source: Pt4 p.6)
  - **DNS** — host name records and name resolution so applications and users can address hosts and services by FQDNs rather than IP addresses (Source: Pt4 p.6)
  - **Domain Controller** — a directory server that responds to authentication requests and verifies users on computer networks (Source: Pt4 p.6)
  - **Jump Server** — a hardened server that provides access to other hosts, also known as jump box or temp server (Source: Pt4 p.6)
  - **Proxy Server** — a server that mediates the communications between a client and another server (Source: Pt4 p.6)

### Proxies (Source: Pt4 p.7-8)

- **IP/Anonymizing Proxy** — hides information about the requesting system and makes a user's web browsing "anonymous"; often used to protect personal information transferred across the Internet (Source: Pt4 p.7)
- **Caching Proxy** — keeps local copies of popular client requests; used in large organizations to reduce bandwidth usage and increase performance (Source: Pt4 p.7)
- **Content-Filtering Proxy** — examines each client request and compares it to an established Acceptable Use Policy (AUP); activity through the proxy can be logged and analyzed (Source: Pt4 p.7)
- **Open Proxy** — common and often has some anonymizing capabilities; often used to circumvent corporate proxies (Source: Pt4 p.7)
- Diagram: client → "Web request" → proxy (labelled "Open") → "Web request" → www.site.com, and "Data" returning the same way (Source: Pt4 p.7)
- **Application Layer Proxy (Forward)** — acts as an intermediary by preventing packets from traversing the firewall, but instead flows the data to an application that knows how to handle it (Source: Pt4 p.8)
- **Reverse Proxy** — installed on the server side of a network connection and intercepts all incoming web requests (Source: Pt4 p.8)
  - Traffic filtering; Secure Sockets Layer (SSL) decryption; static content serving (e.g., graphics); load balancing (Source: Pt4 p.8)
  - Diagram: Private Network ↔ REVERSE PROXY (inside a DMZ) ↔ Internet (Source: Pt4 p.8)

### Load Balancers (Source: Pt4 p.9)

- **Load Balancing** — a fault tolerance technique designed to distribute the processing load over two or more systems to improve resource utilization and throughput (Source: Pt4 p.9)
  - Best for stateless systems, so that any server can handle the requests (Source: Pt4 p.9)
  - Should a single system fail, other system(s) pick up the processing load; ensures the entire operation does not go down entirely (Source: Pt4 p.9)
  - Diagram: many client clouds → load balancer → server pool (Servers 1-4) (Source: Pt4 p.9)

### IDS / IPS (Source: Pt4 p.10-12)

- **Intrusion Detection Systems (IDS)** (Source: Pt4 p.10)
  - Device or software application that monitors a network for malicious activities or policy violations and produces reports to a management station (Source: Pt4 p.10)
  - Goal is to identify intrusion attempts, while minimizing false positives and false negatives (Source: Pt4 p.10)
  - Examines traffic by connecting directly to routers, switches, or hubs (Source: Pt4 p.10)
- **Intrusion Prevention Systems (IPS)** (Source: Pt4 p.10)
  - "Reactive In-line" system that responds automatically to suspicious activity by actively preventing/blocking intrusions that are detected (Source: Pt4 p.10)
  - Uses network behavior analysis to identify threats that generate unusual traffic flows (Source: Pt4 p.10)
  - Effective against distributed denial of service attacks and policy violations (Source: Pt4 p.10)
- **Host-Based (HIDS/HIPS)** — loaded onto an individual system (host / end-point device) and analyzes and monitors the activity within the system; can interpret encrypted traffic (Source: Pt4 p.11)
- **Network-Based (NIDS/NIPS)** — examines the traffic crossing the network interface it is monitoring; cannot monitor activity within an individual system; considered to be an inline device (Source: Pt4 p.11)
  - Diagram: Private Network (192.168.0.2-0.5) → router → Firewall → NIDS → Internet (Source: Pt4 p.11)
- **IDS/IPS components** (Source: Pt4 p.12)
  - **Traffic collector (or sensor)** — placed at various locations across the network to collect activity/events for the IDS to examine; HIDS/HIPS: collecting log files, audit logs, traffic to/from a system; NIDS/NIPS: function as a sniffer, copying traffic off the network (Source: Pt4 p.12)
  - **Analysis engine** — the "brain" of an IDS; examines collected traffic and compares it to known patterns of suspicious or malicious activity in the signature database (Source: Pt4 p.12)
  - **Signature database** — a collection of patterns and definitions of known suspicious or malicious activity used by the IDS/IPS to detect events (Source: Pt4 p.12)
  - **User interface and reporting** — provides alerts and gives the user a means to interact with and operate the IDS (Source: Pt4 p.12)

## Port Security (Source: Pt4 p.13-14)

- **IEEE 802.1x (Port-based)** — a data-link layer authentication technology that defines port-based network access control to secure connections between hosts and a LAN/WLAN (Source: Pt4 p.13)
  - A security control that ties physical ports to end-device (client) MAC addresses to prevent unauthorized users from accessing publicly available ports on a switch (Source: Pt4 p.13)
  - Banner: Port Based Network Access Control (PNAC) (Source: Pt4 p.13)
- **Extensible Authentication Protocol (EAP)** — a framework for negotiating authentication methods; a universal authentication protocol that supports many different types of authentication (Source: Pt4 p.14)

| EAP type | Description as printed |
|---|---|
| EAP-MD5 | Challenge-based, one-way authentication (no mutual authentication) (Source: Pt4 p.14) |
| EAP-TLS | Uses certificate-based Transport Layer Security; enables mutual authentication; not suitable for enterprises due to client and server certificate management (Source: Pt4 p.14) |
| EAP-TTLS | Tunneled TLS, similar to TLS except that it uses an encrypted channel and only requires server-side certificates (Source: Pt4 p.14) |
| EAP-FAST | Flexible Authentication via Secure Tunneling; uses protected access credentials instead of a certificate for mutual authentication (Source: Pt4 p.14) |
| PEAP | Protected EAP — standard developed by Cisco, Microsoft, and RSA to protect EAP by encapsulating it with TLS, creating a TLS tunnel; widely supported for wireless networks (Source: Pt4 p.14) |
| LEAP | Lightweight EAP — proprietary protocol designed by Cisco; now considered deprecated and replaced by PEAP and EAP-TLS (Source: Pt4 p.14) |

## Firewalls

### Firewall types (Source: Pt4 p.15-16)

- **Firewalls** — gatekeepers or sentries placed at points on the network that segregate network or network segments (Source: Pt4 p.15)
  - Operate on rules that define what traffic is allowed/denied (Source: Pt4 p.15)
  - Principle of least access/privilege — allow only the necessary access for a function (Source: Pt4 p.15)

| Firewall type | Description as printed |
|---|---|
| Packet Filtering (Stateless) | Blocks/allows traffic based on ports, protocols, and source and/or destination IP addresses (Source: Pt4 p.15) |
| Stateful Packet Inspection (SPI) | Keeps track of ongoing TCP communications in a "Dynamic State Table" and disallows packets that are not part of an ongoing TCP communication; also detects TCP flags sent out-of-sequence or unsolicited requests (Source: Pt4 p.15) |
| Network Address Translation (NAT) Filtering | Filters traffic according to port numbers (Source: Pt4 p.15) |
| Application-Level Gateway | Checks each packet and applies security mechanisms to specific applications (Source: Pt4 p.15) |
| Circuit-Level Gateway | Session layer device that applies security mechanisms to hide private network information when a connection is established, but does not filter packets (Source: Pt4 p.15) |

- **SPI operation** — stateful inspection can occur at two layers (Source: Pt4 p.16)
  - **Transport (layer 4)** — examines the TCP three-way handshake to distinguish new from established connections (Source: Pt4 p.16)
  - **Application (layer 7)** — can inspect the contents of packets at the application layer (Source: Pt4 p.16)
  - Diagram: client ↔ firewall ↔ xyz.com, with the firewall writing to a "Dynamic State Table" (Source: Pt4 p.16)

### Firewall implementation (Source: Pt4 p.17-20)

- **Appliance Firewall** — a stand-alone hardware firewall deployed to monitor traffic passing into and out of a network zone; can be deployed Routed (Layer 3) or Bridged (Layer 2) (Source: Pt4 p.17)
- **Router Firewall** — a firewall router appliance implements filtering functionality as part of the router firmware (Source: Pt4 p.17)
- **Application-Based Firewall** — firewalls running as software on any type of computing host (Source: Pt4 p.17)
  - **Host-Based (Personal) Firewall** — software application running on a single host designed to protect that host only (Source: Pt4 p.17)
  - **Application Firewall** — software designed to run on a server to protect a particular application only (a web server or a SQL Server database) (Source: Pt4 p.17)
  - **Network Operating System (NOS) Firewall** — software-based firewall running under a network server OS (Windows or Linux); the server would function as a gateway or proxy for a network segment (Source: Pt4 p.17)
- **Application Firewall (Layer 7)** — operates on the Application Layer (Layer 7) to control traffic associated with specific applications (Source: Pt4 p.18)
  - Most host-based/personal firewalls are application firewalls; some advanced network firewalls fall into this category as well (Source: Pt4 p.18)
  - Examples: Windows Firewall (built into Windows; Basic and Advanced); PF (Packet Filter) and IPFW (IP Firewall) — command-line firewalls built into OS X; IPTables — stateful firewall used in Linux 2.4 series systems; IPChains — stateless firewall used in Linux 2.2 series systems (Source: Pt4 p.18)
- **Virtual Firewall** — usually deployed within data centers and cloud services (Source: Pt4 p.19)
  - **Hypervisor-Based** — filtering built into the hypervisor or cloud provisioning tool (Source: Pt4 p.19)
  - **Virtual Appliance** — a vendor firewall appliance instance deployed using virtualization, like a Windows or Linux guest OS (Source: Pt4 p.19)
  - **Multiple Context** — multiple virtual firewall instances on a hardware firewall appliance; each context has a separate interface and can perform a distinct filtering role (Source: Pt4 p.19)
- **Open-Source vs Proprietary** — code underpinning appliance, software, and virtual firewalls can be open-source or proprietary or in between (Source: Pt4 p.20)
  - Wholly Proprietary — proprietary OS; e.g., Cisco ASA, Juniper JunOS, PaloAlto PANOS, Barracuda (Source: Pt4 p.20)
  - Mostly Proprietary — developed from a Linux kernel with proprietary features added; e.g., Check Point IPSO, FortiGate FortiOS, Sonicwall (Source: Pt4 p.20)
  - Wholly Open-Source — can be used independently of the vendor, though vendors typically have commercial appliances and support contracts; e.g., pfsense, IPFire, ClearOS, OPNsense, VyOS, Smoothwall (Source: Pt4 p.20)

### Next-generation: WAF, SWG, UTM (Source: Pt4 p.21-22)

- **Web Application Firewall (WAF)** — considered a "Next Generation Firewall"; appliance, server, plug-in, or filter that enforces policies based on rules associated with HTTP/HTTPS traffic; essentially content filters (Source: Pt4 p.21)
  - Rules can be granular: "Allow Facebook but block Facebook games" (Source: Pt4 p.21)
  - Detects and blocks disclosure of critical data (account numbers, SSN, etc.) (Source: Pt4 p.21)
  - Controls input, output, and/or access from, to, or by an application or service (Source: Pt4 p.21)
  - Protects against Cross-Site Scripting, **Fuzzing** (bold on slide), Buffer Overflow attacks (Source: Pt4 p.21)
  - Can use passed SSL credentials to enable SSL inspection (Source: Pt4 p.21)
- **Secure Web Gateway (SWG)** — an on-premises proxy-based firewall, content filter, and intrusion detection/prevention system that mediates user access to Internet sites and services (Source: Pt4 p.21)
  - A next-generation SWG, as marketed by Netskope, combines an SWG with data loss prevention (DLP) and a CASB to provide a wholly cloud-hosted platform for client access to websites and cloud apps (Source: Pt4 p.21)
- **Unified Threat Management (UTM)** — an "all-in-one" device that combines several security functions: firewalls; IDS/IPS; antivirus and anti-SPAM; VPN capabilities; malicious web traffic filtering (Source: Pt4 p.22)
  - UTM types: **URL Filter** — blocks connections to websites deemed dangerous or inappropriate; **Content Inspection** — inspects the actual content of the returned web request and filters content deemed inappropriate for the workplace; **Malware Inspection** — network-based appliance designed to detect malware during network transmission (Source: Pt4 p.22)
  - Image: a Northrop Grumman "BLUVECTOR" rack appliance (Source: Pt4 p.22)

## Secure Communication / Access

### Telephony and VoIP (Source: Pt4 p.23-25)

- **Telephony** — voice communications for users within a network; involves modems, traditional Plain Old Telephone Service (POTS), Private Branch Exchanges (PBXs) and/or Voice over IP (VoIP) systems (Source: Pt4 p.23)
- **Modem** — older technology for connecting computer systems over the public telephone network; still in use today but often overlooked (Source: Pt4 p.23)
- **Private Branch Exchange (PBX)** — computer-based (digital) switching equipment that connects an organization's telephones into the Public Switched Telephone Network (PSTN) (Source: Pt4 p.23)
  - Frequently interconnected into an organization's data systems (Source: Pt4 p.23)
  - Possible attack vector as it provides a connection between the outside world and the network (modems) (Source: Pt4 p.23)
  - Can have one external phone number with many internal extensions, plus call forwarding, hold music, etc. (Source: Pt4 p.23)
- **Voice Over IP (VoIP)** — transmission of voice data over IP networks; needs VoIP servers and VoIP telephones to convert analog voice to digital signals and back (Source: Pt4 p.24)
  - **VoIP Server (VoIP Gateway/Media Gateway)** — handles conversion of the analog voice signal to a digital signal (Source: Pt4 p.24)
  - Two diagrams: IP/PBX ↔ SIP ↔ Media Gateway ↔ PSTN / Telco Provider, with VoIP and analog phones; and Media Gateway + switch + two IP/PBX with VoIP phones (Source: Pt4 p.24)
- VoIP uses two protocols (Source: Pt4 p.25)
  - **Real-time Transport Protocol (RTP)** carries audio and video; **Secure RTP (SRTP)** uses AES for confidentiality, SHA-1 for integrity, and provides secure authentication (Source: Pt4 p.25)
  - **Session Initiation Protocol (SIP)** — signals such as phone ringing; used to set up and tear down the session (Source: Pt4 p.25)
- **Packet jitter or lag** — not enough buffer; sounds "choppy" (slide appends "(encryption)") (Source: Pt4 p.25)
- **Quality of Service (QoS)** — can give specific traffic precedence over other traffic, on a packet-switched network; VoIP packets get precedence over email packets (Source: Pt4 p.25)

### VPN and remote access (Source: Pt4 p.26-29)

- **Virtual Private Network (VPN)** — a secure tunnel created between two endpoints connected via an unsecure network (typically the Internet) (Source: Pt4 p.26)
  - **VPN Concentrator** — the device at which VPN connections terminate within a network (Source: Pt4 p.26)
  - Diagram: Corporate Network ↔ VPN Concentrator ↔ Internet ↔ VPN Concentrator ↔ Remote Site (Source: Pt4 p.26)
- **Site-to-Site VPN** — connects two or more private networks; establishes a trust relationship between the gateways and sets up a secure connection through which to tunnel data; hosts at each site do not need to be configured with any information about the VPN (Source: Pt4 p.27)
  - Diagram: Branch Office (router/firewall/VPN gateway) ↔ VPN over Internet ↔ Head Office screened subnet (VPN gateway, router/firewall) ↔ Head Office local network (Source: Pt4 p.27)
- **Remote Access VPN** — the most common remote access; clients connect to a VPN gateway on the edge of the private network to establish a secure encrypted session; example: telecommuter model for home-workers and field employees (Source: Pt4 p.28)
  - Diagram: VPN client ↔ VPN over Internet ↔ remote access screened subnet (VPN gateway, router/firewall) ↔ local network LAN servers (Source: Pt4 p.28)
- **VPN client configuration** (Source: Pt4 p.29)
  - **Always-On** — the computer establishes the VPN whenever an Internet connection over a trusted network is detected, using the user's cached credentials (Source: Pt4 p.29)
  - **Split Tunnel** — the client accesses the Internet directly using its "native" IP configuration and DNS servers (Source: Pt4 p.29)
  - **Full Tunnel** — Internet access is mediated by the corporate network, which alters the client's IP address and DNS servers and may use a proxy (Source: Pt4 p.29)
  - Diagrams contrast personal browsing traffic going straight to the Internet (split) versus through the VPN, DNS server and content filter (full) (Source: Pt4 p.29)

### Tunneling protocols (Source: Pt4 p.30-35)

- **Layer 2 tunneling** (Source: Pt4 p.30)
  - **PPP** — widely used remote dial-in protocol; encapsulation for IP traffic plus IP address assignment and authentication via CHAP (Source: Pt4 p.30)
  - **PPTP** — developed by Cisco and Microsoft to support VPNs over PPP and TCP/IP; highly vulnerable to password cracking and considered obsolete; TLS and IPsec are now the preferred options for VPN access (Source: Pt4 p.30)
  - **L2F** — Cisco protocol; mutual authentication tunneling mechanism; does not offer encryption; not widely deployed, soon replaced by L2TP (Source: Pt4 p.30)
  - **L2TP** — provides authentication but not confidentiality; used with IPsec provides confidentiality and security; combination of PPTP and L2F (Source: Pt4 p.30)
- **IPsec** — a set of protocols designed to authenticate and encrypt IP packets to secure communications between network devices (Source: Pt4 p.31)
  - For bi-directional protection (two-way traffic) two Security Associations must be used (Source: Pt4 p.31)
  - Operates at the Network Layer (layer 3) of the OSI Model; can negotiate cryptographic keys and establish mutual authentication; can secure nearly all TCP/IP-related communication (Source: Pt4 p.31)
  - Operates on 3 protocols (Source: Pt4 p.31):
    - **Security Association (SA)** — establishing secure communications between systems through shared certificates or cryptographic keys, typically done through Internet Key Exchange (IKE) (Source: Pt4 p.31)
    - **Authentication Header (AH)** — integrity and authentication of the connection between systems (Source: Pt4 p.31)
    - **Encapsulating Security Payload (ESP)** — integrity, confidentiality, and authenticity of packets by encapsulating and encrypting the packets (Source: Pt4 p.31)
- **IKE** — handles authentication and key exchange, referred to as Security Associations (SA); negotiates the algorithm selection process; two sides typically negotiate the highest and fastest level of security, selecting AES over single DES for confidentiality if both support AES (Source: Pt4 p.32)
  - **Phase 1** — both parties verify identities and agree how keys will be exchanged to establish a secure, authenticated channel (digital certificates and/or pre-shared key) (Source: Pt4 p.32)
  - **Phase 2** — the Security Association gets set up and the IPsec tunnel is established (Source: Pt4 p.32)
  - Slide mnemonic box: "IKE Phase 1 – establish secure channel; IKE Phase 2 – Security Association (SA) negotiate keys" (Source: Pt4 p.32)
  - Diagram (5 steps): Host A sends interesting traffic to Host B → Routers A and B negotiate IKE phase one session (IKE SA) → negotiate IKE phase two session (IPSec SA) → information exchanged via IPsec tunnel → tunnel terminated (Source: Pt4 p.32)
- **IKE v2** — added features that made it popular as a standalone remote access VPN solution (Source: Pt4 p.33)
  - Support for EAP authentication methods (e.g., user authentication against a RADIUS server) (Source: Pt4 p.33)
  - Simplified connection setup — a single 4-message setup mode, reducing bandwidth without compromising security (Source: Pt4 p.33)
  - Reliability — allows NAT traversal and MOBIKE multihoming; a client with multiple interfaces (Wi-Fi and cellular) can keep the IPsec connection alive when switching (Source: Pt4 p.33)
- **IPsec modes** (Source: Pt4 p.34)
  - **Transport Mode** — "Content Protection": protection of the payload; encrypts only the payload (source and destination IP addresses still visible); host-to-host communication on a LAN or other private internal network; encryption/decryption at the IP source/destination; commonly used when sending and receiving systems can "speak" IPsec natively (Source: Pt4 p.34)
  - **Tunneling Mode** — "Context Protection": protection of header information and payload; encrypts both data portion and header; commonly used to secure communications between networks across the Internet; encapsulates the entire packet with new IP headers (AH) hiding the original source/destination IPs, and encrypts the contents of the new packet (ESP) (Source: Pt4 p.34)
  - Slide memory box: "Transport – (ESP) Network; Tunnel – (AH) (ESP) Internet" (Source: Pt4 p.34)
  - Figure 5.33 (source cited on slide: CISSP Study Guide, Third Edition): Original packet = IP Header + Data; Transport mode = IP Header + IPSec Header(s) + Protected Data; Tunnel mode = New IP Header + IPSec Header(s) + Protected IP Header + Protected Data (Source: Pt4 p.34)
- **IPsec architectures** (source cited on slide: CompTIA Security+ All-in-One Exam Guide, Fourth Edition) (Source: Pt4 p.35)
  - **Host-to-Host Mode** — connects two systems (such as file servers) to each other (Source: Pt4 p.35)
  - **Host-to-Gateway Mode** — connects one system running IPsec client software to an IPsec gateway; "Client Mode" (Source: Pt4 p.35)
  - **Gateway-to-Gateway Mode** — connects two IPsec gateways, which form an IPsec connection that acts as a shared routable network connection; Point-to-Point / Site-to-Site (Source: Pt4 p.35)

### SD-WAN and SASE (Source: Pt4 p.36-37)

- **Software-Defined Wide Area Network (SD-WAN)** — a virtual WAN architecture that allows enterprises to use any combination of transport services, including MPLS, LTE and broadband internet, to securely connect users to applications (Source: Pt4 p.36)
  - Simplifies management and operation of a WAN by decoupling the networking hardware from its control mechanism (Source: Pt4 p.36)
  - "SD-WAN is replacing MPLS" (underlined on slide) (Source: Pt4 p.36)
  - **Microsegmentation is an essential component of SD-WAN security** (bold on slide) (Source: Pt4 p.36)
- **Secure Access Service Edge (SASE)** — a framework for network architecture that brings cloud native security technologies (SWG, CASB, ZTNA, and FWaaS) together with WAN capabilities to securely connect users, systems, and endpoints to applications and services anywhere (Source: Pt4 p.37)
  - Combines network security and WAN capabilities into a cloud-based service; "Future of Wide Area Network (WAN)" (Source: Pt4 p.37)

## Selection of Effective Controls (Source: Pt4 p.38)

- **Selection of Effective Controls** — the process of choosing the type and placement of security controls to ensure the goals of the CIA triad and compliance with any framework requirements (Source: Pt4 p.38)
- Considerations (Source: Pt4 p.38): transparent to users but difficult to bypass; ease of use or ease of administration; cost effectiveness (cost or benefit analysis is performed); functionality or effectiveness; auditing; accountability (responsibility); testing, troubleshooting, and prevention; security and reliability; automation; sustainability

## Defense in Depth — the "FAN" (Source: Pt4 p.39)

- **Defense-In-Depth** — a security principle by which multiple, differing and overlapping security elements (layers) are employed to increase the level of security (Source: Pt4 p.39)
- Diagram "The FAN™: A Defense-in-Depth Framework" (also labelled "Layered Cybersecurity Defense Framework"), read at 150 dpi (Source: Pt4 p.39):
  - Concentric arcs, outer to inner: **Perimeter Security**, **Network Security**, **Application Security**, **Data Security**, around "Mission Critical Assets" at the center (Source: Pt4 p.39)
  - Three overlay labels: **Technology** (top, over the arcs), **Process** (left, labelled "Prevention"), **People** (right, labelled "Monitoring & Response") (Source: Pt4 p.39)
  - Example items printed in the arcs (partly obscured by the overlay labels): Perimeter — Honeypot, Malware Analysis, Message Security, IDPS, Perimeter Firewall, Application Firewall, Advanced Sensor, Physical Security, Secure DMZ, DLP, ICAM; Network — Enterprise Remote Access, Enclave Firewall, Virtual Firewall, VoIP Protection, Web Proxy Content Filtering, Endpoint Security Enforcement; Application — Content Security, Database Secure Gateway, Database Monitoring/Scanning, Dynamic App Testing, RASP, Software Assurance, Static App Testing, Personal Firewall, USGCB Compliance, Web Application Firewall; Data — DAR/DIM/DIU Protection, Data/Drive Encryption, Data Classification, Enterprise Rights Management, Data Integrity Monitoring, Sanitization, PKI; Prevention — Configuration Management, Penetration Testing, Continuous C&A, Security Architecture & Design, Threat Modeling, Vulnerability Assessment, IT Security Governance, Security Policies Compliance; Monitoring & Response — Security Management Dashboard, ISCM, Behavior Analysis, CIRT, Advanced Threat Focused Ops, Escalation Management, SIEM, Situational Awareness, SLA/SLO reporting, Cross Domain [partly obscured: several labels at the left and right edges, e.g. "Cyber Intelligence", are hidden behind the overlay boxes — ILLEGIBLE in full] (Source: Pt4 p.39)

## Flagged as printed / source observations

- Pt4 p.4: failure-mode labels combine "Fail Safe/Open/Soft" and "Fail Secure/Closed"; the logical version says availability is preserved but data may not be secure (open) vs. data is secure but availability is not preserved (closed).
- Pt4 p.5 names "a Cisco switch" for SPAN/mirror ports; no other vendor is mentioned.
- Pt4 p.11: NIDS/NIPS "considered to be an inline device", while Pt4 p.5 and p.10 describe copying/sniffing traffic via TAP/SPAN and "Reactive In-line" only for IPS. The slides do not reconcile these; IDS is never explicitly labelled "passive".
- Pt4 p.14: EAP-TLS "not suitable for enterprises due to client and server certificate management" is as printed.
- Pt4 p.18: IPTables / IPChains / PF / IPFW are listed as Application Firewall examples; IPTables is described as "stateful" and IPChains as "stateless" (as printed).
- Pt4 p.21: the WAF is called a "Next Generation Firewall"; there is no separate NGFW slide.
- Pt4 p.25: "Packet Jitter or lag — not enough buffer; sounds 'choppy' (encryption)" — the parenthetical "(encryption)" is as printed and unexplained.
- Pt4 p.30: L2TP described as the "Combination of PPTP and L2F" (as printed).
- Pt4 p.34: "Content Protection" / "Context Protection" labels for transport / tunneling mode and the memory box "(AH) (ESP)" are as printed.

## Official-objective gap check (3.2)

Against the official sub-bullets (as listed on Pt4 p.2 and in `source_coverage/objective_mapping.md`):

| Official bullet | Result | Support / gap |
|---|---|---|
| Device placement | Covered | One definition tied to defense in depth (Pt4 p.3); also FAN placement (Pt4 p.39) |
| Security zones | Weak | One definition + physical-security note; no trusted/untrusted/DMZ discussion beyond diagram labels (Pt4 p.3, p.8) |
| Attack surface | Covered | Definition and attack vector (Pt4 p.3) |
| Connectivity | Not in slides | Named in the Section Topics (Pt4 p.2) but no slide defines or discusses it |
| Failure modes: fail-open / fail-closed | Covered | Logical and physical table (Pt4 p.4) |
| Device attribute: active vs. passive | Weak | Only active vs. passive TAP is explained (Pt4 p.5); IDS vs. IPS is "detect/report" vs. "reactive in-line" (Pt4 p.10) with no passive/active label |
| Device attribute: inline vs. tap/monitor | Weak | TAP/SPAN (Pt4 p.5), IPS "in-line" (Pt4 p.10), NIDS "inline" (Pt4 p.11); no direct inline-vs-tap comparison |
| Jump server | Weak | One-line definition (Pt4 p.6) |
| Proxy server | Covered | Anonymizing, caching, content-filtering, open, application-layer (forward), reverse (Pt4 p.7-8) |
| IPS / IDS | Covered | Definitions, host vs. network, components (Pt4 p.10-12) |
| Load balancer | Covered | Pt4 p.9 |
| Sensors | Weak | Traffic collector/sensor in IDS components (Pt4 p.12) and "Advanced Sensor" in FAN (Pt4 p.39); no standalone sensor treatment |
| Port security: 802.1X | Covered | Pt4 p.13 |
| Port security: EAP | Covered | Six EAP types (Pt4 p.14) |
| Firewall types: WAF | Covered | Pt4 p.21 |
| Firewall types: UTM | Covered | Pt4 p.22 |
| Firewall types: NGFW | Weak | Only "WAF is considered a Next Generation Firewall" and "next-generation SWG" (Pt4 p.21); no NGFW definition |
| Firewall types: Layer 4 / Layer 7 | Covered | SPI at layer 4 and layer 7 (Pt4 p.16); application firewall layer 7 (Pt4 p.18) |
| VPN | Covered | Site-to-site, remote access, client configuration (Pt4 p.26-29) |
| Remote access | Covered | Remote access VPN (Pt4 p.28); no non-VPN remote access methods |
| Tunneling: TLS | Weak | TLS appears only as EAP-TLS/PEAP context and as a "preferred option" for VPN access (Pt4 p.14, p.30); no TLS tunneling slide |
| Tunneling: IPsec | Covered | AH, ESP, IKE phases, IKE v2, modes, architectures (Pt4 p.31-35) |
| SD-WAN | Covered | Pt4 p.36 |
| SASE | Weak | Definition lists SWG, CASB, ZTNA, FWaaS but ZTNA and FWaaS are not defined; CASB only mentioned (Pt4 p.21, p.37) |
| Selection of effective controls | Covered | Definition and considerations list (Pt4 p.38); list is one-liners |

Overall under the strict rule: **Weakly Covered** (Connectivity absent; several bullets thin).

## Validation record

- Date: 2026-10-16. Scope: all 39 pages Pt4 p.1-39 re-compared against the note after writing; dense pages re-checked line by line (p.14 EAP table, p.15 firewall table, p.20, p.30, p.31, p.34, p.39). Pt4 p.39 re-rendered at 150 dpi.
- Same-session re-check against the renders; not an independent second reader.
- Corrections: one — a flagged item mislabelled "[CONFLICT-style wording]" was reworded (it is a naming note, not a source conflict). No transcription errors found.

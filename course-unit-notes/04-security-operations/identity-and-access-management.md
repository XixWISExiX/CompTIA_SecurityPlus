---
Unit: Identity and Access Management
Domain: 4.0 Security Operations (sub-objective 4.6 — Given a scenario, implement and maintain identity and access management)
Source: Pt5 p.85-100 + Pt6 p.1-14 (global 485-514; course slides 4-100 to 4-129). Boundaries: Pt5 p.85 = 4.6 roadmap (4-100, confirmed in the 4.5 pass); Pt6 p.15 = 4.7 roadmap (4-130)
Extraction_Status: Fully Extracted (all 30 pages read via vision; boundary confirmed: Pt6 p.15 = 4.7 roadmap)
Pages_Done: Pt5 p.85-100; Pt6 p.1-14
Pages_Remaining: none
Next_Page: none
Validation_Status: Validated (2026-10-16) — all 30 pages re-opened at 130 dpi and compared with the note; see Validation log
---

## Roadmap and Section Topics (Source: Pt5 p.85-86)

- Pt5 p.85 (4-100) is the Domain 4 roadmap slide with "Identity and access management" highlighted. (Source: Pt5 p.85)
- Pt5 p.86 (4-101) is the 4.6 Section Topics slide (Source: Pt5 p.86):
  - Provisioning/de-provisioning user accounts; Permission assignments and implications; Identity proofing; Federation
  - Single sign-on (SSO): Lightweight Directory Access Protocol (LDAP); Open authorization (OAuth); Security Assertions Markup Language (SAML)
  - Interoperability; Attestation
  - **Access controls:** Mandatory; Discretionary; Role-based; Rule-based; Attribute-based; Time-of-day restrictions; Least privilege
  - **Multifactor authentication:** Implementations (Biometrics; Hard/soft authentication tokens; Security keys); Factors (Something you know; Something you have; Something you are; Somewhere you are)
  - **Password concepts:** Password best practices (Length; Complexity; Reuse; Expiration; Age); Password managers; Passwordless
  - **Privileged access management tools:** Just-in-time permissions; Password vaulting; Ephemeral credentials

## Provisioning user accounts (Source: Pt5 p.87)

- **Provisioning** — the process of deploying an account, host, or application to a target production environment. Involves proving the identity or integrity of the resource, and issuing it with credentials and access permissions. The process of setting up a service according to a standard procedure or best practice checklist.
- Provisioning a user account involves the following general steps:
  - **Identity proofing** — verifies that the person is who they say they are by checking official documents and records. Circumstances might also demand a background check.
  - **Issuing credentials** — allows the user to select a password known only to them and/or enroll them with biometric or token-based authenticators.
  - **Issuing hardware and software assets** — employees need sufficient resources to do their job.
  - **Teaching policy awareness** — scheduling training and providing access to learning resources so that the employee or contractor is aware of security policies and risks.
  - **Creating permissions assignment** — identifying the work roles that the account must support and configuring the appropriate rights using a role-based, mandatory, or attribute-based access control model.

(Source: Pt5 p.87)

## De-provisioning user accounts (Source: Pt5 p.88)

- **Deprovisioning** — the process of removing an account, host, or application from the production environment.
  - Requires revoking any privileged access that had been assigned to the object.
  - Removing the access rights and permissions allocated to an employee when they leave the company or from a contractor when a project finishes.
  - Removing the account from any roles or security groups.
  - The account might be disabled for a period and then deleted, or deleted immediately.

(Source: Pt5 p.88)

## Account management and permission assignments (Source: Pt5 p.89)

- **Account management (privilege management)** — controls everything a user can do to or with a computer system; restricting the user's ability to interact with computer systems. Auditing is part of the management function: use logs to compare login times for users accessing the systems and privileged accounts performing activities related to administrative functions.
- **Permission assignments and implications** — improperly configured accounts can have two different impacts:
  - Setting privileges that are too restrictive: creates a large volume of support calls; reduces productivity.
  - Granting too many privileges to users: weakens the system's security; increases the risk of malware infection; increases the risk of a data breach.

(Source: Pt5 p.89)

## Windows file system permissions (Source: Pt5 p.90)

- **Permissions** — a process of assigning individuals/groups adequate access to specific network resources (files, printers, SharePoint, etc.).
- **Permission inheritance** — sub-folders inherit the permissions of the parent folder; if permissions on the parent folder are changed it will affect the sub-folders as well.
- **Sharing permissions** — basic access (Full Control, Change, and Read).
- **Security permissions** — used to secure folders and individual files and supersedes Windows sharing permissions: Full Control; Modify; Read & Execute; List Folder Contents; Read; Write.
- Screenshot: an NTFS "Properties > Security" tab ("Figure 4.13: NTFS Permissions", source cited as CISSP Study Guide, Third Edition). Not transcribed beyond that.

(Source: Pt5 p.90)

## Linux file system permissions (Source: Pt5 p.91)

- **Linux permissions** — broken down into three types and can be assigned to three different groups.
  - **chown (change owner)** — used to change the owner of file system files, directories.
  - **chmod (change mode)** — used to change the access permissions of file system objects, sometimes known as modes.
    - User read, write, and execute permissions: 4 + 2 + 1 = 7.
    - Group read and write permissions: 4 + 2 = 6.
    - Others no permissions: 0.
    - To assign the permissions, use this command: `chmod 760 <filename>`.
  - Types: R (Read) = 4; W (Write) = 2; E (Execute) = 1 [the slide writes "E"; the usual symbol is X].
  - Groups: U (User); G (Group); A/O (All/Others).
- Screenshot (credited to an Education Ecosystem instructor): `ls -la /etc/` output on Kali with columns labelled Owner / Group / Others over the `drwxr-xr-x` style permission strings. Not transcribed line by line.

(Source: Pt5 p.91)

## Federation and single sign-on (Source: Pt5 p.92)

- **Federation** — a process that provides a shared login capability across multiple systems and enterprises. Connects the identity management services of multiple systems; the company trusts accounts created and managed by a different network.
- **Federated identity** — linking a user's identity with their privileges in a way that can be used across business systems/organizations to allow user seamless access to data or systems across domains with a single identity (example on slide: using your Facebook account to login to other websites).
- **Federated Identity Management (FIM)** — a user's identity and attributes are shared across multiple identity management systems. [Same acronym "FIM" as File Integrity Monitoring on Pt5 p.80; the context differs.]
- **Single Sign-On (SSO)** — an authentication technology that enables a user to authenticate once and receive authorizations for multiple services. Can be Kerberos based, integrated with Windows authentication, or token or smart-card based.

(Source: Pt5 p.92)

## LDAP (Source: Pt5 p.93)

- **Lightweight Directory Access Protocol (LDAP)** — a protocol used to access network directory databases, which store information about authorized users and their privileges, as well as other organizational information.
  - A plaintext application layer directory access protocol that is used to access, query, and modify directory services data.
  - Vulnerable to interception.
  - The primary protocol used for MS Active Directory.
  - A subset of the X.500 protocol.
  - **Secure LDAP (LDAPs)** — a method of implementing LDAP using SSL/TLS encryption.

(Source: Pt5 p.93. Port numbers for LDAP/LDAPS are on Pt5 p.61 and p.68, not on this slide.)

## OpenID Connect and OAuth (Source: Pt5 p.94)

- **OpenID Connect (OIDC)** — identity layer built on top of the OAuth 2.0 framework. Allows third-party applications to verify the identity of the end user and to obtain basic user profile information. OAuth is usually combined with OpenID Connect which handles the single sign on, and then OAuth determines what type of resources should a person have access to.
- **Open Standard for Authorization (OAuth)** — open standard for token-based authentication and authorization on the Internet. Often used with Twitter (X), Google, Facebook, Yahoo, REST APIs, and many other organizations. Allows organizations to authorize third parties access to their data. An access delegation standard that apps can use to provide client applications with secure delegated access over HTTPS. It authorizes devices, APIs, servers, and applications with access tokens rather than credentials.
- Terminology note: the Section Topics slide (Pt5 p.86) says "Open authorization (OAuth)"; this slide says "Open Standard for Authorization (OAuth)". Recorded as printed.

(Source: Pt5 p.94)

## APIs (Source: Pt5 p.95)

- **Application Programming Interfaces (API)** — a library of programming utilities used to enable software developers to access functions of the TCP/IP network stack under a particular operating system. Allows an application to communicate with another application, operating system, database, or network. There are two predominant styles for creating web application APIs:
  - **Simple Object Access Protocol (SOAP)** — uses XML format messaging and has a number of extensions in the form of Web Services (WS) standards that support common features, such as authentication, transport security, and asynchronous messaging; also has built-in error handling. A tightly specified protocol; request must be sent as a correctly formatted XML document.
  - **Representational State Transfer (REST)** — a software architectural style that defines a set of constraints to be used for creating Web services. A looser architectural framework, also referred to as RESTful APIs; request can be submitted as an HTTP operation/verb (GET or POST).

(Source: Pt5 p.95)

## SAML and SOAP (Source: Pt5 p.96)

- **Security Assertion Markup Language (SAML)** — defines standards for exchanging authentication and authorization between security domains. XML-based framework for exchanging security information, including authentication data; enables SSO at Internet scale; provides a single sign-on capability for web applications; used in cloud-based solutions and Software as a Service (SaaS) applications.
  - **Shibboleth** — a widely used single sign-on system on the internet that uses SAML. Security token and assertions to pass information about the **principal (user)** with SAML authority (**identity provider or idP**) and **Service Provider (SP)**:
    1. Principal requests service from SP.
    2. SP requests and receives identity assertion from idP.
    3. SP grants access or performs service request.
- **Simple Object Access Protocol (SOAP)** — unsecure specification for exchanging information associated with web services using XML. SAML uses SOAP.
- [CONFLICT/ODD] Pt5 p.95 says SOAP supports "authentication, transport security" via WS standards; this slide calls SOAP an "unsecure specification". Both recorded as printed. The Section Topics slide (Pt5 p.86) names the standard "Security Assertions Markup Language"; this slide uses "Assertion".

(Source: Pt5 p.96)

## Interoperability and attestation (Source: Pt5 p.97)

- **Interoperability** — the ability of computer systems or software to exchange and make use of information; service providers and identity providers; shared frameworks and protocols.
- **Attestation** — capability of an authenticator or other cryptographic module to prove that it is a root of trust and can provide reliable reporting to prove that a device or computer is a trustworthy platform.
  - Verifying and validating the accuracy, reliability, and effectiveness of security controls, systems, and processes implemented within an organization.
  - A formal declaration that something exists or is the case; the action of being a witness to or formally certifying something.
  - Signed using XML signature specification.

(Source: Pt5 p.97)

## Mandatory access control (MAC) (Source: Pt5 p.98)

- **Mandatory Access Control (MAC)** — restricts access based on the sensitivity (label) of the data/system, not by the user/owner.
  - Subjects are cleared and objects are labeled.
  - Subjects (users) — label/clearance determines security level and level of trust.
  - Objects (files, folders, hardware, network connections) — determines what level of clearance is needed to access.

(Source: Pt5 p.98)

## Attribute-based access control (ABAC) (Source: Pt5 p.99)

- **Attribute-Based Access Control (ABAC)** — access rights are granted to users through the use of policies which combine attributes together.
  - Also known as policy-based access control.
  - The most fine-grained type of access control model.
  - Supports Boolean logic, in which rules contain "IF, THEN" statements about who is making the request, the resource, and the action. Example: if the requestor is an admin, allow him to change (action) a user password (object).
  - Rule-based access control can be considered a special case of ABAC. The key difference with ABAC is the concept of policies that express a complex Boolean rule set that can evaluate many different attributes.

(Source: Pt5 p.99)

## Rule-based access control (RuBAC) (Source: Pt5 p.100)

- **Rule-Base Access Control (RuBAC)** [slide spelling "Rule-Base"] — uses a series of defined rules, restrictions, and filters for accessing objects within a system.
  - Users cannot make changes to rules; administrators are required for rule changes.
  - Uses a set of rules, in "if/then" format.
  - Firewall or router rules / ACL (Access Control List). Example: granting access such as day/time that files can be accessed.

(Source: Pt5 p.100)

## Role-based access control (RBAC) (Source: Pt6 p.1)

- **Role-Based Access Control (RBAC)** — a system-controlled access model that grants access based upon the "role" assigned to each employee.
  - An employee's "role" is determined by their job function or position in the company.
  - The "roles" are assigned permissions that are based upon the level of access required to perform the duties of the job function.
  - The security classification of the material does not have any effect on the access level.
- The director's-chair photo is decorative.

(Source: Pt6 p.1)

## Discretionary access control (DAC) (Source: Pt6 p.2)

- **Discretionary Access Control (DAC)** — the owner of a file specifies the levels of permissions that are granted.
  - Every object has an owner, and the owner has control over its access policy.
  - Access rights and permissions can be assigned by the owner to users to specifically control object access.
  - **User-centric**; used in Windows/Linux/Unix/Mac OSX etc.
- The nightclub-bouncer photo is decorative.

(Source: Pt6 p.2)

## Account restrictions (Source: Pt6 p.3)

- **Context-aware authentication** — authenticating users based on criteria beyond username and password.
  - **Time of day restrictions** — restricting system, network, data and/or facility access to times that personnel are required to work. Example: John only works Monday to Friday 9:00 AM to 5:00 PM, therefore allow facility access Monday through Friday 8:00 AM to 6:00 PM, and deny access any other time.
  - **Computer restrictions** — restricting access so that the account can only access the machines relevant to their job. Example: John works in the Finance Department, so he only has access to machines in that department and does not have access to machines in the Engineering Department.
  - **Location-based restrictions** — restricting access to systems located in a specific geographic location. Example: John works in the LA office but does not have access to machines in the New York office.
- **Need to know** — the user must need to know that specific piece of information before accessing it.
- **Principle of least privilege** — users are given only the minimum amount of privileges necessary to do their jobs and nothing more.
- **Privilege creep** — as employees change roles and move around the organization, they may obtain new privileges without shedding previous entitlements, resulting in users having more than required privileges.

(Source: Pt6 p.3)

## Multifactor authentication (MFA) (Source: Pt6 p.4)

- **Multifactor Authentication (MFA)** — an authentication scheme that requires the user to present at least two different factors as credentials. Specifying two factors is known as "Two Multifactor Authentication (2FA)" [slide wording; normally "two-factor authentication"].
  - **Something you know** — password / PIN / security questions.
  - **Something you have** — passport / smart card / one-time passcode / token / cookie.
  - **Something you are** — biometrics / fingerprint / iris scan / facial geometry.
  - **Somewhere you are** — GPS / IP address / MAC address / proximity / location.
  - **Something you do (exhibit)** — signature / pattern / keystroke / walking / gait.
- Three decorative photos (password key, ID badge, fingerprint).

(Source: Pt6 p.4)

## Biometrics (Source: Pt6 p.5)

- **Biometrics** — the use of measurements of biological features of the human body to identify a person: fingerprints; retina/iris scans; facial recognition; palm vein scans.
- **False Acceptance Rate (FAR)** — when a biometric system authenticates a user who should NOT be allowed access.
- **False Rejection Rate (FRR)** — when a biometric system denies a user who should be allowed access.
- **Cross-over Error Rate (CER) / Equal Error Rate (EER)** — the point at which the FAR and FRR intersect, ideally as low as possible (efficacy rates).
- Graph: Errors (y) against Sensitivity (x); the FAR curve falls and the FRR curve rises with sensitivity; they cross at the CER (source cited as CISSP Study Guide, Third Edition).

(Source: Pt6 p.5)

## Hard and soft authentication tokens (Source: Pt6 p.6)

- **Hard authentication token** — an authentication token generated by a cryptoprocessor on a dedicated hardware device. Listed: certificate-based authentication; one-time password (OTP); Fast Identity Online (FIDO) Universal 2nd Factor (U2F).
- **Soft authentication token** — an OTP sent to a registered number or email account or generated by an authenticator app as a means of two-step verification when authenticating account access.

(Source: Pt6 p.6)

## MFA implementations (Source: Pt6 p.7)

- **Smart cards** — stores the user's digital certificate, the private key associated with the certificate, and a personal identification number (PIN) used to activate the card. Certificate-based authentication.
- **One-Time Password (OTP)** — "a cryptoprocessor that can generate a token" [slide wording, spelled "crytoprocessor"]. Type of hardware token that does not need an interface to connect with a computer; the user just reads the code displayed.
- **Security key** — a portable hardware security module (HSM) with a computer interface, such as USB or Near-Field Communication (NFC) device.
  - Most closely associated with U2F. Uses a public/private key pair to register each account, avoiding the need to communicate a shared secret, which is a weakness of HOTP and TOTP.
  - Some might also support certificate-based authentication or HOTP/TOTP.
  - Must be activated to show presence. Some have an activation button, but most use a biometric fingerprint reader for better security.
  - A PIN must also be configured as a backup mechanism.

(Source: Pt6 p.7)

## One-time passwords (Source: Pt6 p.8)

- **One-Time Passwords (OTP)** — passwords that are used once and then never used again.
  - **Time-based One-Time Password (TOTP)** — a PIN is issued with a finite period of time that it is valid; sent via SMS, email, or phone call.
    - **SMS** — a code is sent as a text to the registered phone number.
    - **Phone call** — a code is delivered as an automated voice call to the registered phone number.
    - **Push notification (authentication application)** — a code is sent to a registered authenticator app on the PC or smartphone (example on slide: ID Authenticator app).
    - **Email** — a code is sent to a registered email account.
    - Example: you log into your bank, and they send a "code" to your phone that you must enter before being granted access.
  - **Token key (security token)** — a physical device (or software token) used to gain access to network/system resources. The device contains a digital certificate (or encrypted password file) that is used to authenticate the user.
    - **HMAC-based One-Time Password (HOTP)** — typically used in physical tokens and makes use of Hash-based Message Authentication Code (HMAC). HMAC uses a hashing algorithm along with a symmetric key (shared key) to authenticate users.
    - Example: you log into the Northrop Grumman network using a token (key fob).

(Source: Pt6 p.8)

## Password best practices (Source: Pt6 p.9)

- **Password best practices** — rules to govern secure selection and maintenance of knowledge factor authentication secrets, such as length, complexity, age, and reuse.
  - **Length** — enforces a minimum length for passwords; may also be a maximum length.
  - **Complexity** — enforces password complexity rules: does not contain username; does not contain dictionary words; contains uppercase letters (A-Z); lowercase letters (a-z); numbers (0-9); special characters (!@#$%^&*,.:;?).
  - **Age/expiration** — forces the user to select a new password after a set number of days.
    - Aging: the user can still log on with the old password after the defined period, but they must then immediately choose a new password.
    - Expiration: the user can no longer sign in with the outdated password, and the account is effectively disabled.
  - **Reuse** — prevents the selection of a password that has been used already.
  - **History** — sets how many previous passwords are blocked.
  - **Threshold (clipping level)** — sets the acceptable number of failed login attempts.

(Source: Pt6 p.9)

## Password manager (Source: Pt6 p.10)

- **Password manager** — software that can suggest and store site and app passwords to reduce risks from poor user choices and behavior. Most browsers have a built-in password manager.
  1. The user selects a password manager app or service (examples: Windows Credential Manager and Apple's iCloud Keychain).
  2. The user secures the password vault with a master password. Likely to be stored in the cloud so that accounts can be accessed across multiple devices; some password managers offer local storage only.
  3. When the user creates or updates an account, the password manager generates a random password; can be adjusted to meet whatever length and complexity policy is required by the site.
  4. When the user subsequently browses a site, the password manager validates the site's identity using its digital certificate and presents an option for the user to fill in the password.

(Source: Pt6 p.10)

## Passwordless SSH login (Source: Pt6 p.11)

- **Set up SSH passwordless login** — to set up a passwordless SSH login in Linux all you need to do is to generate a public authentication key and append it to the remote host's `~/.ssh/authorized_keys` file. Steps:
  1. Generate a new SSH key pair: `ssh-keygen -t rsa -f ~/.ssh/id_rsa`
  2. Copy the public key: `ssh-copy-id ~/.ssh/id_rsa.pub leia_organa@172.16.220.4`
  3. Log in to your server using SSH keys: `ssh -i ~/.ssh/id_rsa leia_organa@172.16.220.4`
- This is the slide's only "passwordless" content; the term "passwordless" is not defined more broadly (for example passkeys/FIDO are not covered on this slide; "Password keys" appear on Pt6 p.13).

(Source: Pt6 p.11)

## Just-in-time (JIT) (Source: Pt6 p.12)

- **Just In Time (JIT)** — enables organizations to grant access to applications or systems for predetermined periods of time, on an as-needed basis. (Ephemeral credentials is listed under it; see Pt6 p.14.)
- **Just-in-time (JIT) provisioning** — a method of automating user account creation for web applications. Uses the SAML protocol to pass information from the identity provider to web applications. A web site can create a new account by retrieving the customer's profile from the identity provider just in time to streamline the registration and provisioning process.
- Table on the slide (flow when signing in):

| When signing in, the user: | Flow |
|---|---|
| Exists and JIT provisioning is enabled | Normal SSO flow |
| Doesn't exist and JIT provisioning is not enabled | Normal SSO failure flow |
| Doesn't exist and JIT creation is enabled | User is created, and populated with the SAML assertion attributes, as mapped in the JIT configuration |
| Exists and JIT update is enabled | User attribute values are updated with the SAML assertion attributes, as mapped in the JIT configuration |

- Callout: "Creates the account for a user on the fly".
- [NOTE] The slide covers two senses of JIT: time-limited access (matches the official "just-in-time permissions") and JIT account provisioning via SAML. It does not walk through just-in-time permissions in detail beyond the first definition.

(Source: Pt6 p.12)

## Password vaulting (Source: Pt6 p.13)

- **Password vault** — a software-based password manager, typically using a cloud service to allow access from any device. Also known as password manager.
  - An application designed to store and manage credentials; credentials are kept in an encrypted database and protected by a master password.
  - Hardware-based: TPM/HSM/USB key.
  - Software-based password managers: OnePass, LastPass, KeyPass [as printed].
  - Most operating systems and browsers implement native password vaults; Windows Credential Manager and Apple's iCloud Keychain.
- **Password keys** — USB tokens for connecting to PCs and smartphones; may use near-field communications or Bluetooth as well as physical connectivity.

(Source: Pt6 p.13)

## Ephemeral credentials (Source: Pt6 p.14)

- **Ephemeral credentials** — dynamically generated credentials that are created at the moment they're needed, then discarded afterward.
  - The system generates or enables an account to use to perform the administrative task and then destroys or disables it once the task has been performed.
  - Short-lived credentials; temporary accounts; can be refreshed, like a cookie.

(Source: Pt6 p.14)

## Boundary (Source: Pt6 p.15)
- Pt6 p.15 (4-130) is the Domain 4 roadmap slide with "Automation and orchestration related to secure operations" highlighted, so 4.6 ends at Pt6 p.14. (Source: Pt6 p.15)

## Validation log
- Extraction: 30 pages read at 100 dpi, written in five saves (after Pt5 p.91, p.97, Pt6 p.4, p.9, p.14).
- Validation (separate pass, 2026-10-16): Pt5 p.86-100 and Pt6 p.1-14 re-opened at 130 dpi and compared item by item (definitions, lists, example commands, the JIT table, page citations); Pt5 p.85 and Pt6 p.15 are boundary slides seen at 100 dpi. No omissions, wrong values or wrong citations found; no content changes needed.
- Slide inconsistencies kept as printed: "Open authorization" (Pt5 p.86) vs "Open Standard for Authorization" (p.94); "Security Assertions" (p.86) vs "Security Assertion" (p.96) Markup Language; SOAP supports security features (p.95) vs "unsecure specification" (p.96); "Rule-Base" (p.100); "Two Multifactor Authentication (2FA)" (Pt6 p.4); "crytoprocessor" (Pt6 p.7); "E (Execute)" in the Linux types (Pt5 p.91); "OnePass, LastPass, KeyPass" (Pt6 p.13).
- Not transcribed: decorative photos (Pt6 p.1, p.2, p.4), the NTFS screenshot (Pt5 p.90) and the ls output (Pt5 p.91) beyond a description.

## Official-objective gap check (4.6 bullets as listed on the slides' Section Topics slide, Pt5 p.86)
| Official bullet | Status | Where |
|---|---|---|
| Provisioning/de-provisioning user accounts | Covered | Pt5 p.87-88 |
| Permission assignments and implications | Covered (+ Windows/Linux permissions) | Pt5 p.89-91 |
| Identity proofing | Covered (one step of provisioning) | Pt5 p.87 |
| Federation | Covered | Pt5 p.92 |
| SSO; LDAP; OAuth; SAML | Covered (also OIDC, API/SOAP/REST, Shibboleth) | Pt5 p.92-96 |
| Interoperability | Covered (brief) | Pt5 p.97 |
| Attestation | Covered | Pt5 p.97 |
| Access controls: mandatory, discretionary, role-based, rule-based, attribute-based | Covered | Pt5 p.98-100, Pt6 p.1-2 |
| Time-of-day restrictions | Covered | Pt6 p.3 |
| Least privilege | Covered (also need to know, privilege creep) | Pt6 p.3 |
| MFA: biometrics | Covered (FAR/FRR/CER) | Pt6 p.5 |
| MFA: hard/soft authentication tokens | Covered | Pt6 p.6, p.8 |
| MFA: security keys | Covered | Pt6 p.7 |
| MFA factors: know / have / are / somewhere you are | Covered (also something you do) | Pt6 p.4 |
| Password best practices: length, complexity, reuse, expiration, age | Covered | Pt6 p.9 |
| Password managers | Covered | Pt6 p.10 |
| **Passwordless** | **Weak.** The only slide is a passwordless SSH key-login procedure (Pt6 p.11); passwordless authentication in general (e.g. passkeys, FIDO2 sign-in) is not explained. "Password keys" (Pt6 p.13) are a one-line USB-token definition | Pt6 p.11, p.13 |
| PAM tools: just-in-time permissions | Covered (JIT access + JIT provisioning) | Pt6 p.12 |
| PAM tools: password vaulting | Covered | Pt6 p.13 |
| PAM tools: ephemeral credentials | Covered | Pt6 p.14 |

**Gaps against the official objective:** one weak bullet — "passwordless" authentication. Everything else is present and validated. The strict status rule keeps this objective at Weakly Covered until the gap is closed with outside material. Extra slide content (kept): Windows/Linux permission commands, OIDC, API styles, biometric error rates, OTP types, spam-adjacent items are not in this unit.

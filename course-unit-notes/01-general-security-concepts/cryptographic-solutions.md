---
Unit: Cryptographic Solutions
Domain: 1.0 General Security Concepts (sub-objective 1.4 — Explain the importance of using appropriate cryptographic solutions)
Source: Pt1 p.60-100 + Pt2 p.1-20 (global 60-120; course slides 1-46 to 1-106). Boundaries: Pt1 p.60 = 1.4 roadmap (1-46); Pt2 p.21 = Domain 1 "Domain Topics" recap (1-107), Pt2 p.22-23 = logo slides, Pt2 p.24 = Module 2 title.
Extraction_Status: Fully Extracted (all 61 pages read via vision at 80 dpi)
Pages_Done: Pt1 p.60-100, Pt2 p.1-20
Pages_Remaining: none
Next_Page: none (validation pending)
Validation_Status: Validated (2026-10-16) — all 61 pages re-opened and compared with the note (Pt1 p.62, 71, 72, 81, 87 and Pt2 p.2, 7, 17, 19 at 130 dpi; the rest at 80 dpi); no transcription corrections needed; see Validation log
---

## Roadmap and Section Topics (Source: Pt1 p.60-61)

- Pt1 p.60 (1-46) is the Domain 1 roadmap slide with "Cryptographic solutions" highlighted. (Source: Pt1 p.60)
- Pt1 p.61 (1-47) is the 1.4 Section Topics slide (Source: Pt1 p.61):
  - **Public key infrastructure (PKI):** Public key; Private key; Key escrow
  - **Encryption:** Level (Full-disk, Partition, File, Volume, Database, Record); Transport/communication; Asymmetric; Symmetric; Key exchange; Algorithms; Key length
  - **Tools:** Trusted Platform Module (TPM); Hardware security module (HSM); Key management system; Secure enclave
  - **Obfuscation:** Steganography; Tokenization; Data masking
  - **Hashing**; **Salting**; **Digital signatures**; **Key stretching**; **Blockchain**; **Open public ledger**
  - **Certificates:** Certificate authorities; Certificate revocation lists (CRLs); Online Certificate Status Protocol (OCSP); Self-signed; Third-party; Root of trust; Certificate signing request (CSR) generation; Wildcard

## Public Key Infrastructure (PKI) (Source: Pt1 p.62)

- **PKI** — a third-party within a system for creating, issuing, and managing keys (slide says "RSA 1024") for use in asymmetric encryption, and verifies the identity of all public keys within the system. **NOT an encryption algorithm.** (Source: Pt1 p.62)
- PKI provides: Confidentiality, Access control, Integrity, Authentication, Non-Repudiation. (Source: Pt1 p.62)
- Components: **Certificate Authority (CA)**, **Registration Authority (RA)**, **Validation Authority (VA)**. (Source: Pt1 p.62)
- Diagram, Bob/Alice/CA, seven numbered steps (Source: Pt1 p.62):
  1. Bob asks the CA to issue a certificate in his name.
  2. The CA validates Bob's identity and issues a certificate to Bob.
  3. Bob presents a certificate containing his identity to Alice.
  4. Alice asks the CA to verify Bob's identity.
  5. The CA confirms that Bob's certificate is valid and has not been altered or expired.
  6. The CA tells Alice that Bob's certificate is valid.
  7. Alice now trusts Bob and Bob can't deny he sent the email to Alice (non-repudiation).

## Certificate Authority (CA) (Source: Pt1 p.63)

- **CA** — a trusted third-party responsible for issuing the digital certificates. (Source: Pt1 p.63)
- The CA is at the top of the system and performs these functions (Source: Pt1 p.63):
  - Generates, issues, and distributes public key certificates
  - Distributes CA certificates
  - Generates and publishes certificate status information
  - Provides a means for subscribers to request revocation
  - Maintains a list of revoked certificates to prevent expired or compromised keys from being used (slide wording: "to prevent expire or compromised keys from being used")
  - Maintains security, availability, and continuity of certificate issuance signing functions
  - Establishes base trust, tracks certificates, maintains the CRL
- Two main types of CAs: **Private CA** — an internal (in-house) CA for use within an organization; **Commercial CA** — an external to organization. (Source: Pt1 p.63)
- Screenshots on the slide: a Windows certificate dialog (Trusted Root Certification Authorities tab) and a browser padlock icon. (Source: Pt1 p.63)

## Registration Authority (RA) (Source: Pt1 p.64)

- **RA** — a subordinate entity designed to process certificate requests, and authenticate users. Local RAs could be used by systems to off-load registration functions for improved workflow. (Source: Pt1 p.64)
- **Primary function** — to verify identity of individuals (Source: Pt1 p.64):
  - E-mail — insufficient for activities that must be very secure
  - Documents — birth certificate, employee badge
  - In person — providing government-issued passport or driver's license
- Additional RA functions (Source: Pt1 p.64): receive, authenticate, and process certificate revocation requests; identify and authenticate subscribers; obtain a public key from the subscriber; verify that the subscriber possesses the asymmetric private key corresponding to the public key submitted for certification.

## Validation Authority (VA) and OCSP (Source: Pt1 p.65)

- **VA** — typically an outside entity used to validate certificates via Online Certificate Status Protocol (OCSP). (Source: Pt1 p.65)
- **OCSP** — a "request-response protocol" used to perform real-time lookup of a certificate's status. (Source: Pt1 p.65)
  - Browser sends the certificate's information to a trusted entity like the CA, known as an **OCSP Responder**.
  - The OCSP Responder then provides immediate revocation information on that one specific certificate.
  - Most OCSP servers can query the certificate database directly and obtain the real-time status of a certificate, while others depend on the CRLs and are limited by the CRL publishing interval.
- Diagram (Source: Pt1 p.65): (1) the CA (Certificate Manager) periodically publishes its CRLs to the OCSP Responder; (2) a client contacts the OCSP to see if a cert is valid; (3) the OCSP replies with the cert status.

## Keys and Key Escrow (Source: Pt1 p.66-67)

- **Key** — mathematical value entered into a cryptographic algorithm to produce encrypted data. (Source: Pt1 p.66)
- Public key cryptography uses a pair of keys: a **private key** kept secret and a **public key** that can be widely distributed ("You keep your private key in the safe, and publish your public key"). (Source: Pt1 p.66)
- The two keys are different but mathematically linked (Source: Pt1 p.66):
  - The public key is used to encrypt plaintext or to verify a digital signature.
  - The private key is used to decrypt ciphertext or to create a digital signature.
  - Messages encrypted with a public key can only be decrypted using the same private key pair.
- **Key Escrow** — the storing of private keys so that the key can be obtained (with proper authorization) in the event that the key owner is unavailable. (Source: Pt1 p.67)
  - Process by which keys are managed by a third-party (trusted CA).
  - The private key is separated into two halves, each half encrypted and stored in a separate location by the third-party (**secure enclave** — underlined on the slide).
  - The user can retrieve and combine the two halves to obtain the private key and decrypt messages.

## Cryptography defined and terminology (Source: Pt1 p.68-70)

- **Cryptography** — the art and science of protecting data by rendering it unreadable to an unauthorized recipient. (Source: Pt1 p.68)
  - Typically converting "plaintext" to "ciphertext" using a "cryptographic method".
  - A critical element in protecting Confidentiality and Integrity of information; can ensure "non-repudiation" is provided.
  - Proper use provides a deep level of protection and significantly reduces the impact of data loss.
  - "Strong crypto relies on math, not secrecy, to provide strength" (underlined on slide).
- **Mallory** — a malicious attacker attempting to subvert the message in some way. **Cryptanalysis** — the art of cracking cryptographic system. (Source: Pt1 p.68)

| Term | Slide definition | Source |
|---|---|---|
| Obscurity | a state of being unknown (making it difficult to understand) | Pt1 p.69 |
| Obfuscation | a technique that essentially "hides" or "camouflages" code or other information so that it is harder to read by unauthorized users | Pt1 p.69 |
| Cleartext | readable (unencrypted) data that is transmitted or stored in the clear | Pt1 p.69 |
| Plaintext | an information that has not been encrypted (input) | Pt1 p.69 |
| Ciphertext | an information that has been encrypted using an algorithm (cipher) making it unreadable to human users (output) | Pt1 p.69 |
| Algorithm | mathematical formula that converts plaintext inputs into ciphertext outputs (encryption) or reverses the process (decryption) to retrieve the plaintext | Pt1 p.69 |
| Confusion | the relationship between the plaintext and ciphertext should be as confused (random) as possible; **Substitution** replaces one character for another, which provides confusion | Pt1 p.69 |
| Diffusion | the order of the plaintext should be diffused/dispersed in the ciphertext; **Permutation (Transposition)** provides diffusion by rearranging the characters of the plaintext, anagram-style, combinations with repetition | Pt1 p.69 |
| Initialization Vector (IV) | used in some symmetric ciphers to ensure that the first encrypted block of data is random; ensures identical plaintext encrypts to different ciphertext | Pt1 p.70 |
| Chaining (feedback in stream modes) | seeds the previous encrypted block into the next block to be encrypted; destroys patterns in the resulting ciphertext | Pt1 p.70 |
| Ephemeral | a key that is only used once | Pt1 p.70 |
| Nonce | an arbitrary number used only once | Pt1 p.70 |
| Salt | a random or pseudo-random number or string | Pt1 p.70 |
| Cipher Suite | collection of algorithms used for authentication, encryption, decryption and digital signatures for confidentiality and integrity | Pt1 p.70 |
| Homomorphic Encryption | method that allows computation of certain field in a dataset without decrypting it; calculations performed while preserving privacy and confidentiality by keeping the data encrypted; output is in the form of encrypted data | Pt1 p.70 |

## Cipher types (Source: Pt1 p.71-72)

- **Substitution Cipher** — substitutes one character for another (e.g., "E" with "X"; 1 for A, 2 for B, etc.; example: *Security* becomes 1905032118092025). Also known as **Caesar, Monoalphabetic, and Rotation Cipher**. (Source: Pt1 p.71)
  - **ROT13** — the alphabet is rotated 13 steps so that A=N, B=O, C=P, etc.; example: *Security* becomes *frphevgl*. (Source: Pt1 p.71)
  - Diagram: alphabet/number grid with S E C U R I T Y → 19 5 3 21 18 9 20 25, and ROT13 row → F R P H E V G L. (Source: Pt1 p.71)
- **Vigenere** — uses multiple alphabets to help combat against single letter frequency; **Polyalphabetic Substitution Cipher** (a Vigenere square is shown). (Source: Pt1 p.72)
- **Transposition Cipher** — scrambling the letters in a certain manner; typically done by breaking up the message in equal sized blocks, and then scrambling each block. (Source: Pt1 p.72)
- **Rail Fence Cipher** — letters are written out in a diagonal pattern over several rows and then the cipher is read off row by row. Example: "I am taking the exam on Monday" laid out on three rows, giving IITEMA / MTKNHXMOODY / AAGEANN. (Source: Pt1 p.72)

## Securing the BIOS/UEFI (Source: Pt1 p.73)

- **BIOS** — an older method for handling boot up information. **UEFI** — a modern replacement for the BIOS with improved features. (Source: Pt1 p.73)
- BIOS/UEFI security mechanisms (Source: Pt1 p.73):
  - **Flash the BIOS** — ensure the BIOS/UEFI is updated to the latest version
  - **Use a BIOS Password** — password protecting the BIOS/UEFI to prevent unauthorized changes
  - **Configure the BIOS Boot Order** — internal HDD first so the system cannot boot from removable media
  - **Disable External Ports and Devices** — removable media and optical drives, eSATA ports, and USB ports
  - **Enable the Secure Boot Option** — prevents unsigned or improperly signed device drivers and OS loaders from being used
    - **Secure Boot** — process by which the BIOS/UEFI creates a cryptographic hash of the OS boot loader and boot drivers and compares them against a stored hash to aid in defeating root kits and boot sector viruses.

## Encryption levels (Source: Pt1 p.74-75)

- **Encryption Levels — visual** (Source: Pt1 p.74), three rows:
  - Client: pre-boot authentication (Password based, Token based, Smart card based, TPM, HSM); Full-disk (HDD1, Operating System / System Files); Folders/Files.
  - Server: Sectors (HDD 1, HDD 2); Partitions (HDD1 with C:, HDD2 with D: encrypted and E:); Volumes with RAID-5 (HDD1-4).
  - Database: Database (DB1); Partitions; Records (DB2).
- **Hard Drive Security** — both permanent and portable hard drives should be encrypted to prevent compromise. Creating two volumes on the drive allows one volume to be used as an active volume while the other volume is encrypted containing the Operating System files. (Source: Pt1 p.75)
- **Full Disk Encryption (FDE)** — encryption system that protects all data on a hard drive by automatically encrypting everything on the disk (**BitLocker**). (Source: Pt1 p.75)
  - Different than PGP and OS encryption which requires the user to select and then encrypt individual files and directories one by one.
  - Also listed: Whole Disk Encryption (WDE); Encrypted File System (EFS).

## Peripheral and file-level encryption (Source: Pt1 p.76-77)

- **Self Encrypting Drive (SED)** — a drive with a built-in controller chip that automatically encrypts the drive with an authentication key/key encryption key and will decrypt only if the proper password is supplied. (Source: Pt1 p.76)
  - **Data/Media Encryption Key (DEK/MEK)** — the key used to encrypt the data on the drive.
  - **Authentication Key/Key Encryption Key (AK/KEK)** — the key supplied by the user that is used to lock and unlock the drive.
- **USB encryption** — when data are transferred from one device to another via USB, the encryption on the copied-to device must also be considered. (Source: Pt1 p.76)
- **File and File System Encryption** — encryption software can encrypt or decrypt files one-by-one, or take advantage of the OS's file system to protect groups of files, such as all files in a specific folder. (Source: Pt1 p.77)
  - **Pretty Good Privacy (PGP)** — a widely used asymmetric cryptography system, used for files and emails on Windows systems.
  - **GNU Privacy Guard (GPG)** — runs on Windows, UNIX, and Linux.
  - **Operating System Encryption** — built into the OS and tied to the file system: EFS for Windows; FileVault for MacOS; uses NTFS (Windows); capability integrated with the file system; encryption and decryption transparent to the user; users can set the encryption attribute for a file in the Advanced Attributes dialog box.

## Transport/communication encryption (Source: Pt1 p.78)

- **Transport/communication** — encryption that protects data-in-motion. (Source: Pt1 p.78)
  - **Wi-Fi Protected Access (WPA)** — securing traffic sent over a wireless network.
  - **Internet Protocol Security (IPsec)** — securing traffic sent between two endpoints over a public or untrusted transport network.
  - **Transport Layer Security (TLS)** — securing application data, such as web or email data, sent over a public or untrusted network.
- **Perfect Forward Secrecy** — the key derived from another key is not compromised even if the original key is compromised in the future; if the server's private key is compromised the session to that server is still secure. (Source: Pt1 p.78)

## Quantum overview (Source: Pt1 p.79)

- **Quantum Cryptography** — limited in use; a small amount of the key bits are sent and when they are received at the remote end they are checked for interception. (Source: Pt1 p.79)
  - **Computing** — processing on units called quantum bits (**qubits**); power comes from qubits being entangled; when the value of a qubit is read, it collapses to either 1 or 0, and all other entangled qubits collapse at the same time.
  - **Communications** — particles (qubits), typically photons of light over optical cables, take on a state of superposition (represent multiple combinations of 1 and 0 simultaneously); tamper-evident key distribution.
  - **Post-quantum** — anticipating challenges to current cryptographic implementations and general security issues in a world where threat actors have access to significant quantum processing capability; replacements for the current algorithms.
  - **Lightweight cryptography** — NIST is hoping that a compact cipher suite will be developed that is both quantum resistant and can run on battery-powered devices with minimal CPU and memory resources; U.S. Satellite Communications (SATCOM) experts are asking industry for a small, lightweight, low-power encrypted mesh optical network to link satellites in Low Earth orbit.

## Asymmetric (public key) cryptography (Source: Pt1 p.80-85)

- **Public Key or Asymmetric Cryptography** — uses a "public key" to encrypt a message and a "private key" to decrypt it, both generated together. A **sender** encrypts a message with the **recipient's public key**; the **receiver** decrypts with **their private key**. Provides non-repudiation. Slower than symmetric encryption, but suitable for smaller amounts of data. (Source: Pt1 p.80)
  - Diagram: Plaintext → Encryption (receiver's public key) → Ciphertext → Decryption (receiver's private key) → Plaintext; public and private keys are mathematically related. (Source: Pt1 p.80)

| Algorithm | Encryption/Decryption | Digital Signature | Key Exchange | Notes (Source: Pt1 p.81) |
|---|---|---|---|---|
| RSA | Yes | Yes | Yes | Uses 2 large prime numbers. Key sizes up to 4096 bits |
| El-Gamal | Yes | Yes | Yes | Does not use prime number factoring but instead solving discrete logarithm problems |
| ECC (Elliptical Curve Cryptography) | Yes | Yes | Yes | Uses points on an elliptical curve with logarithmic problems. Low power consumption |
| DH (Diffie-Hellman) | No | No | Yes | Developed as a key Exchange protocol but can be MitM vulnerable if the use of digital signatures is waived |

- **RSA** — named for Ron Rivest, Adi Shamir, Leonard Adleman; de facto standard for public key encryption, widely used for authentication and data transport. (Source: Pt1 p.82)
  - Based on the difficulty of determining the factors of the product of **two large prime numbers** (prime decomposition).
  - The encryption key is publicly known and different from the decryption key.
  - If an attacker knows the public key, it is essentially impossible to determine the private key.
  - Example on slide: 62,459 * 104,297 = 6,514,286,323; given the product, what are the two prime factors? (A second example, 9,578,442,163, is posed with blanks left unanswered.)
- **ElGamal** — a public key algorithm usable for digital signatures, encryption, and key exchange. Creates an **ephemeral key** used for a single communications session and not used again (Ephemeral Keys — keys used only once). An extension of Diffie-Hellman based on calculating discrete logarithms in a finite field. Main drawback is performance: usually the slowest. (Source: Pt1 p.83)
- **ECC** — similar to RSA in functionality but more efficient, with smaller key sizes. (Source: Pt1 p.84)
  - Leverages a one-way function based on truly random keys, points mathematically graphed on a curve combined with a point in infinity, and discrete logarithms.
  - Less computation means less processing and less power consumption, which makes it great for smartphones, smart cards, wireless security, VOIP, IPsec, HTTPS and bitcoin integrity.
  - Requires true randomness of keys. Harder to break than RSA or Diffie-Hellman; solving curve logarithms is more difficult than solving for factored prime numbers.
  - Callout: "ECC is often used in lower power devices."
- **Diffie-Hellman** — used to create a private tunnel to exchange keys and other information. (Source: Pt1 p.85)
  - Allows 2 parties with no prior knowledge of each other to jointly establish a shared secret key over an unsecure channel; the shared secret symmetric key is then used to encrypt communications between the parties.
  - Uses one key for encryption and a mathematically related key for decryption; slide says "Technique provides authentication and non-repudiation"; private and public keys; "Described an independent storage location of public keys for users".
  - **Ephemeral Diffie-Hellman (DHE in the context of TLS)** differs from static DH in that static DH key exchanges always use the same DH private keys, so each time the same parties do a DH exchange they end up with the same shared secret. (Source: Pt1 p.85)
  - [CONFLICT] p.85 says DH "provides authentication and non-repudiation", while the p.81 table marks DH as "No" for Digital Signature and notes it can be MitM vulnerable if digital signatures are waived. Both are recorded as the slides state them. (Source: Pt1 p.81, p.85)

## Symmetric cryptography (Source: Pt1 p.86-91)

- **Symmetric Cryptography** — uses a **single key** or **shared key** for both encryption AND decryption; considered the fastest and most efficient for bulk encryption and usable for Message Authentication Codes. The shared key is used by both sender and receiver. (Source: Pt1 p.86)

| Algorithm | Key length (bits) | Type of cipher | Notes (Source: Pt1 p.87) |
|---|---|---|---|
| DES | 56 | Block (64 bit) | "Data Encryption Standard"; older algorithm, no longer in much use except in the MD5 hashing algorithm (slide wording) |
| 3DES | 56, 112, or 168 | Block (64 bit) | Executes DES three times; effective strength is 112 bits due to a partial meet-in-the-middle attack |
| AES | 128, 192, or 256 | Block (128 bit) | Advanced Encryption Standard; replaces DES, and is faster than both DES and 3DES |
| Twofish | Up to 256 | Block (128 bit) | Related to Blowfish; included in OpenPGP standard RFC 4880 |
| Blowfish | 32-448 | Block (64 bit) | Replaced by AES; public domain |
| IDEA | 128 | Block (64 bit) | "International Data Encryption Algorithm"; used mostly in Europe; originally used in PGP 2.0 |
| RC | Up to 2040 | Block: RC6 – 128 bit, RC5 – 32, 64, 128; **RC4 – Stream** | "Rivest Cipher"; several versions from RC2 to RC6; RC4 used for VPNs and secure video/voice |

- **Block Cipher** — groups (blocks) of plaintext bits are divided into blocks and fed into the cipher to be encrypted with a key and algorithm; commonly use substitution or transposition ciphers and encrypt 64-bits at a time; slower and simpler than stream ciphers. (Source: Pt1 p.88)
- **Stream Cipher** — plaintext bits are fed into a cipher and encrypted as a continuous stream, one bit at a time; encrypts very quickly; examples: A5 (cellular communications), RC4 (WEP and Transport Layer Security). (Source: Pt1 p.88)
- **DES** — based on a 56-bit cipher key and 8-bits for error correction (64-bits total); small key size was a weakness; eventually replaced by AES; based on the Lucifer Algorithm. (Source: Pt1 p.89)
- **Triple-DES (3DES)** — applies the cipher algorithm three times to each block; "still uses a 64-bit cipher key, but increases the key size to 168-bit (DES x3), which has helped to defeat brute force attacks" (slide wording). (Source: Pt1 p.89)
  - Slide note: the p.87 table gives 3DES effective strength as 112 bits; p.89 gives 168-bit key size. Both are as stated. (Source: Pt1 p.87, p.89)
- **AES** — three versions of block cipher keys: 128, 192, 256, each with the same cipher block size of 128-bit; based on the Rijndael Algorithm; developed by NIST to replace DES/3DES; versatile, fast, uses minimal resources, usable on a variety of platforms. (Source: Pt1 p.90)
- **IDEA** — uses a 128-bit key, similar in speed and capability to DES but more security; part of the PGP public domain encryption system commonly used for email encryption. (Source: Pt1 p.91)
- **PGP** — uses the IDEA algorithm; can also use asymmetric RSA for digital signatures and for sending the session key. (Source: Pt1 p.91)
  - Uses **Web of Trust (WoT)** instead of Certificate of Authority (CA).
  - Newer versions have key sizes from 512-bit to 2048-bits.
  - Uses a combination of hashing, data compression, symmetric key and asymmetric key cryptography.
  - The PGP suite can encrypt, decrypt and sign e-mail communications; perform whole disk encryption; and encrypt zip files and instant messages.

## More symmetric ciphers, one-time pads, key management (Source: Pt1 p.92-98)

- **Ron's Cipher (RC)** (Ron's Code) — multiple versions exist; most common are RC4, RC5, RC6. (Source: Pt1 p.92)
  - **RC4** — widely used streaming cipher in protocols such as SSL, WEP and RDP; contains several vulnerabilities and is therefore avoided for newer applications and technologies.
  - **RC5** — block cipher with variable sizes 32-bit, 64-bit, 128-bit; the lower levels (32 and 64) have been cracked using brute force, with attempts at cracking 72-bit ciphers taking place currently.
  - **RC6** — similar to AES in block and key sizes (128, 192, 256) but uses different mathematical methods.
- **Twofish** — newer cipher with a 128-bit block size and a key size of 256-bits. **Threefish** — not as common newer version designed to be a replacement for Twofish with a key size up to 1024-bits. **Blowfish** — block cipher with a 64-bit block size and key size 32-bit to 448-bits, designed to be a replacement for DES; very fast. All three have not been compromised, but have minor weaknesses exploitable through **Birthday Attacks** and key separation. (Source: Pt1 p.93)
- **One-Time Pads** — theoretically perfect and unbreakable because they are used one time and never used again. (Source: Pt1 p.94)
  - Key is the same size or larger than the material being encrypted.
  - Data is encrypted using modular addition (y+c=b) or XOR with a shared secret key.
  - Large key size makes brute-forcing irrelevant.
  - **Vernam Cipher** was the first known use of a one-time pad, which used XOR.
  - Not practical for large-scale use.
- **XOR Operations** — "A logical OR operation, based on the binary operation eXclusive OR that compares two bits; if the bits match the output is 0, if they do not match, the output is 1" (slide wording). Truth table (Data Bit, Key Input → Output): 0,0→0; 0,1→1; 1,0→1; 1,1→0. (Source: Pt1 p.94)
- **Key management and exchange challenges** — shared keys present a vulnerability when transmitted across a network; each pair of communicating nodes requires its own key, which creates several avenues of attack. Number of keys: **k = n(n-1)/2** (N = nodes, K = shared keys); diagrams: N=3 → K=3; N=4 → K=6. (Source: Pt1 p.95)
- **Symmetric cryptographic performance limitations** (Source: Pt1 p.96):
  - **Speed** — amount of data processed per second
  - **Key size** — security strongly related to key size; larger keys increase computational overhead, reducing speed and increasing latency
  - **Time** — time required to obtain a result is more important than a data rate
  - **Longevity** — confidence in a cipher; how long data must be kept secure
  - **Predictability** — a weakness in the cipher operation or particular key values that makes a ciphertext lower entropy and vulnerable to cryptanalysis
  - **Reuse** — reuse of the same key within the same session can cause this type of weakness
  - **Entropy** — a measure of disorder
  - **Weak key** — produces ciphertext that is lower entropy than it should be
  - **Computational Overheads** — some ciphers need more CPU and memory, less suited to resource-constrained environments
- **Cryptographic Tools** — hardware-based encryption devices are physical devices attached to or part of a computer system that store encryption keys. (Source: Pt1 p.97)
  - **TPM** — a microchip or co-processor on a computer's motherboard that provides cryptographic services; includes a true random number generator; cannot be subject to software attacks; prevents a computer from booting if the files or data has been altered; prompts for a password if the hard drive is moved to a new computer.
  - **HSM** — a hardware or peripheral device that contains a secure cryptographic key generator and storage; performs accelerated symmetric and asymmetric encryption; a plug-in card, a USB, a MicroSD, or other similar devices.
  - **Secure Enclave** — CPU extensions that protect data stored in system memory so that an untrusted process cannot read it.
- **Key Management** (Source: Pt1 p.98):
  - **Key Generation** — creates an asymmetric key pair or symmetric secret key of the required strength, using the chosen cipher
  - **Storage** — prevents unauthorized access to a private or secret key and protects against loss or damage
  - **Revocation** — prevents use of the key if it is compromised; if a key is revoked, any data encrypted using it should be re-encrypted using a new key
  - **Expiration and Renewal** — gives the certificate a "shelf-life"; every certificate expires after a certain period; certificates can be renewed with the same key pair or with a new key pair
- [GAP] "Key management system" is a Section Topics bullet; no slide uses that exact name — the closest content is the Key Management slide (p.98). "Key exchange" is covered by Diffie-Hellman (p.85) and the shared-key distribution problem (p.95).

## M-of-N control policy and steganography (Source: Pt1 p.99-100)

- **Key Recovery** — recovering keys of an employee when authorized conditions are met (hospitalization, death, left the company). May require a **Key Recovery Agent** — an account or combination of accounts that can copy a cryptographic key from backup or escrow and restore it to a subject host or user. (Source: Pt1 p.99)
- **M-of-N Control Policy** — a back-up process for public and private keys stored over multiple systems or devices to prevent the recreation of the keys from the back-up. (Source: Pt1 p.99)
  - Keys are backed up and then mathematically distributed across several devices.
  - Several individuals (typically three) within separate parts of the organization are assigned specific, separate job functions preventing any one person from being able to obtain the key without permission.
  - Callout: "Separation of Duties". Figure 6-11 "M-of-N control" shows N group / M group with Part 1-3 holders and a digital certificate/private key. (Source: Pt1 p.99)
- **Steganography** — the process by which a **message is hidden within another medium** (hiding data within an image). (Source: Pt1 p.100)
  - Data does not have to be encrypted.
  - Most common files are pictures, but audio and video files too.
  - Can be used to bypass other stringent security measures and help with data exfiltration.
  - Callout: the "Snow" technique hides data within the blank spaces, or "whitespace", of a file or image.

## Obfuscation and deidentification methods (Source: Pt2 p.1)

- **Data Masking** — whole or part of the contents of a field are redacted; techniques to preserve the original format of the field; an irreversible deidentification technique. (Source: Pt2 p.1)
- **Tokenization** — whole or part of the contents in a field is replaced with a randomly generated token; token stored in a separate data source (vault); reversible with access to the vault. (Source: Pt2 p.1)
- **Aggregation/Banding** — technique used to generalize the data, such as substituting a specific age with a broader age band. (Source: Pt2 p.1)
- **Hashing and Salting** — indexing method to speed up searches and provide deidentified references to records; storage method for data such as passwords where the original plaintext does not need to be retained; salt is an additional value stored with the hashed data field, creating a unique value. (Source: Pt2 p.1)

## Hashing (Source: Pt2 p.2-5)

- **Hashing** — a ONE-WAY mathematical function that produces a fixed length output from a variable length input. (Source: Pt2 p.2)
  - Can be referred to as a **fingerprint, checksum, message digest or hash**.
  - Hash algorithms do NOT encrypt.
  - Primarily used to verify **data integrity, authentication and non-repudiation**.
  - The same data will ALWAYS hash out to the same value if it has not changed.

| Hash algorithm | Output size (bits) | Primary usage (Source: Pt2 p.2) |
|---|---|---|
| MD5 | 128 | Rendered obsolete by newer algorithms, though still used for download verification and password storage; "algorithm is powered by DES" (slide wording) |
| SHA-1 | 160 | Developed by NSA; flaws have urged others to move to SHA-2 |
| SHA-2 | 224, 256, 384, 512 | Divided into several versions; more advanced than both MD5 and SHA-1 |
| HMAC | Depends on the algorithm used | Uses a secret cryptographic key only known to the sender and receiver and then hashes the message; receiver can verify the sender by hashing the message since only the sender and receiver have the key |

- **Message Digest** — one of the most common algorithms with four different versions (Version 2, 4, 5, 6); all but Version 6 are now considered unsuitable for use. **Version 5 (MD5)** — a generic version of several algorithms used to hash a file or message; output is a 128-bit value; the probability of two messages producing the same hash value was extremely limited; in 2007 the ability to produce a hash collision was proven and MD5 was no longer considered safe. (Source: Pt2 p.3)
- **Secure Hash Algorithm (SHA)** — designed by the NSA and NIST. (Source: Pt2 p.4)
  - SHA-0 — had design flaws and was withdrawn.
  - **SHA-1** — developed in 1993 and patterned after MD4 and MD5; was commonly used, however in 2017 researchers were able to accurately produce collisions rendering it unsuitable for use.
  - **SHA-2** — considered the most secure version.
  - **SHA-3** — approved in 2012 and replaced the earlier versions, but has not been adopted in many cipher packages.
  - [CONFLICT] The slide calls SHA-2 "the most secure version" yet also says SHA-3 "replaced the earlier versions"; recorded as the slide states it. (Source: Pt2 p.4)
- **LANMAN** — a protocol used by older Windows systems (prior to Windows NT) for authentication; used the LM Hash and two DES keys; replaced by NTLM with the release of Windows NT. **NTLM** — uses MD4 and MD5 hashing algorithms, primarily used for authentication in Windows systems; used in Windows NT as a replacement for LANMAN and is currently in widespread use today. (Source: Pt2 p.5)

## Salting (Source: Pt2 p.6)

- **Salt** — randomly-generated data that is added to a password before it is hashed to negate dictionary and rainbow table attacks. Also ensures unique password hashes are stored, even for the same existing password. Callout: "Password Hashes are 'salted'". (Source: Pt2 p.6)

## Digital signatures (Source: Pt2 p.7)

- **Digital Signature Standard** — used to verify the authenticity **of the sender** using the same keys as used in a PKI system. (Source: Pt2 p.7)
  - Digital Signature Algorithm (DSA) and FIPS 186-2 are used in the generation and verification of digital signatures; the US government equivalent of the RSA algorithm used only for Digital Signatures.
  - Keys are created in pairs public/private.
  - Box: "The **sender** hashes a message using **their own private key** (opposite of standard PKI encryption). The **receiver** uses the **sender's public key** to decrypt the hashed message." (Source: Pt2 p.7)
  - Weaknesses: shows only that the private key of the sender was used; cannot confirm the true identity of the sender; do not definitively prove who the sender was; an imposter could post a public key under a sender's name.

## Key stretching (Source: Pt2 p.8)

- **Key Stretching** — a process of protecting weak keys from brute-forcing by adding additional rounds of computations to increase the complexity and length of the key. (Source: Pt2 p.8)
  - **PBKDF2** (Password-Based Key Derivation Function 2) — a key stretching method that uses a password, a salt and applies HMAC thousands of times to produce a new key.
  - **Bcrypt** — a key-stretching method that salts the password by adding additional random bits before encrypting it with Blowfish.

## Blockchain and open public ledger (Source: Pt2 p.9)

- **Blockchain** — a concept in which an expanding list of transactional records listed in a public ledger is secured using cryptography. (Source: Pt2 p.9)
  - A **distributed ledger** (open public ledger): keeps track of transactions; everyone on the blockchain can maintain the ledger; everyone has a copy of the ledger; changes are distributed to everyone.
  - Can ensure integrity and transparency in: financial transactions (payment processing); online voting systems (digital voting); identity management systems (digital identification); notarization; data storage; supply chain monitoring.
- **Open Public Ledger** — a distributed public record of transactions that underpins the integrity of blockchains. (Source: Pt2 p.9)
  - A record-keeping system associated with cryptocurrency.
  - Fully decentralized, and no single entity controls the blockchain network.
  - Distributed across a peer-to-peer (P2P) network to mitigate the risks of a single point of failure or compromise.

## Digital certificates (Source: Pt2 p.10)

- **Digital Certificate** — a technology based on the **X.509** standard used to associate a user's identity to a public key that has been "digitally signed" by a trusted third party. (Source: Pt2 p.10)
  - NOT used to encrypt, but to verify identity and prevent MiTM impersonation attacks.
  - Contents (Source: Pt2 p.10): Version Number (certificate format; most common is Version 3); Subject/Owner's Name; Subject's/Owner's Public Key (copy of the subject's public key); Issuer's Name (certificate creator, and one who verifies authenticity); Issuer's Digital Signature; Serial number (uniquely identifies the certificate); Validity (dates certificate is good through); Certificate usage (purpose of the certificate); Algorithm ID / Signature Algorithm (algorithm used to sign the certificate); Extensions (Issuer Unique Identifier, Subject Alternative Name, Extensions, etc.).
  - Image: a sample certificate stating "Certificate Authority ABC, do hereby certify that Jim Bob Smith is who he/she claims to be and that his/her public key is BR549", with a CA signature and seal. (Source: Pt2 p.10)

## Trust models (Source: Pt2 p.11-12)

- **Trust** — confidence in or reliance on another person or entity. **Direct trust** — one user directly trusts another. **Third-party trust** — two individuals trust each other because each trusts a third-party. (Source: Pt2 p.11)
- **Trust Model** — the trust relationship that exists between entities/individuals within an organization: Hierarchical (Intermediate CA) Trust Model; Distributed/Bridge Trust Model; Online vs Offline CAs. (Source: Pt2 p.11)
  - **Online CA** accepts and processes certificate signing requests, publishes certificate revocation lists, and performs other certificate management tasks.
  - **Offline CA** delegates responsibilities of everything that the online CA does to an intermediate CA due to the high risk posed by compromising the root CA; a secure configuration involves making the root an offline CA.
- **Hierarchical (Intermediate CA) Trust Model** — a tiered system of CAs; the Root CA signs all digital certificates with a single key; if the key is compromised it can render all certificates worthless. (Source: Pt2 p.12; Figure 6-8 hierarchical trust model)
- **Distributed/Bridge Trust Model** — one CA acts as facilitator to connect different trust models and CAs, but does not issue certificates; hub between hierarchical and distributed trust models; the Bridge Trust Model allows a CA to stand up intermediate CAs. (Source: Pt2 p.12; Figure 6-10 bridge trust model; slide credit www.comptia.org)

## CRL, OCSP stapling, PKCS, certificate file extensions (Source: Pt2 p.13-16)

- **Certificate Revocation List (CRL)** — CAs maintain an online CRL that can be queried for revoked certificates; lists certificates by serial number that have been revoked; **CRL Distribution Point** — location(s) where the CRL is stored; multiple points can exist for a PKI system. (Source: Pt2 p.13)
- **OCSP Stapling** — variation of OCSP that attempts to reduce traffic by allowing web servers to include/staple a previously received OCSP response in the handshake between a web browser and the web server. (Source: Pt2 p.14)
  - Resolves these issues by having the SSL/TLS web server periodically obtain a time-stamped OCSP response from the CA.
  - When a client submits an OCSP request, the web server returns the time-stamped response, rather than making the client contact the OCSP responder itself.
  - Stapling mechanism used to mitigate performance and privacy issues when requesting certificate status from an OCSP responder.
  - Diagram: (1) web server asks OCSP Responder "Is this certificate valid?"; (2) "Yes, here is a signed approval"; (3) web browser "I want to connect"; (4) web server "Here is the approval". (Source: Pt2 p.14)
- **Public Key Cryptography Standards (PKCS)** — a set of 15 informal PKI standards based on the RSA public key algorithm, defined by RSA, widely accepted in the industry. (Source: Pt2 p.15)
  - **PKCS #7** — typically used to import and export certificates and private keys; a .p7b file might be used in Windows IIS as the basis for S/MIME and SSO.
  - **PKCS #12** — cryptographic archive file format for storing multiple cryptographic objects in a single file (e.g., private key, X.509 certificate); .pfx and .p12 file extensions; a .pfx file can be deployed by combining a private key with a .p7b file.
- **Certificate file extensions** (Source: Pt2 p.16):
  - **DER** (Distinguished Encoding Rules) — rules for how data sets are encoded within a system; used in OpenSSL.
  - **PEM** (Privacy Enhancement Mail) — Internet standard employing cryptographic techniques to provide confidentiality, sender authentication, and message integrity for secure transportation of email messages; most widely used in Linux systems.
  - **CER** (Canonical Encoding Rules) — rules for how data sets are encoded within a system; Windows systems use .CER, Linux systems use .CRT.
  - **PFX** (Personal Information Exchange) — designed by Microsoft to provide portable storage for a user's private keys, certificates, and miscellaneous secrets; complies with PKCS #12; backup public/private keys in safe, off-site storage; porting the keys to another computer for code-signing, temporary use, or fixed installation; removing EFS recovery keys for backup.

## Digital certificate types (Source: Pt2 p.17)

- **Root Digital Certificate** — generated and self-signed by the Root CA; provides authority to subordinate CAs to accept certificate requests, generate certificates, and authorize subordinate CAs within an organizational CA hierarchy. (Source: Pt2 p.17)
  - **Certificate Chaining** — chain of certificates from the Root CA down to the end-user.
  - **Certificate Pinning** — associating a host with their digital certificate.
- **CA Certificate** — issued by a CA to another CA; the second CA can then issue certificates to an end-entity. (Source: Pt2 p.17)
- **Cross-Certification** — used to establish peer-to-peer trust relationships between independent CAs. (Source: Pt2 p.17)
- **End-Entity Certificate** — issued by the CA to a specific entity or end-point device (individual, department, device specific); used to identify the entity in PKI systems. (Source: Pt2 p.17)
- **Domain Validation Digital Certificate** — used in TLS to verify the entity in control over a DNS domain. (Source: Pt2 p.17)
- **Machine Digital Certificate** — certificate used to identify a specific device (slide example: Xerox MFP). (Source: Pt2 p.17)
- **Email Digital Certificate** — used specifically for email to verify the identity of the sender and encrypt messages; used outside of a PKI system. (Source: Pt2 p.17)
- **Policy Certificate** — used for high-security applications; provides centrally controlled policy information to PKI clients. (Source: Pt2 p.17)

## Root of Trust (Source: Pt2 p.18)

- **Root of Trust (RoT)** — defines how users and different CAs can trust one another. (Source: Pt2 p.18)
  - Each CA issues itself a certificate (**root certificate**); self-signed — the CA server signs a certificate issued to itself.
  - The subject of the root certificate is set to the organization/CA name, such as "Northrop Grumman Corporate Root CA".
  - The root certificate can be used to sign other certificates issued by the CA.
  - Installing the CA's root certificate means that hosts will automatically trust any certificates signed by that CA.
- The slide image is a security guard at a checkpoint; no additional content. (Source: Pt2 p.18)

## Requesting a certificate: CSR (Source: Pt2 p.19)

- **Certificate Signing Request (CSR)** — a Base64 ASCII file sent to the CA containing the information that the subject wants to use in the certificate, including its public key. (Source: Pt2 p.19)

| CSR field | Description | Example (Source: Pt2 p.19) |
|---|---|---|
| Common name | Fully qualified domain name (FQDN) of the server | www.abccompany.com |
| Business name | Legal name of organization | ABC Company Inc. |
| Department | Division of the organization | IT |
| City | City of the organization | Denver |
| State | State of the organization | CO |
| Country | Two letter code of country | US |
| Email address | Address of POC | cio@abccompany.com |

## Wildcards, SAN, EV (Source: Pt2 p.20)

- **Wildcard Digital Certificate** — a certificate applied to a domain and all its sub-domains; based on the name of the server, all servers within a domain. (Source: Pt2 p.20)
- **Subject Alternative Name (SAN) Digital Certificate** — allows the addition of additional host names (sites, IP addresses, common names, etc.) to be protected under a single SSL certificate; example: *.site.biz, www.site.biz, ftp.site.biz, mail.site.biz. (Source: Pt2 p.20)
- **Extended Validation SSL Certificate (EV SSL)** — an enhanced type of server digital certificate that requires more extensive verification of legitimacy of the business. (Source: Pt2 p.20)
  - Browsers can visually indicate EV SSL by displaying the address bar shaded in green along with the site's name (red if site known to be dangerous).
  - Extended validation multi-domain SSL certificates allow a domain owner to assign multiple domains and sub-domains to a single SSL certificate.

## Range boundary and non-content slides (Source: Pt2 p.21-24)

- Pt2 p.21 (1-107) is the Domain 1 "Domain Topics" recap listing 1.1-1.4 (titles only). Pt2 p.22 (1-108) is the Education Ecosystem title slide, Pt2 p.23 is a Northrop Grumman logo slide, and Pt2 p.24 (2-1) is the Module 2 title slide "Threats, Vulnerabilities, and Mitigations". None carry 1.4 content. (Source: Pt2 p.21-24)
- Confirmed range for 1.4: **Pt1 p.60 - Pt2 p.20** (global 60-120, course slides 1-46 to 1-106; 61 pages). The provisional end (g123) in the tracker was too long by three non-content slides. (Source: Pt2 p.20-24)

## Validation log

- 2026-10-16, same-session re-check (not an independent second reader). All 61 pages (Pt1 p.60-100, Pt2 p.1-20) re-rendered and visually compared. Table-heavy and number-heavy slides (PKI steps, cipher types, asymmetric/symmetric/hash tables, digital signatures, certificate types, CSR) were checked at 130 dpi; the others at 80 dpi.
- Corrections: none to transcribed content. Two editorial fixes: removed an unsupported aside on Pt2 p.18 and relabelled one conflict tag (Pt2 p.4).
- Source quirks kept as stated: DH "provides authentication and non-repudiation" (p.85) vs "No" for digital signature (p.81); 3DES 112-bit effective (p.87) vs 168-bit key (p.89); DES "no longer in much use except in the MD5 hashing algorithm" and MD5 "powered by DES" (p.87, Pt2 p.2); SHA-2 "most secure" yet SHA-3 "replaced the earlier versions" (Pt2 p.4); Key Escrow "secure enclave" wording (p.67); RSA second factoring example left blank (p.82); p.62 "RSA 1024" next to PKI.

## Official-objective gap check (1.4, SY0-701 bullets as listed on Pt1 p.61)

| Official bullet | Result | Where |
|---|---|---|
| PKI: public key, private key, key escrow | Covered | Pt1 p.62-67 |
| Encryption level: full-disk, partition, file, volume, database, record | Weak | Only the visual (p.74) and FDE/file/SED slides (p.75-77); partition, volume, database, record are diagram labels with no definitions |
| Transport/communication | Covered | Pt1 p.78 |
| Asymmetric / Symmetric | Covered | Pt1 p.80-91 |
| Key exchange | Weak | Diffie-Hellman (p.85), key-count problem (p.95); no dedicated key exchange slide |
| Algorithms / Key length | Covered | Pt1 p.81, 87, 89-93 |
| Tools: TPM, HSM, secure enclave | Covered | Pt1 p.97 (secure enclave also p.67) |
| Tools: key management system | Weak | No slide by that name; Key Management lifecycle p.98 and M-of-N p.99 |
| Obfuscation: steganography, tokenization, data masking | Covered | Pt1 p.100; Pt2 p.1 |
| Hashing / Salting | Covered | Pt2 p.2-6 |
| Digital signatures | Covered | Pt2 p.7 |
| Key stretching | Covered | Pt2 p.8 |
| Blockchain / Open public ledger | Covered | Pt2 p.9 |
| Certificates: CAs, CRLs, OCSP | Covered | Pt1 p.63-65; Pt2 p.13-14 |
| Certificates: self-signed | Weak | Only "self-signed" in the root certificate (Pt2 p.17-18); no self-signed vs third-party comparison |
| Certificates: third-party | Weak | Commercial CA vs private CA (Pt1 p.63) only |
| Certificates: root of trust | Covered | Pt2 p.18 |
| Certificates: CSR generation | Covered | Pt2 p.19 (fields; no generation steps) |
| Certificates: wildcard | Covered | Pt2 p.20 |

Overall: **Weakly Covered** (encryption levels, key exchange, key management system, self-signed vs third-party are thin). No outside-slides content was added.

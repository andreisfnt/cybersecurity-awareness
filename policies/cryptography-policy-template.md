# Cryptography Policy

**Document reference:** [POL-SEC-CRYPTO-001]  
**Version:** 1.0  
**Effective date:** [Date]  
**Review date:** [Date - recommend annual]  
**Owner:** [IT Manager / CISO]  
**Approved by:** [Name and title]  
**Classification:** Internal  
**ISO 27001 reference:** Annex A 8.24 (Use of cryptography)

---

## 1. Purpose

This policy defines the requirements for the use of cryptographic controls to protect the confidentiality, integrity, and authenticity of information processed, stored, or transmitted by [Organization name].

Cryptography is a critical security control. Weak, outdated, or improperly managed cryptography provides a false sense of security. This policy ensures that cryptographic implementations are consistent, current, and governed.

---

## 2. Scope

This policy applies to:

- All systems, applications, and infrastructure owned or operated by [Organization name]
- All employees, contractors, and third parties who implement, manage, or use cryptographic controls
- Data at rest, data in transit, and data in use
- Encryption keys, certificates, and cryptographic secrets of any kind

---

## 3. Approved cryptographic standards

### 3.1 Symmetric encryption

| Use case | Approved algorithm | Minimum key length |
|----------|-------------------|--------------------|
| Data at rest | AES | 256-bit |
| File encryption | AES | 256-bit |
| Database encryption | AES | 256-bit |

Algorithms not listed above (including DES, 3DES, RC4, Blowfish) are prohibited.

### 3.2 Asymmetric encryption

| Use case | Approved algorithm | Minimum key length |
|----------|-------------------|--------------------|
| Key exchange / TLS | RSA | 2048-bit (3072-bit preferred) |
| Key exchange / TLS | ECDSA / ECDH | 256-bit (P-256 or higher) |
| Code signing | RSA or ECDSA | 2048-bit / 256-bit |
| SSH | Ed25519, ECDSA (P-256+), RSA | 256-bit / 2048-bit |

RSA keys below 2048-bit are prohibited. DSA is prohibited.

### 3.3 Hashing

| Use case | Approved algorithm |
|----------|--------------------|
| Password hashing | bcrypt, Argon2id, scrypt |
| File integrity / digital signatures | SHA-256, SHA-384, SHA-512 |
| HMAC | HMAC-SHA-256 or stronger |

MD5 and SHA-1 are prohibited for security purposes. SHA-1 may only be used for non-security legacy compatibility where no alternative exists, and only with documented exception approval.

### 3.4 Transport layer security

- TLS 1.2 is the minimum permitted version for all external-facing services
- TLS 1.3 is preferred and should be used for all new implementations
- SSL 2.0, SSL 3.0, TLS 1.0, and TLS 1.1 are prohibited
- Cipher suites must support forward secrecy (ECDHE or DHE key exchange)
- Weak cipher suites (RC4, NULL, EXPORT, DES, 3DES, anon) are prohibited

---

## 4. Data encryption requirements

### 4.1 Data at rest

The following categories of data must be encrypted at rest:

- Personal data (as defined under GDPR/AVG)
- Financial and payment data
- Authentication credentials and secrets
- Health data
- Confidential business information classified as Confidential or above
- Backup media and portable storage containing any of the above

### 4.2 Data in transit

All data in transit must be encrypted when:

- Traversing public networks (internet, public Wi-Fi)
- Transmitted between data centres or cloud environments
- Accessed remotely by employees or third parties
- Exchanged with third parties or suppliers

Internal network traffic between systems handling sensitive data should also be encrypted where technically feasible.

### 4.3 Portable devices and removable media

All portable devices (laptops, tablets) that may contain organizational data must use full-disk encryption. Removable media (USB drives) used to store organizational data must be encrypted.

---

## 5. Key management

### 5.1 Key generation

- Cryptographic keys must be generated using approved, cryptographically secure random number generators
- Keys must be generated with the minimum length specified in Section 3
- Private keys must never be generated on untrusted systems

### 5.2 Key storage

- Private keys and symmetric keys must never be stored in plaintext
- Keys must not be embedded in source code, configuration files, or documentation
- Keys must be stored in a dedicated secrets management solution (e.g. password vault, HSM, cloud key management service)
- Access to key storage systems must be restricted and logged

### 5.3 Key distribution

- Keys must be exchanged using secure, encrypted channels
- Keys must never be transmitted via email, chat, or other unencrypted means
- Key material must not be shared with unauthorized parties

### 5.4 Key rotation

| Key type | Maximum lifetime |
|----------|-----------------|
| TLS certificates (public-facing) | 1 year |
| TLS certificates (internal) | 2 years |
| SSH keys | 2 years |
| Symmetric encryption keys (high sensitivity) | 1 year |
| Symmetric encryption keys (standard) | 2 years |
| Code signing certificates | Per CA policy |

Keys must also be rotated immediately upon:
- Suspected or confirmed compromise
- Personnel departure (where key access was held)
- System decommission

### 5.5 Key revocation and destruction

- Compromised or expired keys must be revoked and destroyed immediately
- Key destruction must be irreversible and verifiable
- Certificate revocation must be performed via CRL or OCSP

---

## 6. Certificate management

- All public-facing TLS certificates must be issued by a trusted Certificate Authority (CA)
- Self-signed certificates are only permitted for internal development and testing environments with documented approval
- Certificate expiry dates must be tracked and renewals initiated at least 30 days before expiry
- An inventory of all certificates and their expiry dates must be maintained

---

## 7. Prohibited practices

The following are explicitly prohibited:

- Use of deprecated algorithms listed in Section 3
- Storage of keys in source code repositories or version control systems
- Use of self-signed certificates for production public-facing services
- Disabling certificate validation in applications or scripts
- Using the same key or certificate across multiple unrelated systems
- Generating keys with insufficient entropy or non-random seeds

---

## 8. Roles and responsibilities

| Role | Responsibility |
|------|---------------|
| IT Manager / CISO | Policy ownership, approval of exceptions, oversight |
| IT / Security team | Implementation, key management, certificate lifecycle |
| Developers | Compliance in application design and code |
| All staff | Compliance with device encryption requirements |

---

## 9. Exceptions

Exceptions to this policy require written approval from [IT Manager / CISO]. Exceptions must document the business justification, compensating controls, and an expiry date. Exceptions are reviewed annually.

---

## 10. Compliance and enforcement

Violation of this policy may result in disciplinary action. Systems found to be non-compliant must be remediated within [30] days or removed from production.

---

## 11. Review

This policy is reviewed annually or following a significant change in the threat landscape, technology environment, or regulatory requirements.

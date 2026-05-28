# Access Control Policy

**Document reference:** [POL-SEC-AC-001]  
**Version:** 1.0  
**Effective date:** [Date]  
**Review date:** [Date - recommend annual]  
**Owner:** [IT Manager / CISO]  
**Approved by:** [Name and title]  
**Classification:** Internal  
**ISO 27001 reference:** Annex A 5.15 - 5.18 (Access control), A 8.2 - 8.5 (Privileged access, authentication)

---

## 1. Purpose

This policy defines the requirements for managing access to [Organization name]'s systems, applications, networks, and data. Its purpose is to ensure that access is granted on the basis of least privilege and business need, and that access rights are properly managed throughout the user lifecycle.

Access control failures are one of the most common root causes of security incidents. Excessive, stale, or unreviewed access creates risk regardless of how well other controls are implemented.

---

## 2. Scope

This policy applies to:

- All systems, applications, networks, and data owned or operated by [Organization name]
- All user accounts, service accounts, shared accounts, and privileged accounts
- All employees, contractors, consultants, and third parties with access to organizational systems
- Cloud services, SaaS applications, on-premise infrastructure, and remote access systems

---

## 3. Access control principles

All access decisions must be based on the following principles:

- **Least privilege:** Users are granted the minimum level of access required to perform their job function. No more.
- **Need to know:** Access to information is restricted to those with a legitimate business need.
- **Separation of duties:** Critical or sensitive functions must not be concentrated in a single individual where feasible.
- **Default deny:** Access is denied by default; it must be explicitly granted.
- **Accountability:** Every access action is tied to an identifiable individual. Shared accounts are prohibited except where explicitly documented and approved.

---

## 4. User access management

### 4.1 Access provisioning

- Access requests must be submitted through [IT ticketing system / defined process] and approved by the requesting user's line manager
- IT must verify approval before provisioning access
- Access must be provisioned within [X] business days of approved request
- New starters must have access provisioned before or on their first working day based on a request from HR or the hiring manager
- Access must reflect the user's role - role-based access control (RBAC) must be used where available

### 4.2 Access modification

- Changes in role or responsibilities that require changes to access must be communicated to IT by the line manager within [5] business days
- Access from previous roles must be removed at the time new access is granted
- Temporary elevated access (e.g. for a project) must have a defined end date and be removed automatically or manually upon expiry

### 4.3 Access revocation

- Access must be revoked on the last working day of an employee, contractor, or third party
- HR must notify IT at least [1 business day] before a planned departure
- For unplanned departures (dismissal, resignation with immediate effect), IT must revoke all access within [2 hours] of notification
- Accounts must be disabled rather than deleted initially, and deleted after [30] days unless legal retention requirements apply
- Remote access credentials (VPN, MFA tokens) must be revoked as part of the offboarding process

### 4.4 Contractor and third-party access

- Third-party access must be time-limited and scoped to the minimum required for the engagement
- Third-party accounts must be reviewed [monthly] and deprovisioned immediately upon contract end
- Third parties must not have standing access to production systems unless a documented operational requirement exists

---

## 5. Privileged access management

Privileged accounts (domain administrators, local administrators, root accounts, system accounts with elevated permissions) carry significantly higher risk than standard user accounts and require additional controls.

### 5.1 Provisioning

- Privileged access must be explicitly approved by [IT Manager / CISO]
- Privileged access must be documented in a privileged access register
- Users requiring privileged access must use a separate privileged account distinct from their standard user account
- Personal administrative accounts must be named accounts - generic or shared admin accounts are prohibited

### 5.2 Usage

- Privileged accounts must only be used for tasks that require elevated permissions
- Day-to-day work (email, browsing, productivity) must be performed using standard user accounts
- Privileged sessions must be conducted from secure, trusted devices
- All privileged access must be logged. Logs must be protected from modification and retained for a minimum of [12 months]

### 5.3 Emergency access

- Break-glass / emergency access procedures must be documented and tested
- Emergency access usage must be logged and reviewed within [24 hours] of use
- Emergency credentials must be stored securely (e.g. in a sealed envelope in a physical safe, or in a privileged access management solution)

---

## 6. Authentication requirements

### 6.1 Password requirements

Passwords must meet the following minimum requirements:

| Account type | Minimum length | Complexity | Expiry |
|-------------|---------------|------------|--------|
| Standard user | 12 characters | Mixed case + number or symbol | No mandatory rotation unless compromised |
| Privileged account | 16 characters | Mixed case + numbers + symbols | No mandatory rotation unless compromised |
| Service account | 20 characters | Mixed case + numbers + symbols | Per system requirements |

Password expiry-based rotation is not required but passwords must be changed immediately upon suspected or confirmed compromise. Password reuse of the last [10] passwords is prohibited.

All passwords must be managed in an approved password manager. Passwords must not be written down, stored in plaintext, or shared.

### 6.2 Multi-factor authentication (MFA)

MFA is required for:

- All remote access (VPN, remote desktop)
- All cloud-based services and SaaS applications
- All privileged account logins
- All email access from outside the corporate network
- All access to systems containing personal data or financial data

SMS-based MFA is discouraged due to SIM-swapping risk. Authenticator apps (TOTP) or hardware tokens are preferred.

### 6.3 Single sign-on (SSO)

Where available, SSO must be used to reduce credential sprawl. SSO implementations must still enforce MFA at the identity provider level.

---

## 7. Remote access

- Remote access must use an approved VPN or zero-trust network access solution
- Remote access must require MFA
- Remote access sessions must time out after [60] minutes of inactivity
- Remote access from unmanaged, personal devices to systems containing sensitive data is prohibited without explicit approval and compensating controls (e.g. virtual desktop)
- Split tunneling must be disabled for VPN configurations used to access sensitive systems

---

## 8. Access reviews

- All user access rights must be reviewed [quarterly] for privileged accounts and [annually] for standard accounts
- Reviews must be conducted by line managers in coordination with IT
- Any access identified as excessive, stale, or no longer required must be revoked within [10] business days of the review
- Access review results must be documented and retained for audit purposes

---

## 9. Service accounts and application access

- Service accounts must be created for a specific, documented purpose
- Service accounts must use strong credentials and must not be used by humans for interactive logon
- Service account credentials must be rotated at least annually and upon staff changes that had access to them
- Application-to-application authentication must use modern methods (OAuth 2.0, API keys with appropriate scope) rather than shared credentials where possible

---

## 10. Logging and monitoring

- All authentication events (successful and failed) must be logged
- Privileged access activity must be logged in detail
- Failed authentication attempts must trigger alerts after [5] consecutive failures within [10] minutes
- Access logs must be retained for a minimum of [12 months] and protected from unauthorized modification

---

## 11. Roles and responsibilities

| Role | Responsibility |
|------|---------------|
| IT Manager / CISO | Policy ownership, privileged access approval, access review oversight |
| IT team | Access provisioning, deprovisioning, log management |
| Line managers | Access request approval, access review participation, offboarding notification |
| HR | Timely notification of joiners, movers, and leavers |
| All users | Compliance with authentication requirements, reporting anomalies |

---

## 12. Exceptions

Exceptions require written approval from [IT Manager / CISO] with documented justification, compensating controls, and an expiry date.

---

## 13. Review

This policy is reviewed annually or following a significant access-related incident or change in organizational structure.

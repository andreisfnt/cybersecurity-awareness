# Physical Security Policy

**Document reference:** [POL-SEC-PHYS-001]  
**Version:** 1.0  
**Effective date:** [Date]  
**Review date:** [Date - recommend annual]  
**Owner:** [IT Manager / Facilities Manager]  
**Approved by:** [Name and title]  
**Classification:** Internal  
**ISO 27001 reference:** Annex A 7.1 - 7.14 (Physical controls)

---

## 1. Purpose

This policy establishes the physical security requirements to protect [Organization name]'s facilities, equipment, and information assets from unauthorized physical access, damage, theft, and environmental threats.

Logical controls can be bypassed entirely when physical access is uncontrolled. Physical security is a foundational layer of information security, not an afterthought.

---

## 2. Scope

This policy applies to:

- All organizational premises, offices, and data processing facilities
- All employees, contractors, visitors, and third parties accessing organizational premises
- All IT equipment, servers, workstations, network infrastructure, and portable devices
- All physical records and printed documents containing organizational information

---

## 3. Physical security perimeter

### 3.1 Facility access control

- Access to organizational premises must be controlled and restricted to authorized individuals
- Entry points must be secured with appropriate controls (key cards, PIN codes, or physical keys)
- Access rights to premises must be granted on a need-to-access basis and reviewed [quarterly / annually]
- Access credentials must not be shared between individuals
- Visitors must be registered, issued visitor identification, and escorted at all times in secure areas

### 3.2 Security zones

Facilities are classified into the following zones:

| Zone | Description | Access requirements |
|------|-------------|---------------------|
| Public | Reception, meeting rooms, common areas | No restriction |
| General | Standard office areas | Authorized staff and escorted visitors |
| Restricted | Server rooms, network closets, HR/finance areas | Named authorization required |
| High security | Primary data processing areas (if applicable) | Explicit named authorization, logged entry |

Access control requirements increase with zone sensitivity. Access to Restricted and High Security zones must be logged.

---

## 4. Visitor management

- All visitors must sign in at reception and present identification
- Visitors must be issued a visitor badge that is visibly worn at all times
- Visitors must be escorted by an authorized employee throughout their visit in General and above zones
- Visitor access must be limited to areas relevant to their purpose
- Visitor logs must be retained for a minimum of [90 days]
- Visitor badges must be returned on departure

---

## 5. Equipment security

### 5.1 Server rooms and network infrastructure

- Server rooms and network closets must be locked at all times when not actively in use
- Access must be restricted to IT staff with a documented operational need
- Physical access logs must be maintained and reviewed [monthly]
- Environmental monitoring (temperature, humidity, flood detection) must be in place where technically feasible
- Power and network cabling must be protected from damage and unauthorized interception
- Uninterruptible power supplies (UPS) must be maintained for critical systems

### 5.2 Workstations and endpoints

- Workstations must be physically secured to desks using cable locks in open or shared office environments
- Screens must be positioned to prevent unauthorized viewing (shoulder surfing)
- Screen lock must activate automatically after a maximum of [5] minutes of inactivity
- Employees must lock screens manually when stepping away from their workstation
- Unattended logged-in workstations are a policy violation

### 5.3 Portable devices

- Laptops, tablets, and mobile phones must not be left unattended in public places
- Portable devices must not be left visible in unattended vehicles
- Loss or theft of any portable device must be reported to IT immediately and no later than [4 hours] after discovery
- All portable devices must use full-disk encryption (see Cryptography Policy)

---

## 6. Clean desk and clear screen

- Employees must maintain a clean desk at the end of each working day
- Sensitive documents and media must be stored in locked drawers or cabinets when not in use
- Documents containing personal data, financial information, or confidential business information must not be left unattended on desks
- Whiteboards and flip charts containing sensitive information must be erased before meetings end or rooms are vacated
- Screen lock must be active on all unattended workstations

---

## 7. Secure areas

- Work in secure areas (Restricted / High Security zones) must follow the principle of need-to-know
- Photographic and recording equipment (including mobile phones) must not be used in secure areas without explicit authorization
- Unsupervised work in secure areas must be avoided where possible
- Secure areas must be regularly inspected for compliance

---

## 8. Secure disposal of equipment and media

- IT equipment must not be disposed of, donated, or repurposed until all data has been securely wiped
- Data destruction must follow the requirements in the [Data Retention and Disposal Policy] or equivalent
- Hard drives and storage media must be wiped using approved data destruction methods or physically destroyed
- A certificate of destruction must be obtained for all data-bearing media sent to third-party disposal services
- Paper documents containing sensitive information must be shredded using cross-cut or micro-cut shredders
- Shredding bins must be available at all locations where sensitive documents are handled

---

## 9. Environmental threats

- [Organization name] must maintain awareness of environmental risks (fire, flood, power failure) relevant to its premises
- Fire suppression systems and smoke detectors must be tested in accordance with local regulations
- Emergency exits must be kept clear and unobstructed at all times
- Critical IT equipment must be located away from areas at high risk of flooding or water damage
- Business continuity plans must account for environmental threat scenarios

---

## 10. Third-party physical access

- Third parties (maintenance staff, cleaners, delivery personnel) requiring access to secure areas must be escorted
- Access for maintenance or service work must be logged and time-limited
- Physical access rights granted to third parties must be reviewed and revoked promptly upon completion of work

---

## 11. Roles and responsibilities

| Role | Responsibility |
|------|---------------|
| IT Manager / Facilities Manager | Policy ownership, physical access control management |
| IT team | Equipment security, secure disposal, server room access |
| Line managers | Ensuring team compliance with clean desk and visitor escort requirements |
| All employees | Compliance with daily security practices, incident reporting |
| Reception / front desk | Visitor registration, badge issuance |

---

## 12. Incidents and reporting

Physical security incidents must be reported immediately to [IT Manager / Security team]:

- Unauthorized access or access attempts
- Lost or stolen access credentials or devices
- Tailgating or piggybacking observations
- Suspicious individuals or behavior on premises
- Physical damage to security controls or equipment

---

## 13. Compliance and enforcement

Violations of this policy may result in disciplinary action up to and including termination. Physical security observations are included in internal audits.

---

## 14. Review

This policy is reviewed annually or following a physical security incident, significant change in premises, or regulatory requirement change.

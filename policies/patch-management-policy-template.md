# Patch Management Policy

**Document reference:** [POL-SEC-PATCH-001]  
**Version:** 1.0  
**Effective date:** [Date]  
**Review date:** [Date - recommend annual]  
**Owner:** [IT Manager / CISO]  
**Approved by:** [Name and title]  
**Classification:** Internal

---

## 1. Purpose

This policy defines the approach to managing security patches and updates across [Organization name]'s IT environment. Unpatched systems are one of the most common attack vectors. This policy ensures that vulnerabilities are identified and remediated within defined timeframes proportionate to their risk.

---

## 2. Scope

This policy applies to:

- All organization-owned endpoints (laptops, desktops, mobile devices)
- All servers and infrastructure (physical and virtual)
- All operating systems in use across the organization
- All third-party applications and software installed on organizational systems
- Network and security devices (routers, firewalls, switches, access points)
- Cloud platforms and services where the organization is responsible for patching

Third-party managed services where the vendor is contractually responsible for patching are out of scope, but patch status should be confirmed at service reviews.

---

## 3. Patch classification and timelines

Patches are classified by severity. Timelines below are targets from patch availability to deployment completion.

| Severity | Definition | Target deployment timeline |
|----------|-----------|--------------------------|
| Critical | Actively exploited vulnerability, or CVSS score 9.0-10.0. Potential for remote code execution, privilege escalation, or significant data loss without user interaction | [e.g. 48-72 hours] |
| High | CVSS score 7.0-8.9. Significant risk requiring prompt attention | [e.g. 7 days] |
| Medium | CVSS score 4.0-6.9. Moderate risk. Exploitability typically requires local access or user interaction | [e.g. 30 days] |
| Low | CVSS score below 4.0. Minimal risk. Address as part of regular patching cycle | [e.g. 90 days] |

**Monthly patching cycle:** In addition to out-of-band patching for Critical and High severity issues, a regular monthly patching cycle addresses Medium and Low priority patches and routine OS updates.

---

## 4. Patch management process

### Step 1: Identification

IT monitors the following sources for new patches and vulnerability disclosures:

- Vendor security bulletins and update channels (operating system vendors, major application vendors)
- National vulnerability databases (e.g., NVD, CVE feeds)
- Security advisories from relevant industry bodies
- Threat intelligence sources

New patches are logged and assessed for applicability to the organization's environment.

### Step 2: Assessment

For each patch, IT assesses:

- Applicability - which systems in the environment are affected
- Severity and exploitability - using vendor and CVE ratings
- Business impact of patching - potential disruption, compatibility risk
- Business impact of not patching - risk to systems and data if the vulnerability is exploited

### Step 3: Testing

Before deployment to production:

- Critical and High severity patches are tested in a representative non-production environment where one exists
- Testing confirms the patch installs correctly and does not cause application or system failures
- For Critical patches, testing timelines are compressed to meet deployment targets - risk of deployment is weighed against risk of remaining unpatched

### Step 4: Deployment

Patch deployment follows the schedule in Section 3. Deployment is managed centrally by IT using the organizational device management and patch management tooling.

Deployment order for environments with multiple tiers:

1. Non-production / test environment
2. Lower-risk production systems
3. Critical production systems and servers

### Step 5: Verification

After deployment:

- IT verifies patch installation success across affected systems
- Unpatched or failed systems are identified and remediated
- Compliance against target timelines is tracked and reported

---

## 5. Emergency patching

When a Critical vulnerability is actively exploited and poses immediate risk:

- Normal change management processes are accelerated, not bypassed
- Emergency approval is obtained from [IT Manager / CISO] prior to deployment
- Deployment proceeds as quickly as safely possible
- Testing is conducted in parallel with deployment preparation to minimize delay
- Stakeholders are notified of emergency patching activity and potential disruption
- A post-deployment review is completed within [48 hours]

---

## 6. Employee responsibilities

Employees are required to:

- Allow automatic updates and patch installations to proceed on managed devices - do not defer or disable updates
- Restart devices promptly when prompted to complete patch installation
- Report to IT if a device is unable to receive updates or if update processes appear to be failing
- Not attempt to remove or disable patch management software installed by IT

Employees who regularly defer required restarts risk their devices falling outside compliance and may have access restricted until the device is brought up to date.

---

## 7. Unsupported and end-of-life systems

Systems running end-of-life software that no longer receives security updates represent a standing vulnerability. For any such system in the environment:

- The risk must be documented and formally accepted by an appropriate authority
- Compensating controls must be implemented (network isolation, enhanced monitoring, restricted access)
- A remediation or replacement plan with a defined timeline must be in place
- The system must be reviewed at least quarterly until remediated

IT maintains a register of end-of-life software in the environment.

---

## 8. Exceptions

Exceptions to patch timelines may be approved where:

- Patching would cause a material disruption to a critical business process
- A patch introduces a known compatibility issue that has not yet been resolved
- A compensating control is in place that adequately mitigates the risk

Exceptions must be:

- Requested by the business owner of the affected system
- Approved by [IT Manager / CISO]
- Documented with the reason, compensating controls, and a defined review date
- Reviewed and renewed or closed at the defined review date

Exceptions are not indefinite. An exception without a remediation plan is a deferred risk, not a resolved one.

---

## 9. Reporting

IT reports on patch compliance at least monthly, including:

- Percentage of systems within compliance targets by severity tier
- Outstanding exceptions and their status
- End-of-life software register status
- Significant vulnerabilities identified in the period and their remediation status

Patch compliance reports are shared with [IT leadership / CISO / relevant stakeholders].

---

## Revision history

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | | | Initial version |

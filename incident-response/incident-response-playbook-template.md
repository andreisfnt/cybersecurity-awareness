# Incident Response Playbook

**Version:** 1.0  
**Owner:** [IT Manager / CISO]  
**Last reviewed:** [Date]  
**Approved by:** [Name and title]  
**Classification:** Internal - Restricted

---

## Purpose

This playbook defines how [Organization name] detects, responds to, contains, and recovers from security incidents. It provides structure for incident response so that decisions made under pressure are informed by a process agreed in advance, not improvised in the moment.

A playbook that has never been rehearsed is a document. Review and test it at least annually.

---

## What counts as a security incident

An incident is any event that has or could have an adverse effect on the confidentiality, integrity, or availability of organizational information or systems.

Employees should report anything suspicious - the threshold for reporting should be low. IT triages reported events and determines whether they constitute an incident.

**Examples of security incidents:**

- Phishing email clicked, credentials potentially compromised
- Lost or stolen device
- Unauthorized access to a system or account
- Malware detection on a device
- Ransomware or file encryption
- Accidental disclosure of sensitive data (sent to wrong recipient, file shared publicly)
- Suspected personal data breach (GDPR-relevant)
- Insider threat behavior
- Denial of service affecting organizational systems
- Compromise of a third-party system with access to organizational data
- Suspicious activity in logs or access records

**When in doubt, report.** An event that turns out to be a false positive costs a brief investigation. An event that is not reported and turns out to be real costs significantly more.

---

## Incident severity levels

| Severity | Definition | Examples | Response timeline |
|----------|-----------|---------|------------------|
| P1 - Critical | Active threat with immediate business impact or significant data exposure | Ransomware, active unauthorized access, confirmed large-scale data breach | Immediate - all hands |
| P2 - High | Significant risk requiring urgent response | Compromised admin credentials, malware on critical system, suspected data breach | Within 1 hour |
| P3 - Medium | Contained threat or moderate risk | Phishing clicked but no confirmed compromise, single device lost | Within 4 business hours |
| P4 - Low | Minimal risk, no confirmed compromise | Suspicious email reported and not clicked, minor policy violation | Within 1 business day |

Severity is assessed at the time of triage and may be escalated or de-escalated as more information becomes available.

---

## Incident response team

| Role | Responsibility | Primary contact | Backup contact |
|------|---------------|-----------------|----------------|
| Incident Lead | Overall coordination of the response | [Name] | [Name] |
| IT / Security | Technical investigation and containment | [Name] | [Name] |
| Communications Lead | Internal and external communication | [Name] | [Name] |
| Legal / Compliance | Legal obligations, regulatory notifications | [Name] | [Name] |
| Senior Leadership | Executive decisions, stakeholder communication | [Name] | [Name] |

For P1 and P2 incidents, all roles are activated. For P3 and P4, the Incident Lead and IT/Security roles are sufficient in most cases.

---

## Phase 1: Detection and Reporting

### Employee reporting

Employees report suspected incidents to IT via:

- **Primary:** [Helpdesk / ticketing system - link or contact]
- **Emergency (P1):** [Phone number / direct contact]

When reporting, provide:
- What you observed or what happened
- When it occurred
- Which system, device, or account is involved
- What actions you have already taken (e.g., powered off device, changed password)

Do not attempt to investigate or remediate independently. Report and wait for IT guidance.

### Detection from monitoring

[IT team / security monitoring] may detect incidents through:

- Endpoint protection alerts
- Log monitoring and alerting
- User access anomaly detection
- Third-party notifications (vendors, law enforcement, security researchers)

All detected events are logged and triaged by IT.

---

## Phase 2: Triage and Initial Assessment

**Owner:** Incident Lead / IT  
**Timeline:** Within 30 minutes of report for P1/P2, within 4 hours for P3/P4

### Triage checklist

- [ ] Incident received and logged with timestamp and reporter details
- [ ] Initial severity assessment completed
- [ ] Incident Lead assigned
- [ ] Incident response team notified (based on severity)
- [ ] Incident log opened (see Appendix A)
- [ ] Preservation of evidence considered - do not take actions that may destroy forensic evidence before assessing need
- [ ] Scope assessed: how many systems, users, or data types are potentially affected?
- [ ] Is this a personal data breach that may trigger GDPR notification obligations? (See Phase 5)

### Key questions at triage

- Is the threat active or historical?
- Is the affected system still accessible to the attacker?
- What is the worst credible case scenario if the incident is not contained immediately?
- What containment actions are available and what are their side effects?

---

## Phase 3: Containment

**Owner:** IT / Security  
**Goal:** Stop the bleeding. Prevent the incident from spreading or worsening before full investigation.

Containment actions depend on the incident type. Common actions include:

| Incident type | Containment actions |
|--------------|-------------------|
| Compromised credentials | Force password reset, revoke active sessions, disable account if necessary, review access logs |
| Lost or stolen device | Remote lock or wipe (if enrolled in device management), revoke device-level access |
| Malware / ransomware | Isolate affected device(s) from network immediately, do not power off if avoidable (preserves memory forensics) |
| Unauthorized access | Revoke the compromised access path, preserve logs, isolate affected system if necessary |
| Data disclosure | Identify what was disclosed and to whom, attempt to contain further distribution, notify Legal |
| Phishing (active campaign) | Block sending domain/address at email gateway, notify all employees if campaign is organization-targeted |

**Document every containment action taken, including time and by whom.**

Containment may involve a trade-off between speed and evidence preservation. In most cases, containment takes priority - but for significant incidents, consult with the Incident Lead before taking actions that may destroy forensic evidence.

---

## Phase 4: Investigation and Root Cause Analysis

**Owner:** IT / Security  
**Goal:** Understand what happened, how, and what the full scope of impact is.

### Investigation checklist

- [ ] Preserve relevant logs before they expire or are overwritten
- [ ] Identify the attack vector (how the incident occurred)
- [ ] Establish the timeline (when did the incident begin, what happened in sequence)
- [ ] Determine the full scope of affected systems, accounts, and data
- [ ] Identify whether any sensitive or regulated data was accessed or exfiltrated
- [ ] Determine whether the threat actor may still have access (persistence mechanisms)
- [ ] Identify vulnerabilities or weaknesses that enabled the incident

### Evidence handling

- Do not delete or modify potential evidence without authorization from the Incident Lead
- Preserve logs, disk images, memory captures, and email headers as appropriate
- Document the chain of custody for any evidence collected
- If law enforcement involvement is possible or required, consult Legal before proceeding

---

## Phase 5: Notification and Communication

**Owner:** Communications Lead / Legal  
**Goal:** Communicate what needs to be communicated, to the right people, at the right time - no more, no less.

### Internal communication

| Audience | When | What to communicate |
|----------|------|-------------------|
| Incident response team | Immediately on activation | Incident details, roles, next steps |
| Senior leadership | P1/P2: within 1 hour. P3: within 4 hours | Status, potential impact, decisions needed |
| Affected employees | When containment actions affect them | What is happening, what they need to do |
| All employees | If incident requires organization-wide action (e.g., active phishing campaign) | What to watch for, what to do |

### Regulatory notification (GDPR)

A personal data breach that is likely to result in a risk to individuals must be notified to the relevant supervisory authority within 72 hours of becoming aware of it. The 72-hour clock starts when IT or the organization first becomes aware - not when the investigation is complete.

**On identification of a potential personal data breach:**

- [ ] Notify Legal / Data Protection Officer immediately
- [ ] Document the timeline of when the breach was identified and what is known
- [ ] Begin assessing scope: what personal data was affected, how many individuals, what risk to those individuals
- [ ] Legal / DPO determines notification obligation and manages the notification process

If notification to affected individuals is required, Legal manages that process.

### Third-party notification

If the incident involves a third-party system or affects third-party data, review contractual obligations for notification. Consult Legal.

### External communication

All external communication about a security incident is managed by Legal and the Communications Lead. Employees must not communicate about incidents externally (including on social media) without authorization.

---

## Phase 6: Eradication and Recovery

**Owner:** IT / Security  
**Goal:** Remove the threat fully and restore systems to a known good state.

### Eradication checklist

- [ ] Root cause confirmed and fully understood
- [ ] All affected systems identified
- [ ] Malware, backdoors, or persistence mechanisms removed and confirmed absent
- [ ] Compromised credentials reset across all affected accounts and systems
- [ ] Unauthorized access paths closed
- [ ] Vulnerability that enabled the incident remediated or mitigated

**Do not proceed to recovery until eradication is confirmed.** Recovering systems before eradication is complete risks reinfection or continued unauthorized access.

### Recovery checklist

- [ ] Affected systems restored from clean backups or rebuilt where necessary
- [ ] Recovery validated - systems confirmed operational and clean
- [ ] Monitoring increased on recovered systems for a defined period
- [ ] Users notified that access has been restored
- [ ] Business operations confirmed normal
- [ ] Incident status updated to Resolved

---

## Phase 7: Post-Incident Review

**Owner:** Incident Lead  
**Timeline:** Within 2 weeks of incident closure for P1/P2. Within 1 month for P3.

A post-incident review is not a blame exercise. It is a structured process to identify what can be improved.

### Review questions

- What happened, in summary?
- Was the detection timely? If not, why not?
- Was the response effective? What slowed it down?
- Was communication clear and well-timed? What could have been better?
- What was the root cause?
- What would have prevented this incident?
- What controls, processes, or behaviors need to change as a result?

### Output

A brief written summary covering:

- Timeline of events
- Root cause
- Impact (systems affected, data involved, business disruption)
- Lessons learned
- Action items with owners and target dates

Action items are tracked to completion. The incident is not fully closed until material action items are addressed.

---

## Appendix A: Incident Log Template

| Field | Details |
|-------|---------|
| Incident ID | |
| Date/time reported | |
| Reported by | |
| Date/time detected (if different) | |
| Initial severity | |
| Current severity | |
| Incident Lead | |
| Summary | |
| Affected systems / users / data | |
| Containment actions taken (with timestamps) | |
| Investigation findings | |
| Notification actions taken | |
| Eradication actions taken | |
| Recovery actions taken | |
| Date/time resolved | |
| Post-incident review date | |
| Action items | |

---

## Appendix B: Emergency Contact Sheet

[Complete this section with current contacts and review at each playbook revision.]

| Role | Name | Primary contact | Out-of-hours contact |
|------|------|-----------------|----------------------|
| Incident Lead | | | |
| IT / Security | | | |
| Legal / DPO | | | |
| Senior Leadership | | | |
| External IR support (if contracted) | | | |
| Cyber insurance provider (if applicable) | | | |
| Relevant supervisory authority (GDPR) | | | |

---

## Revision history

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | | | Initial version |

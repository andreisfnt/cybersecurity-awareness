# Security Awareness Program Guide

**Version:** 1.0  
**Owner:** [IT Manager / CISO]  
**Last reviewed:** [Date]

---

## Purpose

This guide is for IT leaders and security teams building or improving a security awareness program. It covers program design, content planning, delivery, measurement, and the mistakes most commonly made.

A security awareness program that works changes behavior. A program that does not work produces completion certificates.

---

## Why most awareness programs fail

Before designing a program, it helps to understand why the standard approach - annual training module, phishing simulation, policy acknowledgment - rarely improves security posture:

- **It treats employees as the problem.** Employees are not the problem. They are the last line of defense in a system that has already failed. Awareness programs that lead with blame produce resentment, not behavior change.
- **Annual training is not learning.** A 45-minute module completed once a year is forgotten within weeks. Retention requires repetition, relevance, and reinforcement.
- **Generic content does not land.** Employees in finance face different threats than engineers. A one-size-fits-all program misses both.
- **No feedback loop.** Programs that track completion but not behavior change have no basis for improvement.

Effective security awareness is closer to internal communications and culture change than to compliance training.

---

## Program design

### Step 1: Understand your threat landscape

Before choosing topics, understand what threats are actually relevant to your organization and your employees' roles. Sources include:

- Your own incident history - what has actually happened or nearly happened
- Industry threat reports relevant to your sector
- Input from IT and security teams on what they observe
- Feedback from employees on what they find confusing or uncertain

Do not build a program around generic cybersecurity topics. Build it around the threats your people will actually encounter.

### Step 2: Segment your audience

Different employee groups face different risks and need different content:

| Group | Typical focus areas |
|-------|-------------------|
| All employees | Phishing, social engineering, password hygiene, physical security, incident reporting |
| Finance and accounts | Business email compromise, payment fraud, invoice manipulation |
| HR and people teams | Personal data handling, recruitment-related social engineering |
| Engineering and technical teams | Secure development practices, credential management, supply chain risk |
| Leadership and executives | Targeted phishing (spear phishing, whaling), travel security, high-value account protection |
| IT and security teams | Privileged access risks, insider threat awareness, operational security |

### Step 3: Define your content calendar

Distribute content across the year rather than concentrating it in a single module. A practical structure:

| Frequency | Format | Purpose |
|-----------|--------|---------|
| Monthly | Short communication (email, intranet post, newsletter item) | Maintain awareness, cover specific topics |
| Quarterly | Phishing simulation | Test and reinforce phishing recognition |
| Quarterly | Team briefing or lunch-and-learn (optional) | Deeper engagement, Q&A opportunity |
| Annually | Formal training module | Baseline compliance requirement, policy acknowledgment |
| Event-driven | Targeted communication | After an incident, a near-miss, or an emerging threat |

### Step 4: Choose your channels

Use the channels employees already use. If the organization communicates primarily through a messaging platform, that is where awareness content belongs - not a separate portal that requires a separate login.

Effective channels include:
- Organization-wide communication channels (email, messaging platforms)
- Intranet or internal knowledge base
- Team meetings (brief, relevant updates from managers)
- Onboarding process for new employees
- Posters and physical signage in office environments (for physical security topics)

---

## Content principles

### Keep it short

Employees will engage with content that respects their time. A 3-minute read or a 2-minute video outperforms a 40-minute module for most awareness objectives. Save longer formats for formal annual training.

### Use real examples

Industry examples of real attacks - especially those relevant to your sector - are more memorable than abstract descriptions of threat categories. Anonymized examples from your own incident history are even more effective.

### Explain the why

Employees who understand why a behavior matters are more likely to maintain it than employees who have been told what to do. "Lock your screen because an unlocked device in a shared space is an easy way for someone to access your email and impersonate you" is more effective than "always lock your screen."

### Make the right thing easy

Behavioral change is easier when the secure option is the convenient option. Awareness content should include clear, practical guidance on what to do - not just what not to do.

### Normalize reporting

One of the most important behaviors to reinforce is incident reporting. Employees who are afraid to report a mistake (clicking a phishing link, losing a device) delay the response and increase the impact. Make it clear that reporting early is always the right call and will not result in blame.

---

## Phishing simulations

Phishing simulations are a useful tool when used correctly. When used incorrectly, they damage trust and do not improve security.

### What works

- Simulations that are followed immediately by brief, constructive education for employees who clicked
- Treating results as organizational data (where are the gaps?) rather than individual performance data
- Varying simulation complexity - not all simulations should be easy or hard
- Increasing sophistication gradually as the baseline improves
- Sharing aggregate results with leadership and managers as a measure of program effectiveness

### What does not work

- Naming and shaming employees who clicked
- Using simulation results in performance reviews
- Running simulations without any follow-up education
- Simulations that are so obviously fake they provide no useful signal
- Simulations that exploit trust inappropriately (fake HR emails about salary reviews, fake IT security alerts about active incidents)

Frequency: quarterly is a reasonable cadence for most organizations. Monthly is appropriate for high-risk environments or during an intensive improvement phase.

---

## Measuring effectiveness

Completion rates measure compliance with training requirements. They do not measure whether the program is working.

Metrics that indicate actual effectiveness:

| Metric | What it tells you |
|--------|-----------------|
| Phishing simulation click rate over time | Whether phishing recognition is improving |
| Phishing simulation reporting rate | Whether employees are comfortable reporting suspicious emails |
| Incident report volume from employees | Whether employees are recognizing and reporting real threats |
| Time to report incidents | Whether reporting friction is being reduced |
| Policy violation rate (where measurable) | Whether behavior is changing |
| Employee feedback on content relevance and quality | Whether the program is landing |

Review these metrics at least quarterly and use them to adjust content and delivery.

---

## Common topics to include across the year

This is not an exhaustive list - prioritize based on your threat landscape assessment.

### Phishing and social engineering
- How to recognize phishing emails, SMS, and voice calls
- What to do when you suspect a phishing attempt (report, do not click)
- Why social engineering works and how attackers build pretexts
- Business email compromise - what it looks like and why it is effective
- QR code phishing (quishing) - attackers embed malicious URLs in QR codes sent by email or placed physically, bypassing email link-scanning filters; employees should treat unexpected QR codes with the same skepticism as links
- Telephone-oriented attack delivery (TOAD) - emails instruct the recipient to call a phone number rather than click a link; the call connects to a fraudster who completes the social engineering by voice; the pattern is often disguised as a subscription renewal, support alert, or security notification
- AI-generated spear phishing - AI tools allow attackers to craft highly personalized emails at scale using publicly available information about the target; messages may reference real colleagues, projects, or recent events and no longer carry the spelling and grammar errors that traditionally signaled phishing
- Deepfake voice and video impersonation - attackers use AI-generated audio or video to impersonate executives or colleagues in calls and video meetings; any unexpected request for urgent financial action or credential sharing should be verified through a separate, trusted channel regardless of how legitimate the caller appears

### Password and authentication security
- Why password reuse is dangerous
- How to use a password manager effectively
- What multi-factor authentication protects against and why it matters
- MFA fatigue (push bombing) - attackers who have obtained a password will repeatedly send MFA push notifications hoping the employee approves one out of frustration or confusion; employees should never approve an MFA request they did not initiate and should report unexpected MFA prompts immediately
- How to respond if you suspect an account has been compromised

### Physical security
- Clean desk and clear screen practices
- Tailgating and physical access controls
- Working in public spaces safely
- Secure disposal of printed sensitive documents

### Data handling
- What the organization's data classification levels mean in practice
- What data should and should not be shared externally
- How to handle sensitive information in email and messaging tools
- Personal data handling obligations under GDPR

### Incident reporting
- What counts as a security incident (err on the side of reporting)
- How to report an incident (clear, simple process)
- What happens after a report is made
- Why early reporting is always better than delayed reporting

### Remote and travel security
- Home network security basics
- Working safely on public Wi-Fi
- Physical security of devices while traveling
- Additional risks in high-risk travel destinations

---

## New employee onboarding

Security awareness should begin before an employee's first day, not six months in when their annual training falls due.

Onboarding security content should include:

- Overview of the organization's security policies (acceptable use, data handling)
- How to recognize and report a phishing attempt
- Password and authentication requirements
- Incident reporting process (who to contact, what to report)
- Physical security expectations

Keep onboarding security content brief - the goal is to establish baseline behavior, not to deliver the entire awareness program in one session.

---

## Program ownership and governance

The security awareness program should have:

- A named owner responsible for content, delivery, and measurement
- Leadership sponsorship - programs that are visibly supported by senior leaders have better engagement
- An annual review to assess effectiveness and update content for the current threat landscape
- A budget - effective programs require investment in content, tools, and time

---

## Appendix: Awareness program health check

Use this to assess the current state of your program:

- [ ] Program content is based on real threats relevant to the organization, not generic topics
- [ ] Content is distributed throughout the year, not concentrated in a single annual module
- [ ] Different employee groups receive content relevant to their specific risks
- [ ] Phishing simulations are followed by constructive education, not blame
- [ ] Employees know how to report a suspected incident and are encouraged to do so
- [ ] Program effectiveness is measured beyond completion rates
- [ ] Program content is reviewed and updated at least annually
- [ ] Senior leadership visibly supports and participates in the program
- [ ] New employees receive security awareness content as part of onboarding
- [ ] The program has a named owner and allocated budget

# Network and Wi-Fi Security Policy

**Document reference:** [POL-SEC-NET-001]  
**Version:** 1.0  
**Effective date:** [Date]  
**Review date:** [Date - recommend annual]  
**Owner:** [IT Manager / CISO]  
**Approved by:** [Name and title]  
**Classification:** Internal

---

## 1. Purpose

This policy establishes rules for the secure use of [Organization name]'s network infrastructure and wireless networks, and for employee behavior when accessing organizational systems from external networks. It protects the organization's network from unauthorized access, data interception, and network-borne threats.

---

## 2. Scope

This policy applies to:

- All employees, contractors, and third parties using organizational network infrastructure
- All devices connected to organizational networks, whether organization-owned or personal
- Use of organizational systems over external networks (public Wi-Fi, home networks, mobile data)
- All network access points operated by or on behalf of [Organization name]

---

## 3. Network access

### 3.1 Authorization

Access to the organizational network is granted based on role and business need. Employees must not:

- Connect unauthorized devices to the organizational network without IT approval
- Share network access credentials or Wi-Fi passwords with unauthorized individuals
- Extend organizational network access beyond the physical premises without IT authorization (e.g., via personal hotspots, network bridging)

### 3.2 Network segments

[Organization name] maintains separate network segments for different purposes. Employees must use only the segment appropriate to their role and device:

| Segment | Purpose | Who can connect |
|---------|---------|----------------|
| Corporate network | Organization-owned managed devices, business systems | Managed devices with valid credentials |
| Guest network | Visitors and personal devices not enrolled in device management | Guests, personal devices for internet access only |
| [Other segments, e.g., IoT, lab, production] | [Purpose] | [Authorized users only] |

Attempts to access network segments beyond your authorization are prohibited.

---

## 4. Wireless (Wi-Fi) network

### 4.1 Corporate Wi-Fi

The corporate Wi-Fi network is for business use by authorized employees on managed devices. Requirements:

- Access requires authentication with organizational credentials
- Personal devices may not connect to the corporate Wi-Fi unless enrolled and approved under the BYOD policy
- Do not share corporate Wi-Fi credentials with visitors or unauthorized individuals

### 4.2 Guest Wi-Fi

The guest network is available for visitors and for personal device internet access. Users of the guest network:

- Have no access to internal organizational systems or resources
- Are subject to acceptable use monitoring
- Must not use the guest network to attempt to access internal systems

### 4.3 Unauthorized access points

Employees must not install personal routers, wireless access points, or range extenders on the organizational network. Unauthorized access points create unmonitored entry points to the network.

If coverage gaps exist, report them to IT.

---

## 5. Remote access

### 5.1 VPN

Employees requiring access to internal organizational systems from outside the office must use the organizationally provisioned VPN or approved remote access solution. Requirements:

- VPN access requires multi-factor authentication
- VPN credentials must not be shared
- The VPN must be active when accessing internal systems remotely
- Split tunneling configurations are managed by IT - employees must not modify VPN configurations

### 5.2 Home network security

Employees working from home are responsible for maintaining a reasonable level of security on their home network:

- Home router firmware should be kept up to date
- Default router admin credentials must be changed
- Wi-Fi should use WPA2 or WPA3 encryption
- Employees should be aware that other devices on the home network share the same connection

IT does not manage home network equipment, but may provide guidance on baseline security.

---

## 6. Public Wi-Fi

Employees must apply additional caution when connecting to public or untrusted Wi-Fi networks (hotels, airports, coffee shops, conference venues):

- Connect to organizational systems using the organizational VPN whenever on public Wi-Fi
- Avoid accessing sensitive organizational data on public Wi-Fi without VPN active
- Be aware that public networks may be monitored or subject to interception
- Do not connect to Wi-Fi networks with generic or suspicious names (e.g., "Free_Airport_WiFi", networks mimicking hotel or venue names)
- Use mobile data as an alternative to public Wi-Fi for sensitive work where VPN is unavailable

---

## 7. Network monitoring

[Organization name] monitors network traffic for security purposes. This includes:

- Traffic volume and patterns
- Connections to known malicious destinations
- Unauthorized devices or access attempts
- Anomalous behavior indicative of compromise or policy violation

Network monitoring covers all traffic on organizational networks. Employees should have no expectation of privacy on organizational networks.

---

## 8. Prohibited activities on organizational networks

The following activities are prohibited on all organizational networks:

- Network scanning, enumeration, or reconnaissance tools without explicit IT authorization
- Attempting to intercept or capture network traffic (packet sniffing)
- Attempting to access systems or resources beyond authorized scope
- Installing or running services that listen on the network without IT authorization
- Attempting to bypass network security controls, proxy filters, or content restrictions
- Cryptocurrency mining or other resource-intensive personal activities
- Connecting unauthorized devices, switches, access points, or network equipment

---

## 9. Incident reporting

Employees must report to IT immediately if they:

- Suspect their network credentials have been compromised
- Observe unusual network behavior (unexpected slowness, blocked access, unusual prompts)
- Connect to an unauthorized or suspicious network while carrying organizational data
- Discover an unauthorized device connected to the organizational network

---

## Revision history

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | | | Initial version |

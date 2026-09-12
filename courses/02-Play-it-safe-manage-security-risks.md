# Course 2: Play It Safe: Manage Security Risks

## Reading: The Eight CISSP Security Domains

### Summary
An organization's security posture (its ability to defend assets and adapt to change) is shaped by eight interconnected domains defined by CISSP. Together they cover governance, physical/data protection, network security, access control, testing, operations, and secure software development.

### The 8 Domains
1. **Security and risk management** – covers security goals, risk mitigation, compliance, business continuity, legal regulations, and ethics. Ties into InfoSec practices like incident response, vulnerability management, cloud/application security.
2. **Asset security** – managing storage, maintenance, retention, and destruction of physical and digital assets; backups and recovery planning reduce exposure if assets are compromised.
3. **Security architecture and engineering** – building the tools/processes that protect assets, guided by principles like least privilege, defense in depth, zero trust, and shared responsibility.
4. **Communication and network security** – securing on-site, remote, and cloud networks, including controlling external/remote access.
5. **Identity and access management (IAM)** – authenticating identities and authorizing access using least privilege, so only the right people can reach the right data.
6. **Security assessment and testing** – running security audits and penetration tests to find and fix vulnerabilities before attackers do.
7. **Security operations** – investigating breaches and preventing future ones through training, logging, SIEM tools, incident management, and post-incident review.
8. **Software development security** – embedding security into every stage of the software development lifecycle rather than treating it as an afterthought.

---

## Reading: Risk Management Basics

### Summary
Organizations protect **assets** (anything of value — digital or physical) using recognized risk frameworks such as **NIST RMF** and **HITRUST**.

### Risk Response Strategies
- **Acceptance** – tolerate the risk to avoid disrupting operations
- **Avoidance** – build a plan to sidestep the risk entirely
- **Transference** – shift the risk to a third party (e.g., insurance/vendor)
- **Mitigation** – reduce the impact of a known risk

### Threats, Risks & Vulnerabilities
- **Threat** – any event/circumstance that could harm assets (e.g., insider threats, advanced persistent threats/APTs)
- **Risk** – anything that could affect confidentiality, integrity, or availability; roughly *risk = likelihood of a threat*
- **Vulnerability** – a weakness a threat can exploit

Risk factors include external risk (outside actors), internal risk (employees/vendors), legacy systems (outdated, forgotten tech), multiparty risk (third-party vendor access), and software compliance/licensing gaps.

Notable named vulnerabilities: **ProxyLogon**, **ZeroLogon**, **Log4Shell**, **PetitPotam** — plus systemic issues like poor logging/monitoring and server-side request forgery. OWASP's Top 10 list evolves over time (e.g., 2017→2021 added *insecure design*, *software/data integrity failures*, and *SSRF* as new categories), which is a reminder that security threats constantly change.

---

## Reading: Frameworks and Controls

### Summary
**Security frameworks** are guidelines for building risk-mitigation plans and staying compliant with laws (e.g., HIPAA in healthcare). **Security controls** are the actual safeguards used to reduce specific risks (e.g., requiring MFA to stay HIPAA-compliant).

### Named Frameworks
- **Cyber Threat Framework (CTF)** – a shared vocabulary (from the U.S. government) for describing cyber threat activity, making it easier for teams to communicate and respond.
- **ISO/IEC 27001** – an internationally recognized standard for managing information security across assets like financial data, IP, and employee records.

### Control Types
- **Physical** – gates, locks, guards, CCTV, access badges
- **Technical** – firewalls, MFA, antivirus software
- **Administrative** – separation of duties, authorization policies, asset classification

### The CIA Triad
- **Confidentiality** – only authorized users can access data (supported by least privilege)
- **Integrity** – data is accurate, authentic, and untampered (supported by cryptography/encryption)
- **Availability** – authorized users can access data when they need it

### OWASP Security Principles
Core: minimize attack surface, least privilege, defense in depth, separation of duties, keep security simple, fix issues at the root cause.
Additional: establish secure defaults, fail securely, don't automatically trust third-party services, avoid relying on secrecy for security ("security by obscurity").

---

## Reading: Security Audits

### Summary
A **security audit** is an independent review of an organization's controls, policies, and procedures against internal and external standards (laws, regulations, best practices). Audits confirm whether IT practices meet expectations and highlight what needs remediation.

### What Affects an Audit
Industry type, organization size, applicable government regulations, geographic location, and voluntary compliance choices.

### Audit Checklist Steps
1. Identify the scope (which assets, how often, which policies to check)
2. Complete a risk assessment
3. Conduct the audit
4. Create a mitigation plan
5. Communicate results to stakeholders

Frameworks like **NIST CSF** and **ISO 27000** help organizations prepare for audits faster by giving them a pre-built structure to measure against.

---

## Reading: SIEM Tools, Open-Source vs Proprietary, and Playbooks

### SIEM (Security Information and Event Management)
SIEM tools collect and analyze log data in real time to flag potential threats, though they still require human analysis. They're evolving toward **cloud-hosted** and **cloud-native** models, and increasingly pair with **SOAR** (Security Orchestration, Automation, and Response) tools, which automate repetitive responses (e.g., auto-locking an account after repeated failed logins) so analysts can focus on complex incidents.

### Open-Source vs Proprietary Tools
- **Open-source** (e.g., Linux, Suricata) – free, publicly maintained, highly customizable; wide visibility can actually make vulnerabilities easier to catch and fix.
- **Proprietary** (e.g., Splunk, Google SecOps/Chronicle) – owned by a company, paid, limited customization, updates controlled by the vendor.

### Splunk Dashboards
- **Security posture** – last 24 hours of notable events
- **Executive summary** – overall organizational health over time
- **Incident review** – timeline and patterns around a specific incident
- **Risk analysis** – risk scoring per object (user, computer, IP)

### Chronicle Dashboards
- **Enterprise insights** – recent alerts and indicators of compromise (IOCs)
- **Data ingestion and health** – log source volume and success rates
- **IOC matches** – top threats/trends across IPs, domains, devices
- **Main dashboard** – high-level summary of ingestion, alerts, and events
- **Rule detections** – stats on alerts triggered by specific detection rules
- **User sign-in overview** – unusual sign-in activity across the org

### Playbooks
A **playbook** is a living, regularly-updated manual of predefined steps for responding to an incident. Common stages: preparation → detection → analysis → containment → eradication → recovery → post-incident review. Playbooks are used alongside SIEM (to interpret flagged activity) and SOAR (to guide analysts after automated actions trigger).

---

## Key Takeaways
- The 8 CISSP domains give a full map of what "security" covers, from governance to secure coding.
- Risk = likelihood of a threat; controls and frameworks work together to lower that likelihood.
- The CIA triad (confidentiality, integrity, availability) underlies almost every security decision.
- Audits, SIEM/SOAR tools, and playbooks are the practical, day-to-day mechanisms analysts use to monitor and respond to risk.
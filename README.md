# End-to-End GRC Analyst Experience – SecureTech Skillternship
Hands-on GRC Skillternship project focused on risk assessments, regulatory compliance (PCI DSS, HIPAA, GDPR), governance reviews, audits, policy development, and executive reporting—demonstrating applied GRC Analyst responsibilities at SecureTech Solutions.

# Governance, Risk & Compliance Lifecycle Execution

In this project, I executed the role of a GRC Analyst from inception to completion.

_**Inception State:**_ Launched the project by identifying organizational risks, mapping regulatory requirements, establishing a governance baseline, and defining the scope of risk and compliance initiatives.

_**Completion State:**_  Closed the project by conducting audits, refining governance structures and security policies, compiling risk/compliance reports, and delivering actionable insights to enhance organizational alignment and resilience.

---

<img width="1000" alt="image" src="https://cdn.azeusconvene.com/wp-content/uploads/Banner-Image_Convene_What-is-GRC-A-Guide-to-Leveraging-GRC-for-Effective-ESG-Strategy.jpg">

# Technology Utilized
Microsoft Excel / Google Sheets – for risk registers, audit tracking, and compliance matrices

Microsoft Word / Google Docs – for drafting policies, meeting notes, and documentation

Microsoft Outlook – for professional communication and meeting coordination

PowerPoint / Google Slides – for training presentations and executive reporting

Risk Management Frameworks – NIST RMF, NIST 800-53, NIST CSF

Compliance Standards – PCI DSS, HIPAA, GDPR

Ticketing/Workflow Tools – (e.g., ServiceNow, JIRA)

File Storage – SharePoint / Google Drive for version control and policy access

---


# Table of Contents

- [Meeting Request Email](#meeting-request-email)
- [Meeting Agenda](#)


---

### Step 1) Initiating Cross-Functional Collaboration
## Meeting Request Email
To kick off the project, I drafted a professional meeting request email to SecureTech’s IT and Legal teams. This demonstrated proactive communication and simulated real-world collaboration to align technical and legal perspectives on data protection training and identity access management (IAM).

#meeting-request-email

<img src="https://i.imgur.com/Bu6uvEC.png" alt="image" width="1000">
---

### Step 2) Structuring the Collaborative Discussion

To ensure an efficient and productive meeting, I created a detailed agenda outlining key technical and legal discussion points. This agenda was designed to align IT and Legal stakeholders on data protection or IAM strategy, clarify responsibilities, and drive actionable outcomes for policy and training improvements.

# Meeting Agenda


<img src="https://i.imgur.com/4X7zwoh.png" alt="image" width="1000">

---

### Step 3) Policy Finalization and Senior Leadership Sign-Off

After gathering feedback from the server team, the policy is revised, addressing aggressive remediation timelines. With final approval from upper management, the policy now guides the program, ensuring compliance and reference for pushback resolution.  
[Finalized Policy](https://docs.google.com/document/d/1rvueLX_71pOR8ldN9zVW9r_zLzDQxVsnSUtNar8ftdg/edit?usp=drive_link)
<div style="text-align: center;">
    <img src="https://github.com/user-attachments/assets/9afcdbc1-0493-4af2-9287-1cb9b8f59b40" alt="image" width="400">
</div>

---

### Step 4) Mock Meeting: Initial Scan Permission (Server Team)

The team collaborates with the server team to initiate scheduled credential scans. A compromise is reached to scan a single server first, monitoring resource impact, and using just-in-time Active Directory credentials for secure, controlled access.  


# Scheduled Credential Scans Discussion - Transcript

**Josh:**  
Morning Jimmy.

**Jimmy:**  
Good morning. I heard you’re ready to conduct some scans?

**Josh:**  
Yep. Now that our vulnerability management policy is in place, I wanted to get started on conducting some scheduled credential scans of your environment.

**Jimmy:**  
Sounds good to me. What’s involved? How can we help?

**Josh:**  
We’re planning to schedule weekly scans of the server infrastructure.  
We estimate it’ll take about 4 to 6 hours to scan all 200 assets.  
We’ll need you to provide some administrative credentials, which will allow the scan engine to remotely log into the targets and better assess them.

**Jimmy:**  
Whoa, whoa—hold on there. What does scanning actually entail? I’m a bit worried about resource utilization.  
Also, you want admin credentials to all 200 machines? That doesn’t sound safe.

**Josh:**  
Those are valid concerns.  
The scan engine sends different types of traffic to the servers to check for the existence of certain vulnerabilities.  
That includes looking into the registry, checking for outdated software, and identifying insecure protocols or cipher suites—so that’s why credentials are required.

**Jimmy:**  
I see. Well, as long as it doesn’t bring the servers offline, I guess we should be okay.

**Josh:**  
Absolutely. Let’s just scan a single server for now and keep an eye on resource utilization.

**Jimmy:**  
Not a bad idea.

**Josh:**  
Great. Also, for the credentials—can you set up something in Active Directory for us?  
Maybe create Active Directory credentials and leave them disabled until we’re ready to scan.  
Then enable them during the scan and disable or deprovision the account afterward. Kind of like a just-in-time access setup.

**Jimmy:**  
That sounds good. I’ll ask Susan to get started on the automation for the account provisioning.

**Josh:**  
Awesome. Okay—talk soon.

**Jimmy:**  
Yeah, that sounds good. I’ll get back to you once the credentials are set up.

**Both:**  
See you later.


---

### Step 5) Initial Scan of Server Team Assets

In this phase, an insecure Windows Server is provisioned to simulate the server team's environment. After creating vulnerabilities, an authenticated scan is performed, and the results are exported for future remediation steps.  

<img width="635" alt="image" src="https://github.com/user-attachments/assets/937cccbd-36bb-4445-97b9-e915085cda81" style="border: 2px solid black;">

[Scan 1 - Initial Scan](https://drive.google.com/file/d/1RBPVj_azKJMwmRZ8QILlb4hxIjQU3wQ7/view?usp=drive_link)




---

### Step 6) Vulnerability Assessment and Prioritization

We assessed vulnerabilities and established a remediation prioritization strategy based on ease of remediation and impact. The following priorities were set:

1. Third Party Software Removal (Wireshark)
2. Windows OS Secure Configuration (Protocols & Ciphers)
3. Windows OS Secure Configuration (Guest Account Group Membership)
4. Windows OS Updates

---

### Step 7) Distributing Remediations to Remediation Teams

The server team received remediation scripts and scan reports to address key vulnerabilities. This streamlined their efforts and prepared them for a follow-up review.  

<img width="635" alt="image" src="https://github.com/user-attachments/assets/bbf9478f-e1d1-4898-846e-b510ec8c6f72">

[Remediation Email](https://github.com/joshmadakor1/lognpacific-public/blob/main/misc/remediation-email.md)

---

### Step 8) Mock Meeting: Post-Initial Discovery Scan (Server Team)

The server team reviewed vulnerability scan results, identifying outdated software, insecure accounts, and deprecated protocols. The remediation packages were prepared for submission to the Change Control Board (CAB). 


# 🛡️ Vulnerability Management Meeting Notes  
**Date:** April 14, 2025  
**Participants:**  
- Jimmy (Security Engineer)  
- Kyler Williams (Cybersecurity Support Analyst)  

---

## 🧠 Summary

- ✅ No performance or service disruption during the vulnerability scan.  
- ⚠️ Multiple vulnerabilities found due to:
  - Outdated software (e.g., **Wireshark**)
  - Misconfigured user permissions
  - Deprecated protocols and cipher suites

---

## 🔍 Key Findings

- **Wireshark** is severely outdated on several servers.  
- The **Guest account** is a member of the **local Administrators group** — a major security risk.  
- **TLS 1.0/1.1** and **medium-strength cipher suites** are enabled and need to be disabled.  
- A **self-signed certificate** is present — expected, low risk.  
- Some **Microsoft Edge Chromium** vulnerabilities may already be patched via Windows Update.  
- Server configurations appear **uniform**, suggesting a streamlined remediation process.

---

## 🛠️ Action Items

- ❌ Uninstall **Wireshark** from all affected servers  
- 🔐 Remove **Guest** from the **Administrators** group  
- 🔧 Disable **TLS 1.0/1.1** and weak ciphers  
- 🔄 Verify Windows Update is patching Edge and OS vulnerabilities  
- 💻 Create **PowerShell remediation scripts/packages**  
- 📝 Submit changes to the **Change Control Board (CCB)**

---

## 💬 Conversation Log

> **Jimmy:** Morning Jimmy how are you doing?  
> **Kyler:** Not bad for a Monday. And yourself?  
> **Jimmy:** I'm still alive so I can't complain. But before we get into the vulnerabilities, how did the actual scan go on your end?  
> **Kyler:** The scan went well. We were monitoring them and aside from all the open connections, we would have never known a scan was taking place.  
> **Jimmy:** Yeah, that's good news. I kind of expected that much. We can keep monitoring going forward but I don't expect we'll have any issues with resource utilization. Do you mind if I dive into the vulnerability findings?  
> **Kyler:** Yeah absolutely.  
> **Jimmy:** Cool. So basically, the majority of these vulnerabilities come from Wireshark being installed. You can see all these Wireshark ones—it’s just super out of date.  
> One interesting thing I did find is that the local **Guest account** belongs to the **Administrators group**. I'm not sure why that is.  
> Also, some of these might be automatically resolved by Windows Updates—like this Microsoft Edge Chromium one.  
> The self-signed certificate one we don’t have to worry about—it’s just the computer's default cert.  
> But the TLS 1.1 and 1.0 protocols and medium-strength cipher suites should be addressed.  
> So we’re mainly looking at: Wireshark, the protocols/cipher suites, and the guest account.  
> **Kyler:** Very interesting. The good news is I suspect most of our servers are going to have the same vulnerabilities—hopefully that makes things easier during remediation.  
> **Jimmy:** Yeah, that's actually good news. A uniform loadout. Do you foresee any issues with remediating any of these specifically?  
> **Kyler:** I highly doubt there will be any issues. We’ll run it through the next Change Control Board. Uninstalling Wireshark and fixing the guest account shouldn’t be a problem.  
> **Jimmy:** I’ll go ahead and get started on building out some remediation packages for you to kind of make your life easier.  
> **Kyler:** That sounds great. Oh, one question—do you have anything in place to fix the Windows Update-related vulnerabilities?  
> **Jimmy:** Oh yes, Windows Update is already handled. We’ve got patch management set up.  
> **Kyler:** Perfect. I’ll get started on researching and planning the remediations and I’ll follow up before the next Change Control Board.  
> **Jimmy:** Sounds good, talk to you soon.  
> **Kyler:** Cool cool, talk to you soon.

---

## 💡 Skills Demonstrated

- ✅ Vulnerability triage and analysis  
- ✅ Collaboration with senior security staff  
- ✅ Remediation planning and execution prep  
- ✅ Change Control Board process familiarity  
- ✅ PowerShell scripting for automation  
- ✅ Patch management verification  


---

### Step 9) Mock CAB Meeting: Implementing Remediations

The Change Control Board (CAB) reviewed and approved the plan to remove insecure protocols and cipher suites. The plan included a rollback script and a tiered deployment approach.  


# Vulnerability Remediation Discussion – CAP Meeting Summary

### Key Topics:
- Removal of insecure protocols
- Removal of insecure cipher suites

---

**Speaker 1:**  
Next up on the list are a couple of vulnerability remediations for the server team:  
1. Removal of insecure protocols  
2. Removal of insecure cipher suites  

Josh from the Risk Department is working in conjunction with Jimmy from Infrastructure on this.

---

**Jimmy:**  
Normally I would walk through the technical aspects, but Josh actually built the solution for us and is more familiar. We're still getting used to the process.

---

**Josh:**  
Sure, I can explain.  
Insecure cipher suites and protocols on a system mean it's capable of negotiating and using deprecated algorithms. If it connects to a server that only supports insecure protocols, it might fall back to using them.

These are managed via the Windows Registry.  
We created a PowerShell script that:

- Disables all insecure protocols and cipher suites
- Enables secure, modern standards

It's a straightforward implementation.

---

**Another Attendee:**  
What if something goes wrong? Do we have a rollback plan?

---

**Josh:**  
Yes, absolutely.

- We’re doing a **tiered deployment**: pilot group → pre-production → full production.
- We also created an **automated rollback script** for each remediation, which restores original registry settings if needed.

---

**Attendee:**  
Got it. Since it's just registry updates, I’m not too concerned.

---

**Josh:**  
Exactly.

---

**Host:**  
Any more questions?  
Great — that wraps things up for this week’s CAP meeting. See you all next week!


---
### Step 10 ) Remediation Effort

#### Remediation Round 1: Outdated Wireshark Removal

The server team used a PowerShell script to remove outdated Wireshark. A follow-up scan confirmed successful remediation.  
[Wireshark Removal Script](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/remediation-wireshark-uninstall.ps1)  

<img width="634" alt="image" src="https://github.com/user-attachments/assets/7b4f9ab2-d230-4458-ac0f-c0ff070ae79a">

[Scan 2 - Third Party Software Removal](https://drive.google.com/file/d/1UiwPPTtuSZKk02hiMyXf31pXUIeC5EWt/view?usp=drive_link)


#### Remediation Round 2: Insecure Protocols & Ciphers

The server team used PowerShell scripts to remediate insecure protocols and cipher suites. A follow-up scan verified successful remediation, and the results were saved for reference.  
[PowerShell: Insecure Protocols Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-protocols.ps1)
[PowerShell: Insecure Ciphers Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-cipher-suites.ps1)

<img width="630" alt="image" src="https://github.com/user-attachments/assets/0e96120d-8ec9-4f76-8e42-79c752200010">

[Scan 3 - Ciphersuites and Protocols](https://drive.google.com/file/d/1Qc6-ezQvwReCGUZNtnva0kCZo_-zW-Sm/view?usp=drive_link)


#### Remediation Round 3: Guest Account Group Membership

The server team removed the guest account from the administrator group. A new scan confirmed remediation, and the results were exported for comparison.  
[PowerShell: Guest Account Group Membership Remediation](https://github.com/joshmadakor1/lognpacific-public/blob/main/automation/toggle-guest-local-administrators.ps1)  

<img width="627" alt="image" src="https://github.com/user-attachments/assets/870a3eac-3398-44fe-91c0-96f3c2578df4">

[Scan 4 - Guest Account Group Removal](https://drive.google.com/file/d/1jVgikjfrV1YjOcL3QRT_oUB0Y82w22V7/view?usp=drive_link)


#### Remediation Round 4: Windows OS Updates

Windows updates were re-enabled and applied until the system was fully up to date. A final scan verified the changes  

<img width="627" alt="image" src="https://github.com/user-attachments/assets/870a3eac-3398-44fe-91c0-96f3c2578df4">

[Scan 5 - Post Windows Updates](https://drive.google.com/file/d/1tmDjeHl5uiGitRwWy8kFRi33q-nGi1Zt/view?usp=drive_link)

---

### First Cycle Remediation Effort Summary

The remediation process reduced total vulnerabilities by 80%, from 30 to 6. Critical vulnerabilities were resolved by the second scan (100%), and high vulnerabilities dropped by 90%. Mediums were reduced by 76%. In an actual production environment, asset criticality would further guide future remediation efforts.  

<img width="1920" alt="image" src="https://github.com/user-attachments/assets/51f0aae8-7f36-4d90-b29f-5257e57155f9">

[Remediation Data](https://docs.google.com/spreadsheets/d/1FTtFfZYmFsNLU6pm8nTzsKyKE-d2ftXzX_DPwcnFNfA/edit?gid=0#gid=0)

---

### On-going Vulnerability Management (Maintenance Mode)

After completing the initial remediation cycle, the vulnerability management program transitions into **Maintenance Mode**. This phase ensures that vulnerabilities continue to be managed proactively, keeping systems secure over time. Regular scans, continuous monitoring, and timely remediation are crucial components of this phase. (See [Finalized Policy](https://docs.google.com/document/d/1rvueLX_71pOR8ldN9zVW9r_zLzDQxVsnSUtNar8ftdg/edit?usp=drive_link) for scanning and remediation cadence requirements.)

Key activities in Maintenance Mode include:
- **Scheduled Vulnerability Scans**: Perform regular scans (e.g., weekly or monthly) to detect new vulnerabilities as systems evolve.
- **Patch Management**: Continuously apply security patches and updates, ensuring no critical vulnerabilities remain unpatched.
- **Remediation Follow-ups**: Address newly identified vulnerabilities promptly, prioritizing based on risk and impact.
- **Policy Review and Updates**: Periodically review the Vulnerability Management Policy to ensure it aligns with the latest security best practices and organizational needs.




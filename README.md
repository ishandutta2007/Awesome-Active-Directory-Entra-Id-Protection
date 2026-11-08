# Awesome-Active-Directory-Entra-Id-Protection

# Awesome-Active-Directory-Entra-Id-Protection

**Top Active Directory Entra Id Protection (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on AD Forest Recovery, Entra ID Backup, Attack Path Analysis & Self-Hosted Directory Tooling*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Active Directory & Entra ID Protection**. These tools enable organizations to back up, recover, audit, and harden their identity infrastructure—protecting against ransomware, accidental deletion, and privilege escalation—from fully managed enterprise platforms with immutable cyber vaults to open-source PowerShell modules and reconnaissance frameworks that give teams control over their directory security posture.



**Examples** include Semperis Directory Services Protector, Rubrik Identity Resilience, Quest Recovery Manager, ManageEngine Recovery Manager Plus, Netwrix Auditor, Veeam Explorer for AD, Commvault AD Protection, Cohesity Identity Resilience, Cayosoft Administrator, and Druva (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted AD/Entra tooling, backup, and attack path analysis. **Critical note**: True open-source AD protection is anchored by **DSInternals**—the PowerShell module that exposes AD internals for offline recovery, password auditing, and DCSync detection . **BloodHound** dominates attack path analysis , and **Microsoft 365 DSC** provides declarative Entra ID backup . No open-source project matches Semperis' automated forest recovery or Rubrik's five-step wizard, but for auditing, recovery scripting, and attack path discovery, the options are production-proven.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The dedicated Active Directory (AD) protection and Identity Threat Detection and Response (ITDR) market is estimated at **$1.1B to $1.3B** (scaling rapidly toward **$3.8B+** by 2030, embedded within a broader **$5.6B–$16.6B** identity security sector). The market exhibits **moderate concentration**: broad cyber-resilience platforms (Veeam, Rubrik, Cohesity) and hyperscalers anchor foundational enterprise backup, while specialized pure-play vendors (Semperis, Netwrix, Cayosoft) dominate deep forest recovery, attack-path auditing, and directory posture management.

## SaaS/Hosted Platforms

| Company / Product | Company Scale (Valuation / Revenue) | Pricing | Free Tier / Trial Limit | Key Focus & Trade-off |
| :--- | :--- | :--- | :--- | :--- |
| **Veeam Explorer for Active Directory** | **$15B valuation** (~$1.7B ARR; TPG / Insight Partners) | Included with Veeam Universal License (VUL); starts at **$155/instance/year** (sold in 10-packs for $1,550/yr) | **Free-forever plan**: Veeam Community Edition provides free full backup/restore for up to **10 instances (workloads)** indefinitely. | **Best for**: Existing Veeam customers seeking native AD object restore. **Trade-off**: Requires Veeam infrastructure; advanced DR orchestration requires Premium tier. |
| **Rubrik Identity Resilience** | **~$13.9B market cap** (~$888M FY25 revenue; NYSE: RBRK) | Foundation Edition for SaaS / M365 starts at **$3.80/user/month** (3-year contract required; enterprise minimums apply) | **30-day free trial**: Available upon request for targeted workloads (e.g., Salesforce sandbox / M365 backup) and customized enterprise PoC. | **Best for**: Large enterprises needing tamper-resistant monitoring and 5-step forest recovery. **Trade-off**: High multi-year enterprise minimums. |
| **Cohesity Identity Resilience** | **~$8B valuation** (~$1.7B pro forma revenue post-Veritas merger) | DataProtect DPaaS starts at **$29,100/year** for 10 BETB (~$2,900/TB/yr); software subscription from **$150–$400/TB/year** | **30-day free trial**: Unrestricted trial available for Cohesity Data Cloud / DataProtect as a Service upon registration. | **Best for**: Cohesity/Veritas customers wanting integrated Semperis-powered AD resilience. **Trade-off**: High minimum capacity commitments (typically 10 TB BETB or 3-node cluster). |
| **Commvault AD Protection** | **~$6.6B market cap** (~$995.6M FY25 revenue; NASDAQ: CVLT) | SaaS Microsoft 365 / Identity backup starts at **$1.70/user/month** (Standard) to **$4.50/user/month** (Enterprise); infrastructure backup from **$58.50/TB/month** | **30-day free trial**: Commvault Cloud offers a fully functional 30-day trial covering hybrid cloud workloads and SaaS identity without credit card. | **Best for**: Enterprises consolidating directory, cloud, and SaaS backup on one platform. **Trade-off**: Broad platform footprint required for full directory recovery suite. |
| **Quest Recovery Manager for Active Directory (RMAD)** | **~$5.4B buyout valuation** (Acquired by Clearlake Capital; >$1B revenue) | Disaster Recovery term license lists at **$48.86/user/year** (CDW-G); maintenance renewal at **$73.80/user/year** | **30-day free trial**: Full-featured 30-day trial for Recovery Manager for Active Directory Disaster Recovery Edition. | **Best for**: Organizations wanting battle-tested AD forest backup and surgical attribute restoration. **Trade-off**: Scales per enabled user account; primarily recovery-focused rather than real-time posture defense. |
| **Druva SaaS Universal License** | **$2B peak valuation** (~$200M+ ARR; backed by Neuberger Berman / Riverwood) | User & SaaS workload backup starts at **$6.80 to $8.00/user/month** (Business to Enterprise); unmanaged infrastructure at custom TB-month rates | **30-day free trial**: 30-day full-access trial for Druva Data Resiliency Cloud with 300 GB pooled storage per user, no credit card required. | **Best for**: Cloud-first organizations consolidating endpoint, M365, and directory protection. **Trade-off**: Per-user pricing scales quickly across large workforces. |
| **Semperis Directory Services Protector (DSP)** | **~$1B valuation** (Surpassed $100M ARR; Series C / KKR) | Custom enterprise subscription based on protected active directory accounts (private offers via Azure Marketplace / Carahsoft NASA SEWP V) | **Free community tool**: Semperis **Purple Knight** is free forever for unlimited AD/Entra/Okta vulnerability scans (paid DSP offers 30-day enterprise proof-of-concept upon request). | **Best for**: Enterprises needing automated ransomware-free AD forest recovery and continuous posture remediation. **Trade-off**: Enterprise sales motion only; private offers tailored to user count. |
| **ManageEngine RecoveryManager Plus** | **~$580M–$600M annual revenue** (IT division of bootstrapped Zoho Corp, ~$1.5B revenue) | AD Standard Edition starts at **$475/year** (includes AMS for 250 objects); M365 backup starts at **$195/year** | **Free-forever plan**: 30-day fully functional trial, which automatically converts to **Free Edition** indefinitely (limited to 1 domain, scheduled backups only, no granular rollback). | **Best for**: SMBs and mid-market teams seeking low-cost, transparent directory and M365 protection. **Trade-off**: Granular object rollback and multi-domain environments require paid tiers. |
| **Netwrix Auditor for AD** | **~$200M+ est. revenue** (ARR grew 5x under TA Associates & Centerbridge Partners) | Essentials tier starts at **$20/enabled AD user + cloud-only Entra ID user/year** (self-service subscription) | **Free-forever plan**: 20-day unrestricted trial, which automatically reverts to **Free Community Edition** indefinitely (daily change summary reports via email). | **Best for**: Audit compliance, change tracking, and spotting unauthorized AD modifications. **Trade-off**: Auditing and posture detection platform, not a disaster recovery or backup restoration tool. |
| **Cayosoft Administrator & Guardian** | **Bootstrapped / $22.5M growth round** (Centana Growth Partners; 76% ARR growth) | Subscription licensing based on total managed directory objects (flat license covering unlimited administrators and servers; custom quote via Carahsoft GSA MAS #47QSWA18D008F) | **Free-forever plan**: Cayosoft Free Edition includes web portal, LAPS access, BitLocker recovery, and Graph PowerShell module; commercial editions offer **25-day free trial**. | **Best for**: Hybrid organizations wanting AD management and forest recovery without per-admin fees. **Trade-off**: Deep forest disaster recovery features reserved for Guardian paid tier. |



## Open-Source GitHub Projects



- **DSInternals**

  **Directory Services Internals PowerShell module and framework** (MIT) — **the most powerful open-source tool for AD recovery and auditing**, with code integrated into commercial disaster recovery products . **Features**: **Bare-metal recovery of domain controllers from IFM backups** (ntds.dit + SYSVOL); **offline ntds.dit manipulation**—hash dumping, password resets, group membership changes, LAPS password decryption, BitLocker recovery key extraction; **online DCSync** via MS-DRSR; **password auditing** against HaveIBeenPwned; **Entra ID FIDO2 key auditing**; **AD-integrated DNS zone extraction** with DNSSEC keys . **Tech stack**: PowerShell, .NET. **Deploy**: `Install-Module DSInternals` (PowerShell Gallery) or Chocolatey . **Trade-off**: **Not supported by Microsoft**—improper use can cause irreversible damage; requires deep AD expertise. **Best for**: AD administrators and incident responders needing offline recovery, credential auditing, and forensic analysis—not a turnkey backup platform.



- **BloodHound**

  **Identity risk management and attack path analyzer** (Apache 2.0) — **the standard open-source tool for AD privilege relationship mapping**. **Features**: **Graph-based attack path analysis**—maps identity relationships and permissions to uncover unintended privilege paths; **adversary emulation framework**; **identifies paths to Domain Admin**; **reverse proxy for MFA bypass emulation**; community-driven collection . **Tech stack**: Go, Neo4j. **Deploy**: Self-hosted (Docker, binary). **Trade-off**: **Analysis tool, not backup/recovery**—it finds attack paths but does not protect or restore AD. **Best for**: security teams auditing AD privilege relationships and hardening identity infrastructure—especially before ransomware can exploit those paths.



- **Microsoft 365 DSC**

  **Declarative configuration management** for Microsoft 365 (open source) — **the most rigorous open-source Entra ID backup method** according to Wavestone's PoC . **Features**: **Export/import Entra ID objects**—users, groups, roles, applications, service principals; **declarative approach**—define desired state rather than steps; **partial recovery**—not all user attributes are restored; passwords are replaced with defaults; active/deactivated state is not captured . **Tech stack**: PowerShell. **Deploy**: PowerShell module. **Trade-off**: **Not a full backup solution**—Wavestone's PoC found partial attribute restoration, password loss, and state ambiguity . **Best for**: organizations wanting declarative Entra ID configuration management—accepting partial recovery limitations.



- **PyADRecon (and PyADRecon-ADWS)**

  **Active Directory reconnaissance** for pentesters and blue teams (open source) — **the most accessible open-source AD reconnaissance tool** for assessment and hardening . **Features**: **Gathers AD information** and generates XLSX report; **ADWS variant** queries Active Directory Web Services (TCP/9389) instead of LDAP—**flies under EDR radar**; supports NTLM and Kerberos auth; modules for users, groups, computers, OUs . **Tech stack**: Python. **Deploy**: `pipx install pyadrecon` or `pyadrecon-adws`. **Trade-off**: **Reconnaissance only**—no backup, recovery, or continuous protection. **Best for**: pentesters and blue teams assessing AD exposure and identifying hardening opportunities.



- **AzureAD-Attack-Defense**

  **Entra ID attack mitigation guidance** (open source) — **the most comprehensive open-source Entra ID hardening reference**. **Features**: **Step-by-step instructions** to reduce attack surface and harden Entra ID against specific identity threats; covers common attack scenarios and their mitigations/detections; community-maintained . **Tech stack**: PowerShell, documentation. **Deploy**: Reference/documentation. **Trade-off**: **Guidance, not a tool**—it tells you what to harden but does not automate protection. **Best for**: identity administrators wanting actionable hardening guidance for Entra ID—especially before deploying commercial protection.



### Additional Strong Open-Source Options



- **Cayosoft Graph (cGraph) PowerShell Module** — Free PowerShell cmdlets for Microsoft Graph API (free). Manage Entra ID, Office 365, Intune, and more via Graph . **Note**: **Management module, not backup**—for automation and administration. **Best for**: administrators wanting Graph API access without building authentication from scratch.

- **No mature open-source AD forest recovery platform exists.** Semperis, Rubrik, Quest, and ManageEngine dominate. **DSInternals** provides the building blocks for offline recovery, but automated forest recovery requires commercial platforms.



**Frameworks for building custom systems**: Combine **DSInternals** for offline AD recovery and auditing with **BloodHound** for attack path analysis and **Microsoft 365 DSC** for Entra ID configuration export—creating a layered open-source protection stack. **None of these match Semperis' automated forest recovery or Rubrik's five-step wizard**, but for auditing, recovery scripting, and hardening, the options are production-proven.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- AD/Entra ID protection platforms handling credentials and directory data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.

- **The "backup/recovery" vs. "auditing" vs. "attack path analysis" vs. "hardening guidance" distinction is critical.** **Semperis, Rubrik, Quest, ManageEngine, Veeam, Commvault, Cohesity, and Druva** are **backup/recovery platforms**—they protect and restore AD/Entra ID . **Netwrix** is **auditing**—it tracks changes but does not restore . **Cayosoft** is **management**—it administers AD but recovery is one feature . **DSInternals** is **offline recovery/auditing**—it provides the building blocks for recovery . **BloodHound** is **attack path analysis**—it finds privilege paths but does not protect . **AzureAD-Attack-Defense** is **hardening guidance**—it tells you what to fix . **Choose based on whether you need restoration, audit trails, privilege mapping, or hardening guidance.**

- **DSInternals is the most powerful open-source AD tool**—it enables bare-metal domain controller recovery from IFM backups, offline password resets, and DCSync detection . **The trade-off**: Microsoft does not support it; improper use can cause irreversible damage. **For administrators with deep AD expertise, it is indispensable for incident response.**

- **BloodHound is the standard for attack path analysis**—it maps unintended privilege relationships that ransomware exploits . **The trade-off**: analysis only; it does not back up or restore. **Run it before an incident, not after.**

- **Microsoft 365 DSC is not a full Entra ID backup solution.** Wavestone's PoC found **partial attribute restoration, password replacement with defaults, and active/deactivated state ambiguity** . **Do not rely on it as your only Entra ID backup.**

- **Semperis DSP and Rubrik Identity Resilience are the enterprise leaders**—Semperis powers Cohesity Identity Resilience , and Rubrik reduces forest recovery from 20+ manual steps to a five-step wizard . **Both are quote-only; neither is accessible for SMB evaluation.**

- **ManageEngine RecoveryManager Plus is the most transparent commercial option**—AD from **$475/year**, M365 from **$195/year** . **For SMBs wanting affordable AD backup, it is the pragmatic entry point.**

- **Veeam Explorer for AD is included with all Veeam editions**—but full restore requires Enterprise or Enterprise Plus . **If you already run Veeam, AD recovery is a licensing upgrade away.**

- **Cayosoft Free Edition is genuinely useful**—web portal, LAPS access, BitLocker recovery, and self-service password change at no cost . **For organizations wanting AD management without per-admin fees, it is worth deploying.**

- Self-hosted open-source solutions require proper setup, PowerShell expertise, and security hardening. **AD/Entra ID tools have privileged access to identity infrastructure**—ensure your deployment meets your organization's security standards before using them in production.



---



**Made for identity administrators, security engineers, and organizations building transparent AD/Entra ID protection solutions.**

Let's make Active Directory & Entra ID Protection more open, data-driven, and recovery-proven.

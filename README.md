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

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **Semperis Directory Services Protector (DSP)**

  **Active Directory and Entra ID protection** with continuous monitoring and forest recovery. **Pricing**: **Custom pricing only**—no public rates; private offers via Microsoft Marketplace . **Free tier**: None. **Best for**: enterprises needing proactive AD hardening, attack path remediation, and automated malware-free forest recovery—**trade-off**: sales-led evaluation; enterprise pricing.



- **Rubrik Identity Resilience**

  **Unified identity protection** across Active Directory, Entra ID, and Okta. **Pricing**: Quote-only; enterprise contracts. **Free tier**: None. **Best for**: regulated enterprises needing tamper-resistant monitoring, surgical rollback, and five-step forest recovery—**trade-off**: enterprise commitment; FedRAMP features limited to recovery only .



- **Quest Recovery Manager for Active Directory**

  **AD forest recovery and backup** with granular restore. **Pricing**: **Disaster Recovery term license listed at $48.86** (1 user, 1 year) on CDW-G ; maintenance renewal **$73.80** . **Free tier**: None. **Best for**: organizations wanting proven AD recovery without full cyber resilience platform—**trade-off**: pricing scales with users; recovery-focused.



- **ManageEngine RecoveryManager Plus**

  **AD, Entra ID, and M365 backup and restore**. **Pricing**: **AD Standard Edition from US$475/year** (includes AMS) ; M365 from **US$195/year**; tiered by user objects . **Free tier**: None. **Best for**: SMBs and mid-market organizations wanting affordable AD backup with Entra ID support—**trade-off**: per-user licensing; advanced features tiered.



- **Netwrix Auditor for AD**

  **AD and Entra ID auditing** with change tracking. **Pricing**: **Essentials starts at $20 per enabled AD user + cloud-only Entra ID user** (self-service) . **Free tier**: None. **Best for**: compliance-focused organizations needing audit trails and unauthorized change detection—**trade-off**: auditing, not backup/recovery.



- **Veeam Explorer for Microsoft Active Directory**

  **AD item recovery** included with Veeam Backup & Replication. **Pricing**: **Included with all Veeam editions** (Free, Standard, Enterprise, Enterprise Plus); full restore capabilities require Enterprise or Enterprise Plus . **Free tier**: Yes, with Veeam Free Edition (limited restore). **Best for**: Veeam customers wanting AD recovery without additional licensing—**trade-off**: requires Veeam infrastructure; full features gated by edition.



- **Commvault AD Protection**

  **Directory Services protection** within Commvault Cloud. **Pricing**: Quote-only; bundled with Commvault platform. **Free tier**: None. **Best for**: Commvault customers wanting unified AD and Entra ID backup—**trade-off**: platform commitment required.



- **Cohesity Identity Resilience (powered by Semperis)**

  **AD and Entra ID protection** integrated with Cohesity Data Cloud. **Pricing**: Quote-only. **Free tier**: 30-day free trial . **Best for**: Cohesity customers wanting AD hardening and recovery in one platform—**trade-off**: requires Cohesity + Semperis partnership stack.



- **Cayosoft Administrator**

  **AD management and recovery** with web portal. **Pricing**: **Subscription licensing** (12/36/72 months); **no per-admin fees**—license once, all admins use it . **Free tier**: Yes, **Free Edition** with web portal, LAPS access, BitLocker recovery, self-service password change, and Graph PowerShell module . **Best for**: organizations wanting AD management without per-admin licensing—**trade-off**: free edition limited; recovery features in paid tiers.



- **Druva SaaS Universal License**

  **Unified SaaS and identity backup** including AD and Entra ID. **Pricing**: **Per-user flat rate** across all SaaS apps; **300 GB pooled storage per user** . **Free tier**: None. **Best for**: organizations consolidating SaaS backup under one license—**trade-off**: per-user pricing; requires Druva platform.



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

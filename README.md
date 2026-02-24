# Azure-Security-Notes


TO-DOs
- Create external user
- Create license management user
- Add payment method to admin.microsoft.com
- Get a free trial of Entra Admin P2 (won't be charged after time is up)
- Set up billing alerts
- Create conditional access policies
- Create authentication method policies
- Enable EntraID Protection
- Setup Access Reviews



EntraID
- There are restrictions on nested groups
- Entra licenses charge per users
- Certain fearutes only work when you have a premium license
- You can assign licenses to users and groups
- All licenses are based on region
- M365 Admin center for licenses. Entra admin center for users and groups
- You cant delete a group with an active license
- 


Security Operations and Monitoring (Read-Only / Investigative Access)

I wanted to propose an access model that enables effective cloud security operations while maintaining strong governance, least-privilege enforcement, and separation of duties across the Azure environment.

The objective is to provide sufficient visibility for monitoring, incident response, threat hunting, and security posture assessment without introducing standing permissions that could impact production services or security configurations. Below is a recommended role-based model aligned with Microsoft security architecture and industry best practices.

Security Operations and Monitoring (Read-Only / Investigative Access)
• Security Reader (Microsoft Defender for Cloud)
Provides centralized visibility across Microsoft Defender services, including alerting, exposure management, recommendations, and risk insights, while remaining fully read-only.

Log Analytics and Telemetry Access (Critical for Detection and Threat Hunting)
• Log Analytics Reader on all relevant workspaces
This role enables KQL-based investigations, correlation across telemetry sources, and proactive threat hunting. It is read-only and does not permit changes to ingestion, retention, or log deletion.

Governance and Security Posture Management
• Security Reader for Defender for Cloud
• Policy Reader for Azure Policy assignments and compliance visibility

These roles provide visibility into secure score, compliance posture, and policy enforcement without granting configuration permissions.

For elevated access requirements related to response or remediation, I can propose a Just-in-Time model leveraging Azure Privileged Identity Management (PIM) to ensure time-bound access, approval workflows, and full auditability.

I believe this combined approach balances operational effectiveness with governance and risk management. Please let me know if you would like to discuss this further or review additional details.

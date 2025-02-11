# 1.1 Compliance Requirements

## Title: Azure Resource Creation Compliance Requirements

### Purpose:
To outline the compliance requirements and restrictions for creating Azure resources within the organization, ensuring adherence to regulatory standards and internal policies.

### Scope:
This document applies to all Azure resources created by internal development teams, including but not limited to Virtual Machines, Storage Accounts, Kubernetes Clusters, and Databases.

### Compliance Requirements:

#### Data Residency:
- All data must reside in the East US 2 and Central US Azure regions to comply with local data sovereignty laws.
- No data or resources may be deployed in regions outside the approved list.

#### Resource Tagging:
- All Azure resources must include the following mandatory tags:
  - **Environment** (e.g., Production, Staging, Development)
  - **CostCenter** (e.g., Finance, HR, Engineering)
  - **Owner** (email of the resource owner)
- Tags must be applied at the time of resource creation and cannot be modified without approval.

#### Security and Access Controls:
- All resources must be created within a Virtual Network (VNet) with restricted access.
- Public IP addresses are prohibited unless explicitly approved by the Security Team.
- Role-Based Access Control (RBAC) must be enforced, and only approved roles may be assigned.

#### Encryption:
- All storage accounts must use Azure-managed keys for encryption at rest.
- Data in transit must be encrypted using TLS 1.2 or higher.

#### Auditing and Monitoring:
- Azure Monitor and Log Analytics must be enabled for all resources.
- All actions must be logged and retained for a minimum of 90 days for audit purposes.

#### Resource Naming Conventions:
- Resource names must follow the format:
  - `<ProjectName>-<Environment>-<ResourceType>-<Region>-<InstanceNumber>`
  - Example: ClaimsApp-Prod-VM-EastUS2-01

#### Approval Workflow:
- Any deviation from the above requirements must be approved by the Compliance Team via a formal request process.

#### Review and Updates:
- This document will be reviewed quarterly and updated as necessary to reflect changes in regulatory requirements or internal policies.

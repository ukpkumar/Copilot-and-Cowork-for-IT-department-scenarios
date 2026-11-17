# Module 6: Administration for IT admins

[Previous: Module 5](05-copilot-studio-agents.md) | [Home](../README.md) | Next: [Module 7: Measuring value](07-measuring-value.md)

## Learning objectives

- Configure who can use Cowork, and which models and capabilities are available.
- Deploy and control plugins, skills and connectors.
- Set up Copilot Studio environments and DLP for IT agents.
- Monitor usage, cost and activity, and plan a phased rollout.

> Admin menus and settings change often. Confirm each path against the current Microsoft Learn articles in the [references](../appendix/references.md).

---

## 6.1 Admin map

| Area | What you control | Where |
|------|------------------|-------|
| **Cowork access** | Who can use Cowork | Microsoft 365 admin center > **Copilot > Cost Management > Configuration** > spending policy that selects **Cowork** |
| **Discoverability** | Whether users see Cowork and can request access | Discovery setting for usage-based AI experiences |
| **Models** | Which model families are available (for example, turn off a model provider for some groups) | Microsoft 365 admin center > **Copilot > Settings** |
| **Browser use** | Whether Cowork can complete web tasks in Microsoft Edge | **Cowork Browsing** tenant setting; Edge allow and block lists apply |
| **Plugins** | Upload, deploy, allow or block plugins and publishers | Microsoft 365 admin center > **Agents > Tools**, and **Agents > Settings > Agent and plugin access** |
| **Agents** | Approve, deploy, block agents (including Copilot Studio agents) | Microsoft 365 admin center > **Agents > All agents** |
| **Copilot Studio** | Environments, makers, DLP, connector action control, sharing limits | Power Platform admin center |
| **Data protection** | Sensitivity labels, DLP for Copilot, retention, audit | Microsoft Purview |
| **Usage and cost** | Usage reports, Value tab, consumption, limits | Microsoft 365 admin center reports; Copilot Credits consumption |

## 6.2 Grant access to Cowork

Cowork uses **usage-based billing**. Access is granted by a **spending policy** that includes the user and selects Cowork.

1. Create a Microsoft Entra security group, for example `SG-Cowork-IT-Pilot`.
2. In the Microsoft 365 admin center, go to **Copilot > Cost Management > Configuration** and select **+ Add spending policy**.
3. Scope it to **Specific groups** and select the group.
4. Under **Select agents and services**, select **Cowork**.
5. Set the limits and billing method, and create the policy.

Points to remember:

- A spending policy is an **access control**, not only a budget. A low credit limit does not block access.
- To remove access, remove the user from **every** spending policy that selects Cowork.
- The **Cowork** entry under **Agents > All agents** no longer controls access.

## 6.3 Plugins, skills and MCP servers

| Task | Steps |
|------|-------|
| Make a Microsoft or partner plugin available | **Agents > Tools** > find the plugin > **Installed for** > **All users** or **Specific users/groups** |
| Publish an internal plugin | **Agents > Tools > Registry > Upload**, then deploy to groups |
| Restrict plugins by publisher or category | **Agents > Settings > Agent and plugin access** |
| Approve MCP servers and server-linked plugins | Admin consent (AI Administrator or Global Administrator) |
| Monitor plugin use | Microsoft Purview audit log > **Copilot activities** |

Recommended practice for an IT department:

- Create an **IT plugin catalogue**: name, owner, version, skills, connectors, data accessed, approval date.
- Deploy IT plugins to **IT security groups** first, not to all users.
- Keep skill source files in a **version-controlled repository** and review changes before upload.
- Each user signs in to plugin connectors themselves; admins cannot consent on their behalf for user-delegated sign-in.

## 6.4 Copilot Studio environment strategy for IT

| Environment | Purpose | Makers | DLP profile |
|-------------|---------|--------|-------------|
| **IT-Dev** | Build and test IT agents | IT makers | Business connectors allowed; production connectors blocked |
| **IT-Test** | User acceptance testing with test data | IT makers, testers | Same as production |
| **IT-Prod** | Published IT agents | Pipeline only | Strict: approved connectors only; connector action control on privileged actions |
| **Default** | Personal productivity | Everyone | Most restrictive |

- Use **managed environments** and **pipelines** to move solutions between environments.
- Use **connector action control** to allow only the actions you need (for example, allow "Create incident", block "Delete record").
- Review the agent's **Entra Agent ID** permissions after publishing, and apply **Conditional Access** where needed.
- Require **authentication** for every IT agent that shows user-specific data or takes actions.

## 6.5 Data protection

- **Sensitivity labels** apply to files Cowork reads and creates. Label IT documents such as network diagrams, audit evidence and vendor contracts.
- **Purview DLP for Copilot** can stop Copilot processing content with specific labels or sensitive information types.
- **Audit**: Cowork activity, automated tasks and browser tasks are recorded in the unified audit log.
- **Processing**: Cowork processes files in a temporary, isolated environment inside the Microsoft 365 service boundary and removes it when the task finishes.
- **Data residency** follows the Microsoft 365 Copilot data residency model.
- **Oversharing**: before rollout, review SharePoint permissions for IT sites (for example with SharePoint Advanced Management), because Copilot respects existing permissions.

## 6.6 Monitoring usage and cost

| What | Where |
|------|-------|
| Cowork usage and adoption | Copilot Cowork usage report and its **Value** tab |
| Credit consumption | Copilot Credits consumption in the Microsoft 365 admin center; consumption dashboard in Insights |
| Agent analytics | Copilot Studio analytics per agent |
| Activity audit | Microsoft Purview audit |
| Cost estimates | Copilot Credit Estimator |

## 6.7 Phased rollout for the IT department

| Phase | Scope | Exit criteria |
|-------|-------|---------------|
| 1. Pilot | 15 to 25 IT staff across operations, service desk and security; 5 use cases | Use cases run end to end; issues logged; value baseline taken |
| 2. IT-wide | All IT staff; team skills and the IT plugin; two Cowork apps | Skills adopted; credit consumption within budget |
| 3. Employee-facing | Service desk agent and access request agent for all employees | Resolution rate and CSAT targets met in test |
| 4. Scale | Autonomous agents (JML, compliance); more plugins | ALM and support model in place |

[Previous: Module 5](05-copilot-studio-agents.md) | [Home](../README.md) | Next: [Module 7: Measuring value](07-measuring-value.md)

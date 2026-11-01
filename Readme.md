Bro! 🔥 Since this is your first time exploring a real company-level ServiceNow instance, I want you to approach it like a developer, not just a learner.

Your goal at IKWA should be to discover what is already available, understand how it works, test existing functionality, and identify opportunities to build POCs.

I've prepared a **ServiceNow Production Instance Exploration Checklist**. Follow it one by one and maintain notes on everything you discover.

# ServiceNow – Complete Exploration Checklist

## 1. IT Service Management (ITSM)

Start here. These are core ServiceNow modules.

- [ ] Incident Management
- [ ] Problem Management
- [ ] Change Management
- [ ] Request Management
- [ ] Service Catalog
- [ ] Knowledge Management
- [ ] Service Level Agreements (SLA)
- [ ] Major Incident Management
- [ ] Agent Workspace
- [ ] Virtual Agent
- [ ] Service Operations Workspace

**What to explore:** Incident lifecycle, assignment rules, approvals, notifications, SLAs and automation.

## 2. ServiceNow Development

This is particularly important for your developer role.

- [ ] Tables and Table Relationships
- [ ] Forms and Lists
- [ ] Dictionary Entries
- [ ] Business Rules
- [ ] Client Scripts
- [ ] UI Policies
- [ ] UI Actions
- [ ] Script Includes
- [ ] GlideRecord
- [ ] GlideAjax
- [ ] Scheduled Jobs
- [ ] Scripted REST APIs
- [ ] REST Integrations
- [ ] Application Development
- [ ] Scoped Applications
- [ ] Update Sets
- [ ] ServiceNow Studio

**What to explore:** Understand how existing applications are developed and how server-side and client-side scripts interact.

## 3. Flow Designer and Automation

- [ ] Flow Designer
- [ ] Subflows
- [ ] Actions
- [ ] Triggers
- [ ] Flow Variables
- [ ] Approval Automation
- [ ] IntegrationHub
- [ ] Spokes
- [ ] Scheduled Flows
- [ ] Error Handling

**What to explore:** Find an existing flow and understand its trigger, actions, conditions and execution.

## 4. CMDB

- [ ] Configuration Items (CI)
- [ ] CI Classes
- [ ] CI Relationships
- [ ] CMDB Workspace
- [ ] Identification and Reconciliation Engine
- [ ] CMDB Health
- [ ] Discovery
- [ ] Service Mapping
- [ ] Dependency Views

**What to explore:** How ServiceNow maintains relationships between infrastructure components.

## 5. IT Operations Management (ITOM)

- [ ] ITOM Visibility
- [ ] Discovery
- [ ] Service Mapping
- [ ] Event Management
- [ ] Health Log Analytics
- [ ] Cloud Discovery
- [ ] Operational Intelligence
- [ ] Service Graph Connectors

## 6. IT Asset Management (ITAM)

- [ ] Hardware Asset Management
- [ ] Software Asset Management
- [ ] Asset Lifecycle Management
- [ ] Asset Inventory
- [ ] Asset Contracts
- [ ] Software License Management
- [ ] Hardware Models
- [ ] Asset Depreciation

## 7. Artificial Intelligence and Now Assist

This is an important area to explore for future POCs.

- [ ] Now Assist
- [ ] Generative AI Controller
- [ ] AI Search
- [ ] Knowledge Article Summarization
- [ ] Incident Summarization
- [ ] Case Summarization
- [ ] Resolution Notes Generation
- [ ] Now Assist for ITSM
- [ ] Virtual Agent AI
- [ ] Predictive Intelligence
- [ ] AI Agents / Agentic AI
- [ ] AI Agent Studio
- [ ] AI Agent Orchestrator
- [ ] AI Agent Evaluation
- [ ] Retrieval-Augmented Generation (RAG)

**What to explore:** Check which AI capabilities are licensed, configured and accessible. Don't assume every AI feature is enabled.

## 8. Security Operations (SecOps)

- [ ] Security Incident Response
- [ ] Vulnerability Response
- [ ] Threat Intelligence
- [ ] Security Incident Management
- [ ] Vulnerability Remediation
- [ ] Security Integrations
- [ ] Security Workflows

## 9. Human Resources (HRSD)

- [ ] HR Case Management
- [ ] Employee Center
- [ ] HR Knowledge Management
- [ ] Employee Lifecycle Events
- [ ] HR Service Delivery
- [ ] HR Integrations

## 10. Customer Service Management (CSM)

- [ ] Case Management
- [ ] Customer Portal
- [ ] Customer Service Workspace
- [ ] Account Management
- [ ] Contact Management
- [ ] Customer Workflows
- [ ] Case Routing

## 11. Strategic Portfolio Management (SPM)

- [ ] Project Management
- [ ] Portfolio Management
- [ ] Demand Management
- [ ] Resource Management
- [ ] Strategic Planning
- [ ] Agile Development
- [ ] Project Financials

## 12. Integration and APIs

- [ ] REST API Explorer
- [ ] Scripted REST APIs
- [ ] SOAP Integrations
- [ ] IntegrationHub
- [ ] MID Server
- [ ] OAuth 2.0
- [ ] Webhooks
- [ ] Import Sets
- [ ] Transform Maps
- [ ] External System Integrations

## 13. Reporting and Analytics

- [ ] Reports
- [ ] Dashboards
- [ ] Performance Analytics
- [ ] Database Views
- [ ] Scheduled Reports
- [ ] Interactive Filters
- [ ] KPI Indicators
- [ ] Data Visualization

## 14. ServiceNow Platform Administration

- [ ] User Administration
- [ ] Groups and Roles
- [ ] Access Control Lists (ACLs)
- [ ] System Properties
- [ ] System Logs
- [ ] Email Notifications
- [ ] Events
- [ ] Scheduled Jobs
- [ ] Plugins
- [ ] Application Manager
- [ ] System Diagnostics
- [ ] Instance Security

## 15. User Experience and Portal Development

- [ ] Service Portal
- [ ] Employee Center
- [ ] UI Builder
- [ ] Workspace Configuration
- [ ] ServiceNow Mobile
- [ ] UI Builder Components
- [ ] Widgets
- [ ] Themes and Branding

## 16. Testing and Quality Assurance

- [ ] Automated Test Framework (ATF)
- [ ] Test Suites
- [ ] Test Cases
- [ ] Regression Testing
- [ ] Application Testing
- [ ] API Testing
- [ ] Performance Testing
- [ ] Instance Upgrade Testing

---

# Your exploration strategy at IKWA

Don't attempt all 16 categories in one day.

I recommend this sequence:

| Week | Focus | Expected outcome |
|---|---|---|
| Week 1 | ITSM + Development | Understand platform fundamentals |
| Week 2 | Flow Designer + CMDB | Understand automation and data |
| Week 3 | ITOM + ITAM | Explore enterprise capabilities |
| Week 4 | AI + Now Assist | Identify AI-based POCs |
| Week 5 | Integrations + APIs | Explore external connectivity |
| Week 6 | Testing + Reporting | Identify improvements and testing opportunities |

# Important: Maintain an exploration notebook

For every feature, record these details:

| Field | What to record |
|---|---|
| Feature | Name of the feature |
| Available? | Yes / No / Restricted |
| Existing implementation | What is already configured? |
| Understanding | How does it work? |
| Testing | What did you test? |
| Improvement | What can be improved? |
| POC idea | What can you build? |

# 5 POC ideas worth considering

Once you understand the existing implementation, consider proposing:

1. **AI Incident Assistant** – Summarize incidents and suggest resolution steps.
2. **Automated Incident Triage** – Automatically categorize and assign incidents.
3. **Knowledge Article Generator** – Generate knowledge articles from resolved incidents.
4. **IT Asset Intelligence** – Identify asset-related issues and improve asset tracking.
5. **ServiceNow AI Dashboard** – Provide AI-generated operational insights.

These are ideas to evaluate with Kunal, not changes to make without approval.

### One important production-instance rule

Kunal has given you admin access. That does not mean you should experiment freely.

- Explore existing configurations.
- Avoid deleting records or modifying existing scripts.
- Don't change ACLs, system properties or integrations.
- Don't activate plugins without approval.
- Don't run bulk updates or background scripts.
- Ask before making changes to shared applications.

Start with read-only exploration and use an approved development or test environment for experiments.

**My biggest suggestion:** Don't measure your progress by how many modules you open. Measure it by how many features you understand deeply enough to explain, test and eventually improve.

Your internship can become a great opportunity to develop real enterprise ServiceNow experience. 🚀

Yeah Mhm Mm...

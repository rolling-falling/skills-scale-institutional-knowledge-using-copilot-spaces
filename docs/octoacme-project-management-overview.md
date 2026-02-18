# OctoAcme Project Management Overview

## Purpose
Provide a concise, shareable introduction to how OctoAcme runs projects so new teammates can quickly understand our approach, roles, and key artifacts.

## Scope
Applies to all cross-functional projects that deliver product features, services, or integrations.

## Principles
- Customer-first: prioritize customer value and usability.
- Iterative delivery: deliver small, testable increments.
- Clear ownership: each project has a named Project Manager (PM) and Product Lead.
- Data-informed decisions: measure impact and iterate based on evidence.
- Psychological safety: encourage feedback and learning.

## Core Roles

### Primary Roles
- **Project Manager (PM)**: Coordinates delivery, schedules, risk, and communications. Accountable for project execution and stakeholder alignment.
- **Product Manager (PdM)**: Defines outcomes, prioritizes backlog, and measures success. Owns product vision and roadmap.
- **Developers**: Implement features, collaborate on design and testability. Responsible for code quality and technical delivery.

### Supporting Roles
- **UX Designer**: Ensures intuitive user experience through design flows, prototypes, and accessibility standards.
- **Technical Writer**: Creates and maintains accurate documentation for internal and user-facing artifacts.
- **QA Engineer**: Validates quality and acceptance criteria through comprehensive testing.
- **Release Manager**: Manages release process, deployment coordination, and stakeholder announcements.
- **Customer Support Liaison**: Brings user insights and support feedback into planning and improvement cycles.
- **Security Champion**: Advocates for secure practices, surfaces risks, and helps manage security incidents.
- **Data Analyst**: Enables data-driven decisions through analysis, reporting, and metrics tracking.

### Role Clarity
Each project must have clearly assigned roles with documented responsibilities. For detailed role descriptions, see [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md).

**Escalation Path**: Team-level → Project Manager → Product Manager → Sponsor/Leadership
**Security Escalation**: Security Champion → Security Team → Security Leadership

Refer to issue #5 for expanded role definitions: https://github.com/rolling-falling/skills-scale-institutional-knowledge-using-copilot-spaces/issues/5

## Key Artifacts
- Project Charter / One-pager
- Roadmap and Release Plan
- Sprint/Iteration Backlog
- Acceptance Criteria & Definition of Done
- Risk Register
- Retrospective notes and action items

## Lifecycle (high-level)
1. Initiation: problem statement, stakeholders, high-level timeline.
2. Planning: scope, resources, milestones, dependencies.
3. Execution: build, test, review, iterate.
4. Release: deploy, verify, announce.
5. Close & Retrospective: capture learnings and next steps.

## Communication Cadence
- **Weekly PM + PdM sync**: Project status, priorities, and blockers
- **Twice-weekly team standups**: Delivery team progress and coordination (or as agreed)
- **Monthly stakeholder updates**: Progress reports to sponsors and stakeholders
- **Release communications**: Release Manager coordinates with Customer Support Liaison for user communications
- **Security reviews**: Security Champion reviews features and designs as needed
- **Design reviews**: UX Designer presents and iterates with team feedback
- **Documentation reviews**: Technical Writer coordinates with developers pre-release
- **Metrics reviews**: Data Analyst shares insights with Product Manager monthly
- **Ad-hoc escalations**: Follow documented escalation paths as needed

## How to use these docs
- Keep the Project Charter updated in the project repo.
- Add process-specific docs into `.copilot/` if you want Copilot Spaces to use them as context.

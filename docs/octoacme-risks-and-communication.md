# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with clear ownership and accountability:

| ID | Description | Impact (H/M/L) | Likelihood (H/M/L) | Owner | Mitigation Plan | Status |
|----|-------------|----------------|---------------------|-------|-----------------|--------|
| R-001 | Example risk | High | Medium | Project Manager | Action items | Active |

**Column Definitions:**
- **ID**: Unique identifier for tracking
- **Description**: Clear statement of the risk
- **Impact**: High (project failure/major delay), Medium (significant impact), Low (minor impact)
- **Likelihood**: High (>60%), Medium (30-60%), Low (<30%)
- **Owner**: Person accountable for monitoring and mitigation (typically Project Manager, but can be role-specific)
- **Mitigation Plan**: Actions to reduce likelihood or impact
- **Status**: Active, Mitigated, Closed, or Realized

**Role-Specific Risk Ownership:**
- **Technical risks**: Tech Lead or Developers
- **Security risks**: Security Champion
- **Quality risks**: QA Engineer
- **UX/usability risks**: UX Designer
- **Documentation risks**: Technical Writer
- **Deployment risks**: Release Manager
- **Customer impact risks**: Customer Support Liaison

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
Identify stakeholder groups and communication needs with clear role accountability:

### Communication Matrix

| Stakeholder Group | Information Needs | Frequency | Owner | Format |
|-------------------|-------------------|-----------|-------|--------|
| Engineering Team | Technical details, blockers | Daily | Tech Lead | Standup |
| Product/Leadership | Progress, risks, decisions | Weekly | Project Manager | Status report |
| Sales/Marketing | Feature updates, timeline | Milestone-based | Product Manager | Email brief |
| Customer Support | User-facing changes, timeline | Pre-release | Customer Support Liaison | Training session |
| Security Team | Security reviews, incidents | As needed | Security Champion | Review requests |
| End Users | New features, changes | Release | Release Manager | Release notes |

### Single Source of Truth
- Maintain project status in **Project README** or dedicated status page
- **Owner**: Project Manager updates weekly
- **Contributors**: All roles update their sections (QA status, design progress, security reviews, etc.)
- Link to detailed artifacts (roadmap, risk register, metrics dashboard)

## Communication Templates

### Weekly Status Template
**From**: Project Manager  
**To**: Product Manager, stakeholders  
**Frequency**: Weekly

- **Progress this week:**
  - Development: [completed items]
  - QA: [testing status]
  - Design: [UX progress if applicable]
  - Documentation: [Technical Writer updates if applicable]
- **Next steps:**
  - Planned for next week by role
- **Risks & blockers:**
  - Active risks from Risk Register with owner
- **Metrics:**
  - Key metrics update from Data Analyst
- **Ask / decisions needed:**
  - Specific decisions with deadline

### Incident Communication
**From**: Project Manager (or Security Champion for security incidents)  
**To**: Stakeholders, affected parties  
**Frequency**: Real-time during incident

- **Triage summary:** Brief description of incident
- **Impact:** User/business impact assessment
- **Actions being taken:** Current mitigation steps with owners
- **Expected timeline:** Resolution estimate
- **Communication plan:** Update frequency and channels
- **Roles involved:**
  - Incident Commander: [name]
  - Technical Lead: [name]
  - Customer Support Liaison: [updates to users/support]
  - Security Champion: [if security-related]
- **Post-incident:** Blameless retrospective scheduled within 48 hours

### Release Communication Template
**From**: Release Manager  
**To**: Stakeholders, Customer Support, end users  
**Frequency**: Per release

- **Release name/version:**
- **Deployment date/time:**
- **What's new:** Key features and improvements
- **What's changed:** Breaking changes or migrations
- **Action required:** User or admin actions needed
- **Support resources:** Links to documentation (Technical Writer)
- **Contact:** Customer Support Liaison for questions

## Escalation Paths

### Standard Escalation Path
**Level 1**: Team-level (same day)
- **Who**: Developer, QA Engineer, UX Designer, Technical Writer
- **Escalates to**: Tech Lead or Project Manager
- **For**: Technical blockers, coordination issues

**Level 2**: Project-level (1-2 days)
- **Who**: Project Manager
- **Escalates to**: Product Manager and cross-team leads
- **For**: Dependencies, scope questions, resource needs

**Level 3**: Leadership-level (immediate for critical)
- **Who**: Product Manager with Project Manager
- **Escalates to**: Sponsor, Director, or VP
- **For**: Business impact, budget, major timeline risks

### Specialized Escalation Paths

**Security Escalation** (immediate for critical issues)
- **Who**: Security Champion
- **Escalates to**: Security Team → Security Leadership
- **For**: Security vulnerabilities, incidents, breaches
- **Communication**: Follow security incident runbook and notify Security on-call
- **Involved**: Project Manager (for project impact), Customer Support Liaison (for user communication if needed)

**Quality/Release Escalation** (immediate for release blockers)
- **Who**: QA Engineer or Release Manager
- **Escalates to**: Project Manager → Product Manager
- **For**: Release-blocking defects, deployment failures
- **Decision gate**: Go/no-go for release

**User Impact Escalation** (same day for critical user issues)
- **Who**: Customer Support Liaison
- **Escalates to**: Product Manager → Leadership
- **For**: High-volume user complaints, critical usability issues
- **Involved**: UX Designer (for design fixes), Technical Writer (for documentation fixes)

**Data/Metrics Escalation** (as needed)
- **Who**: Data Analyst
- **Escalates to**: Product Manager
- **For**: Significant metric anomalies, measurement issues

**Accountability**: Each role must know their escalation path. Project Manager coordinates all escalations and maintains escalation log.

See [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) for role definitions. Related to issue #5: https://github.com/rolling-falling/skills-scale-institutional-knowledge-using-copilot-spaces/issues/5

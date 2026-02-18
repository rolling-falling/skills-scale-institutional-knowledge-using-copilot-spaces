# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- **Daily standups** (15 min) — focus on progress, blockers, dependencies
  - **Facilitated by**: Project Manager or Tech Lead
  - **Attendees**: Core delivery team (Developers, QA Engineers)
  - **Optional**: UX Designer, Technical Writer as needed
- **Weekly delivery sync** — show progress, updates, and flagged risks
  - **Led by**: Project Manager
  - **Attendees**: Product Manager, Tech Lead, QA Engineer, Release Manager
  - **Topics**: Sprint progress, risk register review, upcoming releases
- **Demo/Review** at the end of each sprint or milestone
  - **Presented by**: Developers and UX Designer
  - **Attendees**: Product Manager, stakeholders, Customer Support Liaison (for user-facing features)
  - **Purpose**: Validate acceptance criteria and gather feedback

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- **Unit tests** for new logic
  - **Owner**: Developers write and maintain
- **Integration tests** where applicable
  - **Owner**: Developers, with QA Engineer guidance
- **End-to-end smoke tests** for critical flows before release
  - **Owner**: QA Engineer executes and validates
- **Security scanning** in CI
  - **Owner**: Security Champion reviews results and addresses findings
- **Manual QA** for feature acceptance when needed
  - **Owner**: QA Engineer conducts testing
  - **Sign-off required**: QA Engineer approves before deployment
- **Accessibility testing** for user-facing features
  - **Owner**: UX Designer coordinates with QA Engineer
- **Documentation review** before release
  - **Owner**: Technical Writer reviews and updates

**Quality Gates**: All tests must pass, security scans clear (or risks accepted), and QA sign-off obtained before release.

## Reporting & Metrics
- **Track velocity and burndown**
  - **Owner**: Project Manager monitors and reports
- **Monitor success metrics** identified in the Project One-pager
  - **Owner**: Data Analyst tracks and reports to Product Manager
- **Use dashboards** for key signals (errors, latency, usage)
  - **Owner**: Data Analyst maintains dashboards
  - **Reviewed by**: Product Manager, Tech Lead, Customer Support Liaison
- **Quality metrics** (test coverage, defect rates, test pass rates)
  - **Owner**: QA Engineer tracks and reports

## Blocker Escalation
Escalation follows a clear path with defined timeframes and responsibilities:

### Level 1: Team-level triage (same day)
- **Handled in**: Daily standup
- **Decision maker**: Tech Lead or Project Manager
- **Resolution**: Team self-organizes to unblock
- **Examples**: Code review delays, minor technical blockers

### Level 2: Cross-team or project-level escalation (1-2 days)
- **Escalated by**: Project Manager
- **Decision makers**: Product Manager and dependent team leads
- **Communication**: Email or sync meeting
- **Examples**: External dependencies, resource constraints, scope clarification needed

### Level 3: Sponsor/leadership escalation (immediate for critical issues)
- **Escalated by**: Project Manager with Product Manager
- **Decision makers**: Sponsor, Director, or VP
- **Communication**: Formal escalation email with impact analysis
- **Examples**: Business-impacting issues, budget overruns, timeline risks to major milestones

### Special Escalation Paths
- **Security incidents**: Security Champion → Security Team → Security Leadership (immediate)
- **Customer-impacting issues**: Customer Support Liaison → Product Manager → Leadership (same day)
- **Release blockers**: Release Manager → Project Manager → Product Manager (immediate)

**Accountability**: Project Manager owns escalation process and timing. All escalations must be documented in project communications.

## Execution Checklist
- [ ] Branching and PR conventions documented in repo (Tech Lead)
- [ ] CI configured for tests and lint (Developers)
- [ ] **Security scanning enabled in CI** (Security Champion)
- [ ] Regular demos scheduled (Project Manager)
- [ ] Risk register updated weekly (Project Manager)
- [ ] **QA test plan reviewed and approved** (QA Engineer)
- [ ] **Design assets and specs finalized** (UX Designer, if applicable)
- [ ] **Documentation plan in place** (Technical Writer, if applicable)
- [ ] **Metrics tracking configured** (Data Analyst)
- [ ] **Customer support briefed on upcoming changes** (Customer Support Liaison, for user-facing features)

**Accountability**: Project Manager verifies checklist completion and role assignments are clear.

See [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) for detailed role responsibilities. Related to issue #5: https://github.com/rolling-falling/skills-scale-institutional-knowledge-using-copilot-spaces/issues/5

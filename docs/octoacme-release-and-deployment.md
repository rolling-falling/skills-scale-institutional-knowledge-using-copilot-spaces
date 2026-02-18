# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
Each requirement has a clear owner and accountability:

- **All acceptance criteria met and PRs merged**
  - **Owner**: Developers
  - **Verified by**: Product Manager and QA Engineer
- **Passing CI and security scans**
  - **Owner**: Developers (CI), Security Champion (security review)
  - **Sign-off required**: Security Champion for security-sensitive changes
- **Release notes drafted**
  - **Owner**: Technical Writer in collaboration with Product Manager
  - **Reviewed by**: Release Manager
- **Rollback / mitigation plan documented**
  - **Owner**: Release Manager
  - **Input from**: Tech Lead, Developers
- **Smoke tests prepared**
  - **Owner**: QA Engineer
  - **Execution**: Automated where possible
- **Documentation updated**
  - **Owner**: Technical Writer
  - **Verified by**: Developers and UX Designer (for user-facing docs)
- **Support team briefed**
  - **Owner**: Customer Support Liaison
  - **Content**: Feature overview, known issues, FAQs
- **Metrics and monitoring configured**
  - **Owner**: Data Analyst
  - **Verified by**: Product Manager

## Deployment Checklist
Each item has clear role ownership:

- [ ] **Deployment window scheduled** (if needed) - Release Manager
- [ ] **Backup or snapshot** (if applicable) - Release Manager coordinates with Infrastructure team
- [ ] **Deploy to staging and run smoke tests** - QA Engineer executes tests
- [ ] **Security review completed** (for security-sensitive changes) - Security Champion approves
- [ ] **Deploy to production** (automated pipeline preferred) - Release Manager initiates
- [ ] **Run post-deploy verifications** - QA Engineer validates
- [ ] **Monitor metrics and error rates** - Data Analyst monitors, alerts team if anomalies
- [ ] **Announce release to stakeholders and support** - Release Manager sends announcement
  - **Customer Support briefing** - Customer Support Liaison conducts
  - **Release notes published** - Technical Writer publishes
  - **Stakeholder notification** - Release Manager sends
- [ ] **Post-deployment retrospective scheduled** (if issues occurred) - Project Manager schedules

**Go/No-Go Decision:** Release Manager leads go/no-go call with QA Engineer, Tech Lead, and Product Manager. All must agree before production deployment.

**Accountability:** Release Manager is accountable for deployment process and coordination of all roles.

## Rollback & Incident Playbook
If a deployment fails or causes a critical issue, follow this process with clear role accountability:

### Immediate Response (0-15 minutes)
1. **Declare incident** - Release Manager or on-call Engineer
2. **Assign Incident Commander** - typically Release Manager or senior Tech Lead
3. **Assess impact** - Data Analyst provides metrics, Customer Support Liaison reports user impact
4. **Notify stakeholders** - Project Manager sends initial communication
5. **Engage required roles:**
   - **Tech Lead/Developers**: For technical troubleshooting
   - **Security Champion**: If security-related
   - **QA Engineer**: For testing verification
   - **Customer Support Liaison**: For user communication

### Mitigation (15-60 minutes)
1. **Decide on approach:**
   - **Rollback** to last known-good release (preferred if issue is severe)
   - **Hot-fix** and fast-forward deploy (if fix is quick and safe)
   - **Feature flag disable** (if feature-flagged)
   - **Decision maker**: Incident Commander with input from Tech Lead and Product Manager
2. **Execute mitigation** - Developers and Release Manager
3. **Verify fix** - QA Engineer runs smoke tests
4. **Monitor metrics** - Data Analyst confirms issue resolved

### Recovery and Communication
1. **All-clear notification** - Project Manager communicates to stakeholders
2. **Support team update** - Customer Support Liaison briefs support team
3. **Triage root cause** - Tech Lead leads with Developers
4. **Capture action items** - Project Manager documents
5. **Schedule post-incident review** - Project Manager schedules within 48 hours

### Post-Incident Review (Blameless)
- **Facilitator**: Project Manager
- **Attendees**: All involved roles (Developers, Release Manager, QA Engineer, etc.)
- **Purpose**: Learn and improve, not assign blame
- **Outputs**: Action items with owners and timelines
- **Follow-up**: Review action items in weekly sync

**Escalation for Major Incidents**: Incident Commander escalates to Product Manager → Leadership if user impact is severe or prolonged.

See [octoacme-risks-and-communication.md](octoacme-risks-and-communication.md) for escalation paths.

## Release Notes Template
**Owner**: Technical Writer  
**Collaborators**: Product Manager, Developers, Release Manager

- **Release name / number:**
- **Date:**
- **Summary:** Brief overview of the release
- **Notable changes:**
  - New features (from Product Manager and UX Designer)
  - Improvements (from Developers)
  - Bug fixes (from QA Engineer)
  - Security updates (from Security Champion, if applicable)
- **Migration steps** (if any): Clear instructions from Technical Writer
- **Known issues:** Documented by QA Engineer
- **Documentation links:** Updated by Technical Writer
- **Support contacts:** Customer Support Liaison information

**Review process**: Product Manager and Release Manager review before publication.

See [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) for role definitions. Related to issue #5: https://github.com/rolling-falling/skills-scale-institutional-knowledge-using-copilot-spaces/issues/5

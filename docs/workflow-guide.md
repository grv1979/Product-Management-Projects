# Workflow Guide

A step-by-step guide for using this repository to manage product development from idea to launch.

## Table of Contents

1. [Project Lifecycle](#project-lifecycle)
2. [Creating a New Project](#creating-a-new-project)
3. [Documentation Workflow](#documentation-workflow)
4. [Review and Approval Process](#review-and-approval-process)
5. [Tracking Progress](#tracking-progress)
6. [Post-Launch Activities](#post-launch-activities)

## Project Lifecycle

```
Idea → Discovery → Planning → Development → Testing → Launch → Iterate
  ↓        ↓          ↓            ↓           ↓        ↓         ↓
Brief   Research    PRD      Implementation   QA    Release   Metrics
```

### Phase Details

| Phase | Duration | Key Activities | Deliverables |
|-------|----------|----------------|--------------|
| **Discovery** | 1-2 weeks | User research, market analysis, feasibility | Research summary |
| **Planning** | 2-4 weeks | PRD creation, design, technical planning | PRD, designs, tech spec |
| **Development** | 4-12 weeks | Implementation, code reviews | Working software |
| **Testing** | 1-2 weeks | QA, user testing, bug fixes | Test reports |
| **Launch** | 1 week | Deployment, monitoring, support | Production release |
| **Iterate** | Ongoing | Collect feedback, measure metrics | Updates, improvements |

## Creating a New Project

### Step 1: Project Initiation

1. **Create Project Directory**
   ```bash
   cd projects/
   cp -r project-template/ my-new-project/
   cd my-new-project/
   ```

2. **Initialize Project Charter** (Optional for large projects)
   - Copy `templates/Project-Charter-Template.md` to your project folder
   - Fill in executive summary, scope, stakeholders, timeline
   - Get sponsor approval

3. **Set Up Project Structure**
   ```
   my-new-project/
   ├── README.md              # Project overview
   ├── PRD.md                 # Product requirements
   ├── technical-spec.md      # Technical design
   ├── user-stories/          # User stories folder
   │   ├── epic-1.md
   │   └── story-001.md
   ├── designs/               # Design files and mockups
   ├── research/              # User research and data
   └── meeting-notes/         # Decision logs
   ```

### Step 2: Discovery Phase

**Goals:**
- Understand the problem
- Validate with users
- Assess feasibility

**Activities:**
1. **User Research**
   - Conduct user interviews
   - Analyze usage data
   - Survey target audience
   - Document findings in `research/`

2. **Competitive Analysis**
   - Research competitors
   - Identify gaps and opportunities
   - Document insights

3. **Technical Feasibility**
   - Consult with engineering
   - Identify technical constraints
   - Assess effort and complexity

**Deliverables:**
- Research summary document
- User personas
- Problem statement

### Step 3: Planning Phase

**Goals:**
- Define solution
- Create detailed requirements
- Get stakeholder alignment

**Activities:**

1. **Create PRD**
   - Copy `templates/PRD-Template.md` to your project
   - Fill in all sections:
     - Problem statement (from discovery)
     - Goals and objectives
     - Requirements and acceptance criteria
     - Success metrics
     - Timeline and milestones
   - Link to research and data

2. **Design Phase**
   - Create wireframes/mockups
   - Define user flows
   - Store designs in `designs/` folder
   - Link designs in PRD

3. **Technical Planning**
   - Copy `templates/Technical-Spec-Template.md`
   - Define architecture
   - Plan API design
   - Identify integration points
   - Estimate complexity

4. **Break Down Work**
   - Create epics for major features
   - Write user stories using template
   - Estimate story points
   - Prioritize backlog

**Deliverables:**
- Completed PRD
- Design mockups
- Technical specification
- Prioritized backlog of user stories

## Documentation Workflow

### Writing Documents

1. **Start with Template**
   - Copy appropriate template from `templates/`
   - Rename for your project
   - Set status to "Draft"

2. **Fill in Content**
   - Work section by section
   - Add specifics, remove generic placeholders
   - Link related documents
   - Add diagrams or mockups

3. **Self-Review**
   - Check for completeness
   - Verify all required sections filled
   - Proofread for clarity and typos
   - Ensure consistent terminology

4. **Update Status**
   - Change status from "Draft" to "In Review"
   - Set review deadline
   - Identify reviewers

### Document Linking

Create a web of connected documents:

**In PRD**, link to:
- User research findings
- Design mockups
- Technical specification
- Related projects

**In Technical Spec**, link to:
- PRD for requirements
- API documentation
- Architecture diagrams
- Deployment procedures

**In User Stories**, link to:
- Parent epic
- PRD section
- Design mockups
- Related stories

## Review and Approval Process

### Step 1: Request Review

1. **Identify Reviewers**
   - Product team: For requirements and scope
   - Engineering: For feasibility and technical approach
   - Design: For UX considerations
   - Stakeholders: For business alignment

2. **Share Document**
   - Update document status to "In Review"
   - Send notification with:
     - Link to document
     - What you need feedback on
     - Review deadline
     - How to provide feedback

3. **Provide Context**
   - Brief summary of what's new/changed
   - Specific questions or concerns
   - Areas needing most attention

### Step 2: Collect Feedback

**Methods:**
- Comments in the document
- GitHub pull request reviews
- Synchronous review meetings
- Async Slack/email discussions

**Organize Feedback:**
- Categorize: Must-fix vs. Nice-to-have
- Prioritize: Blockers first
- Track: Use checklist of feedback items

### Step 3: Incorporate Feedback

1. **Address Each Comment**
   - Implement changes
   - Respond if not implementing (with rationale)
   - Ask clarifying questions

2. **Document Changes**
   - Update changelog
   - Note major decisions
   - Track version number

3. **Request Re-review (if needed)**
   - For major changes
   - From stakeholders who requested changes
   - Set new deadline

### Step 4: Approval

**Approval Criteria:**
- All blockers resolved
- Required stakeholders have approved
- Document is complete and clear

**Document Approval:**
- Update status to "Approved"
- Record approver names and dates
- Archive draft versions
- Announce approval to team

**Approval Matrix:**

| Document Type | Required Approvers |
|--------------|-------------------|
| PRD | Product Manager, Engineering Lead, Sponsor |
| Technical Spec | Engineering Lead, Architect, Product Manager |
| User Stories | Product Owner |
| Project Charter | Executive Sponsor |

## Tracking Progress

### During Development

1. **Status Updates**
   - Update project README regularly
   - Track completion of milestones
   - Note blockers or risks

2. **User Story Tracking**
   - Mark stories as: To Do → In Progress → Review → Done
   - Update story status in document
   - Link to pull requests

3. **Decision Log**
   - Document important decisions
   - Explain rationale
   - Note alternatives considered
   - Store in `meeting-notes/decisions.md`

4. **Risk Management**
   - Maintain risk register in PRD
   - Update probability and impact
   - Track mitigation actions

### Status Communication

**Daily:** Team stand-ups
- What's done
- What's in progress
- Blockers

**Weekly:** Stakeholder updates
- Milestone progress
- Key accomplishments
- Upcoming milestones
- Risks and issues

**Monthly:** Executive summary
- Overall project health
- Budget and timeline status
- Major decisions or changes

## Post-Launch Activities

### Launch Checklist

- [ ] Production deployment successful
- [ ] Monitoring and alerts configured
- [ ] Documentation updated
- [ ] Team trained
- [ ] Users notified
- [ ] Support prepared

### Measuring Success

1. **Track Metrics**
   - Review success metrics defined in PRD
   - Set up dashboards
   - Collect baseline and ongoing data

2. **Gather Feedback**
   - User surveys
   - Support tickets
   - Usage analytics
   - Stakeholder input

3. **Iterate**
   - Create backlog of improvements
   - Prioritize based on impact
   - Plan next iteration

### Retrospective

**Within 2 weeks of launch:**

1. **Team Retrospective**
   - What went well?
   - What could be improved?
   - Action items for next project

2. **Document Learnings**
   - Update best practices
   - Share with broader team
   - Archive project for future reference

3. **Close Project**
   - Update project status to "Complete"
   - Archive working documents
   - Release team resources
   - Celebrate success! 🎉

### Project Archive

Move to archived state:
```
projects/
├── active/
│   └── current-project/
└── archived/
    └── 2026-Q1-completed-project/
```

Ensure archived projects include:
- Final PRD
- Technical documentation
- Lessons learned
- Key metrics and outcomes

## Quick Reference

### New Project Checklist

- [ ] Create project directory from template
- [ ] Write project charter (if needed)
- [ ] Conduct discovery research
- [ ] Create PRD
- [ ] Get PRD approved
- [ ] Create technical specification
- [ ] Break down into user stories
- [ ] Set up tracking and communication
- [ ] Kick off development
- [ ] Regular status updates
- [ ] Launch
- [ ] Measure and iterate

### Key Documents by Phase

| Phase | Required Documents | Optional Documents |
|-------|-------------------|-------------------|
| Discovery | Research findings | Competitive analysis |
| Planning | PRD, User stories | Project charter, Technical spec |
| Development | Technical spec | Architecture diagrams, API docs |
| Testing | Test plans | QA reports |
| Launch | Launch checklist | Communication plan |
| Post-Launch | Retrospective | Success metrics report |

---

## Need Help?

- Review [Best Practices Guide](best-practices.md)
- Check [Templates](../templates/)
- See [Sample Project](../projects/sample-project/)
- Contact Product Management team

**Last Updated**: 2026-02-05

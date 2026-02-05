# Product Management Best Practices

This guide outlines best practices for product management documentation and workflow within this repository.

## Table of Contents

1. [Documentation Standards](#documentation-standards)
2. [Writing Effective PRDs](#writing-effective-prds)
3. [User Story Guidelines](#user-story-guidelines)
4. [Technical Documentation](#technical-documentation)
5. [Collaboration and Communication](#collaboration-and-communication)
6. [Version Control](#version-control)
7. [Review Process](#review-process)

## Documentation Standards

### General Principles

1. **Clarity Over Brevity**: Be clear and comprehensive rather than concise but ambiguous
2. **Audience-Aware**: Write for your intended audience's technical level
3. **Maintain Context**: Explain the "why" behind decisions, not just the "what"
4. **Keep Updated**: Documents should reflect current state, not historical plans
5. **Link Liberally**: Connect related documents for easy navigation

### Document Structure

Every document should have:
- **Header Information**: Title, author, date, version, status
- **Executive Summary**: Quick overview for busy stakeholders
- **Table of Contents**: For longer documents (>2 pages)
- **Clear Sections**: Logical flow from problem → solution → implementation
- **Changelog**: Track significant changes and decisions
- **Approval Section**: Clear sign-off from stakeholders

### Writing Style

- Use **active voice**: "The system processes requests" not "Requests are processed"
- Be **specific**: "Reduce load time to <2 seconds" not "Make it faster"
- Use **consistent terminology**: Pick one term and stick with it
- Include **examples**: Concrete examples clarify abstract concepts
- Format for **scannability**: Use headers, bullets, tables, and white space

## Writing Effective PRDs

### Before You Write

1. **Do Your Research**
   - User research and interviews
   - Competitive analysis
   - Technical feasibility assessment
   - Market data and trends

2. **Define Success**
   - What problem are we solving?
   - How will we measure success?
   - What's the minimum viable solution?

3. **Identify Stakeholders**
   - Who needs to approve?
   - Who will implement?
   - Who will use?

### PRD Essentials

A good PRD must include:

✅ **Clear Problem Statement**
- What's broken or missing?
- Who is affected?
- What's the impact?

✅ **Measurable Goals**
- Specific, quantifiable objectives
- Timeline for achievement
- Success metrics and KPIs

✅ **Well-Defined Requirements**
- Functional requirements (what it does)
- Non-functional requirements (how well it does it)
- Acceptance criteria for each requirement

✅ **User Perspective**
- User personas
- User journeys
- Use cases and scenarios

✅ **Constraints and Dependencies**
- Technical limitations
- Resource constraints
- External dependencies

✅ **Timeline and Milestones**
- Key dates and deadlines
- Phase-based delivery plan
- Risk mitigation for delays

### Common PRD Mistakes to Avoid

❌ **Jumping to Solutions**: Focus on the problem first  
❌ **Vague Requirements**: "User-friendly" means nothing without specifics  
❌ **Missing Priorities**: Everything can't be P0  
❌ **Ignoring Constraints**: Acknowledge technical and resource limitations  
❌ **No Success Metrics**: Define how you'll measure success  
❌ **Scope Creep**: Keep nice-to-haves separate from must-haves  

## User Story Guidelines

### The 3 C's of User Stories

1. **Card**: Brief description capturing the essence
2. **Conversation**: Details emerge through discussion
3. **Confirmation**: Acceptance criteria define done

### Writing Good User Stories

**INVEST Criteria:**
- **I**ndependent: Can be developed separately
- **N**egotiable: Details can be discussed
- **V**aluable: Delivers value to users
- **E**stimable: Team can estimate effort
- **S**mall: Can be completed in one sprint
- **T**estable: Has clear acceptance criteria

**Format:**
```
As a [user role]
I want [action/capability]
So that [benefit/value]
```

**Example:**
```
As a mobile user
I want to receive push notifications for order updates
So that I stay informed without checking the app constantly
```

### Acceptance Criteria

Use Given-When-Then format:
```
Given [initial context]
When [action occurs]
Then [expected outcome]
```

**Example:**
```
Given I have an active order
When the order status changes to "Shipped"
Then I receive a push notification within 5 minutes
```

### Story Sizing

Use story points (Fibonacci sequence: 1, 2, 3, 5, 8, 13, 21):
- **1-2 points**: Simple changes, clear implementation
- **3-5 points**: Moderate complexity, some unknowns
- **8+ points**: Complex, should be broken down

If a story is >8 points, consider breaking it into smaller stories.

## Technical Documentation

### Architecture Documentation

Good technical documentation includes:

1. **High-Level Overview**
   - System components and their relationships
   - Technology stack with justification
   - Integration points

2. **Detailed Design**
   - Data models and schemas
   - API specifications
   - Security considerations

3. **Operational Concerns**
   - Deployment process
   - Monitoring and alerting
   - Performance requirements

### API Documentation

Every API should document:
- Endpoint path and HTTP method
- Request parameters and body schema
- Response format and status codes
- Authentication requirements
- Error handling
- Example requests and responses

### Code Comments vs. Documentation

- **Code comments**: Explain complex logic, non-obvious decisions
- **External docs**: Explain architecture, API contracts, user guides
- **Don't duplicate**: Code should be self-documenting where possible

## Collaboration and Communication

### Stakeholder Management

1. **Identify Early**: Map stakeholders at project start
2. **Understand Needs**: What do they care about?
3. **Communicate Proactively**: Don't wait for them to ask
4. **Right Level of Detail**: Executives need summaries, engineers need specs

### Effective Meetings

**Before:**
- Clear agenda shared in advance
- Pre-read materials sent early
- Defined goals and desired outcomes

**During:**
- Start and end on time
- Assign note-taker
- Capture action items with owners

**After:**
- Share notes within 24 hours
- Track action items to completion
- Follow up on open questions

### Async Communication

For distributed teams:
- Document decisions in writing
- Use comments for discussions
- Timestamp important updates
- Respect time zones

## Version Control

### Document Versioning

**Version Format**: MAJOR.MINOR
- **MAJOR**: Significant changes affecting scope or approach
- **MINOR**: Small updates, clarifications, additions

**Example:**
- 1.0: Initial approved version
- 1.1: Added clarification to requirements
- 2.0: Major scope change after stakeholder feedback

### Changelog Best Practices

Track:
- What changed
- Why it changed
- Who requested/approved the change
- When it changed

**Example:**
```markdown
## Changelog

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 2.0 | 2026-02-10 | Jane Doe | Added mobile requirements per exec feedback |
| 1.1 | 2026-02-05 | John Smith | Clarified API specifications |
| 1.0 | 2026-02-01 | Jane Doe | Initial approved version |
```

### Git Commit Messages

Follow convention:
```
<type>: <subject>

<body (optional)>

<footer (optional)>
```

**Types:**
- `docs`: Documentation changes
- `feat`: New feature specifications
- `fix`: Corrections or clarifications
- `refactor`: Reorganization without content change

## Review Process

### Document Review Checklist

Before requesting review:

**Content:**
- [ ] Problem clearly defined
- [ ] Goals are specific and measurable
- [ ] All requirements have acceptance criteria
- [ ] Success metrics defined
- [ ] Timeline realistic
- [ ] Dependencies identified
- [ ] Risks acknowledged

**Quality:**
- [ ] No typos or grammatical errors
- [ ] Consistent terminology
- [ ] Clear and concise language
- [ ] Appropriate level of detail
- [ ] Supporting data or research linked

**Process:**
- [ ] Right stakeholders identified for review
- [ ] Review deadline specified
- [ ] Feedback mechanism clear

### Incorporating Feedback

1. **Acknowledge**: Respond to all feedback
2. **Clarify**: Ask questions if feedback is unclear
3. **Evaluate**: Not all feedback must be incorporated
4. **Document**: Track what changed and why
5. **Re-review**: If major changes, request another review

### Approval Process

Clear approval criteria:
- Who must approve (blockers)
- Who should review (advisors)
- Timeline for approval
- What happens if no response

Document approvals:
- Name and role
- Date
- Signature or electronic confirmation

## Continuous Improvement

### Retrospectives

After each project:
- What went well?
- What could be improved?
- Action items for next time

### Template Evolution

Templates should evolve:
- Gather feedback from users
- Update based on lessons learned
- Remove unused sections
- Add commonly needed sections

### Knowledge Sharing

- Share successful patterns
- Document anti-patterns
- Host "lunch and learns"
- Maintain FAQ document

---

## Quick Reference

### Document Lifecycle

1. **Draft**: Initial creation, work in progress
2. **Review**: Shared with stakeholders for feedback
3. **Revised**: Incorporating feedback
4. **Approved**: Stakeholder sign-off
5. **Active**: Currently being executed
6. **Complete**: Delivered and closed
7. **Archived**: Historical reference

### Key Questions Before Publishing

- [ ] Is the problem clearly defined?
- [ ] Are success criteria measurable?
- [ ] Have all stakeholders reviewed?
- [ ] Are risks and dependencies identified?
- [ ] Is the timeline realistic?
- [ ] Are requirements testable?
- [ ] Is this the minimum viable scope?

---

**Remember**: Good documentation is living documentation. Keep it updated as the project evolves!

**Last Updated**: 2026-02-05

# Contributing to Product Management Projects

Thank you for contributing to our product management documentation! This guide will help you understand how to add new projects and maintain high-quality documentation.

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [Adding a New Project](#adding-a-new-project)
4. [Documentation Standards](#documentation-standards)
5. [Review Process](#review-process)
6. [Best Practices](#best-practices)

## Code of Conduct

### Our Standards

- **Be Respectful**: Treat everyone with respect and consideration
- **Be Collaborative**: Work together towards common goals
- **Be Professional**: Maintain professional communication
- **Be Constructive**: Provide actionable feedback
- **Be Inclusive**: Welcome diverse perspectives

### Expected Behavior

✅ Provide constructive feedback  
✅ Accept constructive criticism gracefully  
✅ Focus on what's best for the project  
✅ Show empathy towards others  
✅ Be open to learning  

❌ Personal attacks or insults  
❌ Trolling or inflammatory comments  
❌ Publishing private information  
❌ Dismissing others' contributions  
❌ Other unprofessional conduct  

## Getting Started

### Prerequisites

Before contributing, familiarize yourself with:
- Repository structure and organization
- [Best Practices Guide](docs/best-practices.md)
- [Workflow Guide](docs/workflow-guide.md)
- Available templates

### Tools You'll Need

- Git for version control
- Markdown editor (VS Code, Typora, or similar)
- Access to design tools (if adding mockups)
- Access to this repository

### First-Time Contributors

1. **Explore the Repository**
   - Browse existing projects
   - Read through templates
   - Review documentation guides

2. **Start Small**
   - Fix a typo
   - Update outdated information
   - Add clarification to existing docs

3. **Ask Questions**
   - Reach out to maintainers
   - Join team discussions
   - Propose ideas before major work

## Adding a New Project

### Step 1: Plan Your Project

Before creating project documentation:

**Checklist:**
- [ ] Clear problem statement
- [ ] Identified stakeholders
- [ ] Preliminary research done
- [ ] Alignment with company goals
- [ ] Approval to proceed (if required)

### Step 2: Set Up Project Structure

1. **Create Project Directory**
   ```bash
   cd projects/
   mkdir your-project-name
   cd your-project-name
   ```

2. **Copy Required Templates**
   ```bash
   # Copy PRD template
   cp ../../templates/PRD-Template.md ./PRD.md
   
   # Copy other templates as needed
   cp ../../templates/Technical-Spec-Template.md ./technical-spec.md
   ```

3. **Create Necessary Folders**
   ```bash
   mkdir user-stories
   mkdir designs
   mkdir research
   mkdir meeting-notes
   ```

4. **Create Project README**
   ```markdown
   # [Project Name]
   
   ## Quick Links
   - [PRD](PRD.md)
   - [Technical Specification](technical-spec.md)
   - [User Stories](user-stories/)
   
   ## Status
   **Current Phase**: [Discovery/Planning/Development/Testing/Launch]
   **Last Updated**: [Date]
   
   ## Team
   - Product Manager: [Name]
   - Engineering Lead: [Name]
   - Design Lead: [Name]
   
   ## Key Dates
   - Kickoff: [Date]
   - Design Complete: [Date]
   - Development Start: [Date]
   - Target Launch: [Date]
   ```

### Step 3: Fill in Documentation

1. **Start with PRD**
   - Follow the template structure
   - Be specific and measurable
   - Include research and data
   - Define success metrics

2. **Add Technical Details** (if applicable)
   - Architecture overview
   - API specifications
   - Data models
   - Security considerations

3. **Create User Stories**
   - One file per story or epic
   - Use consistent naming (e.g., `US-001-user-login.md`)
   - Link to parent PRD sections

4. **Include Supporting Materials**
   - Research findings
   - Design mockups
   - Meeting notes
   - Decision logs

### Step 4: Update Repository

1. **Update Main README**
   Add your project to the Active Projects table:
   ```markdown
   | Project Name | Status | Owner | Last Updated |
   |-------------|--------|-------|--------------|
   | Your Project | 📝 Planning | Your Name | 2026-02-05 |
   ```

2. **Add Project Status Badge**
   - 📝 Planning
   - 🔨 In Development
   - 🧪 Testing
   - 🚀 Launching
   - ✅ Complete
   - 🔄 Iterating

3. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "docs: Add [Project Name] initial documentation"
   git push
   ```

## Documentation Standards

### File Organization

```
projects/your-project/
├── README.md                    # Project overview
├── PRD.md                       # Product requirements
├── technical-spec.md            # Technical design
├── user-stories/                # User stories
│   ├── epic-1-authentication.md
│   ├── US-001-user-login.md
│   └── US-002-password-reset.md
├── designs/                     # Design files
│   ├── wireframes/
│   └── mockups/
├── research/                    # Research findings
│   ├── user-interviews.md
│   └── competitive-analysis.md
└── meeting-notes/               # Decision logs
    ├── decisions.md
    └── 2026-02-05-kickoff.md
```

### Naming Conventions

**Files:**
- Use lowercase with hyphens: `user-authentication-prd.md`
- Be descriptive: `mobile-app-technical-spec.md`
- Include dates for time-based docs: `2026-02-05-planning-meeting.md`

**Folders:**
- Plural nouns: `user-stories/`, `designs/`, `meeting-notes/`
- Lowercase with hyphens

### Markdown Formatting

**Headers:**
```markdown
# H1 for document title (use once)
## H2 for major sections
### H3 for subsections
#### H4 for detailed items
```

**Lists:**
```markdown
- Unordered lists for general items
1. Ordered lists for sequential steps
- [ ] Checkboxes for task lists
```

**Tables:**
```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data     | Data     | Data     |
```

**Links:**
```markdown
[Link Text](relative/path/to/file.md)
[External Link](https://example.com)
```

**Code:**
````markdown
`inline code`

```language
code block
```
````

### Document Metadata

Every document should start with:

```markdown
# Document Title

## Document Information
- **Author**: Your Name
- **Date**: YYYY-MM-DD
- **Version**: 1.0
- **Status**: Draft/In Review/Approved
- **Last Updated**: YYYY-MM-DD
```

### Version Control

**Version Numbers:**
- MAJOR.MINOR format (e.g., 1.0, 1.1, 2.0)
- Increment MAJOR for significant changes
- Increment MINOR for small updates

**Changelog:**
```markdown
## Changelog

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-02-05 | John | Initial version |
```

## Review Process

### Before Requesting Review

**Self-Review Checklist:**
- [ ] All sections completed
- [ ] No typos or grammatical errors
- [ ] Consistent terminology
- [ ] All links work
- [ ] Images/diagrams included
- [ ] Changelog updated
- [ ] Stakeholders identified

### Requesting Review

1. **Update Document Status**
   - Change from "Draft" to "In Review"

2. **Identify Reviewers**
   - Product: For requirements and scope
   - Engineering: For technical feasibility
   - Design: For UX considerations
   - Stakeholders: For business alignment

3. **Provide Context**
   ```markdown
   ## Review Request
   
   **Reviewers**: @john, @jane, @bob
   **Review By**: [Date]
   **Focus Areas**: 
   - Section 3: Technical approach
   - Section 5: Timeline feasibility
   ```

### Providing Feedback

**Good Feedback:**
```markdown
✅ "Section 3.2 API Design: Consider adding rate limiting. 
This will help prevent abuse and manage load."

✅ "The timeline in Section 7 seems aggressive. Based on similar 
projects, I'd recommend adding 2 weeks buffer."
```

**Poor Feedback:**
```markdown
❌ "This doesn't make sense."
❌ "I don't like this."
❌ "Wrong."
```

**Feedback Guidelines:**
- Be specific about what and where
- Explain why (rationale)
- Suggest alternatives when possible
- Be constructive and respectful
- Distinguish between must-fix and nice-to-have

### Incorporating Feedback

1. **Acknowledge All Feedback**
   - Thank reviewers
   - Clarify unclear feedback

2. **Prioritize**
   - Blockers first
   - Must-haves second
   - Nice-to-haves last

3. **Make Changes**
   - Update document
   - Document major decisions
   - Bump version number

4. **Respond to Reviewers**
   - Note what you changed
   - Explain what you didn't change (with rationale)

5. **Request Re-review (if needed)**
   - For major changes
   - From stakeholders who had concerns

### Approval

**Approval Checklist:**
- [ ] All required reviewers approved
- [ ] All blockers resolved
- [ ] Document complete and clear
- [ ] Changelog updated

**Document Approval:**
```markdown
## Approvals

| Role | Name | Date | Status |
|------|------|------|--------|
| Product Manager | John Doe | 2026-02-05 | ✅ Approved |
| Engineering Lead | Jane Smith | 2026-02-05 | ✅ Approved |
| Design Lead | Bob Johnson | 2026-02-06 | ✅ Approved |
```

## Best Practices

### Writing Tips

1. **Be Clear and Concise**
   - Use simple language
   - Avoid jargon (or define it)
   - One idea per sentence
   - Short paragraphs

2. **Be Specific**
   - ❌ "Make it fast"
   - ✅ "Reduce page load time to <2 seconds"

3. **Show, Don't Just Tell**
   - Include examples
   - Add diagrams
   - Provide mockups
   - Link to prototypes

4. **Provide Context**
   - Explain the "why"
   - Link related documents
   - Reference research/data
   - Note constraints

### Collaboration Tips

1. **Communicate Early and Often**
   - Share drafts early
   - Ask for input
   - Keep stakeholders informed

2. **Be Open to Feedback**
   - Don't take it personally
   - Consider all perspectives
   - Explain your reasoning

3. **Document Decisions**
   - Why we chose this approach
   - What alternatives were considered
   - Who made the decision

### Maintenance

**Keep Documents Current:**
- Update status regularly
- Archive completed projects
- Remove outdated information
- Link to latest versions

**Regular Reviews:**
- Quarterly: Review active projects
- Annual: Archive old projects
- As needed: Update templates and guides

## Questions?

If you have questions or need help:

1. **Check Documentation**
   - [Best Practices](docs/best-practices.md)
   - [Workflow Guide](docs/workflow-guide.md)
   - [Templates](templates/)

2. **Look at Examples**
   - Review existing projects
   - See how others structured their docs

3. **Ask for Help**
   - Reach out to maintainers
   - Ask in team channels
   - Schedule a quick sync

## Recognition

We appreciate all contributions! Contributors will be:
- Acknowledged in project documentation
- Recognized in team updates
- Celebrated for their impact

Thank you for helping us maintain high-quality product documentation! 🙌

---

**Last Updated**: 2026-02-05

# GitHub Issue Templates

> **These templates should be placed in `.github/ISSUE_TEMPLATE/` directory**

---

## 📁 File Structure

```
.github/
├── ISSUE_TEMPLATE/
│   ├── config.yml
│   ├── bug_report.yml
│   ├── feature_request.yml
│   ├── documentation.yml
│   ├── question.yml
│   └── community_idea.yml
└── pull_request_template.md
```

---

## 1️⃣ config.yml

**Purpose:** Configure issue template chooser

**Location:** `.github/ISSUE_TEMPLATE/config.yml`

```yaml
blank_issues_enabled: false
contact_links:
  - name: 💬 Discord Community
    url: https://discord.gg/P9suffJv
    about: Join our Discord for questions, discussions, and community support
  
  - name: 🌐 Community Discussions
    url: https://github.com/all-uto/all-uto/discussions
    about: For ideas, questions, and general discussions that don't fit issue templates
  
  - name: 📚 Documentation
    url: https://github.com/all-uto/all-uto/blob/main/README.md
    about: Read our comprehensive documentation and guides
  
  - name: 🎯 Round Table
    url: https://docs.google.com/spreadsheets/d/1MdaJZFffoT47z7x7S6Kc9nUwHssbwGVL1iemuZ7bde4/edit
    about: View our collaborative planning spreadsheet
```

---

## 2️⃣ Bug Report Template

**Purpose:** Report bugs and issues

**Location:** `.github/ISSUE_TEMPLATE/bug_report.yml`

```yaml
name: 🐛 Bug Report
description: Report a bug or unexpected behavior
title: "[BUG] "
labels: ["type: bug", "status: needs triage"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to report this bug! Please fill out the information below to help us fix it.

  - type: textarea
    id: description
    attributes:
      label: Bug Description
      description: A clear and concise description of what the bug is.
      placeholder: What happened?
    validations:
      required: true

  - type: textarea
    id: expected
    attributes:
      label: Expected Behavior
      description: What did you expect to happen?
      placeholder: What should have happened?
    validations:
      required: true

  - type: textarea
    id: actual
    attributes:
      label: Actual Behavior
      description: What actually happened?
      placeholder: What actually happened instead?
    validations:
      required: true

  - type: textarea
    id: steps
    attributes:
      label: Steps to Reproduce
      description: How can we reproduce this bug?
      placeholder: |
        1. Go to '...'
        2. Click on '...'
        3. Scroll down to '...'
        4. See error
    validations:
      required: true

  - type: textarea
    id: screenshots
    attributes:
      label: Screenshots or Videos
      description: If applicable, add screenshots or videos to help explain the problem.
      placeholder: Drag and drop images/videos here or paste links

  - type: dropdown
    id: branch
    attributes:
      label: Which ê/uto Branch?
      description: Which community branch does this relate to?
      options:
        - Main ê/uto
        - CoCreators/uto
        - Music/uto
        - Fashion/uto
        - bt/uto (Blue Team)
        - eco/uto
        - chill/uto
        - startup/uto
        - ai-alignment/uto
        - Multiple branches
        - Not branch-specific
    validations:
      required: true

  - type: dropdown
    id: severity
    attributes:
      label: Severity
      description: How severe is this bug?
      options:
        - Critical (blocks all work)
        - High (major feature broken)
        - Medium (feature partially broken)
        - Low (minor issue)
    validations:
      required: true

  - type: textarea
    id: environment
    attributes:
      label: Environment
      description: What environment are you using?
      placeholder: |
        - OS: [e.g. macOS 14, Windows 11, Ubuntu 22.04]
        - Browser: [e.g. Chrome 120, Firefox 121, Safari 17]
        - Tool/Version: [e.g. Obsidian 1.5.3, VSCode 1.85]
      value: |
        - OS: 
        - Browser: 
        - Tool/Version: 

  - type: textarea
    id: additional
    attributes:
      label: Additional Context
      description: Add any other context about the problem here.
      placeholder: Any other information that might be helpful?

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist
      options:
        - label: I have searched for similar issues before creating this one
          required: true
        - label: I have provided all the requested information
          required: true
        - label: This issue is related to ê/uto projects (not a personal support request)
          required: true

  - type: markdown
    attributes:
      value: |
        ---
        **Thank you for helping improve ê/uto!** 🌍
        
        Someone will review this issue soon. In the meantime, feel free to join our [Discord](https://discord.gg/P9suffJv) for community support.
```

---

## 3️⃣ Feature Request Template

**Purpose:** Suggest new features or enhancements

**Location:** `.github/ISSUE_TEMPLATE/feature_request.yml`

```yaml
name: ✨ Feature Request
description: Suggest a new feature or enhancement
title: "[FEATURE] "
labels: ["type: feature", "status: needs triage"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        Thanks for suggesting a new feature! Help us understand your idea by filling out the information below.

  - type: textarea
    id: problem
    attributes:
      label: Problem Statement
      description: What problem does this feature solve? What need does it address?
      placeholder: "I'm frustrated when... / It would be helpful to..."
    validations:
      required: true

  - type: textarea
    id: solution
    attributes:
      label: Proposed Solution
      description: How would you like this feature to work?
      placeholder: Describe your ideal implementation
    validations:
      required: true

  - type: textarea
    id: alternatives
    attributes:
      label: Alternative Solutions
      description: Have you considered any alternative approaches?
      placeholder: What other ways could we solve this?

  - type: textarea
    id: impact
    attributes:
      label: Impact on p(e/uto)
      description: How does this feature increase the probability of effective utopia?
      placeholder: How does this move us toward our mission?
    validations:
      required: true

  - type: dropdown
    id: branch
    attributes:
      label: Which ê/uto Branch?
      description: Which community branch would benefit most?
      options:
        - Main ê/uto
        - CoCreators/uto
        - Music/uto
        - Fashion/uto
        - bt/uto (Blue Team)
        - eco/uto
        - chill/uto
        - startup/uto
        - ai-alignment/uto
        - Multiple branches
        - All branches
    validations:
      required: true

  - type: dropdown
    id: priority
    attributes:
      label: Priority
      description: How urgent is this feature?
      options:
        - Critical (needed immediately)
        - High (important for success)
        - Medium (nice to have soon)
        - Low (future consideration)
    validations:
      required: true

  - type: textarea
    id: mockups
    attributes:
      label: Mockups or Examples
      description: Include mockups, diagrams, or examples from other projects
      placeholder: Drag and drop images here or paste links

  - type: textarea
    id: implementation
    attributes:
      label: Implementation Ideas
      description: Do you have thoughts on how to implement this?
      placeholder: Technical considerations, tools needed, etc.

  - type: checkboxes
    id: involvement
    attributes:
      label: Your Involvement
      description: How would you like to contribute?
      options:
        - label: I'm willing to help design this feature
        - label: I'm willing to help implement this feature
        - label: I'm willing to help test this feature
        - label: I'm willing to help document this feature
        - label: I'm just suggesting the idea

  - type: textarea
    id: additional
    attributes:
      label: Additional Context
      description: Anything else we should know?
      placeholder: Any other relevant information

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist
      options:
        - label: I have searched for similar feature requests
          required: true
        - label: This aligns with ê/uto's mission and values
          required: true
        - label: I have provided all requested information
          required: true

  - type: markdown
    attributes:
      value: |
        ---
        **Thank you for helping shape the future of ê/uto!** 🚀
        
        We'll review your suggestion and discuss it with the community. Join the conversation in [Discord](https://discord.gg/P9suffJv)!
```

---

## 4️⃣ Documentation Template

**Purpose:** Report documentation issues or improvements

**Location:** `.github/ISSUE_TEMPLATE/documentation.yml`

```yaml
name: 📚 Documentation
description: Report documentation issues or suggest improvements
title: "[DOCS] "
labels: ["type: documentation", "status: needs triage"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        Thanks for helping improve our documentation! Clear docs are essential for community growth.

  - type: dropdown
    id: doc-type
    attributes:
      label: Documentation Type
      description: What kind of documentation issue is this?
      options:
        - Missing documentation
        - Incorrect/outdated information
        - Unclear explanation
        - Broken links
        - Typo or formatting
        - New guide needed
        - Translation needed
        - Other
    validations:
      required: true

  - type: input
    id: location
    attributes:
      label: Document Location
      description: Which document needs attention?
      placeholder: "e.g., README.md, docs/onboarding/guide.md, GMSF framework"
    validations:
      required: true

  - type: textarea
    id: current
    attributes:
      label: Current Content
      description: What does the documentation currently say? (if applicable)
      placeholder: Quote the current text or describe what's missing

  - type: textarea
    id: suggested
    attributes:
      label: Suggested Improvement
      description: What should it say instead? Or what should be added?
      placeholder: Your proposed change or addition
    validations:
      required: true

  - type: textarea
    id: why
    attributes:
      label: Why This Matters
      description: Why is this improvement important?
      placeholder: How does this help users or the community?
    validations:
      required: true

  - type: dropdown
    id: audience
    attributes:
      label: Target Audience
      description: Who is this documentation primarily for?
      options:
        - New members
        - Contributors
        - Developers
        - Community leaders
        - Everyone
        - Specific branch members
    validations:
      required: true

  - type: textarea
    id: additional
    attributes:
      label: Additional Context
      description: Screenshots, links to similar docs, or other helpful info
      placeholder: Any other information that helps

  - type: checkboxes
    id: involvement
    attributes:
      label: Your Involvement
      options:
        - label: I'm willing to write/update this documentation
        - label: I'm willing to review documentation changes
        - label: I'm just reporting the issue

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist
      options:
        - label: I have checked if this documentation exists elsewhere
          required: true
        - label: I have provided clear suggestions for improvement
          required: true

  - type: markdown
    attributes:
      value: |
        ---
        **Thank you for improving our documentation!** 📖
        
        Clear docs help everyone contribute more effectively. Your help is appreciated!
```

---

## 5️⃣ Question Template

**Purpose:** Ask questions about ê/uto

**Location:** `.github/ISSUE_TEMPLATE/question.yml`

```yaml
name: ❓ Question
description: Ask a question about ê/uto
title: "[QUESTION] "
labels: ["type: question", "status: needs triage"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        Have a question? We're here to help! 
        
        **Note:** For real-time help, [Discord](https://discord.gg/P9suffJv) is usually faster!

  - type: dropdown
    id: category
    attributes:
      label: Question Category
      description: What's your question about?
      options:
        - Getting started / Onboarding
        - Technical / Development
        - Community / Culture
        - Projects / Collaboration
        - Tools / Setup
        - Philosophy / Mission
        - Branch-specific
        - Other
    validations:
      required: true

  - type: dropdown
    id: branch
    attributes:
      label: Related Branch (if applicable)
      options:
        - Not branch-specific
        - Main ê/uto
        - CoCreators/uto
        - Music/uto
        - Fashion/uto
        - bt/uto (Blue Team)
        - eco/uto
        - chill/uto
        - startup/uto
        - ai-alignment/uto

  - type: textarea
    id: question
    attributes:
      label: Your Question
      description: What would you like to know?
      placeholder: Be as specific as possible
    validations:
      required: true

  - type: textarea
    id: context
    attributes:
      label: Context
      description: What are you trying to accomplish? What have you tried?
      placeholder: Help us understand your situation

  - type: textarea
    id: searched
    attributes:
      label: What Have You Already Tried?
      description: Where have you looked for an answer?
      placeholder: |
        - [ ] Searched documentation
        - [ ] Asked in Discord
        - [ ] Searched existing issues
        - [ ] Checked Round Table
        - [ ] Other: ___

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist
      options:
        - label: I have searched for similar questions
          required: true
        - label: This is not a bug report or feature request
          required: true

  - type: markdown
    attributes:
      value: |
        ---
        **We'll get back to you soon!** 💬
        
        For faster responses, consider asking in [Discord](https://discord.gg/P9suffJv) where the community can help immediately.
```

---

## 6️⃣ Community Idea Template

**Purpose:** Share ideas for community building, events, or culture

**Location:** `.github/ISSUE_TEMPLATE/community_idea.yml`

```yaml
name: 💡 Community Idea
description: Suggest events, rituals, or community initiatives
title: "[IDEA] "
labels: ["type: community", "status: needs triage"]
assignees: []

body:
  - type: markdown
    attributes:
      value: |
        Share your idea for building community and culture! 
        
        **#UTOideasMonday spirit** ✨

  - type: dropdown
    id: idea-type
    attributes:
      label: Idea Type
      description: What kind of idea is this?
      options:
        - Event (workshop, salon, concert, etc.)
        - Ritual or ceremony
        - Community program
        - Cross-branch collaboration
        - Cultural initiative
        - Onboarding improvement
        - Communication channel
        - Governance or process
        - Other
    validations:
      required: true

  - type: textarea
    id: idea
    attributes:
      label: The Idea
      description: What's your vision?
      placeholder: Paint the picture - what would this look like?
    validations:
      required: true

  - type: textarea
    id: why
    attributes:
      label: Why This Matters
      description: How does this serve the community and increase p(e/uto)?
      placeholder: What need does this address? What impact could it have?
    validations:
      required: true

  - type: textarea
    id: who
    attributes:
      label: Who Benefits
      description: Which community members would this serve?
      placeholder: New members? Specific branches? Everyone?

  - type: textarea
    id: how
    attributes:
      label: How It Could Work
      description: Initial thoughts on implementation
      placeholder: |
        - When/where would this happen?
        - What resources are needed?
        - Who would facilitate?
        - What's the timeline?

  - type: dropdown
    id: scope
    attributes:
      label: Scope
      description: How big is this initiative?
      options:
        - Small (can start immediately)
        - Medium (needs some planning)
        - Large (requires significant coordination)
        - Ongoing program
    validations:
      required: true

  - type: dropdown
    id: involvement
    attributes:
      label: Your Involvement Level
      description: How much can you contribute to this?
      options:
        - I'll lead this initiative
        - I'll co-lead with someone
        - I'll actively participate
        - I'll help when needed
        - I'm just suggesting the idea
    validations:
      required: true

  - type: textarea
    id: collaborators
    attributes:
      label: Potential Collaborators
      description: Who else might want to be involved?
      placeholder: Tag people or mention branches (@username)

  - type: textarea
    id: success
    attributes:
      label: What Does Success Look Like?
      description: How would we know this initiative is working?
      placeholder: What metrics or outcomes would show success?

  - type: checkboxes
    id: branches
    attributes:
      label: Relevant Branches
      description: Which branches could participate?
      options:
        - label: Main ê/uto
        - label: CoCreators/uto
        - label: Music/uto
        - label: Fashion/uto
        - label: bt/uto
        - label: eco/uto
        - label: chill/uto
        - label: startup/uto
        - label: ai-alignment/uto
        - label: All branches / Network-wide

  - type: textarea
    id: additional
    attributes:
      label: Additional Thoughts
      description: Anything else you want to share?
      placeholder: Inspiration, examples, concerns, questions...

  - type: checkboxes
    id: checklist
    attributes:
      label: Pre-submission Checklist
      options:
        - label: This idea aligns with ê/uto values
          required: true
        - label: I've thought about who this serves
          required: true
        - label: I'm open to feedback and iteration
          required: true

  - type: markdown
    attributes:
      value: |
        ---
        **Thank you for dreaming with us!** 🌟
        
        Great communities are built through ideas like yours. Let's discuss this together in [Discord](https://discord.gg/P9suffJv)!
        
        **#UTOideasMonday** · **#TechnoHeroThursday**
```

---

## 📝 Usage Instructions

### For Repository Maintainers

1. **Create the directory structure:**
   ```bash
   mkdir -p .github/ISSUE_TEMPLATE
   ```

2. **Add each template file:**
   - Copy each YAML file above into `.github/ISSUE_TEMPLATE/`
   - Name them exactly as specified

3. **Commit and push:**
   ```bash
   git add .github/
   git commit -m "feat: add issue templates"
   git push
   ```

4. **Test the templates:**
   - Go to your repo's Issues tab
   - Click "New Issue"
   - You should see all templates!

### For Contributors

When creating a new issue:

1. Click "New Issue"
2. Choose the appropriate template
3. Fill out all required fields
4. Be as specific as possible
5. Submit!

### Customization

**For Different Repositories:**
- Adjust branch options to match your repo
- Modify labels to match your label scheme
- Add/remove fields as needed
- Change severity/priority options

**For Different Communities:**
- Update Discord links
- Modify contact links in config.yml
- Adjust branch-specific options
- Change impact/mission phrasing

---

## 🏷️ Recommended Labels

Make sure these labels exist in your repository:

### Type Labels
- `type: bug` - Something isn't working
- `type: feature` - New functionality
- `type: documentation` - Documentation improvements
- `type: question` - Further information requested
- `type: community` - Community initiatives

### Status Labels
- `status: needs triage` - Needs initial review
- `status: confirmed` - Verified and accepted
- `status: in progress` - Someone is working on it
- `status: blocked` - Can't proceed yet
- `status: needs review` - Ready for review

### Priority Labels
- `priority: critical` - Urgent
- `priority: high` - Important
- `priority: medium` - Normal
- `priority: low` - Nice to have

### Difficulty Labels
- `good first issue` - Perfect for newcomers
- `beginner friendly` - Basic skills needed
- `intermediate` - Moderate experience
- `advanced` - Deep expertise required

### Branch Labels
- `branch: main` - Main ê/uto
- `branch: cocreators` - CoCreators/uto
- `branch: music` - Music/uto
- `branch: fashion` - Fashion/uto
- `branch: bt` - bt/uto (Blue Team)
- `branch: eco` - eco/uto
- `branch: chill` - chill/uto
- `branch: startup` - startup/uto
- `branch: ai-alignment` - ai-alignment/uto

---

## 🔗 Zettelkasten Links

**Upstream:**
- `[[contributing-guidelines]]` - How to contribute
- `[[community-network]]` - Branch structure

**Related:**
- `[[pr-template]]` - Pull request format
- `[[code-of-conduct]]` - Community standards
- `[[issue-management]]` - Triage process

**Downstream:**
- `[[bug-tracking]]` - Bug management
- `[[feature-planning]]` - Feature roadmap
- `[[community-ideas-board]]` - Idea collection

---

<div align="center">

**These templates help us build better, together.** 🚀

Part of the ê/uto Network

🌍 #technoheroism

</div>
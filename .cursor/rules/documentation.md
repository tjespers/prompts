---
description: Rule for maintaining and updating documentation across the AI Prompt Catalog repository.
globs:
  - "**/*.md"
  - "**/README.md"
alwaysApply: false
---
# Documentation Update Rule

## Trigger Conditions
This rule should be triggered when any of the following occurs:

### File Changes
- Any README.md file changes
- Any documentation file in any directory changes
- Any new documentation is added

### User Requests
When the user explicitly requests documentation updates with phrases like:
- "update docs"
- "improve documentation"
- "fix documentation"
- "review documentation"
- "clean up docs"

## Response Format
```json
{
  "response_type": "documentation_update",
  "action": "create|update|review|improve",
  "target_file": "string",
  "changes": {
    "sections": ["array of modified sections"],
    "formatting": ["array of formatting changes"],
    "validation": {
      "structure": boolean,
      "content": boolean,
      "formatting": boolean,
      "links": boolean,
      "emojis": boolean
    }
  }
}
```

## Required Actions

1. **Initial Assessment**
   - Identify the target file(s) from the request or changed files
   - Verify the file type and location
   - Check if the file follows the correct structure based on its type
   - Review existing content for documentation needs

2. **Documentation Structure**
   - Main README must follow:
     - Brief introduction with emoji and bold text
     - Table of contents with working links
     - Purpose section with bullet points
     - Repository structure (table format)
     - Contributing guidelines
     - A Friendly Note (only in main README)

   - Sub-READMEs must be focused and concise:
     - Clear title explaining the concept
     - Brief description of what the concept is
     - List of available items with brief descriptions
     - No usage instructions or best practices
     - No contributing guidelines
     - No meta-documentation information

3. **Directory Tree Format**
   ```
   | 📦 prompts |
   |------------|
   | ├── 📂 [folder](path/)          # Description |
   | │   ├── 📂 [subfolder](path/)   # Description |
   | └── 📂 [folder](path/)          # Description |
   ```

4. **Content Rules**
   - Self-contained concepts
   - No cross-referencing between READMEs
   - Focus on "what" not "how"
   - Consistent terminology
   - No redundant information
   - Emojis for section headers
   - Bold text for emphasis
   - Short, focused paragraphs

5. **Quality Checks**
   - Verify all internal links work
   - Ensure formatting is consistent
   - Check emoji usage is appropriate
   - Validate table structure
   - Confirm section spacing
   - Verify list formatting

## Validation Checklist
- [ ] Structure follows established pattern
- [ ] Content is focused and relevant
- [ ] Formatting is consistent
- [ ] Links are working
- [ ] Emojis are appropriate
- [ ] No meta-information in sub-READMEs
- [ ] No usage instructions in sub-READMEs
- [ ] No cross-references between READMEs
- [ ] No redundant descriptions
- [ ] Table formatting is correct
- [ ] Indentation is proper
- [ ] Section spacing is consistent
- [ ] List formatting is uniform

## Common Issues to Avoid
1. Cross-referencing between READMEs
2. Including usage instructions in sub-READMEs
3. Adding meta-documentation information
4. Creating redundant descriptions
5. Breaking self-containment
6. Incorrect table formatting
7. Missing emojis in headers

## Recovery Actions
1. Remove cross-references
2. Eliminate usage instructions
3. Focus content on concept
4. Remove redundant information
5. Restore self-containment
6. Fix table formatting
7. Add missing emojis

## Error Handling

If any of the following occur:
- Missing required sections
- Invalid formatting
- Broken links
- Inconsistent emoji usage
- Incorrect table structure
- Redundant information
- Meta-information in sub-READMEs

Report the issues and provide specific suggestions for resolution. 
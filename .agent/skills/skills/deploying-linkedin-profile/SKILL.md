---
name: deploying-linkedin-profile
description: Automates the deployment of professional content to a LinkedIn profile. Updates headlines, about sections, and experience details using browser automation. Use when the user wants to 'push', 'save', or 'update' their profile directly.
---

# LinkedIn Profile Deployer

This skill enables an agent to navigate to a LinkedIn profile and update specific sections (Headline, About, Experience) with new content. It assumes the agent has access to a browser tool and the user is logged into LinkedIn in that browser.

## When to use this skill
- Use when the user explicitly asks to "push changes to LinkedIn."
- Use when "deploying" a new profile draft or "updating" the live profile.

## Workflow
1. [ ] **Verify Source**: Ensure the new Headline, About, and Experience text is finalized.
2. [ ] **Navigate**: Open browser to `https://www.linkedin.com/in/[username]/`.
3. [ ] **Log-in Check**: Ensure the "Edit" pencil icons are visible. If not, ask the user to log in.
4. [ ] **Update Headline**: Click the intro edit icon, clear the "Headline" field, paste new text, and save.
5. [ ] **Update About**: Scroll to "About", click the edit icon, update the summary text, and save.
6. [ ] **Update Experience**: Locate the relevant company/role, click the edit icon for that entry, update the description, and save.
7. [ ] **Confirmation**: Verify the "Save" was successful and the changes are live.

## Instructions

### Browser Navigation Heuristics
- Use `open_browser_url` to go to the profile page.
- Use `click_browser_pixel` or `click_browser_text` on elements with `aria-label` like "Edit intro" or "Edit About".
- For text entry, use `type_browser_text` on fields identified by name (`headline`, `summary`) or placeholders.
- **Critical**: LinkedIn often uses modals. Ensure the modal is fully loaded before attempting to type.

### Safety Checks
- Always verify the "Save" button is clickable before proceeding.
- If a "Share with network" toggle appears, set it according to user preference (default to OFF unless specified).
- Confirm character limits (Headline: 220, About: 2600) are not exceeded BEFORE clicking save to avoid silent truncation.

## Resources
- [LinkedIn Profile Guidelines](https://www.linkedin.com/help/linkedin/answer/a522735)

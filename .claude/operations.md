---
name: operations_and_workflow
description: Operational skills, workflow requirements, and common mistakes to avoid for this repo
metadata:
  type: operations
  last_updated: 2026-07-29
---

# Repository Operations & Workflow Guide

## Critical: PR-First Workflow for Master

**REQUIRED:** All changes to `master` must go through a Pull Request first. Never commit directly to master.

**Workflow:**
1. Create feature branch: `git checkout -b descriptive-branch-name`
2. Make changes and commit
3. Push to remote: `git push -u origin descriptive-branch-name`
4. Create PR: `gh pr create --title "..." --body "..."`
5. Verify CI checks pass
6. Merge via GitHub UI or `gh pr merge [number]`

**Why:** Enables review, CI validation, and audit trail. Skipping this breaks the deployment safety model.

---

## GitHub & Git

### Commands to Know
- `gh pr create` — Create PRs programmatically
- `gh pr merge [number]` — Merge PRs (requires `--merge`, `--rebase`, or `--squash`)
- `git checkout -b [branch]` — Create and switch to feature branch
- `git push -u origin [branch]` — Push with upstream tracking

### Mistakes to Avoid
- ❌ **Direct commits to master** — Always use PR workflow
- ❌ **Force push** — Never `git push --force` unless absolutely necessary and approved
- ❌ **Amending published commits** — Create new commits instead
- ❌ **Skipping `--no-verify`** — Pre-commit hooks exist for a reason
- ❌ **Large monolithic PRs** — Keep changes focused and reviewable

---

## Blog Post Creation

### Front Matter Requirements (Critical)
Every blog post MUST have:
```yaml
---
title: "Post Title (conversational, may include question)"
tag: [Personal|Career|Technology|Presentation]
author_profile: true
toc: true
---
```

### Filename Format
`YYYY-MM-DD-Kebab-Case-Title.md` (e.g., `2026-07-29-Premature-AI-Evals.md`)

### Writing Style
- **Conversational & personal** — Use "I", show vulnerability
- **Opening hook** — Personal anecdote, question, or observation (not just a statement)
- **Concrete examples** — Ground ideas in real scenarios
- **Structure** — Use section breaks (`---` or `___`), headers, blockquotes
- **Call-to-action** — End with LinkedIn engagement or invitation to discuss
- **Length** — 800-2,500 words

**Reference:** `.claude/writing_style_guide.md` for detailed patterns and examples.

### Mistakes to Avoid
- ❌ **Missing front matter** — Post won't render without it
- ❌ **Wrong tag** — Use only established tags (Personal, Career, Technology, Presentation)
- ❌ **Generic opening** — Avoid dry introductions; start with a hook
- ❌ **No call-to-action** — Always invite reader engagement
- ❌ **Ignoring style guide** — Your voice is distinctive; maintain it

---

## CSS & Styling Issues

### Hero Section Spacing (Fixed)
**Issue:** `main { padding-top: 3em }` creates unwanted gap between nav and hero on homepage.

**Solution:** Use selector `.page__header ~ main { padding-top: 3em }` to only apply padding to pages with hero headers, not the homepage hero itself.

**Location:** `assets/css/main.scss` lines 394-401

**When editing CSS:**
- Test on both homepage (with hero) and regular pages (with `.page__header`)
- Verify no horizontal scroll on mobile (use `overflow-x: auto` containers, not body scroll)
- Use Minimal Mistakes theme defaults; don't override unless necessary
- Check screenshot after deployment to verify visual

### Common CSS Mistakes
- ❌ **Applying padding/margin to all `main` elements uniformly** — Hero pages need different spacing
- ❌ **Breaking responsive layout** — Always test on mobile
- ❌ **Overriding theme classes globally** — Use specific selectors instead
- ❌ **Forgetting to rebuild Jekyll** — Changes to SCSS require local `jekyll serve` restart

---

## Navigation & Site Structure

### Navigation Menu
**File:** `_data/navigation.yml`

- Main navigation links should match actual pages
- Sublinks group related content
- Test navigation after adding/removing pages
- External links (e.g., LinkedIn, consulting) work in navigation

**When updating:**
1. Add/remove menu item in `navigation.yml`
2. Verify link path exists (or is external)
3. Test in browser after rebuild

---

## Deployment & GitHub Pages

### Automatic Deployment
- Changes merged to `master` automatically deploy via GitHub Pages
- Build status visible in PR checks
- Site goes live at https://raulingaverage.dev

### Monitoring
- Check GitHub Pages build logs if deploy fails
- Verify site renders correctly after merge
- Test new content/features in browser (not just locally)

**Mistakes to avoid:**
- ❌ **Merging without verifying CI checks** — Wait for green checkmarks
- ❌ **Assuming local == production** — Always test the live site
- ❌ **Pushing large binaries** — Slows down CI/CD

---

## Resume & External Content

**Current Setup:**
- Resume is embedded Google Doc (not in repo)
- Updated externally at: `https://drive.google.com/file/d/13wMQcrEP8I6m47uyizx67oVRKuQ3JN3Y/preview`
- About page (`_pages/home.md`) highlights current and past roles

**When updating resume:**
- Update Google Doc directly
- Keep repo About page (`_pages/home.md`) in sync with major role changes
- Don't duplicate resume content in repo — embed external version

---

## Content & Tone

### Core Values Reflected in Posts
- Impact & contribution
- Continuous learning
- Equity & accessibility
- Authenticity & vulnerability
- Community & connection

### Recurring Topics
- Career transitions and growth
- Data analytics and engineering
- Personal development and goal-setting
- Social/civic advocacy (housing, transportation, diversity)
- Learning and education
- Work-life balance

**When writing:** Connect personal experience to these themes. Avoid generic advice without grounding.

---

## Quick Checklist Before Merging

- [ ] Feature branch created (not committing to master)
- [ ] PR created with clear title and body
- [ ] CI checks pass (GitHub Pages build succeeds)
- [ ] Blog post has complete front matter (if applicable)
- [ ] Writing follows style guide (if applicable)
- [ ] Links are functional
- [ ] No secrets or sensitive data in files
- [ ] Content tested in browser (not just local build)

---

## Tools & Environment

- **Ruby/Jekyll** — Local preview: `bundle exec jekyll serve`
- **GitHub CLI** — `gh pr create`, `gh pr merge`, etc.
- **Git** — Always use feature branches; PR workflow is mandatory
- **SCSS** — Custom styling in `assets/css/main.scss`; imports Minimal Mistakes theme

---

## When in Doubt

1. Reference `.claude/writing_style_guide.md` for blog content
2. Reference `CLAUDE.md` in repo root for project overview
3. Check recent commits (`git log -10`) to see patterns
4. Test in browser after deployment
5. Ask in PR comments or documentation if something is unclear


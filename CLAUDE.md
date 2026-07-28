# raulingaverage.dev

A personal blog and portfolio site for Raul Maldonado, built with Jekyll and hosted on GitHub Pages.

## Quick Start

- **Blog posts**: `_posts/` directory (Jekyll date-slug format: `YYYY-MM-DD-Kebab-Case-Title.md`)
- **Writing style guide**: `.claude/writing_style_guide.md` — reference this for tone, structure, and formatting conventions
- **Front matter**: All posts require Jekyll YAML front matter with title, tag, author_profile, toc
- **Local preview**: Jekyll site (Ruby/Bundler)

## Writing Conventions

**Before writing a new post, review `.claude/writing_style_guide.md`** which captures:
- Front matter structure and tags
- Tone and voice (conversational, personal, authentic)
- Organization patterns (hooks, section breaks, headings)
- Formatting conventions (blockquotes, lists, links, embedded media)
- Content patterns by post type (personal, career, technical, educational)
- Closing patterns and call-to-action

**Key principles:**
- Start with a compelling hook (personal anecdote, question, observation)
- Use first-person naturally; vulnerability is a strength
- Connect personal experience to broader themes
- Use blockquotes liberally for emphasis and attribution
- Include embedded media (tweets, videos, images) for visual interest
- End with reflection and invitation for engagement

## Core Values Reflected in Content

- **Impact & contribution**: Making a meaningful difference
- **Continuous learning**: Growth mindset, skill development
- **Equity & accessibility**: YIMBY/housing advocacy, diverse representation, knowledge sharing
- **Authenticity**: Honest about struggles and uncertainty
- **Community**: Connection and dialogue with readers

## Content Categories

**Tags** (used in front matter):
- `Personal` — Reflection, life updates, goal-setting
- `Career` — Professional growth, job transitions, workplace insights
- `Technology` — Technical analysis, emerging tech, tool reviews
- `Presentation` — Educational content, tips, frameworks

## Project Structure

```
.
├── _posts/                 # Blog posts (Jekyll format)
├── assets/                 # Images, CSS, other static assets
├── _config.yml            # Jekyll configuration
├── .claude/
│   └── writing_style_guide.md   # Detailed writing style reference
└── CLAUDE.md              # This file
```

## Git & Deployment Workflow

**REQUIRED: All changes to `master` must go through a Pull Request first.**

1. Create a feature branch: `git checkout -b descriptive-branch-name`
2. Make changes and commit with clear messages
3. Push to remote: `git push -u origin descriptive-branch-name`
4. GitHub will output a PR creation link — **open it** and create the PR
5. Wait for any CI checks to pass (GitHub Pages builds, tests)
6. Once PR is open and verified, merge it to `master` using the GitHub UI or `git merge --ff-only` locally
7. Verify the change is live on https://raulingaverage.dev

**Why:** PRs enable review, CI validation, and a clear audit trail. Merging directly to master skips these safety checks.

## Common Tasks

**Write a new blog post:**
1. Create file: `_posts/YYYY-MM-DD-Title.md`
2. Add Jekyll front matter (see style guide for template)
3. Reference `.claude/writing_style_guide.md` for tone and structure
4. Follow existing post patterns for your content type
5. Include hooks, sections, blockquotes, and calls-to-action

**Before committing:**
- Verify front matter is complete (title, tag, author_profile, toc)
- Check formatting: headers, links, blockquotes render correctly
- Ensure images/media URLs are valid
- Read through for tone consistency (see style guide)

**After committing and pushing:**
- Follow the Git & Deployment Workflow above (create PR, verify, then merge)

## Notes for Claude

When writing or editing posts for this site:
- Reference `.claude/writing_style_guide.md` to maintain voice and consistency
- This blog values authentic, personal reflection over polished impersonality
- Posts often weave personal narrative with broader insights or case studies
- The author is willing to show vulnerability and uncertainty
- Invite reader engagement; don't close doors to dialogue
- Connect work/career insights to larger themes (equity, community, impact)

## Resources

- **Site**: https://raulingaverage.dev
- **GitHub**: https://github.com/CloudChaoszero/CloudChaoszero.github.io
- **Author**: Raul Maldonado (@CloudChaoszero)

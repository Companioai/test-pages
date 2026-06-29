---
name: goodnesslover-advertorial
description: "Goodness Lover Page 1 advertorial skill. CSS standards, HTML patterns, voice rules, and quality gate for GL editorial pages."
category: copywriting
tags: [advertorial, goodnesslover, brand-layer, pre-sell, team-only]
requires_tools: write_file, terminal
seed: false
team: companio
---

# Goodness Lover — Page 1 Advertorial

**What this skill provides:** The exact CSS, HTML patterns, voice rules, and quality checks for Goodness Lover editorial pages. The HTML template is in `templates/page1.html` — a clean skeleton with all CSS and structure, no copy.

---

## How to Use This Skill

### 1. Get the reference page
If cloning a live GL page, rip it with `curl -sL <url>` first. This gives you the exact HTML/CSS to match. Only use the template skeleton when building from scratch.

### 2. Clone or build
**Clone mode** (preferred when a reference page exists): Give the agent the reference HTML + this prompt:
> Clone this page: [URL]. Keep everything — CSS, HTML structure, image styles, layout, fonts, spacing, footer. Do not restyle. Change only: product, copy, images, CTA URL.

**Build mode** (when no reference exists): Load the template `templates/page1.html`. It contains the complete CSS and HTML skeleton with comment blocks showing where each element goes.

### 3. Write or insert copy
If copy exists (from Paul, Sarah, or a brief), insert it into the content zone. If copy doesn't exist yet, write it following the voice rules below. Paul may not always write copy — the AI may need to generate it using the voice guide.

### 3. Add images
Choose images from verified GL sources or generate them. Insert using the HTML patterns in the template comments.

### 4. Add testimonials
Pull 3 real reviews from GL Shopify (Yotpo). Use the testimonial HTML pattern from the template.

### 5. Run the quality gate (below)

---

## HTML Patterns

The template's content zone has comment blocks showing exact HTML for each element:

| Pattern | CSS Class | When to Use |
|---|---|---|
| Drop-cap paragraph | `.drop-cap` | First paragraph of the article |
| Regular paragraph | `<p>` | Body copy |
| Section heading | `<h2>` | Major content transitions |
| Content image | `.content-image` | Full-width lifestyle/photo images |
| Illustration | `.illustration` | Centred concept illustrations (max-width 360px) |
| Emphasis block | `.emphasis-block` | Key quotes, callouts with orange left border |
| Key insight | `.key-insight` | Centred bold statement (e.g., "I call this the After-40 Digestion Gap") |
| Check list | `.check-list` + `.check-item` | Numbered questions with answers |
| Testimonial | `.testimonial` | Review blocks with stars |
| Product shot | `.product-shot` | Centred product image |
| CTA button | `.btn-cta` | Final call-to-action (teal, 460px max) |

**Do not add new CSS classes.** Use only the classes defined in the template's `<style>` block.

---

## CSS Spec (locked — do not change)

| Element | Value |
|---|---|
| Body font | Georgia, "Times New Roman", serif |
| Body size | 18px → 19px (600px+) → 20px (800px+) |
| Body color | `#111` |
| Container | `max-width: 680px`, `padding: 0 20px` |
| H1 | 1.45rem → 1.7rem → 1.9rem, **italic**, `#100f0d` |
| H2 | 1.1rem → 1.2rem, `#100f0d` |
| Category label | sans-serif, `.7rem`, `#9b433c`, uppercase |
| Author name | `#FFA372` orange |
| CTA button | `.btn-cta` — teal `#105A66`, white text, 8px radius |
| Emphasis block | 4px `#FFA372` left border, `#FFF5F0` bg |
| Testimonial | `#FFF5F0` bg, 4px `#FFA372` left border, 8px radius |

---

## Voice — Sarah Otto

Full voice guide: `references/gl-voice-guide.md`

### 5 Voice Checks
1. Opens like a person, not a brand
2. At least one unnecessary tangent
3. Products described like explaining over tea
4. Fragments carry emotion, not marketing
5. Closes like Sarah ("Don't give up." / "Your body wants to heal.")

### Writing Rules
- Australian English (colour, favour, organisation)
- No em dashes — use ellipsis (...) or line breaks
- Contractions always (I'm, couldn't, wasn't)
- Short paragraphs (1-3 sentences max)
- Questions to reader: "Sound familiar?"

### Never Say
- "Game-changing," "revolutionary," "you NEED this"
- "Buy now," "Act fast," "Limited time only"
- "As a leading expert," "Studies PROVE"
- "Hey there!" "Hey girl!"
- "Introducing...," "comprehensive formula," "advanced blend"

---

## Claims Discipline

- "Studies suggest" — never "Studies PROVE"
- "May help support" — never "Will cure"
- No disease claims without qualification
- Verify product labels before building claims
- Never fabricate testimonials

---

## Quality Gate

### Structure
- [ ] All CSS from template (no new classes, no restyling)
- [ ] Images use real URLs (verify HTTP 200)
- [ ] 3 testimonials from real GL reviews
- [ ] Drop-cap on first paragraph
- [ ] At least 1 emphasis-block
- [ ] CTA button present and styled

### Voice
- [ ] Opens like Sarah (moment/confession/fact)
- [ ] No em dashes
- [ ] Australian English
- [ ] Closes like Sarah

### Compliance
- [ ] No disease claims
- [ ] No fabricated testimonials
- [ ] "Individual results may vary" present

---

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | This file — rules and patterns |
| `templates/page1.html` | Clean HTML/CSS skeleton (no copy) |
| `references/gl-voice-guide.md` | Full Sarah Otto voice guide |
| `references/clone-prompt-pattern.md` | How to build pages by cloning, not interpreting |
| `references/quiz-onramps.md` | Quiz types → product routing |
| `references/pdp-audit-checklist.md` | Full PDP audit framework (structure, compliance, conversion tests) |

---

## Build Approach

**Preferred: Clone prompt.** Give the agent a reference URL and tell it to clone. See `references/clone-prompt-pattern.md` for the exact prompt template.

**Fallback: Template.** If no reference page exists, use `templates/page1.html` as the starting point.

**Never: Write from spec tables.** Spec tables (font sizes, colors, hex values) cause interpretation drift. Either clone a real page or use the template.

---

## Pitfalls (from real builds)

1. **Interpreting specs instead of copying.** The #1 failure mode: reading CSS values from a spec table and generating new HTML from scratch. This introduces drift at every step. Clone the source directly or copy the template. Do not interpret.
2. **Embedding copy in templates.** Templates with product-specific copy waste context tokens and confuse agents into using the wrong copy. Templates must be clean skeletons only.
3. **Adding new CSS classes.** Use only the classes defined in the template. Do not invent new ones.
4. **Restyling.** The CSS is locked. Do not "improve" it. Match the live pages exactly.
5. **Missing image alt text.** Every image needs descriptive alt text. Screen readers and SEO both need it.

---

*Restructured 2026-06-25. Template-first, no copy embedded. Clone-first approach. Voice + CSS + patterns only.*

# Build Brief: Inflammation Pro PDP — Variant B

## Task
Build a NEW product detail page for Inflammation Pro. This is a VARIANT — a different approach from the original. Use the original as a reference for product info, but create a fresh design and copy approach.

## Source files (all in this directory)
- `reference-original.html` — the current live page. Use for product info, ingredients, pricing, reviews. Do NOT clone it.
- `SKILL.md` — GL skill with CSS spec, voice rules, HTML patterns
- `voice-guide.md` — Sarah Otto voice guide
- `gl-template.html` — GL template skeleton (use if building from scratch)

## Improvements to make
1. **Hero headline**: "Your joint pain might start in your gut." (more specific than the original)
2. **Marquee**: Use these 6 unique reviews (no duplicates):
   - "The only way I could wean off NSAIDs after my knee replacement." — Bonny J.
   - "My knees are not as sore as they used to be." — Jean S.
   - "I have RA and use no other pain relievers." — Leia A.
   - "Joints better in 10 days. I can walk much better." — Fred P.
   - "I can't tell you how wonderful I feel since starting Inflammation Pro." — Mary L.
   - "If I forget to take it, my joints are stiffer. This product works!" — Valerie M.
3. **Guarantee**: "Try it for 30 days. If your joints don't feel different — even if you've finished the whole bottle — simply send us an email for a full refund."
4. **Add "How to take it" section**: 3 cards — When (2 capsules with breakfast), With food (best absorbed with a meal), Consistency (90 days for full cycle)
5. **Supply scarcity note**: Move up near pricing, not buried at bottom
6. **Disclaimer near reviews**: "Individual results may vary"

## Product info (from original)
- **Product**: Inflammation Pro by Goodness Lover
- **Price**: $125.90 (3-bottle, 90-day), $50.96 (1-bottle, 30-day)
- **Ingredients**: White Willow Bark, Meriva® Curcumin (29x bioavailable), PepZin GI® Zinc-Carnosine, LP299V® Probiotic
- **Mechanism**: Gut-joint cycle — gut barrier damage → inflammation leaks → joints → NSAIDs → more gut damage → repeat
- **Phases**: Phase 1 (Week 1-2: relief), Phase 2 (Week 3-4: systemic), Phase 3 (Week 6-12: gut repair)
- **Bonuses**: Naturopath Access ($564/yr), Autoimmune Collection ($97), 21-Day Meal Plan ($197)
- **CTA URLs**: 
  - 3-bottle: https://goodnesslover.com/pages/checkout-infpro-3b-subs
  - 1-bottle: https://goodnesslover.com/pages/checkout-infpro-1b-subs
- **Hero image**: https://pages.goodnesslover.com/inflammation-pro-pdp/images/09f9318f9ca60c35.webp
- **Sarah photo**: https://pages.goodnesslover.com/inflammation-pro-pdp/images/f0e6b7e35ca0eb8a.webp
- **All ingredient images** available at the same domain under /inflammation-pro-pdp/images/

## Design approach
- Self-contained HTML with inline CSS (no external stylesheets except Google Fonts)
- Use Fraunces + Montserrat fonts (match original)
- Dark sections for visual rhythm (nasties, comparison)
- Mobile responsive
- Sticky CTA bar on mobile
- Intersection Observer reveal animations

## Quality gates
- All image URLs must be real (curl -sI to verify)
- No em dashes (use ... or line breaks)
- Australian English
- "Individual results may vary" disclaimer
- 30-day money-back guarantee prominent
- CTA buttons link to real checkout URLs

## Output
Write the final HTML to: `index.html` in this directory.

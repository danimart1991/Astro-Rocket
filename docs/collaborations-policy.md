# domoticarte Collaborations Policy

This document is the canonical source of truth for how collaborations work in domoticarte.

Purpose:

- Give humans and AI agents one editable place to understand the collaboration policy.
- Make future updates easier: if this file changes, the website copy in Spanish and English should be reviewed and updated to match.
- Keep the policy explicit, practical, and easy to diff.

How to use this file:

- Edit the statements below when the policy changes.
- After editing, ask an AI agent to review the site and update any affected pages or fragments.
- Treat the "Canonical policy statements" section as the most important source.
- Treat any section explicitly marked as internal-only as non-public. It may guide emails and negotiations, but it must not be surfaced in public website copy unless explicitly reclassified.

Surfaces that should usually be reviewed when this file changes:

- src/i18n/es.json
- src/i18n/en.json
- pages.collaborations.* translations in both locales
- pages.contact.collaborationNotice.* translations in both locales
- Any other page mentioning sponsorships, affiliate links, editorial independence, or brand collaborations

## Canonical policy statements

### 1. Editorial independence

- Brands do not participate in the script.
- Brands do not participate in the editing.
- Brands may review content before publication only to flag factual errors, naming issues, technical inaccuracies, or details that conflict with their own ethics or context.
- This pre-publication review does not give brands control over our opinion, conclusion, or overall editorial direction.
- No collaboration may require softening, hiding, or changing our real opinion.
- No payment buys a positive review.
- Reviews and opinions must be based on real testing whenever applicable.
- If a product does not convince us, we do not recommend it.
- We prefer to lose a collaboration rather than recommend something we do not trust.

### 2. Product and partner selection

- We only recommend products that we genuinely consider useful for our audience.
- We choose carefully which brands we work with.
- If a brand's practices do not align with our ethics, we may reject the proposal.
- If a brand stops aligning with our ethics during or after an agreement, we may end the collaboration.
- Product handling terms are decided case by case with each brand over email.

### 3. Transparency with the community

- Every collaboration must be disclosed clearly.
- Every sponsorship must be disclosed clearly.
- Loaned or gifted products must be disclosed clearly when relevant to the content.
- The audience should always be able to understand when a commercial relationship exists.

### 4. Collaborations with other creators

- We may collaborate with other creators in home automation and technology.
- These collaborations should exist to provide useful content to the audience.
- The same principles of honesty, independence, and transparency apply to creator collaborations.

### 5. Affiliate links

- Some blog links and video description links may be affiliate links.
- Affiliate links may generate a commission at no extra cost to the user.
- Affiliate relationships never influence our opinions.
- Affiliate relationships never determine which products we recommend.
- Current examples mentioned publicly: Amazon Associates and AliExpress affiliate program.

### 6. Sponsored segments in videos

- Some videos may include sponsored segments.
- Sponsored segments may or may not be directly related to the video's main topic.
- Sponsored segments must still follow the same ethical criteria as the rest of the content.
- Sponsored segments must be identified clearly so viewers know they are advertising.

### 7. Operational constraints

- We may work under NDAs when appropriate.
- We may respect embargo dates when appropriate.
- We do not accept exclusivity agreements.

### 8. Contact expectations

- When someone contacts domoticarte with a collaboration proposal, we expect them to have read and understood these principles beforehand.
- Contact copy may remind brands and agencies to read the collaborations page before sending a proposal.

## Internal-only operating notes

Important:

- This section is for internal reference only.
- Do not use it as public website copy.
- Do not mention these negotiation preferences on public pages unless explicitly instructed.

### Internal handling of products and formats

- Preferred working model: brands send the product and domoticarte decides later what to do with it.
- Publicly, this should stay undisclosed unless explicitly approved for publication.
- Possible outcomes may include no coverage, a free showroom appearance, a paid ad-insert, a dedicated video, or another format discussed later.
- The chosen format depends on the product, the brand, the usefulness to the project, and what makes sense commercially and editorially.
- Timing is flexible. A product received in one month may appear much later if that is what best fits the content plan.
- A product sent without payment may later appear in a separate paid mention if a later agreement is reached.
- These decisions are handled over email with each brand and should be treated as negotiation strategy, not public policy.

## Open decisions / pending clarification

- We have not yet fixed a universal rule on whether receiving a product guarantees coverage.
- If needed later, this should be decided explicitly before being reflected in public website copy.

## Editorial intent for website copy

When turning this policy into public website copy:

- Prioritize clarity over legalistic language.
- Sound firm, transparent, and professional.
- Avoid sounding hostile to brands.
- Emphasize community trust and editorial independence.
- Keep Spanish and English versions aligned in meaning, even if phrasing differs slightly.

## Suggested update workflow for AI agents

If this file changes, review at least:

- src/i18n/es.json
- src/i18n/en.json
- src/components/pages/views/ContactView.astro
- src/components/pages/views/CollaborationsView.astro
- Any route or content file linking to the collaborations page

Recommended prompt:
"Review docs/collaborations-policy.md and update all collaboration-related copy in Spanish and English so the website matches the current policy. Also search for outdated mentions elsewhere in the repo."

## Change log

- 2026-07-20: Initial canonical policy file created from the existing domoticarte collaborations page and contact-page guidance.
- 2026-07-20: Added rules for limited pre-publication review, case-by-case product handling, NDAs/embargoes, no exclusivity, and softer contact expectations.
- 2026-07-20: Moved product-format preferences into an internal-only section and marked them as non-public guidance for future agents.

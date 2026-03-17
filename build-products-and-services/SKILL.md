---
name: build-products-and-services
description: Build the products-and-services.md context file through a guided interview. Documents everything your company sells, how you describe each offering, pricing, objections, and competitive positioning. Use this skill when someone says "build products and services," "document our offerings," "product catalog for claude," "services file," or "what we sell." Part of the Team Playbook system (Layer 1, File 3 of 5).
---

# Build Products and Services

You are interviewing a senior leader to build the `products-and-services.md` file. This file ensures that every person on the team, from sales to marketing to support, describes products and services consistently. Without it, Claude invents descriptions that sound plausible but miss the mark.

Your tone should be strategic and thorough. You need to capture not just what the company sells, but how they talk about it, what objections come up, and how they position against competitors.

## Before Starting the Interview

Ask: **"Do you have any existing materials that describe your products or services? Pricing pages, sales decks, one-pagers, proposals, or your website's product/services section. Drop them in and I'll extract what I can."**

Handle uploaded materials the same way: extract, present, fill gaps.

## Interview Flow

### Section 1: The Full Offering
- "Walk me through everything your company offers. Every product, service, tier, add-on, the full menu. Don't worry about being polished, just get it all out."
- "Are any of these seasonal, limited, or being phased out? Anything new that's launching soon?"

### Section 2: How You Describe Each One
For each product/service identified:
- "In your own words, how do you typically describe [product/service] to a prospect? Not the website copy, the way you'd actually explain it in a sales conversation."
- "What's the one-liner version? If someone at a conference asked 'what's that?' what would you say?"

### Section 3: Pricing
- "Can you walk me through the pricing structure? Tiers, packages, hourly rates, project-based, whatever applies."
- "Are there any pricing nuances Claude should know about? Things like 'we don't publish pricing,' 'pricing varies by scope,' or 'we always offer a discovery call before quoting'?"

### Section 4: Common Objections
- "What are the top 3-5 objections you hear from prospects? The real ones, not the polite ones."
- "How does your team typically respond to each? What's the go-to counter?"

### Section 5: Competitive Landscape
- "Who do prospects typically compare you to? Name names if you can."
- "For each competitor, what's the key difference? What do you do better, and where do they have an edge you have to navigate around?"

## After the Interview

### Output Format

```markdown
# Products and Services

## Offerings

### [Product/Service Name 1]
**What it is:** [Plain language description]
**One-liner:** [Conference-ready short description]
**Key details:** [Scope, deliverables, timeline, or any defining characteristics]
**Pricing:** [Structure, range, or "custom/by scope"]

### [Product/Service Name 2]
[Same format, repeat for each offering]

---

## Common Objections and Responses

| Objection | Response |
|-----------|----------|
| [Objection 1] | [How the team handles it] |
| [Objection 2] | [How the team handles it] |

---

## Competitive Landscape

| Competitor | Their Pitch | Our Differentiation |
|-----------|-------------|-------------------|
| [Name] | [What they say] | [How we're different] |
| [Name] | [What they say] | [How we're different] |
```

### Writing Rules
- Third person ("The company offers..." not "We offer...")
- Use the company's actual language for descriptions, not polished marketing copy
- Include pricing specifics only if the user shared them. If pricing is confidential or custom, note that.
- Keep competitor analysis factual, not snarky
- This file can run longer than others if the company has many offerings. Aim for completeness over brevity.

## Saving the File

Save to `context/company/products-and-services.md`.

After saving: "Products and services are documented. Next is the glossary, where we capture all the internal language, acronyms, and shorthand your team uses. Say **'build glossary'** when you're ready."

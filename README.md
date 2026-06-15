# AI Website Copy Generator

> AI-generated website copy and design for **CreativeEdge Digital Agency**, Vijayawada, Andhra Pradesh — built entirely using Claude AI as part of a digital marketing internship project.

---

## Project Overview

This project demonstrates how Artificial Intelligence — specifically **Claude AI by Anthropic** — can be used to generate professional, ready-to-deploy website copy and UI design for a real-world digital agency.

The goal was to create a complete 3-page website for **CreativeEdge Digital Agency**, a fictional digital marketing agency based in Vijayawada, AP, that offers Social Media Marketing, SEO, Graphic Design, and Web Development services to local businesses.

All copy, layout decisions, HTML structure, and CSS styling were generated through carefully written prompts — with zero manual coding from scratch.

---

## Live Pages

| Page | File | Description |
|------|------|-------------|
| Homepage | `creativeedge-homepage.html` | Hero, services overview, about, value proposition |
| Services | `creativeedge-services.html` | Detailed breakdown of all 4 services |
| Contact | `creativeedge-contact.html` | Contact form, business details, final CTA |

---

## Tools Used

### Claude AI (Anthropic)
- **Model:** Claude Sonnet (claude.ai)
- **Use:** 100% of copywriting, HTML structure, CSS styling, and form validation logic was generated via Claude
- **Interface:** Claude.ai chat interface with iterative prompting

### Other Tools
- **Google Fonts** — Syne (display) + Inter (body) loaded via CDN
- **GitHub** — version control and project hosting
- **VS Code** — viewing and minor edits to generated output

---

## Prompt Logic Used

Each page was generated using a structured prompt designed to give Claude the right context, constraints, and output format. Below is the prompt strategy used for each page.

---

### Page 1 — Homepage

**Prompt goal:** Generate a complete homepage with brand identity, persuasive copy, and clean HTML output.

**Key prompt elements used:**
- Defined the agency name, location, and services upfront
- Specified the exact sections required: headline, subheadline, about us, value proposition
- Instructed tone: *"professional yet approachable, simple and persuasive"*
- Asked for *"website-ready"* output to signal clean, deployable HTML

**Prompt extract:**
```
You are a professional website copywriter. Write homepage copy for a digital agency
called CreativeEdge Digital Agency located in Vijayawada, Andhra Pradesh, India.
The agency offers services like social media marketing, SEO, graphic design, and
web development for local businesses. The copy should include: a strong headline,
a subheadline, a brief about us section, and a clear value proposition.
Keep the tone professional yet approachable. Make it simple, persuasive,
and website-ready.
```

**What worked well:**
- Naming the location (Vijayawada) produced locally relevant copy automatically
- Specifying "website-ready" triggered full HTML + CSS output, not just text
- The model chose a distinctive saffron + teal palette inspired by Andhra culture

---

### Page 2 — Services Page

**Prompt goal:** Generate a detailed services page with structured content per service and persuasive benefit copy.

**Key prompt elements used:**
- Listed all 4 services explicitly so none were missed
- Required a specific structure per service: *headline + 3–4 benefit points + short CTA*
- Maintained tone consistency with homepage by reusing tone descriptor
- Specified *"clean HTML"* output format

**Prompt extract:**
```
You are a professional website copywriter. Write a dedicated Services page for
CreativeEdge Digital Agency, a digital agency based in Vijayawada, Andhra Pradesh.
The page should include detailed descriptions for these 4 services:
1) Social Media Marketing, 2) SEO, 3) Graphic Design, 4) Web Development.
For each service include: a headline, 3–4 benefit points, and a short CTA.
Keep the tone professional, persuasive, and simple. Output as clean HTML.
```

**What worked well:**
- Numbered list in the prompt ensured all 4 services were treated equally
- "Benefit points" framing pushed Claude toward outcome-led copy, not feature lists
- Claude automatically added local detail (e.g., "Telugu and English keywords" for SEO) without being asked
- Visual panels with per-service colour gradients were added without prompting — Claude inferred this from the homepage's design system

---

### Page 3 — Contact / CTA Page

**Prompt goal:** Generate a warm, action-oriented contact page with a working form and all business details.

**Key prompt elements used:**
- Provided exact contact details: email (`hello@creativeedge.in`), location (Vijayawada, AP)
- Specified all required form fields: name, email, phone, message
- Requested both a contact form AND a motivating final CTA — two distinct conversion elements
- Tone instruction adjusted to *"warm, professional, and action-oriented"* to suit a contact page

**Prompt extract:**
```
You are a professional website copywriter. Write a dedicated Contact / CTA page
for CreativeEdge Digital Agency, a digital agency based in Vijayawada, Andhra Pradesh,
India. The page should include: a strong headline encouraging visitors to get in touch,
a short persuasive paragraph, a contact form (name, email, phone, message fields),
business contact details (email: hello@creativeedge.in, location: Vijayawada, AP),
and a final motivating CTA. Keep the tone warm, professional, and action-oriented.
Output as clean HTML.
```

**What worked well:**
- Specifying exact field names prevented generic "Name / Email / Submit" forms
- "Final motivating CTA" as a separate requirement produced a distinct banner section, not just a button
- Claude added client-side JavaScript form validation and a success state without being asked — it inferred this as best practice
- Trust signals bar and WhatsApp CTA were added autonomously based on local market context

---

## File Structure

```
ai-website-copy-generator/
│
├── creativeedge-homepage.html      # Homepage — hero, about, services, value prop
├── creativeedge-services.html      # Services page — 4 services with benefits + CTAs
├── creativeedge-contact.html       # Contact page — form, details, final CTA
├── README.md                       # This file
```

> All CSS is embedded within each HTML file (no separate stylesheet). All pages are self-contained and work without a build step or local server.

---

## Design System (AI-Generated)

Claude maintained a consistent design system across all three pages without being explicitly asked to. The emergent design tokens were:

| Token | Value | Usage |
|-------|-------|-------|
| `--ink` | `#0D0D0D` | Primary text, dark backgrounds |
| `--paper` | `#F7F4EF` | Page background |
| `--saffron` | `#E8720C` | Primary accent, CTAs, highlights |
| `--teal` | `#006E6D` | Secondary accent, eyebrows, checkmarks |
| `--mist` | `#E2DDD6` | Borders, dividers |
| Display font | Syne 800 | Headlines, logo, buttons |
| Body font | Inter 300–500 | Paragraphs, labels, UI text |

---

## Key Learnings

### 1. Role + Context = Better Output
Starting every prompt with *"You are a professional website copywriter"* significantly improved the tone and structure of the output. Giving Claude a professional role produces more focused, expert-level results than open-ended requests.

### 2. Structure the Requirements, Not the Answer
Listing what you need (headline, benefit points, CTA) rather than describing what the output should look like gives Claude room to make better design decisions. Over-specifying layout can constrain the output unnecessarily.

### 3. Location Specificity Adds Authenticity
Including "Vijayawada, Andhra Pradesh" in prompts caused Claude to add genuinely local touches — references to Telugu and English keywords, local market context, and culturally informed colour choices — without any additional instruction.

### 4. Claude Infers Best Practices Automatically
Across all three pages, Claude added features not explicitly requested: form validation with error states, a success confirmation message, WhatsApp CTAs, trust signals, and mobile responsiveness. Clear output format instructions ("clean HTML") signal professional deployment intent, which triggers higher quality output.

### 5. Tone Modifiers Do Real Work
Changing the tone descriptor per page ("professional yet approachable" vs. "warm and action-oriented") produced noticeably different copy voices — same agency, same brand, but correctly calibrated for each page's job.

### 6. Iterative Conversation Beats Single Prompts
Because this project was built across multiple messages in one conversation, Claude maintained brand consistency (fonts, palette, nav, footer) across all three pages automatically. Long-context AI conversations act as a shared creative memory.

---

## About This Project

This project was created as part of a **digital marketing internship** to explore the practical application of AI tools in real-world web content creation workflows.

It demonstrates that with well-structured prompts, a non-developer can produce production-quality website copy, HTML, and CSS using Claude AI — in a fraction of the time traditional copywriting and development would require.

---

## Author

**Internship Project — CreativeEdge Digital Agency (Concept)**
Location: Vijayawada, Andhra Pradesh, India
Tool: [Claude AI by Anthropic](https://claude.ai)

---

*Generated with Claude AI · Anthropic · 2026*

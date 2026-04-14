---
name: skill-context
description: >
  Foundational "mother skill" that stores and provides brand or project context to all 
  other skills. Load this skill at the start of any creative, content, or strategy task 
  to give Claude access to: brand identity, tone of voice, mission, target audience, 
  existing materials, and any other project-specific information. Supports single brand 
  or multi-brand/multi-client setups. Always read this skill before executing content 
  tasks if it has been populated by the user. If context is missing or incomplete, 
  Claude should ask the user to fill in the relevant sections.
---

# Skill Context — Brand & Project Reference

This skill is a **container for context**. It holds all the information about a brand,
project, or client that other skills need to produce consistent, on-brand output.

It works in two modes:

- **Single brand**: Fill in the sections once for your own brand
- **Multi-brand / multi-client**: Use the template for each client, switching context
  as needed by telling Claude which brand is active

---

## How other skills use this file

When a child skill (e.g. skill-social-content-text) instructs Claude to load this file:

1. Claude reads the active brand context below
2. Applies TOV, audience, and brand rules to every output
3. If a required field is empty, Claude asks the user before proceeding
4. Claude never invents brand information — it only uses what's provided here

---

## How to populate this skill

You can fill in the sections below in two ways:

**Option A — Edit this file directly**
Replace the placeholder text in each section with real information.

**Option B — Tell Claude in chat**
Say: _"Update my brand context with the following information..."_ and Claude will
confirm what to add. You can paste website copy, a PDF, a brief, or just describe
your brand in your own words.

---

## Active Brand

> If working with multiple brands, specify which is active at the start of a session:
> _"Today we're working on [Brand Name]"_

**Active brand name:** `[Not set]`

---

## Brand Profiles

---

### Brand: [Brand Name]

> Duplicate this entire section for each additional brand or client.

#### 1. Brand Identity

**Brand name:**
`[e.g. Acme Studio]`

**Industry / sector:**
`[e.g. SaaS / B2B Marketing Tools]`

**Founded / background (optional):**
`[Brief origin story or relevant background]`

**Website:**
`[URL]`

**Tagline / slogan:**
`[e.g. "Marketing that moves"]`

**Mission statement:**
`[e.g. "We help small teams punch above their weight with smart, simple marketing tools."]`

**Vision:**
`[Where is the brand going long-term?]`

**Core values:**
`[e.g. Transparency, Speed, Human-first]`

---

#### 2. Target Audience

**Primary audience:**
`[e.g. Marketing managers at B2B SaaS companies, 28–42, EU and US markets]`

**Secondary audience (if any):**
`[e.g. Freelance marketers and consultants]`

**Audience pain points:**
`[What problems do they have that this brand solves?]`

**Audience desires:**
`[What do they want to achieve? What motivates them?]`

**Audience language:**
`[How do they speak? Any specific jargon, terms, or phrases they use?]`

> Duplicate this section for each additional audience.

---

#### 3. Tone of Voice (TOV)

**Overall tone:**
`[e.g. Friendly but sharp. Confident without being arrogant. Direct, never corporate.]`

**TOV adjectives (pick 3–5):**
`[e.g. Clear / Warm / Bold / Witty / Authoritative]`

**TOV — what we sound like:**
`[e.g. A smart colleague explaining something over coffee. We use plain language, short sentences, and the occasional dry joke.]`

**TOV — what we never sound like:**
`[e.g. Formal, stiff, salesy, buzzword-heavy, or condescending.]`

**Writing style notes:**

- Sentence length: `[e.g. Short and punchy preferred]`
- Use of "you": `[e.g. Yes, always address the reader directly]`
- Use of humour: `[e.g. Light and dry — never forced]`
- Use of emoji: `[e.g. Occasional, in informal contexts only]`
- Use of profanity: `[e.g. None / Mild / Acceptable]`
- Oxford comma: `[Yes / No]`
- Numbers: `[e.g. Spell out under 10, use numerals for 10+]`

**Language:**
`[e.g. British English / American English / Italian / bilingual]`

---

#### 4. Content Pillars

> Content pillars are the recurring themes/topics this brand talks about on social media.

**Pillar 1:** `[e.g. Industry insights and trends]`
**Pillar 2:** `[e.g. Behind-the-scenes / company culture]`
**Pillar 3:** `[e.g. Product education and use cases]`
**Pillar 4:** `[e.g. Customer stories and social proof]`
**Pillar 5 (optional):** `[e.g. Thought leadership / founder POV]`

---

#### 5. Active Social Channels

> List the platforms this brand uses, with any platform-specific notes.

| Platform    | Active?    | Notes                                                         |
| ----------- | ---------- | ------------------------------------------------------------- |
| X / Twitter | `[Yes/No]` | `[e.g. Used for thought leadership and real-time engagement]` |
| Threads     | `[Yes/No]` | `[e.g. Brand personality and community]`                      |
| Instagram   | `[Yes/No]` | `[e.g. Visual product content and Reels]`                     |
| LinkedIn    | `[Yes/No]` | `[e.g. B2B content, CEO posts]`                               |
| Facebook    | `[Yes/No]` | `[e.g. Community groups and ads]`                             |
| TikTok      | `[Yes/No]` | `[e.g. Not active]`                                           |
| YouTube     | `[Yes/No]` | `[e.g. Tutorial videos and webinars]`                         |
| Reddit      | `[Yes/No]` | `[e.g. Niche community participation]`                        |

---

#### 6. Existing Materials

> Paste, summarize, or link to any existing brand materials Claude should know about.

**Existing taglines / headlines in use:**

```
[Paste any copy currently in use that Claude should reference or stay consistent with]
```

**Key messages (recurring themes to reinforce):**

```
[e.g. "We're the only tool that does X without Y" / "Built for teams who hate bloat"]
```

**Copy to avoid / retired messaging:**

```
[e.g. "Disruptive" — we no longer use this word / Avoid comparing to [Competitor X] directly]
```

**Sample of approved copy (optional but recommended):**

```
[Paste 2–3 examples of on-brand social posts, emails, or ads that Claude can use as style reference]
```

---

#### 7. Competitors & Positioning

**Main competitors:**
`[e.g. Tool A, Tool B, Tool C]`

**How we're different:**
`[e.g. We focus on simplicity and speed where competitors prioritize features and complexity]`

**What we never do:**
`[e.g. We don't name competitors in content / We don't claim to be "the best" without proof]`

---

#### 8. Current Campaign / Context (optional)

> Update this section when working on a specific campaign or project.

**Campaign name:**
`[e.g. Q2 2025 Product Launch — "Focus Mode"]`

**Campaign goal:**
`[e.g. Drive 500 sign-ups for the new Focus Mode feature]`

**Key dates:**
`[e.g. Launch: May 12 / Campaign runs: May 12 – June 15]`

**Campaign messaging focus:**
`[e.g. Productivity / deep work / fewer distractions]`

**Assets available:**
`[e.g. Landing page URL / 3 product screenshots / 1 demo video link]`

**CTA for this campaign:**
`[e.g. "Try Focus Mode free" → [URL]]`

---

#### 9. Legal / Compliance Notes (optional)

`[e.g. Cannot make revenue claims / Must include disclaimer on financial content / Regulated industry — no superlatives]`

---

## Notes for Claude

When this skill is loaded:

- Never fabricate brand information not listed here
- If a section is empty and it's needed for the task, ask the user before proceeding
- If existing copy samples are provided in Section 6, use them as style anchors
- Apply TOV consistently across all outputs, including when adapting for different platforms
- Platform-specific tone adjustments (e.g. more casual on Threads) are acceptable within the TOV framework — they should never contradict it
- When in doubt about tone: refer to the "what we never sound like" field

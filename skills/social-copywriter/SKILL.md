---
name: skill-social-copywriter
description: >
  Professional social media copywriter skill. Use this skill whenever the user wants 
  to write, create, or generate any social media text content from scratch: single posts, 
  threads, carousels (slide-by-slide scripts), captions for Reels/TikTok/video, or 
  Stories copy. Covers all major platforms: X/Twitter, Threads, Instagram, LinkedIn, 
  Facebook, TikTok, YouTube, Reddit. Always loads skill-context (brand identity, TOV) 
  and skill-platform-knowledge (platform rules and limits) before writing. Trigger this 
  skill whenever the user mentions writing, drafting, creating, or generating any social 
  post, thread, caption, carousel, or copy for any social platform.
---

# Skill — Social Copywriter

This skill produces platform-optimized social media copy in all text formats.
It relies on two mother skills for context and platform rules.

---

## Step 0 — Load mother skills

Before doing anything else, check whether the two required mother skills are available
in the active skill list.

### Required skills

- `skill-context` — brand identity, TOV, audience, content pillars, existing copy
- `skill-platform-knowledge` — platform limits, algorithm rules, format specs

### If both skills are available

Read them now before proceeding to Step 1.

- From `skill-context`: load brand identity, TOV, audience, content pillars,
  active campaign context, and existing copy samples. If key fields are empty,
  note what is missing and ask the user before writing.
- From `skill-platform-knowledge`: load the relevant platform section(s) for the task.

### If one or both skills are missing

Stop immediately and tell the user:

---

To work properly, this skill requires two supporting skills to be active:

- **skill-context** — holds your brand identity, tone of voice, and audience info
- **skill-platform-knowledge** — holds platform rules, limits, and algorithm logic

Please activate the missing skill(s) in **Settings > Capabilities > Skills**, then
restart the task.

If you have not set up skill-context yet, you can either:

- **(a)** Fill in the skill-context template with your brand information first
- **(b)** Tell me your brand details now and I will work with them for this session
  only (without saving them permanently)

---

Do not proceed to Step 1 until both skills are available, or the user has explicitly
chosen option (b) and provided the necessary brand context inline.

Never invent brand information or platform rules from memory.

---

## Step 1 — Brief the user

Before writing, always ask these four questions in a single message.
Keep it conversational — don't make it feel like a form.

**Ask:**

1. **Piattaforma** — Dove viene pubblicato? (X, LinkedIn, Instagram, Threads,
   Facebook, TikTok, YouTube, Reddit)
2. **Formato** — Che tipo di contenuto?
   (post singolo / thread / carosello / caption video / Stories copy)
3. **Obiettivo** — Cosa deve fare questo contenuto?
   (awareness / engagement / traffico / lead / conversione / community)
4. **Approccio narrativo** — Come vuoi raccontarlo?
   (storytelling / listicle / contrarian / how-to / dati e insight / domanda /
   behind the scenes / altro — o lascia decidere a Claude)
5. **Numero di varianti** — Quante versioni vuoi? (default: 1 se non specificato)

If the user has already provided some of this information in their message,
don't ask again — extract it and only ask what's missing.

---

## Step 2 — Write the copy

Apply the following rules for every output:

### Language

Write in the same language the user is writing in.
If the brand in `skill-context` specifies a language and it differs from the
user's language, flag it and ask which to use.

### Tone of Voice

Always apply the TOV from `skill-context`.
Platform-specific tone adjustments are allowed (e.g. more casual on Threads,
more professional on LinkedIn) but must stay within the brand's TOV boundaries.
Never contradict the "what we never sound like" field.

### Platform rules

Apply the exact limits and best practices from `skill-platform-knowledge` for
the chosen platform:

- Never exceed hard character limits
- Use optimal lengths, not maximum lengths
- Apply correct hashtag count and placement
- Apply link placement rules (body vs. first comment/reply)
- Follow algorithm-signal logic (e.g. end with a question on LinkedIn,
  use cliffhangers in threads on X)

### Format-specific instructions

Refer to `references/formats.md` for detailed writing instructions per format.
Always read the relevant format section before writing.

---

## Step 3 — Output structure

Present each variant clearly labeled:

```
---
**Variante 1 — [Approccio: es. Storytelling]**

[Copy completo, pronto da pubblicare]

📊 Note tecniche:
- Caratteri: [X / limite piattaforma]
- Hashtag: [lista]
- Link: [posizione consigliata se presente]
---
```

For carousels, structure each slide:

```
---
**Carosello — [Titolo del carosello]**

**Cover (Slide 1):**
Headline: [testo]
Sottotitolo: [testo opzionale]

**Slide 2:**
Headline: [testo]
Body: [testo]

[...continua per ogni slide...]

**Slide finale (CTA):**
Headline: [testo]
CTA: [azione chiara]

📊 Note: [numero slide / piattaforma / formato]
---
```

---

## Step 4 — After delivering the copy

Always close with:

1. A brief explanation of **why** you made the key creative choices
   (hook type, narrative approach, format decisions) — max 3 bullet points
2. One concrete suggestion for how to **test or improve** the copy
   (e.g. A/B test the hook, try a different CTA, add a data point)
3. Ask: _"Vuoi modifiche, una variante diversa, o adattarlo per un'altra piattaforma?"_

---

## Quality checklist (run before outputting)

Before presenting the final copy, verify:

- [ ] TOV from `skill-context` is applied and consistent
- [ ] Hard character limits from `skill-platform-knowledge` are respected
- [ ] Optimal length (not just maximum) is targeted
- [ ] Hook is strong — would stop the scroll in the first line
- [ ] Each piece of copy has a clear objective and CTA (explicit or implicit)
- [ ] Hashtags: correct count and placement per platform
- [ ] Links: correct placement per platform rules
- [ ] No corporate language unless brand TOV explicitly allows it
- [ ] Copy reads naturally in the chosen language
- [ ] Carousel: each slide has one idea only, flows logically to the next

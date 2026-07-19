# DESIGN.md — OFFGRD STUDIOS · Beirut Music Conservatory

> ⚠️ **DEMO MOCKUP — not a real client.** No live business was researched; this is a
> concept build for the music-school vertical. Per the honesty ledger, **every** name,
> stat, testimonial, phone number and image below is 🔴 placeholder and flagged as such
> in the UI. Nothing here may be presented as real without a real business behind it.

---

## [PER-SITE] 1. The brief
- **Business:** A Beirut music conservatory teaching both Arabic/oriental music (oud, qanun, ney, voice) and Western music (piano, guitar, violin, theory) — one-to-one lessons, ensembles, and recitals.
- **Location / channel:** Beirut, Lebanon. Enquiries via WhatsApp + form.
- **Audience:** Beirut families choosing lessons for children, and adult beginners/returners.
- **The page's single job:** get a **trial-lesson booking** via WhatsApp/form.
- **Real content sourced:** none — demo. All content is invented and flagged.
- **What we must placeholder:** the name (*OFFGRD STUDIOS*), all imagery (Unsplash stock, flagged), the +961 WhatsApp number, all counts/quotes.

## [PER-SITE] 2. Tokens
- **Palette (concert-hall-at-night, NOT the cream/terracotta default):**
  - `--night  #14100e` — deep warm near-black (the darkened hall)
  - `--stage  #1e1815` — lifted panel / stage floor
  - `--paper  #f3ead9` — warm ivory (type on dark; light sections)
  - `--brass  #d59a4e` — brass/amber, the primary glow accent
  - `--oud    #a24a35` — oud-wood warm red, secondary
  - `--verd   #3a6b64` — verdigris/patina teal, cool counterpoint
- **Type pairing:** **Fraunces** (variable, high optical contrast, soft lyrical serifs) for display + **Manrope** (geometric-humanist sans) for body/UI; tracked Manrope caps for eyebrows/labels. Justify: Fraunces' hand-cut, singing serifs read *musical and warm* — not the cold Playfair default; Manrope keeps the interface crisp and fast.
- **Signature element:** a glowing **waveform that grows from one string into an ensemble**.

## [PER-SITE] 3. The signature scroll moment
- **Concept (fits a music school):** on the darkened stage a single amber **string** vibrates alone. As you scroll, more voices layer in — oud red, verdigris, ivory — each a stacked, glowing waveform, until one plucked string has become a full **ensemble**.
- **Scrub phase:** layers fade/scale in one by one; amplitude and glow grow with scroll progress.
- **Hold:** the full ensemble sustains, gently oscillating — the "held chord" beat.
- **Reveal (draft copy):** the waves settle to a calm baseline and the line rises —
  **"One string. Then an orchestra."** / *"Every musician here started with a single note. We stay with you for all the rest."*
- **Images needed:** none — the signature is bespoke animated SVG (fast, self-contained, no stock).

---

## [STANDARD] 4. Page structure
1. Hero — name + value prop, "Book a trial lesson" CTA, scroll cue, ambient waveform.
2. Signature scroll moment (§3).
3. Proof — programme/recital gallery (flagged placeholder) + illustrative counts (labelled *sample*).
4. Process — 3 auto-advancing steps → CTA.
5. Programmes — instrument/discipline cards.
6. Contact — trial-lesson form → WhatsApp.
7. Footer.

## [STANDARD] 5. Motion rules
GSAP + ScrollTrigger + Lenis. Exactly ONE signature pinned-scrub moment; the rest quiet scroll-reveals. Every animation has a `prefers-reduced-motion` fallback showing the end state.

## [STANDARD] 6. Guardrails
Accessibility (reduced-motion, visible focus, alt text, ≥44px targets, AA contrast); performance (LCP < 2.5s, lazy below-fold, < ~1.5 MB, deferred JS); single `--sy` rhythm token; honesty (all placeholders flagged); responsive to 360px.

## [STANDARD] 7. Verify checklist
- [ ] Screenshot: hero, each signature phase, proof, programmes, contact.
- [ ] Reduced-motion path renders end states.
- [ ] Mobile (375px) clean.
- [ ] Console clean; ScrollTrigger.refresh() after fonts load.
- [ ] All placeholder images flagged; no real business implied.
- [ ] Contact CTA composes a real WhatsApp message.

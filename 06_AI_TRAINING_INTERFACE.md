# Syntaxis
## 05_GLYPH_SYSTEM_SPEC
Version: v0.1-draft
Status: Experimental Layer
Depends-On: 01_SYNOPSIS_AND_INTENT.md
            02_CORE_GRAMMAR_SPEC.md
            03_LEXICON_ARCHITECTURE.md
            04_META_LAYER_AND_COGNITIVE_ENCODING.md
Last Updated: 2026-02-15

---

# 1. Overview

The Glyph System is a secondary visual layer for Syntaxis.

It is:

- Optional
- Non-phonetic
- Structurally symbolic
- Optimized for rapid pattern recognition
- Designed for cognitive compression

Canonical ASCII remains authoritative.

Glyphs are render-layer only.

---

# 2. Design Principles

Glyphs must:

- Represent grammatical role clearly
- Be visually distinct
- Be minimal-stroke
- Avoid cultural appropriation of existing scripts
- Map 1:1 to canonical ASCII markers

No ambiguity permitted between glyph and ASCII form.

---

# 3. Role Marker Glyphs

| ASCII | Glyph | Meaning |
|--------|--------|----------|
| -ta | ⊙ | Topic |
| -ka | → | Agent |
| -mo | ◇ | Direct Object |
| -ri | ⇢ | Indirect |
| -se | ⌂ | Locative |
| -nu | ⚙ | Instrument |

Example:

    Self ⊙
    AI →
    Meaning ◇
    clarify-in-ke
    [mdl]

---

# 4. Number Glyph Indicators

Number is indicated by superscript markers:

| ASCII | Glyph |
|--------|--------|
| -un | ¹ |
| -du | ² |
| -pl | ³ |

Example:

    Self² ⊙

Meaning: Dual self (human + AI)

---

# 5. Aspect Glyphs

Aspect may optionally be shown via diacritic overlay.

| ASCII | Glyph |
|--------|--------|
| -in | ~ |
| -tae | ✓ |
| -li | ? |
| -ra | ↑ |
| -su | ∞ |

Example:

    clarify?~ke

Meaning:
Potential + ongoing (if stacked)

ASCII remains canonical:

    clarify-li-in-ke

---

# 6. Modality Glyph Indicators

| ASCII | Glyph |
|--------|--------|
| -ke | ! |
| -mi | ? |
| -zo | ∴ |
| -ha | ♥ |

Example:

    detect✓∴
    [obs]

---

# 7. Meta Layer Glyphs (Optional Visual Compression)

Meta markers may optionally collapse to glyph shorthand.

| ASCII | Glyph |
|--------|--------|
| [obs] | 👁 |
| [inf] | ∵ |
| [mdl] | ⌘ |
| [mem] | 🜂 |
| [hyp] | △ |
| [emo] | ♥ |

Probability:
    [pro=.6] → .6°

Confidence:
    [conf=.7] → .7✓

Example:

    Model ⊙
    err ◇
    detect✓∴
    ∵ .6° .7✓

ASCII canonical still required in storage.

---

# 8. Glyph Block Architecture (Future)

Inspired by Hangul:

Potential future design:

Block structure:

    [Semantic Root]
    [Number Marker]
    [Role Marker]

Stacked as geometric unit.

Not implemented in v0.1.

---

# 9. Rendering Rules

- Glyphs must never replace canonical ASCII in stored corpus.
- Glyphs are presentation-layer only.
- Glyph system must be reversible to ASCII.
- No glyph-only expressions allowed.

---

# 10. Architectural Decision Log (ADL)

## ADL-019
Decision: Glyph layer non-authoritative.
Status: Approved
Rationale: Preserve AI compatibility.

## ADL-020
Decision: One-to-one mapping with ASCII markers.
Status: Approved
Rationale: Deterministic reversibility.

## ADL-021
Decision: Unicode allowed only in render layer.
Status: Approved
Rationale: Avoid encoding issues.

---

# 11. Open Questions

- Should semantic radicals be designed?
- Should glyph blocks be formalized?
- Should emotional valence have dedicated symbol?
- Should a handwritten form exist?

To be resolved in future versions.
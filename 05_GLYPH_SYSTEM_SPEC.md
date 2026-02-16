# Syntaxis
## 05_GLYPH_SYSTEM_SPEC
Version: v0.2-draft
Status: Experimental Render Layer
Depends-On: 01–04
Last Updated: 2026-02-16

---

# 1. Overview

The Glyph System is optional and non-authoritative.

Canonical ASCII remains authoritative for storage, training, and validation.

Glyphs provide:
- Rapid reading
- Visual role separation
- Optional compression

Glyphs must map 1:1 to canonical ASCII constructs.

---

# 2. Role Marker Glyphs (Render Only)

| ASCII | Glyph | Meaning |
|------|-------|---------|
| -ta  | ⊙     | Topic |
| -ka  | →     | Agent |
| -mo  | ◇     | Direct Object |
| -ri  | ⇢     | Indirect |
| -se  | ⌂     | Locative |
| -nu  | ⚙     | Instrument |

---

# 3. Number Glyphs (Render Only)

| ASCII | Glyph |
|------|-------|
| -un  | ¹ |
| -du  | ² |
| -pl  | ³ |

Example:
    Self² ⊙

---

# 4. Event/State Glyphs (Render Only)

| ASCII | Glyph |
|------|-------|
| @E   | ⚡ |
| @S   | ▭ |

Example render:
    Rain ⚡ ⊙ begin…
    System ▭ ⊙ stable…

---

# 5. Procedural Mode Render (Optional)

Reserved prefixes may render as compact symbols:

| ASCII prefix | Render glyph |
|------------|--------------|
| Proc-ta     | ⧉ |
| Step=n:     | n· |
| Req:        | ⟂ |
| Inv:        | ⊨ |
| Out-ta      | ⇣ |

Example render-only (not stored):
    ⧉ clarify-loop…
    1· Input… collect…
    ⟂ Prompt… present…
    ⊨ Meaning… preserve…
    ⇣ summary… emit…

---

# 6. Classifier Render

Classifier tags `term{class}` may render as small corner tags.

Canonical remains ASCII `{class}`.

Example:
    model{sys} → model with a “sys” tag

---

# 7. Meta Layer Glyphs (Optional)

| ASCII | Glyph |
|------|-------|
| [obs] | 👁 |
| [inf] | ∵ |
| [mdl] | ⌘ |
| [mem] | 🜂 |
| [hyp] | △ |
| [emo] | ♥ |

Probability and confidence may render compactly:
- [pro=.6] → .6°
- [conf=.7] → .7✓

---

# 8. Rendering Rules

- Glyphs MUST NOT replace canonical ASCII in stored corpora.
- Glyph system must be reversible to ASCII.
- No glyph-only expressions are valid Syntaxis artifacts.

---

# 9. Architectural Decision Log (ADL)

## ADL-019
Decision: Glyph layer non-authoritative.
Status: Approved

## ADL-020
Decision: One-to-one mapping with ASCII markers.
Status: Approved

## ADL-029
Decision: Add glyph mapping for @E/@S.
Status: Approved

## ADL-031
Decision: Add optional procedural render glyphs.
Status: Approved

---

# 10. Open Questions

- Should a formal block glyph architecture exist (Hangul-like)?
- Should classifier set have standardized glyph radicals?
- Should event subtypes have distinct glyphs?
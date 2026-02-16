# Syntaxis
## 04_META_LAYER_AND_COGNITIVE_ENCODING
Version: v0.2-draft
Status: Cognitive Core
Depends-On: 01–03
Last Updated: 2026-02-16

---

# 1. Overview

The Meta Layer is mandatory in Syntaxis.

It encodes:
- Epistemic classification (mandatory)
- Probability (optional but structured)
- Confidence (optional but structured)
- Emotional valence (optional)
- Cognitive load (optional)
- Clarity (optional)

Meta markers are appended at sentence end as bracketed ASCII tokens.

---

# 2. Primary Epistemic Markers (Mandatory)

Each sentence must include exactly one primary epistemic marker.

| Marker | Meaning |
|--------|---------|
| [obs]  | Direct observation |
| [inf]  | Inference from data |
| [mdl]  | Modeled abstraction |
| [mem]  | Memory recall |
| [hyp]  | Hypothetical |
| [emo]  | Emotional state report |

(Deferred candidate: [rep] reported/hearsay — not in v0.2.)

---

# 3. Probability Encoding

Format:

    [pro=.X]

Where X ∈ [0.0 – 1.0]

## 3.1 Event/State requirement
If `[pro=...]` is present, at least one `@E` or `@S` marker must appear in the sentence.

---

# 4. Confidence Encoding

Format:

    [conf=.X]

Confidence is subjective certainty and does not need to match probability.

---

# 5. Emotional Valence Encoding

Format:
- Polarity: [val=+], [val=-], [val=0]
- Numeric gradient: [val=+.6], [val=-.2]

Valence complements emotional lexical roots; it does not replace them.

---

# 6. Cognitive Load Marker

Format:
- [load=low|mid|high]
- or numeric: [load=.7]

---

# 7. Clarity Marker

Format:

    [cla=.X]

Indicates perceived clarity of thought.

---

# 8. Meta Marker Order (Deterministic)

Meta markers must appear in this order:

1) Primary epistemic marker
2) [pro=]
3) [conf=]
4) [val=]
5) [load=]
6) [cla=]

Valid:
    [mdl][pro=.4][conf=.6][val=-.2][load=.7][cla=.5]

Invalid:
    [conf=.6][mdl]

---

# 9. Interaction Rules

## 9.1 [obs]
- [pro] optional; if omitted, implied 1.0 (not explicitly stored)
- If [pro] used with [obs], still requires @E/@S

## 9.2 [emo]
- [val] strongly encouraged
- [pro] discouraged

## 9.3 [hyp]
- [conf] strongly encouraged
- [pro] optional but common; if used, requires @E/@S

---

# 10. Examples

Inference with probability (event):
    Model{sys}-ta fail@E-li-mi [inf][pro=.5][conf=.6]

State modeling with probability:
    System{sys}@S-ta stable-in [mdl][pro=.7][conf=.6]

Emotional report:
    Self{ent}-un-ta emo-overload{emo}-mo increase-in-ha [emo][val=-.8][load=high]

---

# 11. Architectural Decision Log (ADL)

## ADL-015
Decision: Exactly one primary epistemic marker required.
Status: Approved

## ADL-018
Decision: Fixed meta-marker ordering.
Status: Approved

## ADL-029
Decision: Event/State operators used to ground probability.
Status: Approved

## ADL-030
Decision: Require @E/@S when using [pro].
Status: Approved

---

# 12. Open Questions

- Add reported/hearsay epistemic ([rep])?
- Allow meta markers on subclauses?
- Add event subtypes (@E+, @E-, etc.)?
- Add compact evidential compression later (Quechua-inspired) without changing canonical storage?
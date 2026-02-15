# Syntaxis
## 04_META_LAYER_AND_COGNITIVE_ENCODING
Version: v0.1-draft
Status: Cognitive Core
Depends-On: 01_SYNOPSIS_AND_INTENT.md
            02_CORE_GRAMMAR_SPEC.md
            03_LEXICON_ARCHITECTURE.md
Last Updated: 2026-02-15

---

# 1. Overview

The Meta Layer is mandatory in Syntaxis.

It encodes:

- Epistemic classification
- Probability
- Confidence
- Emotional state (optional but structured)
- Cognitive load
- Valence

This layer differentiates Syntaxis from traditional logical languages.

Meta markers are appended at the end of sentences in bracketed ASCII form.

---

# 2. Epistemic Markers (Mandatory)

Each sentence must include exactly one primary epistemic marker.

| Marker | Meaning |
|---------|---------|
| [obs]   | Direct observation |
| [inf]   | Inference from data |
| [mdl]   | Modeled abstraction |
| [mem]   | Memory recall |
| [hyp]   | Hypothetical |
| [emo]   | Emotional state report |

If multiple epistemic states exist, the dominant one must be chosen.

---

# 3. Probability Encoding

Optional but strongly encouraged for non-[obs] statements.

Format:

    [pro=.X]

Where X ∈ [0.0 – 1.0]

Examples:

    [pro=.3]
    [pro=.75]

Precision beyond two decimals discouraged.

---

# 4. Confidence Encoding

Confidence reflects subjective certainty, not statistical probability.

Format:

    [conf=.X]

Confidence does NOT need to match probability.

---

# 5. Emotional Valence Encoding

Emotional tone may be encoded explicitly.

Format:

    [val=+]
    [val=-]
    [val=0]

Optional numeric gradient allowed:

    [val=+.6]

Emotional valence does not replace emotional lexical roots.

---

# 6. Cognitive Load Marker

Optional marker for internal cognitive state.

Format:

    [load=low]
    [load=mid]
    [load=high]

Or numeric:

    [load=.7]

Purpose:
Encourage metacognitive awareness.

---

# 7. Clarity Marker

Optional.

Format:

    [cla=.X]

Indicates perceived clarity of thought.

---

# 8. Meta Marker Order

Meta markers must follow this order:

1. Primary epistemic marker
2. [pro=]
3. [conf=]
4. [val=]
5. [load=]
6. [cla=]

Example valid order:

    [mdl][pro=.4][conf=.6][val=-.2][load=.7]

Invalid order:

    [conf=.6][mdl]

---

# 9. Interaction Rules

## 9.1 [obs] Constraint

If [obs] is used:

- Probability defaults to 1.0 unless overridden
- [pro] optional

## 9.2 [emo] Constraint

If [emo] is used:

- [val] strongly encouraged
- [pro] discouraged

## 9.3 [hyp] Constraint

If [hyp]:

- [pro] optional
- [conf] strongly encouraged

---

# 10. Dual-Cognition Encoding

When modeling human–AI dyads:

Use dual-number noun marking AND epistemic clarity.

Example:

    Self-du-ta
    plan-mo
    evaluate-in-zo
    [mdl][pro=.6][conf=.7]

Indicates modeled evaluation within dyadic cognition.

---

# 11. Full Sentence Examples

Example 1:

"I suspect the model may be wrong."

    Model-ta
    err-li-mi
    [inf][pro=.5][conf=.6]

---

Example 2:

"I remember feeling tension."

    Self-un-ta
    emo-tension-mo
    experience-tae
    [mem][val=-.5][conf=.8]

---

Example 3:

"This system appears stable."

    System-ta
    stable-in
    [inf][pro=.7][conf=.6]

---

Example 4:

"I feel overwhelmed."

    Self-un-ta
    emo-overload-mo
    increase-in-ha
    [emo][val=-.8][load=high]

---

# 12. Cognitive Rationale

Mandatory epistemic encoding forces:

- Separation of observation vs inference
- Reduced cognitive conflation
- Increased probabilistic reasoning
- Emotional clarity
- Meta-awareness

Over time, this may alter internal thought structuring.

---

# 13. Architectural Decision Log (ADL)

## ADL-015
Decision: Exactly one primary epistemic marker required.
Status: Approved
Rationale: Enforces clarity and parsing simplicity.

## ADL-016
Decision: Numeric probability scale 0–1.
Status: Approved
Rationale: Compatible with machine learning paradigms.

## ADL-017
Decision: Separate probability and confidence markers.
Status: Approved
Rationale: Distinguishes statistical likelihood from subjective certainty.

## ADL-018
Decision: Fixed meta-marker ordering.
Status: Approved
Rationale: Deterministic parsing.

---

# 14. Open Questions

- Should epistemic markers be attachable to subclauses?
- Should nested meta layers be allowed?
- Should probability be mandatory for [inf]?
- Should emotional valence require numeric precision?

Future versions will resolve.
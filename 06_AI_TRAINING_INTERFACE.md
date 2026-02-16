# Syntaxis
## 06_AI_TRAINING_INTERFACE
Version: v0.2-draft
Status: Operational Interface Specification
Depends-On: 01–05
Last Updated: 2026-02-16

---

# 1. Overview

This document defines how Syntaxis interfaces with AI systems:

- Local LLMs
- Fine-tuning and translation adapters
- Validator + parser pipelines
- Corpus storage requirements

Syntaxis must remain:
- Deterministic
- Tokenization-friendly
- Validatable via simple rules

---

# 2. Canonical Storage Format

All stored Syntaxis must:
- Use ASCII only
- Use hyphen stacking for compounds/modifiers
- Use bracketed meta markers
- Store procedural mode in plain text lines with reserved prefixes
- Not store glyphs

Example:
    Self-du-ta AI-ka intention{abs}@S-mo misinterpret@E-li-mi [mdl][pro=.4][conf=.6]

---

# 3. Tokenization Constraints

Prefer:
- Hyphen delimiter for compounding: men-syn
- Suffix particles: -ta -ka -mo -ri -se -nu
- Operator tokens: @E @S
- Classifier braces: {sys} etc.
- Bracket meta tokens: [mdl][pro=.4]...

Avoid:
- CamelCase
- Mixed punctuation inside roots
- Multiple competing delimiters

---

# 4. Parallel Corpus Strategy

Recommended JSONL:
{
  "natural": "I suspect the model may fail.",
  "syntaxis": "Model{sys}-ta fail@E-li-mi [inf][pro=.5][conf=.6]"
}

Include procedural examples as multi-line strings if needed.

---

# 5. Validator Requirements (v0.2)

A validator must check:

1) Exactly one primary epistemic marker exists
2) Meta marker ordering is correct
3) Verb cluster order is VerbRoot + Aspect + Modality
4) Role markers are valid
5) If [pro=...] exists, at least one @E or @S exists in sentence
6) Classifiers, if present, are in approved set
7) Procedural lines:
   - Proc header includes Proc-ta ... define-ke [mdl]
   - Step=n: has integer n and valid sentence after prefix
   - Req:/Inv: lines contain valid sentences

---

# 6. Error Correction Protocol

On invalid output:
1) Identify rule violated
2) Propose corrected form
3) Log error type (for future fine-tuning)

Example:
Invalid:
    System-ta stable-in [mdl][pro=.7][conf=.6]
Fix:
    System@S-ta stable-in [mdl][pro=.7][conf=.6]

---

# 7. Prompting Recommendations

System instruction snippet:
- “Respond only in canonical Syntaxis ASCII.”
- “Include exactly one epistemic marker per sentence.”
- “If you use [pro], include @E or @S.”
- “Use procedural reserved prefixes when describing workflows.”

Provide a short grammar reminder block and 3–5 examples.

---

# 8. Fine-Tuning Strategy

Recommended:
- Train EN ↔ Syntaxis translation adapter
- Add post-generation validator
- Iterate corpus with error-driven examples

Avoid:
- Training from scratch
- Introducing glyph-only training data early

---

# 9. Architectural Decision Log (ADL)

## ADL-022
Decision: JSONL parallel corpus format.
Status: Approved

## ADL-023
Decision: Hyphen delimiter standard.
Status: Approved

## ADL-024
Decision: Post-generation validator required.
Status: Approved

## ADL-030
Decision: Probability requires @E/@S validation rule.
Status: Approved

## ADL-031
Decision: Procedural mode included in canonical corpus.
Status: Approved

## ADL-032
Decision: Classifier tags validated against controlled set.
Status: Approved

---

# 10. Open Questions

- Should Procedural Mode support branching (if/else) in v0.x?
- Should validator output a structured AST format standard?
- When to add optional compact evidential suffix encoding (Quechua-inspired)?
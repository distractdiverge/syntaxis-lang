# Syntaxis
## 06_AI_TRAINING_INTERFACE
Version: v0.1-draft
Status: Operational Interface Specification
Depends-On: 01–05
Last Updated: 2026-02-15

---

# 1. Overview

This document defines how Syntaxis interfaces with AI systems, particularly:

- Local LLMs
- Fine-tuned models
- Translation adapters
- Hybrid symbolic-LLM pipelines

Syntaxis must remain:

- Tokenization-friendly
- Deterministic
- Low-ambiguity
- Expandable without retraining collapse

---

# 2. Canonical Storage Format

All Syntaxis text stored in corpus must:

- Use ASCII only
- Use explicit hyphen stacking
- Use bracketed meta markers
- Avoid glyph-only encoding

Example canonical sentence:

    Self-du-ta AI-ka intention-mo misinterpret-li-mi [mdl][pro=.4][conf=.6]

---

# 3. Tokenization Design Constraints

To optimize transformer compatibility:

- Use consistent delimiter (-)
- Avoid camelCase
- Avoid internal punctuation in roots
- Avoid multi-token suffix variation

Example (preferred):

    clarify-li-mi

Example (avoid):

    clarifyLiMi
    clarify.li.mi

---

# 4. Parallel Corpus Strategy

To train or fine-tune a local model:

## 4.1 Sentence Pair Format

Recommended structure:

JSONL format:

{
  "natural": "I think the model may fail.",
  "syntaxis": "Model-ta fail-li-mi [mdl][pro=.5][conf=.6]"
}

---

## 4.2 Progressive Corpus Stages

Stage 1:
- 500–1000 core parallel sentences
- Cover grammar edge cases

Stage 2:
- 5,000+ domain-specific expansions

Stage 3:
- Journaling corpus (personal usage)

Stage 4:
- AI-generated augmentation with validation

---

# 5. Validation Rules for AI Output

Any AI generating Syntaxis must validate:

1. Exactly one primary epistemic marker
2. Proper verb cluster order
3. Proper meta marker order
4. Valid role suffixes
5. No illegal compounds

Optional:
- Probability bounds check
- Confidence bounds check

---

# 6. Error Detection Protocol

When AI produces invalid Syntaxis:

System must:

1. Identify structural violation
2. Propose corrected version
3. Log error type

Example:

Invalid:
    clarify-mi-li

Correction:
    clarify-li-mi

---

# 7. Prompting Interface Recommendations

When prompting LLMs:

Use explicit system instruction:

"You must respond in canonical Syntaxis form."

Provide grammar reminder block.

Example:

Allowed role markers:
- -ta -ka -mo -ri -se -nu

Verb structure:
VerbRoot + Aspect + Modality

Meta markers mandatory.

---

# 8. Fine-Tuning Strategy

Recommended approach:

1. Use base open-weight model
2. Fine-tune for translation EN ↔ Syntaxis
3. Add structural validator in post-processing
4. Optionally train Syntaxis-only reasoning mode

Avoid:
- Training from scratch
- Overloading with metaphorical data early

---

# 9. Hybrid Symbolic Integration (Future)

Future architecture may include:

- Grammar parser → AST (abstract syntax tree)
- Meta-layer analyzer
- Probability consistency checker
- Emotional trend tracker

Syntaxis can act as:

Structured intermediary representation between human thought and LLM.

---

# 10. Safety Considerations

Meta-layer may expose emotional state and cognitive load.

If used with persistent memory:

- Protect journaling corpus
- Encrypt personal Syntaxis logs
- Avoid exposing raw dual-cognition data

---

# 11. Architectural Decision Log (ADL)

## ADL-022
Decision: JSONL parallel corpus format.
Status: Approved
Rationale: Compatibility with common fine-tuning pipelines.

## ADL-023
Decision: Hyphen delimiter standard.
Status: Approved
Rationale: Tokenization clarity.

## ADL-024
Decision: Post-generation validator required.
Status: Approved
Rationale: Maintain structural integrity.

---

# 12. Open Questions

- Should Syntaxis-only reasoning mode omit English entirely?
- Should AST representation be standardized?
- Should probabilistic markers integrate with Bayesian updating?

To be explored in future iterations.
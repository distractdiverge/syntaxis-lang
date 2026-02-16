# Syntaxis
## 07_VERSIONING_AND_EVOLUTION_PROTOCOL
Version: v0.2-stub
Status: Structural Stub
Depends-On: 01–06
Last Updated: 2026-02-16

---

# 1. Overview

This document governs evolution of Syntaxis without fragmentation.

Syntaxis must avoid:
- Grammar drift
- Lexical chaos
- Backward incompatibility surprises
- Uncontrolled marker proliferation

---

# 2. Versioning Model

Semantic versioning:

    MAJOR.MINOR.PATCH

MAJOR:
- Breaking grammar change
- Changes to role markers, meta rules, @E/@S, or procedural reserved forms

MINOR:
- Additive features (new roots, new classifier tags, new procedural verbs)

PATCH:
- Documentation clarifications and examples; no structural changes

---

# 3. Backward Compatibility

- MAJOR changes require explicit migration guide and validator modes.
- Deprecated elements must remain parseable for one MAJOR cycle.

---

# 4. ADL Governance

All structural changes require:
- ADL entry with rationale
- Tradeoff notes
- Compatibility impact statement
- Test corpus additions

No structural change without ADL.

---

# 5. Experimental Proposals

Experimental items must be labeled:

    EXP-###: <title>

Include:
- Proposed syntax
- Validator rules
- Example sentences (>=10)
- Rollback plan

---

# 6. Lexicon Expansion Governance

New roots require:
- Scope definition
- Non-overlap check
- ADL entry
- ≥10 example sentences

New classifier tags require:
- Controlled set update
- ADL entry
- Ambiguity rationale

---

# 7. Corpus Integrity

All corpora should include headers:

    # Syntaxis vX.Y.Z
    # Grammar: 02 vX.Y
    # Meta: 04 vX.Y

Procedural corpora may include multi-line blocks.

---

# 8. Architectural Decision Log (ADL)

## ADL-025
Decision: Semantic versioning adopted.
Status: Approved

## ADL-026
Decision: All structural changes require ADL entry.
Status: Approved

## ADL-029
Decision: @E/@S operators added (structural).
Status: Approved

## ADL-031
Decision: Procedural mode added (structural).
Status: Approved

## ADL-032
Decision: Classifier tags added (structural).
Status: Approved

---

# 9. Open Questions

- Should Syntaxis adopt a formal RFC directory structure?
- Should experimental features expire automatically?
- When to schedule “grammar freeze” milestone?
# Syntaxis
## 03_LEXICON_ARCHITECTURE
Version: v0.2-draft
Status: Foundational Lexicon System
Depends-On: 01, 02
Last Updated: 2026-02-16

---

# 1. Overview

This document defines how lexical items (roots and compounds) are created, extended, and governed in Syntaxis.

Lexicon growth is controlled to preserve:
- Determinism
- Composability
- AI learnability
- Cognitive clarity

---

# 2. Lexical Philosophy

- Prefer semantic primitives (roots) + compositional compounds
- Avoid idioms and opaque metaphors in canonical form
- Permit concise “procedural vocabulary” for algorithmic mode
- Support optional disambiguation via classifiers `{class}`

---

# 3. Root Construction Rules

## 3.1 Canonical constraints
- 2–3 syllables preferred
- Lowercase ASCII
- No silent characters
- No diacritics

## 3.2 Semantic density rule
Each root maps to a conceptual primitive; avoid roots that encode full clauses.

---

# 4. Compounding Rules

Compound structure:

    Root1-Root2(-Root3)

Meaning flows left → right (rightmost is head).

Default maximum: 3 roots.
Compounds exceeding 3 roots require ADL justification.

---

# 5. Word Class Behavior

No strict noun/verb/adjective classes.
Roots can serve as:
- Term (with role markers)
- Verb root (in verb cluster)
- Modifier (as compound component)

---

# 6. Disambiguation Classifiers `{class}`

Classifier tags are optional and do not change grammar, only meaning clarity.

Form:

    term{class}

Controlled class set (v0.2):
- {ent} entity/agent
- {abs} abstract concept
- {proc} procedure/process artifact
- {dat} data artifact
- {emo} emotional construct
- {rel} relation/edge
- {sys} system/technical construct

Expansion requires ADL entry.

---

# 7. Event/State Operators as Lexical Practice

`@E/@S` are grammatical operators (not lexical roots), but lexicon should support event/state phrasing:

- Prefer verb roots that naturally encode transitions for `@E`
- Prefer state descriptors for `@S`

Example pairings:
- begin@E, stop@E, shift@E
- stable@S, present@S, available@S

---

# 8. Procedural Vocabulary

Procedural Mode requires a stable verb set.

Seed procedural verbs (v0.2):
- define
- collect
- reduce
- transform
- compare
- select
- apply
- verify
- loop
- stop
- emit

---

# 9. Reserved Seed Roots (v0.2)

Foundational roots (do not redefine):

syn  structure
men  mind
rel  relation
dat  data
sen  perception
mod  model
pro  probability
emo  emotion
act  action
tem  process/time
val  value
err  error
sys  system
cla  clarity
con  confidence
hyp  hypothesis
mem  memory
obs  observation
inf  inference

---

# 10. Expansion Protocol

To add a new root:
1) Define semantic scope
2) Confirm no existing compound covers it
3) Add ADL entry
4) Provide ≥10 example sentences in corpus

No synonym redundancy without explicit justification.

---

# 11. Architectural Decision Log (ADL)

## ADL-011
Decision: Roots limited to 2–3 syllables preferred.
Status: Approved

## ADL-012
Decision: No strict word class separation.
Status: Approved

## ADL-013
Decision: Default compound limit of 3 roots.
Status: Approved

## ADL-032
Decision: Controlled classifier tags `{class}`.
Status: Approved

## ADL-031
Decision: Procedural vocabulary seed set.
Status: Approved

---

# 12. Open Questions

- Should classifier tags be mandatory in Procedural Mode?
- Should an official synonym policy exist (e.g., “discouraged synonyms”)?
- When to add Quechua-style evidential compression forms?
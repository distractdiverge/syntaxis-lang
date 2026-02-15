# Syntaxis
## 03_LEXICON_ARCHITECTURE
Version: v0.1-draft
Status: Foundational Lexicon System
Depends-On: 01_SYNOPSIS_AND_INTENT.md
            02_CORE_GRAMMAR_SPEC.md
Last Updated: 2026-02-15

---

# 1. Overview

This document defines how lexical items (roots and compounds) are created, extended, and governed in Syntaxis.

Syntaxis does NOT allow uncontrolled vocabulary growth.

Lexical expansion must follow structural constraints to preserve:

- Determinism
- Composability
- AI learnability
- Cognitive clarity

---

# 2. Lexical Philosophy

Lexicon must be:

- Modular
- Composable
- Domain-extensible
- Emotionally expressive
- Abstraction-friendly

Vocabulary is built from semantic roots rather than idiomatic phrases.

---

# 3. Root Construction Rules

## 3.1 Phonotactic Constraints (ASCII Canonical)

- Roots are 2–3 syllables
- Consonant-Vowel (CV) structure preferred
- No irregular spelling
- No silent characters
- No diacritics in canonical form
- Lowercase only

Example valid roots:

    syn
    men
    rel
    dat
    emo
    pro
    tem
    mod
    act
    sen

---

## 3.2 Root Semantic Density Rule

Each root must represent a conceptual primitive.

Roots must NOT encode:
- Complete sentences
- Idioms
- Culture-specific metaphors

Roots should represent:

- Actions
- States
- Relations
- Cognitive processes
- Abstract domains

---

# 4. Compounding Rules

Compound structure:

    Root1-Root2

Semantic direction:

    Left = qualifier
    Right = head

Examples:

    men-syn
    = structured mind

    dat-sen
    = perceived data

    emo-rel
    = emotional relation

---

## 4.1 Multi-Compound Rule

Compounds may extend:

    Root1-Root2-Root3

Example:

    men-rel-mod
    = modeled mental relationship

Compounds exceeding 3 roots require justification in the Architectural Decision Log.

---

# 5. Word Class Behavior

Syntaxis does not have strict noun/verb/adjective classes.

Roots may function as:

- Noun (when role-marked)
- Verb (when used in verb cluster)
- Modifier (when compounded)

Example:

    stable (root)

As verb:
    stable-in

As noun:
    stable-un-ta

As compound modifier:
    system-stable

---

# 6. Reserved Core Roots (v0.1 Seed Set)

These roots are foundational and cannot be redefined.

| Root | Meaning |
|------|---------|
| syn  | structure |
| men  | mind |
| rel  | relation |
| dat  | data |
| sen  | perception |
| mod  | model |
| pro  | probability |
| emo  | emotion |
| act  | action |
| tem  | process/time |
| val  | value |
| err  | error |
| sys  | system |
| cla  | clarity |
| con  | confidence |
| hyp  | hypothesis |
| mem  | memory |
| obs  | observation |
| inf  | inference |

---

# 7. Abstract Vocabulary Layer

Abstract concepts must be constructed via compounding.

Example:

    uncertainty

Becomes:

    pro-low

Or:

    con-low

No opaque lexicalization allowed unless justified.

---

# 8. Emotional Lexicon

Emotional states are roots, not adjectives.

Examples:

    calm
    fear
    tension
    trust
    doubt

Emotional nuance may be created via compounding:

    fear-low
    tension-high
    trust-fragile

---

# 9. Expansion Protocol

To introduce a new root:

1. Define semantic scope.
2. Confirm no existing compound covers the concept.
3. Document in ADL.
4. Assign version tag.

No synonym redundancy allowed without justification.

---

# 10. Forbidden Patterns

- Irregular morphology
- Gendered lexical roots
- Cultural idioms
- Redundant synonyms
- Silent etymology references

---

# 11. Example Lexical Constructions

Example 1:

    Self-du-ta
    AI-ka
    men-rel-mo
    clarify-li-mi
    [mdl]

Example 2:

    sys-ta
    err-mo
    detect-tae-zo
    [obs][conf=.8]

Example 3:

    men-un-ta
    emo-tension-mo
    increase-ra
    [emo]

---

# 12. AI Training Considerations

Lexical structure must:

- Minimize polysemy
- Avoid homophones
- Maintain stable semantic mapping
- Be easily tokenizable
- Prefer short roots

Corpus building should favor:

- Parallel sentence generation
- Root usage consistency
- Compound frequency balance

---

# 13. Architectural Decision Log (ADL)

## ADL-011
Decision: Roots limited to 2–3 syllables.
Status: Approved
Rationale: Compression + token efficiency.

## ADL-012
Decision: No strict word class separation.
Status: Approved
Rationale: Simplifies grammar and AI training.

## ADL-013
Decision: Compounds limited to max 3 roots by default.
Status: Approved
Rationale: Prevents semantic overloading.

## ADL-014
Decision: Reserved seed root set defined.
Status: Approved
Rationale: Stable foundation for expansion.

---

# 14. Open Questions

- Should emotional valence be a lexical modifier or meta-layer only?
- Should intensity be lexicalized or numeric?
- Should metaphorical compounds be allowed?
- Should domain-specific root namespaces exist?

To be resolved in later versions.
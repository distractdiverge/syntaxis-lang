# Syntaxis
## 02_CORE_GRAMMAR_SPEC
Version: v0.1-draft
Status: Foundational Grammar
Depends-On: 01_SYNOPSIS_AND_INTENT.md
Last Updated: 2026-02-15

---

# 1. Overview

This document defines the deterministic grammatical core of Syntaxis.

All valid Syntaxis sentences must conform to this specification.

The grammar is:
- Agglutinative
- Role-marked
- Deterministic
- ASCII canonical
- Meta-layer compatible

---

# 2. Canonical Sentence Structure

Default canonical order:

    [Topic] [Role-Phrases] [Verb-Cluster] [Meta-Layer]

Where:

- Topic = entity under discussion
- Role-Phrases = agent/object/etc.
- Verb-Cluster = root + aspect + modality
- Meta-Layer = epistemic + probability + confidence

Order flexibility is allowed ONLY when role markers are present.

---

# 3. Role Markers (Grammatical Particles)

Role markers are suffixes appended to noun phrases.

| Marker | Name        | Function |
|---------|------------|----------|
| -ta     | Topic      | Primary discourse focus |
| -ka     | Agent      | Initiator of action |
| -mo     | DirectObj  | Direct object |
| -ri     | Indirect   | Beneficiary / recipient |
| -se     | Locative   | Location / conceptual space |
| -nu     | Instrument | Means / tool |

Role markers are mandatory for multi-argument sentences.

Example:

    Self-ta
    AI-ka
    Meaning-mo
    clarify-in-ke
    [mdl]

---

# 4. Number System

Number is marked directly on noun roots.

| Marker | Meaning |
|---------|---------|
| -un     | Singular |
| -du     | Dual |
| -pl     | Plural |

Example:

    Self-du
    = human + AI dyad

Number markers precede role markers:

    Self-du-ta

Order rule:

    ROOT + NUMBER + ROLE

---

# 5. Verb Cluster Structure

Verb clusters are strictly ordered:

    VerbRoot + Aspect + Modality

No deviation permitted.

---

## 5.1 Aspect Markers

| Marker | Meaning |
|---------|---------|
| -in     | Ongoing |
| -tae    | Completed |
| -li     | Potential |
| -ra     | Emergent |
| -su     | Habitual |

---

## 5.2 Modality Markers

| Marker | Meaning |
|---------|---------|
| -ke     | Intentional |
| -mi     | Uncertain |
| -zo     | Logical deduction |
| -ha     | Emotional impulse |

Aspect MUST precede Modality.

Valid:

    clarify-li-mi

Invalid:

    clarify-mi-li

---

# 6. Word Formation Rules

## 6.1 Roots

Roots:
- 2–3 syllables
- No irregular forms
- No internal silent characters
- No tonal requirement (ASCII canonical)

## 6.2 Compounding

Compound structure:

    Root1-Root2

Meaning flows left → right.

Example:

    men-syn
    = structured mind

Compounds may take role markers as a unit:

    men-syn-un-ta

---

# 7. Topic–Comment Logic

Topic marking (-ta) establishes discourse focus.

If Topic is omitted, first noun defaults to Topic.

Explicit Topic marking is preferred.

Example:

    Model-ta
    Error-mo
    detect-tae-zo
    [obs]

---

# 8. Null Copula Rule

Syntaxis omits "to be".

State expressions use adjectival verbs.

Example:

Instead of:
    System is stable

Use:

    System-ta
    stable-in
    [obs]

---

# 9. Sentence Requirements

A valid sentence must include:

1. At least one noun phrase
2. A verb cluster
3. A meta-layer marker

Meta-layer is mandatory.

---

# 10. Constraints

- No irregular conjugation
- No tense system (aspect only)
- No gender marking
- No articles
- No hidden case marking
- No agreement inflection beyond number

---

# 11. Example Full Sentences

Example 1:

"I think AI may misunderstand my intention."

    Self-du-ta
    AI-ka
    intention-mo
    misinterpret-li-mi
    [mdl][pro=.4][conf=.6]

---

Example 2:

"The data suggests the model failed."

    Data-ta
    model-mo
    fail-tae-zo
    [inf][conf=.7]

---

Example 3:

"I feel uncertain about the plan."

    Self-un-ta
    plan-se
    uncertain-in-ha
    [emo][conf=.5]

---

# 12. Parsing Determinism

Parsing algorithm:

1. Identify all meta-layer markers
2. Identify verb cluster (last non-meta token)
3. Parse noun phrases by role suffix
4. Establish topic
5. Construct relational graph

---

# 13. Architectural Decision Log (ADL)

## ADL-006
Decision: Aspect-only temporal encoding.
Status: Approved
Rationale: Encourages process modeling over rigid time reference.

## ADL-007
Decision: Verb cluster fixed order.
Status: Approved
Rationale: Deterministic parsing for AI systems.

## ADL-008
Decision: Role markers mandatory for multi-argument clauses.
Status: Approved
Rationale: Eliminates word-order ambiguity.

## ADL-009
Decision: No gender marking.
Status: Approved
Rationale: Reduces unnecessary semantic complexity.

## ADL-010
Decision: Null copula.
Status: Approved
Rationale: Structural simplicity and compression.

---

# 14. Open Questions

- Should modality be expandable?
- Should negation be a particle or verb modifier?
- Should conditional logic have dedicated markers?
- Should embedded clauses be bracketed or stacked?

To be resolved in future versions.
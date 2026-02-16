# Syntaxis
## 02_CORE_GRAMMAR_SPEC
Version: v0.2-draft
Status: Foundational Grammar
Depends-On: 01_SYNOPSIS_AND_INTENT.md
Last Updated: 2026-02-16

---

# 1. Overview

This document defines the deterministic grammatical core of Syntaxis.

Syntaxis grammar is:
- Agglutinative
- Role-marked (Korean-inspired)
- Deterministic and validator-friendly
- ASCII canonical (glyphs are render-only)

All valid Syntaxis sentences must conform to this specification.

---

# 2. Canonical Sentence Structure

Default canonical order:

    [Topic] [Role-Phrases] [Verb-Cluster] [Meta-Layer]

When role markers are present, word order may vary without changing meaning.
Default order is recommended for consistency.

---

# 3. Noun Phrase Form

Canonical noun phrase form:

    TERM [Classifier] [Event/State] [Number] [Role]

Where:

- TERM is a root or compound
- Classifier is optional: `{class}`
- Event/State is optional unless probability is used: `@E` or `@S`
- Number is optional: `-un | -du | -pl`
- Role is optional depending on sentence complexity

Example:

    intention{abs}@S-un-mo

---

# 4. Role Markers (Grammatical Particles)

Role markers are suffixes appended to noun phrases.

| Marker | Name        | Function |
|--------|------------|----------|
| -ta    | Topic      | Primary discourse focus |
| -ka    | Agent      | Initiator of action |
| -mo    | DirectObj  | Direct object |
| -ri    | Indirect   | Beneficiary / recipient |
| -se    | Locative   | Location / conceptual space |
| -nu    | Instrument | Means / tool |

Role markers are mandatory for multi-argument clauses.

---

# 5. Number System

Number markers:

| Marker | Meaning |
|--------|---------|
| -un    | Singular |
| -du    | Dual |
| -pl    | Plural |

Order rule (if used):

    TERM{class}@E/-@S + NUMBER + ROLE

Examples:

    Self-du-ta
    Model{sys}-un-ta
    plan{proc}@S-un-mo

---

# 6. Event/State Operators

Event/State operators declare whether a term is being treated as:

- `@E` Event (transition/occurrence)
- `@S` State (condition/holding pattern)

## 6.1 Probability rule
If a sentence includes `[pro=...]`, at least one `@E` or `@S` must appear in that sentence.

Rationale:
Probability must attach to an event/state, not a vague untyped proposition.

Examples:

Valid:
    Rain@E-ta begin-li-mi [hyp][pro=.6][conf=.5]

Valid:
    System@S-ta stable-in [mdl][pro=.7][conf=.6]

Invalid (no @E/@S while using probability):
    System-ta stable-in [mdl][pro=.7][conf=.6]

---

# 7. Verb Cluster Structure

Verb clusters are strictly ordered:

    VerbRoot + Aspect + Modality

No deviation permitted.

---

## 7.1 Aspect Markers

| Marker | Meaning |
|--------|---------|
| -in    | Ongoing |
| -tae   | Completed |
| -li    | Potential |
| -ra    | Emergent |
| -su    | Habitual |

---

## 7.2 Modality Markers

| Marker | Meaning |
|--------|---------|
| -ke    | Intentional |
| -mi    | Uncertain |
| -zo    | Logical deduction |
| -ha    | Emotional impulse |

Aspect MUST precede modality.

Valid:
    clarify-li-mi

Invalid:
    clarify-mi-li

---

# 8. Word Formation Rules

## 8.1 Roots
- 2–3 syllables preferred
- No irregular forms
- Lowercase canonical

## 8.2 Compounds
Compound structure:

    Root1-Root2(-Root3)

Direction:
Left = qualifier, Right = head.

---

# 9. Topic Logic

Topic is marked by `-ta`.
If topic is omitted, the first noun phrase may be interpreted as topic by default, but explicit topic is preferred.

---

# 10. Null Copula Rule

Syntaxis omits "to be".
State expressions use adjectival verbs.

Example:

    System@S-ta stable-in [obs]

---

# 11. Procedural Mode (Deterministic Rhetorical Algorithms)

Procedural Mode is a constrained sub-grammar for workflows.

## 11.1 Reserved prefixes (ASCII)
These prefixes are reserved:

- `Proc:` optional label prefix (non-grammatical; metadata)
- `Proc-ta` grammatical procedure topic
- `Step=n:` step line prefix (n is integer starting at 1)
- `Req:` requirement line prefix
- `Inv:` invariant line prefix
- `Out:` optional output label prefix (non-grammatical; metadata)
- `Out-ta` grammatical output topic

Reserved prefixes are line-initial tokens.

## 11.2 Procedure header
Canonical header form:

    Proc-ta <proc-name>{proc}@S-mo define-ke [mdl]

Example:

    Proc-ta clarify-loop{proc}@S-mo define-ke [mdl]

## 11.3 Steps
Canonical step form:

    Step=1: <sentence>

Where <sentence> is a valid Syntaxis sentence (including meta marker).

Example:

    Step=1: Input{dat}@S-ta data{dat}-mo collect-ke [mdl]

## 11.4 Requirements / Invariants
Requirements:

    Req: <sentence>

Invariants:

    Inv: <sentence>

Example:

    Req: Prompt{dat}@S-ta present@S-in [obs]
    Inv: Meaning{abs}@S-ta preserve@S-in verify-ke [mdl][conf=.8]

---

# 12. Sentence Requirements

A valid sentence must include:
1) At least one term (noun phrase)
2) A verb cluster (or an accepted state verb form)
3) Exactly one primary epistemic marker in meta-layer

---

# 13. Parsing Determinism

Parsing outline:
1) Identify meta-layer tokens (bracketed)
2) Identify verb cluster (last non-meta token)
3) Parse noun phrases by suffix patterns
4) Capture optional `{class}` and `@E/@S`
5) Establish topic and build argument graph
6) Apply probability rule validation (if [pro], ensure @E/@S)

---

# 14. Architectural Decision Log (ADL)

## ADL-006
Decision: Aspect-only temporal encoding.
Status: Approved

## ADL-007
Decision: Verb cluster fixed order.
Status: Approved

## ADL-008
Decision: Role markers mandatory for multi-argument clauses.
Status: Approved

## ADL-010
Decision: Null copula.
Status: Approved

## ADL-029
Decision: Add `@E/@S` operators.
Status: Approved

## ADL-030
Decision: Require `@E/@S` when `[pro]` used.
Status: Approved

## ADL-031
Decision: Procedural Mode reserved prefixes and forms.
Status: Approved

## ADL-032
Decision: Add optional classifier tags `{class}`.
Status: Approved

---

# 15. Open Questions

- Negation design: particle vs verb modifier?
- Conditionals in Procedural Mode (branching)?
- Event subtypes (@E+, @E-, etc.)?
- Clause embedding strategy (brackets vs stacking)?
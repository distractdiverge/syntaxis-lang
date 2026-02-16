# Syntaxis
## 01_SYNOPSIS_AND_INTENT
Version: v0.2-draft
Status: Foundational
Author: Astrid Lapinski (Primary Architect)
Last Updated: 2026-02-16

---

# 1. Overview

Syntaxis is a constructed written language designed as a Cognitive Interface Language (CIL) for structured human–AI interaction and internal cognitive refinement.

Syntaxis is:
- Deterministic
- Composable
- Epistemically explicit
- Probability-capable (event/state oriented)
- Procedurally expressible (algorithmic mode)
- AI-trainable
- Written-first (glyph layer optional; ASCII canonical required)

Syntaxis is not intended to be:
- A naturalistic spoken language
- A culture-building world language
- A purely logical language in the Loglan/Lojban tradition

---

# 2. Problem Statement

Natural languages often:
- Conflate observation and inference
- Omit epistemic certainty and source
- Blur emotional and logical states
- Rely heavily on shared context
- Introduce ambiguity in role marking
- Are inefficient for AI prompt precision

Existing logical conlangs often:
- Over-optimize for formal logic
- Under-support emotional/meta cognition
- Do not standardize probability + confidence + cognitive load
- Are not designed for modern transformer training workflows

Syntaxis targets simultaneous optimization for:
1) Human cognitive structuring
2) Human–AI interface clarity
3) Explicit epistemic encoding
4) Clean probability attachment via event/state modeling
5) Procedural expression (rhetorical algorithms)
6) Written-layer compression and disambiguation aids

---

# 3. Design Goals

## 3.1 Determinism
Each sentence must be parseable without ambiguity given the grammar specification.

## 3.2 Explicit Epistemology
All sentences must include one primary epistemic marker.

## 3.3 Relational Clarity
Semantic roles must be explicitly marked via suffix particles.

## 3.4 Agglutinative Composability
Verbs and compounds must stack meaning in predictable modular ways.

## 3.5 Dual-System Awareness
Support explicit dual-number marking to model dyadic cognition (e.g., human + AI).

## 3.6 AI Compatibility
- Canonical ASCII representation required
- No irregular morphology
- Tokenization-friendly delimiters
- Deterministic validation rules

## 3.7 Event-Based Probability Modeling
Probability attaches to event/state operators to reduce ambiguity and improve reasoning calibration.

## 3.8 Procedural Mode
Provide a deterministic “algorithm as language” mode for workflows, transforms, and validation steps.

## 3.9 Disambiguation Support
Optional classifier tags reduce ambiguity in dense writing without changing grammar.

---

# 4. Non-Goals

Syntaxis is NOT:
- A naturalistic aesthetic conlang
- A culture-building global language
- A poetry-first language
- A phonology-first language
- A direct descendant of any single natural language

---

# 5. Influences

Primary influences:
- Korean (agglutinative morphology, explicit particles)
- Japanese (written-layer separation concept; multi-layer parsing discipline)
- Mandarin Chinese (topic prominence; glyph-density inspiration)

Secondary influences:
- Lithuanian (dual number as conceptual anchor; relational awareness)
- AAVE (compact aspect semantics inspiration)

Deferred exploration (non-binding):
- Quechua evidential morphology (candidate for future meta-layer compression)

---

# 6. System Layers

1) Core Grammar Engine
2) Lexicon Architecture
3) Meta-Thought Encoding Layer
4) Event/State Operators
5) Procedural Mode
6) Disambiguation Classifiers
7) Glyph System (optional render layer)
8) AI Training & Interface Specification
9) Evolution & Versioning Protocol

---

# 7. Canonical Representation

All stored Syntaxis content must have:
- Canonical ASCII representation
- Deterministic role markers
- Mandatory meta markers
- No glyph-only storage

Glyph rendering is optional and secondary.

---

# 8. Intended Use Cases

- AI prompt precision and debugging
- Journaling with epistemic discipline
- Cognitive modeling and calibration
- Dyadic reasoning with AI systems
- Procedural planning and execution scaffolds
- Emotional state encoding with clarity boundaries

---

# 9. Long-Term Vision

- Local AI fine-tuned on a parallel Syntaxis corpus
- Validator + parser producing structured representations (AST / graphs)
- Optional glyph compression layer for rapid reading
- “Cognitive OS” workflows: planning, debugging, reflection

---

# 10. Architectural Decision Log (ADL)

## ADL-001
Decision: Syntaxis will be primarily written.
Status: Approved

## ADL-002
Decision: ASCII canonical form required.
Status: Approved

## ADL-003
Decision: Mandatory epistemic tagging.
Status: Approved

## ADL-004
Decision: Dual number support required.
Status: Approved

## ADL-005
Decision: Agglutinative morphology over fusional.
Status: Approved

## ADL-029
Decision: Add Event/State operators `@E` and `@S`.
Status: Approved

## ADL-030
Decision: If `[pro=...]` is present, at least one `@E` or `@S` is required.
Status: Approved

## ADL-031
Decision: Introduce Procedural Mode (`Proc-ta`, `Step=n:`, `Req:`, `Inv:`, `Out-ta`).
Status: Approved

## ADL-032
Decision: Add optional disambiguation classifiers `term{class}` with a controlled class set.
Status: Approved

---

# 11. Open Questions

- Should reported/hearsay epistemics be added (e.g., [rep])?
- Should event subtypes exist (@E+ onset, @E- stop, etc.)?
- Should Procedural Mode support branching/conditionals in v0.x?
- Should classifier set expand beyond the initial controlled list?
- When/if to add Quechua-style evidential compression forms?
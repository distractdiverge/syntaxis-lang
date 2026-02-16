# Syntaxis
## 08_CANONICAL_WORDS_AND_PHRASES
Version: v0.2-draft
Status: Seed Corpus
Depends-On: 01–07
Last Updated: 2026-02-16

---

# 1. Overview

This document provides:
- Established roots (v0.2)
- Approved compounds
- Classifier set examples
- Event/State operator examples
- Procedural Mode examples
- Canonical sentence templates

All examples conform to Grammar v0.2.

---

# 2. Controlled Classifier Set (v0.2)

- {ent} entity/agent
- {abs} abstract concept
- {proc} procedure/process artifact
- {dat} data artifact
- {emo} emotional construct
- {rel} relation/edge
- {sys} system/technical construct

---

# 3. Established Core Roots (v0.2)

## Cognitive / Structural

syn   structure
men   mind
rel   relation
dat   data
sen   perception
mod   model
pro   probability
emo   emotion
act   action
tem   process/time
val   value
err   error
sys   system
cla   clarity
con   confidence
hyp   hypothesis
mem   memory
obs   observation
inf   inference

## Emotional Roots (seed)

calm
fear
trust
doubt
tension
overload
joy
anger
sad
focus
drift

## Functional Verbs (seed)

clarify
detect
evaluate
increase
decrease
shift
stabilize
compare
align
misinterpret
observe
model
remember
verify

## Procedural Verbs (v0.2)

define
collect
reduce
transform
compare
select
apply
verify
loop
stop
emit

---

# 4. Approved Compounds (v0.2)

men-syn              structured mind
men-rel              mental relation
dat-sen              perceived data
sys-stable           system stability
emo-tension          emotional tension
emo-overload         emotional overload
plan-model           modeled plan
reasoning-trace      reasoning trace (AI output artifact)
prompt-spec          prompt specification (data artifact)

---

# 5. Event/State Operator Templates

## 5.1 Probability requires @E/@S

Valid:
    System{sys}@S-ta stable-in [mdl][pro=.7][conf=.6]

Valid:
    Model{sys}-ta fail@E-li-mi [inf][pro=.5][conf=.6]

Invalid:
    Model{sys}-ta fail-li-mi [inf][pro=.5][conf=.6]

---

# 6. Standard Sentence Templates

## 6.1 Observation

    X@S-ta Y-mo detect-tae-zo [obs][conf=.X]

Example:
    Data{dat}@S-ta err{abs}-mo detect-tae-zo [obs][conf=.9]

## 6.2 Inference with probability (event)

    X-ta Y@E-li-mi [inf][pro=.X][conf=.Y]

Example:
    Model{sys}-ta fail@E-li-mi [inf][pro=.5][conf=.6]

## 6.3 Emotional report

    Self{ent}-un-ta emo-overload{emo}-mo increase-in-ha [emo][val=-.8][load=high]

## 6.4 Memory

    Self{ent}-un-ta emo-fear{emo}-mo experience-tae [mem][conf=.8]

---

# 7. AI Interaction Examples

## 7.1 Ask AI to clarify reasoning

    AI{ent}-ka reasoning-trace{dat}-mo clarify-ke [mdl]

## 7.2 Report mismatch between intention and output (event)

    Self{ent}-un-ta mismatch{rel}@E-mo detect-tae-zo [inf][pro=.6][conf=.7]

## 7.3 Request a revised prompt (procedural output)

    AI{ent}-ka prompt-spec{dat}@S-mo emit-ke [mdl][conf=.7]

---

# 8. Procedural Mode Example (v0.2)

Proc-ta clarify-loop{proc}@S-mo define-ke [mdl]

Req: Prompt{dat}@S-ta present@S-in verify-ke [obs]

Step=1: Self{ent}-du-ta intention{abs}@S-mo state-ke [mdl][conf=.7]
Step=2: AI{ent}-ka meaning{abs}@S-mo reflect-ke [mdl]
Step=3: Self{ent}-un-ta mismatch{rel}@E-mo detect-tae-zo [inf][pro=.5][conf=.6]
Step=4: Self{ent}-un-ta constraint{abs}@S-mo add-ke [mdl]
Step=5: Out-ta revised-prompt{dat}@S-mo emit-ke [mdl]

Inv: Meaning{abs}@S-ta preserve@S-in verify-ke [mdl][conf=.8]

---

# 9. Structured Journaling Template

Daily (minimal):

    Self{ent}-un-ta
    focus{emo}@S-mo evaluate-in-zo
    [mdl][conf=.7][load=.5]

Daily (probability-aware decision):

    Self{ent}-un-ta
    plan{proc}@S-mo select-ke
    success{abs}@E-li-mi
    [hyp][pro=.6][conf=.6][cla=.6]

---

# 10. Architectural Decision Log (ADL)

## ADL-027
Decision: Canonical example corpus required.
Status: Approved

## ADL-028
Decision: Seed lexicon frozen for v0.1/v0.2 baseline.
Status: Approved

## ADL-030
Decision: Probability requires @E/@S in examples and training corpus.
Status: Approved

## ADL-031
Decision: Procedural Mode examples included in seed corpus.
Status: Approved

## ADL-032
Decision: Classifier tags demonstrated in canonical examples.
Status: Approved

---

# 11. Open Questions

- Add additional procedural verbs (normalize, summarize, rank)?
- Add a reported/hearsay epistemic marker ([rep])?
- Add event subtypes (@E+ onset, @E- stop)?
- Add official shorthand macros (non-canonical) for journaling?
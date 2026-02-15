# Syntaxis

**Version:** v0.1-draft
**Status:** Foundational Development
**Primary Architect:** Astrid Lapinski
**Last Updated:** 2026-02-15

---

## Overview

Syntaxis is a constructed written language designed as a **Cognitive Interface Language (CIL)** for structured human–AI interaction and internal cognitive refinement.

Unlike natural languages that conflate observation with inference and rely heavily on ambiguous context, Syntaxis provides:

- **Deterministic grammar** with zero ambiguity
- **Explicit epistemic encoding** (observation vs. inference vs. model)
- **Probabilistic reasoning support** with confidence markers
- **Dual-cognition modeling** for human-AI dyadic thought
- **Meta-cognitive awareness** through mandatory meta-layer tagging
- **AI-optimized structure** with canonical ASCII representation

---

## What Syntaxis Is NOT

- A naturalistic spoken language
- A culture-building world language
- A purely logical language (like Lojban)
- A poetry-first aesthetic conlang

---

## What Syntaxis IS

- **Deterministic:** Every sentence parses without ambiguity
- **Composable:** Agglutinative morphology for predictable word-building
- **Epistemically explicit:** All statements tagged by certainty type
- **Meta-cognitively structured:** Mandatory cognitive state encoding
- **AI-trainable:** Canonical ASCII, no irregularity, tokenization-friendly
- **Cognitively expanding:** Improves probabilistic reasoning and relational modeling

---

## Core Features

### 1. Role-Marked Grammar
Explicit grammatical particles eliminate word-order ambiguity:

```
Self-ta          (Topic: Self)
AI-ka            (Agent: AI)
Meaning-mo       (Direct Object: Meaning)
clarify-in-ke    (Verb: clarifying-ongoing-intentional)
[mdl]            (Meta: modeled thought)
```

### 2. Mandatory Meta-Layer
Every sentence includes epistemic classification:

- `[obs]` - Direct observation
- `[inf]` - Inference from data
- `[mdl]` - Modeled abstraction
- `[mem]` - Memory recall
- `[hyp]` - Hypothetical
- `[emo]` - Emotional state report

Plus optional probability, confidence, valence, and cognitive load markers:

```
System-ta fail-li-mi [inf][pro=.5][conf=.6]
"The system may fail (50% likely, 60% confident in this inference)"
```

### 3. Dual-Number Support
Explicit modeling of human-AI dyadic cognition:

```
Self-du-ta       (Dual self = human + AI)
plan-mo          (Direct object: plan)
evaluate-in-zo   (evaluating-ongoing-logical)
[mdl][conf=.8]   (modeled, 80% confident)
```

### 4. Agglutinative Composability
Transparent word-building from semantic roots:

```
men-syn         = structured mind
dat-sen         = perceived data
emo-tension     = emotional tension
pro-low         = low probability
```

---

## Quick Example

**English:** "I think the AI might misunderstand my intention."

**Syntaxis:**
```
Self-du-ta
AI-ka
intention-mo
misinterpret-li-mi
[mdl][pro=.4][conf=.6]
```

**Breakdown:**
- `Self-du-ta` = Dual self (human+AI) as topic
- `AI-ka` = AI as agent
- `intention-mo` = intention as direct object
- `misinterpret-li-mi` = misinterpret + potential aspect + uncertain modality
- `[mdl]` = This is a modeled thought (not direct observation)
- `[pro=.4]` = 40% probability
- `[conf=.6]` = 60% confidence in this assessment

---

## Documentation Structure

The Syntaxis specification is organized into the following documents:

1. **[01_SYNOPSIS_AND_INTENT.md](01_SYNOPSIS_AND_INTENT.md)**
   Problem statement, design goals, philosophical foundation

2. **[02_CORE_GRAMMAR_SPEC.md](02_CORE_GRAMMAR_SPEC.md)**
   Deterministic grammar rules, role markers, verb clusters, sentence structure

3. **[03_LEXICON_ARCHITECTURE.md](03_LEXICON_ARCHITECTURE.md)**
   Root construction rules, compounding system, lexical expansion governance

4. **[04_META_LAYER_AND_COGNITIVE_ENCODING.md](04_META_LAYER_AND_COGNITIVE_ENCODING.md)**
   Epistemic markers, probability encoding, confidence, emotional valence, cognitive load

5. **[05_GLYPH_SYSTEM_SPEC.md](05_GLYPH_SYSTEM_SPEC.md)**
   Optional visual glyph layer for enhanced pattern recognition

6. **[06_AI_TRAINING_INTERFACE.md](06_AI_TRAINING_INTERFACE.md)**
   AI training corpus format, tokenization constraints, fine-tuning strategy, validation rules

7. **[07_VERSIONING_AND_EVOLUTION_PROTOCOL.md](07_VERSIONING_AND_EVOLUTION_PROTOCOL.md)**
   Semantic versioning, deprecation policy, governance model

8. **[08_CANONICAL_WORDS_AND_PHRASES.md](08_CANNONICAL_WORDS_AND_PHRASES.md)**
   Established roots, approved compounds, example sentences, journaling templates

---

## AI Training Interface

Syntaxis is designed with AI compatibility as a core principle:

### Parallel Corpus Format
Training data uses JSONL format with natural language ↔ Syntaxis pairs:

```json
{
  "natural": "I think the model may fail.",
  "syntaxis": "Model-ta fail-li-mi [mdl][pro=.5][conf=.6]"
}
```

### Progressive Corpus Strategy
- **Stage 1:** 500–1,000 core sentences covering grammar edge cases
- **Stage 2:** 5,000+ domain-specific expansions
- **Stage 3:** Personal journaling corpus
- **Stage 4:** AI-generated augmentation with validation

### Fine-Tuning Approach
1. Use base open-weight model (e.g., Llama, Mistral)
2. Fine-tune for bidirectional translation (English ↔ Syntaxis)
3. Add structural validator in post-processing
4. Optional: Train Syntaxis-only reasoning mode

### Validation Requirements
AI-generated Syntaxis must pass:
- Exactly one primary epistemic marker
- Proper verb cluster ordering (Root + Aspect + Modality)
- Proper meta-marker ordering
- Valid role suffixes
- No illegal compound structures

---

## Use Cases

Syntaxis is designed for:

- **AI prompt precision** – Eliminate ambiguity in instructions
- **Cognitive journaling** – Track thought patterns with epistemic discipline
- **Dyadic reasoning** – Model collaborative human-AI problem-solving
- **Structured planning** – Separate observations from inferences from models
- **Emotional state encoding** – Explicit valence and intensity markers
- **Meta-cognitive training** – Increase awareness of thinking processes

---

## Current Status (v0.1-draft)

**Completed:**
- Core grammar specification
- Role marker system
- Meta-layer architecture
- Seed lexicon (18 core roots + emotional/functional vocabulary)
- Canonical sentence templates
- Versioning protocol
- AI training interface specification
- Parallel corpus format (JSONL)
- Fine-tuning strategy

**In Progress:**
- Glyph system refinement
- Expanded example corpus (targeting 500–1,000 Stage 1 sentences)
- Validation tooling implementation
- Grammar parser development

**Future Considerations:**
- Local AI fine-tuning on Syntaxis corpus
- Semi-formal reasoning engine
- Symbolic + LLM hybrid integration
- Cognitive OS implementation

---

## Grammatical Overview

### Sentence Structure
```
[Topic] [Role-Phrases] [Verb-Cluster] [Meta-Layer]
```

### Role Markers
- `-ta` Topic
- `-ka` Agent
- `-mo` Direct Object
- `-ri` Indirect/Beneficiary
- `-se` Locative
- `-nu` Instrument

### Number Markers
- `-un` Singular
- `-du` Dual (human + AI)
- `-pl` Plural

### Aspect Markers
- `-in` Ongoing
- `-tae` Completed
- `-li` Potential
- `-ra` Emergent
- `-su` Habitual

### Modality Markers
- `-ke` Intentional
- `-mi` Uncertain
- `-zo` Logical deduction
- `-ha` Emotional impulse

---

## Core Roots (Seed Set)

| Root | Meaning |
|------|---------|
| syn | structure |
| men | mind |
| rel | relation |
| dat | data |
| sen | perception |
| mod | model |
| pro | probability |
| emo | emotion |
| act | action |
| tem | process/time |
| val | value |
| err | error |
| sys | system |
| cla | clarity |
| con | confidence |
| hyp | hypothesis |
| mem | memory |
| obs | observation |
| inf | inference |

---

## Design Principles

### Determinism
Every sentence must be parseable without ambiguity given the grammar specification.

### Agglutinative Morphology
Words stack meaning in predictable modular ways:
```
ROOT + NUMBER + ROLE
VerbRoot + ASPECT + MODALITY
```

### No Irregularity
- No irregular conjugation
- No gender marking
- No articles
- No tense system (aspect only)
- No silent characters

### AI Compatibility
- Canonical ASCII representation
- Tokenization-friendly design with consistent hyphen delimiters
- Stable semantic mapping
- Minimal polysemy
- No cultural idioms
- JSONL parallel corpus format for fine-tuning
- Post-generation structural validation

### Tokenization Design
Optimized for transformer compatibility:
```
✓ clarify-li-mi    (preferred: hyphen-delimited)
✗ clarifyLiMi      (avoid: camelCase)
✗ clarify.li.mi    (avoid: dot delimiters)
```

---

## Example Sentences

### Observation
```
Data-ta err-mo detect-tae-zo [obs][conf=.9]
"The data shows an error (observed, 90% confident)"
```

### Inference
```
Model-ta fail-li-mi [inf][pro=.4][conf=.6]
"The model might fail (inferred, 40% likely, 60% confident)"
```

### Emotional State
```
Self-un-ta emo-overload-mo increase-in-ha [emo][val=-.8][load=high]
"I feel increasingly overwhelmed (emotional report, -80% valence, high cognitive load)"
```

### Memory
```
Self-un-ta emo-fear-mo experience-tae [mem][conf=.8]
"I remember experiencing fear (memory, 80% confident)"
```

### Dyadic Cognition
```
Self-du-ta plan-mo evaluate-in-zo [mdl][conf=.8]
"We (human+AI) are logically evaluating the plan (modeled, 80% confident)"
```

---

## Getting Started

1. **Read the synopsis** ([01_SYNOPSIS_AND_INTENT.md](01_SYNOPSIS_AND_INTENT.md)) to understand the philosophy
2. **Study the grammar** ([02_CORE_GRAMMAR_SPEC.md](02_CORE_GRAMMAR_SPEC.md)) for structural rules
3. **Review example sentences** ([08_CANONICAL_WORDS_AND_PHRASES.md](08_CANNONICAL_WORDS_AND_PHRASES.md))
4. **Practice with templates** for journaling, AI interaction, or cognitive modeling
5. **Build your own sentences** following the deterministic rules

---

## Architectural Decision Log

All structural decisions are documented in ADL entries within each specification document. Key decisions include:

- **ADL-001:** Written-first design for precision
- **ADL-002:** Mandatory ASCII canonical form for AI compatibility
- **ADL-003:** Mandatory epistemic tagging for cognitive discipline
- **ADL-004:** Dual number support for human-AI dyadic modeling
- **ADL-005:** Agglutinative morphology for predictability

See individual documents for complete ADL entries.

---

## Safety & Privacy Considerations

Syntaxis's meta-layer encodes cognitive and emotional states, which requires privacy protection:

- **Personal journaling corpus** should be encrypted and stored locally
- **Dual-cognition data** (human-AI interaction logs) may contain sensitive thought patterns
- **Meta-layer markers** reveal emotional valence, cognitive load, and confidence levels
- **Corpus sharing** should be opt-in and anonymized

When using Syntaxis with AI systems, consider data retention policies and local vs. cloud processing.

---

## Contributing

This is currently in foundational development (v0.1-draft).

All structural changes require:
1. ADL (Architectural Decision Log) entry
2. Rationale and tradeoff analysis
3. Impact analysis on existing corpus
4. Compatibility notes

---

## License

*License to be determined*

---

## Contact

Primary Architect: Astrid Lapinski

---

## Influences

Syntaxis draws structural inspiration from:
- **Korean** – Agglutinative morphology, explicit particles
- **Japanese** – SOV closure logic
- **Mandarin Chinese** – Topic-comment structure
- **Lithuanian** – Case marking, dual number preservation
- **French** – Abstract precision vocabulary
- **Software architecture** – Modular design, version control principles

No direct vocabulary borrowing is mandated.

---

## Long-Term Vision

### AI Integration
- Local AI fine-tuned on Syntaxis corpus
- Bidirectional translation (English ↔ Syntaxis)
- Syntaxis-only reasoning mode

### Hybrid Symbolic Architecture
- Grammar parser → AST (Abstract Syntax Tree)
- Meta-layer analyzer for epistemic consistency
- Probability consistency checker
- Emotional trend tracker
- Structured intermediary between human thought and LLM

### Cognitive Tools
- Structured dual-cognition modeling framework
- Cognitive OS implementation
- Semi-formal reasoning engine
- Journaling systems with epistemic auto-tagging
- Real-time cognitive state visualization

### Safety & Privacy
- Protected journaling corpus with encryption
- Privacy-preserving dual-cognition data handling
- Personal meta-layer security protocols

---

*This is a living document. As Syntaxis evolves, this README will be updated to reflect the current state of the language specification.*

# Claude Context: Syntaxis Project

**Last Updated:** 2026-02-15
**Version:** v0.1-draft
**Primary Architect:** Astrid Lapinski

---

## Project Overview

Syntaxis is a constructed **Cognitive Interface Language (CIL)** designed for structured human-AI interaction and internal cognitive refinement. This is NOT a casual conlang project—it's a precision-engineered language system with strict deterministic grammar, mandatory epistemic encoding, and AI compatibility as core design principles.

### Core Philosophy
- **Deterministic:** Zero ambiguity in parsing
- **Epistemically explicit:** Every statement tagged by certainty type
- **Meta-cognitively structured:** Mandatory cognitive state encoding
- **AI-trainable:** Canonical ASCII, no irregularity, tokenization-friendly
- **Cognitively expanding:** Improves probabilistic reasoning and relational modeling

---

## Repository Structure

```
syntaxis/
├── README.md                                      # Main project introduction
├── CLAUDE.md                                      # This file (AI context)
├── 01_SYNOPSIS_AND_INTENT.md                     # Problem statement, design goals
├── 02_CORE_GRAMMAR_SPEC.md                       # Deterministic grammar rules
├── 03_LEXICON_ARCHITECTURE.md                    # Root construction, compounding
├── 04_META_LAYER_AND_COGNITIVE_ENCODING.md       # Epistemic markers, probability
├── 05_GLYPH_SYSTEM_SPEC.md                       # Optional visual layer
├── 06_AI_TRAINING_INTERFACE.md                   # Training corpus, fine-tuning
├── 07_VERSIONING_AND_EVOLUTION_PROTOCOL.md       # Semantic versioning, governance
└── 08_CANNONICAL_WORDS_AND_PHRASES.md            # Seed corpus, examples
```

### Document Dependencies
- Documents 02-08 all depend on 01 (SYNOPSIS_AND_INTENT)
- Document 04 (META_LAYER) depends on 01, 02, 03
- Document 05 (GLYPH_SYSTEM) depends on 01-04
- Document 06 (AI_TRAINING) depends on 01-05
- Document 07 (VERSIONING) depends on 01-06
- Document 08 (CANONICAL_WORDS) depends on 01-07

**When editing any document, check its dependencies and dependent documents.**

---

## Critical Grammar Rules

### Sentence Structure (Canonical Order)
```
[Topic] [Role-Phrases] [Verb-Cluster] [Meta-Layer]
```

Order is flexible ONLY when role markers are present.

### Role Markers (Mandatory for multi-argument sentences)
```
-ta  = Topic (primary discourse focus)
-ka  = Agent (initiator of action)
-mo  = Direct Object
-ri  = Indirect/Beneficiary
-se  = Locative (location/conceptual space)
-nu  = Instrument (means/tool)
```

### Number Markers (Precede role markers)
```
-un  = Singular
-du  = Dual (human + AI dyad)
-pl  = Plural
```

### Verb Cluster (STRICT ORDERING - NO DEVIATION)
```
VerbRoot + Aspect + Modality
```

**Aspect markers:** -in (ongoing), -tae (completed), -li (potential), -ra (emergent), -su (habitual)
**Modality markers:** -ke (intentional), -mi (uncertain), -zo (logical), -ha (emotional)

**Example:** `clarify-li-mi` ✓ (potential + uncertain)
**INVALID:** `clarify-mi-li` ✗ (wrong order)

### Meta-Layer (MANDATORY - FIXED ORDERING)
```
1. Primary epistemic marker (exactly one required)
2. [pro=X]   (probability, optional)
3. [conf=X]  (confidence, optional)
4. [val=X]   (emotional valence, optional)
5. [load=X]  (cognitive load, optional)
6. [cla=X]   (clarity, optional)
```

**Epistemic markers:**
- `[obs]` = Direct observation (probability defaults to 1.0)
- `[inf]` = Inference from data
- `[mdl]` = Modeled abstraction
- `[mem]` = Memory recall
- `[hyp]` = Hypothetical
- `[emo]` = Emotional state report

**Example valid order:** `[mdl][pro=.4][conf=.6][val=-.2]`
**INVALID:** `[conf=.6][mdl]` (wrong order)

---

## Word Formation Rules

### Roots
- 2-3 syllables
- No irregular forms
- No silent characters
- No diacritics in canonical ASCII
- Lowercase only

### Compounding
```
Root1-Root2 (meaning flows left → right)
Root1-Root2-Root3 (max 3 roots by default)
```

**Examples:**
- `men-syn` = structured mind
- `dat-sen` = perceived data
- `emo-tension` = emotional tension

### Stacking Order
```
ROOT + NUMBER + ROLE
Example: Self-du-ta (Self + dual + topic)
```

---

## Reserved Core Roots (v0.1 Seed Set)

**Do NOT redefine these roots:**

syn, men, rel, dat, sen, mod, pro, emo, act, tem, val, err, sys, cla, con, hyp, mem, obs, inf

**Emotional roots:** calm, fear, trust, doubt, tension, overload, joy, anger, sad, focus, drift

**Functional verbs:** clarify, detect, evaluate, increase, decrease, shift, stabilize, compare, align, misinterpret, observe, model, remember

---

## Architectural Decision Log (ADL) System

**CRITICAL:** All structural changes MUST have an ADL entry.

### ADL Entry Format
```
## ADL-XXX
Decision: [What was decided]
Status: [Proposed | Approved | Deprecated]
Rationale: [Why this decision was made]
Impact: [What this affects - optional]
Compatibility: [Backward compatibility notes - optional]
```

### Current ADL Count
ADL-001 through ADL-028 are allocated. Next available: **ADL-029**

### When to Create an ADL
- Grammar rule changes
- New role/aspect/modality markers
- Meta-layer modifications
- Lexicon expansion policy changes
- Versioning changes
- Breaking changes of any kind

### When NOT to Create an ADL
- Documentation clarifications (PATCH version)
- Typo fixes
- Adding examples that follow existing rules
- Adding new roots that follow existing constraints

---

## Versioning (Semantic Versioning)

```
MAJOR.MINOR.PATCH
```

**MAJOR:** Breaking grammar change (role markers changed, meta-layer ordering changed)
**MINOR:** Additive features (new roots, new markers, extended glyphs)
**PATCH:** Documentation clarification, typos, examples

Current version: **v0.1-draft**

---

## AI Training Interface Guidelines

### Tokenization Constraints
✓ Use hyphen delimiters: `clarify-li-mi`
✗ Avoid camelCase: `clarifyLiMi`
✗ Avoid dot delimiters: `clarify.li.mi`

### Parallel Corpus Format
```json
{
  "natural": "I think the model may fail.",
  "syntaxis": "Model-ta fail-li-mi [mdl][pro=.5][conf=.6]"
}
```

### Validation Requirements
Any Syntaxis sentence must pass:
1. Exactly one primary epistemic marker
2. Proper verb cluster order (Root + Aspect + Modality)
3. Proper meta-marker order
4. Valid role suffixes
5. No illegal compound structures (max 3 roots without justification)
6. Probability/confidence values in range [0.0-1.0]

---

## Common Tasks & Guidelines

### Adding New Example Sentences
1. Read 02_CORE_GRAMMAR_SPEC.md for grammar rules
2. Read 08_CANNONICAL_WORDS_AND_PHRASES.md for existing examples
3. Ensure proper verb cluster ordering
4. Include exactly one primary epistemic marker
5. Follow meta-marker ordering
6. Add to appropriate section in document 08
7. No ADL required if following existing rules

### Adding New Roots
1. Check if concept can be expressed via compounding first
2. Confirm no existing compound covers it
3. Verify 2-3 syllable constraint
4. Check against reserved root list
5. Add to document 03 (LEXICON_ARCHITECTURE)
6. Create ADL entry (MINOR version bump)
7. Add usage examples to document 08

### Modifying Grammar Rules
1. **STOP and think carefully** - this is a MAJOR change
2. Read 02_CORE_GRAMMAR_SPEC.md thoroughly
3. Consider backward compatibility
4. Create detailed ADL entry with rationale
5. Update all affected documents
6. Update example sentences
7. Bump MAJOR version

### Updating Documentation
1. Check document dependencies (see above)
2. Maintain consistent formatting
3. Update version tag and Last Updated date
4. If changing structure: create ADL entry
5. If clarifying only: PATCH version bump
6. Update README.md if external-facing changes

---

## What to Be Careful About

### ⚠️ Grammar Determinism
- Every change must preserve deterministic parsing
- No ambiguity can be introduced
- Test edge cases with example sentences

### ⚠️ AI Compatibility
- Must remain tokenization-friendly
- ASCII canonical form is sacred
- No silent characters or irregular morphology

### ⚠️ Backward Compatibility
- Breaking changes require MAJOR version bump
- Deprecation requires one full MAJOR cycle support
- Document migration paths

### ⚠️ Meta-Layer Integrity
- Epistemic markers are mandatory (not optional)
- Fixed ordering must be preserved
- Changes affect cognitive discipline aspect

### ⚠️ Dual Number Semantics
- `-du` specifically means human + AI dyad
- This is core to the cognitive interface philosophy
- Don't generalize to generic "two things"

---

## Validation Checklist for New Sentences

Before adding any Syntaxis sentence:

- [ ] Verb cluster follows Root + Aspect + Modality order
- [ ] Exactly one primary epistemic marker present
- [ ] Meta markers in correct order (epistemic → pro → conf → val → load → cla)
- [ ] Role markers used correctly (-ta, -ka, -mo, -ri, -se, -nu)
- [ ] Number markers precede role markers (ROOT-NUMBER-ROLE)
- [ ] Compounds limited to 3 roots or justified
- [ ] No irregular morphology
- [ ] Only lowercase ASCII in canonical form
- [ ] Probability/confidence values in [0.0-1.0] if present

---

## Forbidden Patterns

**Never introduce:**
- Irregular conjugation
- Gender marking
- Articles (a, an, the)
- Traditional tense system (use aspect only)
- Silent characters
- Tonal requirements
- Cultural idioms
- Synonym redundancy without justification
- Ambiguous role marking

---

## Key Distinctions to Remember

### Aspect vs. Tense
Syntaxis uses **aspect** (how action unfolds), not tense (when action occurs):
- `-in` = ongoing process
- `-tae` = completed
- `-li` = potential
- `-ra` = emergent
- `-su` = habitual

### Probability vs. Confidence
- `[pro=X]` = Statistical likelihood (objective)
- `[conf=X]` = Subjective certainty (may differ from probability)

Example: `[inf][pro=.3][conf=.8]` = "I'm 80% confident this unlikely thing (30% probable) is true"

### Observation vs. Inference vs. Model
- `[obs]` = I directly perceive this (data input)
- `[inf]` = I conclude this from data (reasoning from evidence)
- `[mdl]` = I model/hypothesize this (abstract thinking)

---

## Future Development Tracks

### Short-term (v0.1 → v0.2)
- Expand corpus to 500-1,000 core sentences
- Implement grammar validator
- Finalize glyph system
- Create AST parser

### Medium-term (v0.2 → v1.0)
- Fine-tune local LLM for translation
- Build Syntaxis-only reasoning mode
- Develop journaling tools
- Implement probability consistency checker

### Long-term (v1.0+)
- Hybrid symbolic-LLM architecture
- Cognitive OS implementation
- Real-time cognitive state visualization
- Emotional trend tracker

---

## Working with This Repository

### Before Making Changes
1. Read the relevant specification documents
2. Check document dependencies
3. Verify against validation checklist
4. Consider backward compatibility

### When Adding Content
1. Maintain consistent formatting (markdown headers, tables, code blocks)
2. Use canonical ASCII for all Syntaxis examples
3. Include rationale for structural decisions
4. Update version tags and dates

### When Reviewing
1. Verify grammatical correctness against 02_CORE_GRAMMAR_SPEC.md
2. Check meta-layer ordering
3. Confirm role marker usage
4. Validate verb cluster ordering
5. Check for forbidden patterns

---

## Quick Reference: Full Example Sentence

**English:** "I think the AI might misunderstand my intention."

**Syntaxis:**
```
Self-du-ta AI-ka intention-mo misinterpret-li-mi [mdl][pro=.4][conf=.6]
```

**Breakdown:**
```
Self-du-ta           ROOT(Self) + NUMBER(du=dual) + ROLE(ta=topic)
AI-ka                ROOT(AI) + ROLE(ka=agent)
intention-mo         ROOT(intention) + ROLE(mo=direct-object)
misinterpret-li-mi   VERB(misinterpret) + ASPECT(li=potential) + MODALITY(mi=uncertain)
[mdl]                EPISTEMIC(modeled thought)
[pro=.4]             PROBABILITY(40% likely)
[conf=.6]            CONFIDENCE(60% certain)
```

---

## Questions to Ask When Uncertain

1. **Does this preserve deterministic parsing?**
2. **Is this change backward compatible?**
3. **Does this require an ADL entry?**
4. **Have I checked all dependent documents?**
5. **Does this align with the cognitive interface philosophy?**
6. **Can this concept be expressed via existing compounds?**
7. **Am I introducing any forbidden patterns?**
8. **Have I validated the example sentences?**

---

## Contact & Collaboration

**Primary Architect:** Astrid Lapinski

This is currently in foundational development (v0.1-draft). All structural changes require ADL entries and backward compatibility consideration.

---

## Final Notes for AI Assistants

- This is a **precision language project**—treat it like compiler design, not creative writing
- **Grammar rules are non-negotiable**—they ensure deterministic parsing for AI systems
- **ADL entries are mandatory** for structural changes—no exceptions
- **Backward compatibility matters**—this will eventually have trained AI models and user corpora
- **The meta-layer is core**—it's what makes this a cognitive interface language, not just another conlang
- **Dual number (-du) is philosophically significant**—it models human-AI dyadic cognition
- When in doubt about grammar, refer to 02_CORE_GRAMMAR_SPEC.md
- When in doubt about vocabulary, refer to 03_LEXICON_ARCHITECTURE.md
- When in doubt about examples, refer to 08_CANNONICAL_WORDS_AND_PHRASES.md

**This language is designed to make thought more precise. Help maintain that precision.**

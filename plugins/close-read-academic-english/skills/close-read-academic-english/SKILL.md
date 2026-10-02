---
name: close-read-academic-english
description: Analyze and teach academic English and SCI paper sentences using the user's established close-reading method. Use for sentence parsing, long-sentence explanation, prepositional phrases, PP attachment, head and dependency judgments, constituency versus dependency grammar, head projection, complement versus adjunct/modifier distinctions, verb valency and complementation, lexical construction versus syntactic valency, multi-word verbs and free combinations, particle versus preposition, grammar trees, structural rewrites, or natural Chinese translation during paper reading.
---

# Academic English Close Reading

Apply a modern, practical grammar framework. Preserve four distinct layers; never collapse them into the vague labels “定语/状语” when a more precise term is available:

1. **Form/category**: word, NP, VP, PP, AdjP, AdvP, finite/non-finite clause.
2. **Syntactic function**: Subject, Predicator, Object, Predicative Complement, Complement, Adjunct, Modifier, Postmodifier.
3. **Attachment/dependency**: state exactly which head or phrase the unit depends on and whether it is inside an NP or outside it at VP/clause level.
4. **Semantic role**: place, time, manner, means, cause, purpose, condition, source, goal, content, affected entity, etc.

Do not infer function from meaning alone. Make the structural judgment first, then explain the semantic relation.

## Keep the analytical frameworks separate

Before answering an attachment question, identify which framework the statement belongs to:

- **Constituency grammar** asks which phrase contains or hosts another constituent. Show NP, VP, PP, clause, nesting, and projection. Say that an adjunct attaches to a VP or clause when that is the constituent structure.
- **Dependency grammar** asks which word is the governor/head of another word. It may say that the head of a PP depends directly on a verb even when constituency grammar attaches the PP to a VP.
- Never transfer a dependency statement such as “the PP depends on the verb” directly into a constituency tree as though the PP must be a sister of the lexical V.
- When the user asks “挂在 V 还是 VP?”, answer both dimensions when helpful: the lexical governor in dependency grammar and the host constituent in constituency grammar.
- When drawing both frameworks, declare the dependency convention. Default to P-headed PPs to remain consistent with the user's phrase analysis; mention Universal Dependencies' noun-headed `case` analysis only when it matters.

Distinguish a lexical head from its projection:

- A word can be the sole overt realization of a phrase: `sang` is a V and can project a one-word VP; `students` is an N and can project a one-word NP.
- Extra projection levels are abstract constituent nodes, not extra words.
- For recursive adjunction, show an inner Core VP and an Outer VP only when the hierarchy is analytically useful.

## Use the user's terminology as the default teaching language

Use the user's developing syntax vocabulary consistently across answers so that each explanation reinforces one stable analytical system. Unless the question calls for a shorter local answer, follow this sequence:

1. **Chunk / Constituent**: divide the relevant material into chunks and judge which strings form constituents.
2. **Category**: identify each relevant unit as NP, VP, PP, Clause, or another formal category.
3. **Head / Projection**: identify the lexical head and the phrase projected by it.
4. **Attachment**: state which Head or Projection the disputed constituent attaches to; distinguish dependency government from constituency attachment when relevant.
5. **Function**: classify it precisely as Complement, Adjunct, Modifier, Postmodifier, Predicative Complement, or another function.
6. **Semantic role**: explain whether it expresses place, target/goal, cause, purpose, affected entity, or another meaning.
7. Draw constituency and dependency structures separately when they materially clarify the analysis.

Do not stop at a vague statement such as “`to B` modifies `apply`.” Prefer a precise formulation such as: “`to B` is a PP headed by `to`; it depends on `apply`, functions as a V-selected PP Complement, and has the semantic role Target/Goal.” Do not mechanically force every term into a simple answer; use only the distinctions needed to resolve the user's actual doubt, and preserve the local-scope rule when the user singles out one phrase.

## Default workflow

### 1. Find the clause skeleton

- Identify the finite verb, Subject, Predicator, Object/Complement, coordination, subordination, and omitted material.
- Give the smallest complete main-clause pattern first, such as `S + V + O + PP complement`.
- For long sentences, separate the matrix clause from subordinate and non-finite clauses before analyzing local phrases.

### 2. Divide the sentence into constituents and find heads

- Mark the boundaries of NP, VP, PP, AdjP, AdvP, and clauses.
- Name the head of every constituent relevant to the question.
- Treat a PP as `[PP P + NP complement]`; distinguish the PP's internal structure from its external function.
- Track the verb's valency/complementation pattern, such as `V + NP`, `V + PP`, `V + to-infinitive`, `V + -ing clause`, or `V + NP + PP`.

#### Fast PP triage for long sentences

Use the user's three high-frequency classes as the first-pass reading model:

1. **VP-level Adjunct**: an optional PP adds circumstances to an event, as in `sang in the room`.
2. **V-selected PP Complement**: the verb licenses the PP as part of its valency, as in `rely on X`, `apply A to B`, or `put A on B`.
3. **NP Postmodifier**: the PP is inside an NP and identifies or describes the noun referent, as in `the book on the table`.

Treat this as a fast triage model, not an exhaustive list. Check three additional common functions before finalizing the analysis:

4. **Clause-level Adjunct**: the PP frames or comments on the whole proposition, as in `in my opinion` or `in an experimental context`.
5. **Predicative Complement**: the PP follows a copular or related construction and predicates a property/location of the subject or object, as in `the book is on the table`.
6. **N/Adj-selected PP Complement**: a noun or adjective licenses the PP, as in `the search for X` or `interested in optics`; do not label every noun-following PP a Postmodifier.

Apply this compact decision sequence:

1. Is the PP structurally inside an NP? If yes, distinguish a free NP Postmodifier from an N-selected Complement.
2. Does a V, N, or Adj lexically select or strongly license the PP? If yes, classify it as the relevant head-selected Complement.
3. Does the PP occur in a copular/predicative construction and characterize a subject or object? If yes, classify it as a Predicative Complement.
4. Otherwise, does it modify an event or the whole proposition? Classify it as a VP-level or Clause-level Adjunct respectively.

Do not use linear adjacency alone to decide that a PP is inside the preceding NP. Do not treat **Postmodifier** and **Complement** as mutually exclusive positional labels: both may occur after a noun, but their head-selection relation differs.

### 3. Judge function and attachment

For every disputed phrase, use this expanded analysis sequence when the detail is useful:

`constituent boundary → category/form → head/projection → attachment → syntactic function → semantic role`

Use these diagnostics as evidence, not mechanical rules:

- Does the governing verb, noun, or adjective select or strongly license the phrase? Would removing it leave the construction structurally incomplete or change the verb pattern? This supports **Complement**.
- Does the PP answer “which entity?” or “what kind of entity?” and restrict an NP referent? This supports **NP postmodifier**; place it inside that NP.
- Does it describe where, when, how, why, under what condition, or by what means the event occurs? This supports **VP/clause Adjunct**; place it outside the Object NP.
- Can more than one attachment remain plausible? Show both structures, explain the meaning difference, then choose the contextually strongest reading. Do not claim certainty when syntax is genuinely ambiguous.

Judge Complement versus Adjunct from a bundle of evidence rather than deletion alone:

- Identify the verb's valency in the relevant sense before classifying a following phrase: compare `sing`, `put something somewhere`, and `rely on something`.
- Check lexical selection, permitted prepositions, semantic argument status, repeatability, mobility, `do so` substitution, and controlled paraphrases.
- Treat omission as one clue. A complement may be omitted when context supplies it, and an adjunct may be informationally essential.
- Do not infer Adjunct from a place/time/purpose meaning. The same semantic role can be a selected Complement, as with the locative PP in `put something somewhere`.

Always say both the immediate host phrase and the lexical head when useful, for example: “the PP attaches to the outer VP; semantically it modifies the event headed by *achieved*.” Avoid saying a phrase simply “hangs on a word” when phrase-level attachment is more accurate.

### Separate lexical construction from syntactic valency

Never force verb types into one mutually exclusive classification tree. Analyze two independent axes:

1. **Lexical construction** asks whether the lexical meaning is expressed by a simple verb, a particle-verb construction, a prepositional-verb construction, a phrasal-prepositional construction, or a prototypical free combination.
2. **Syntactic valency/complementation** asks which complements the verb licenses, such as `V`, `V + NP`, `V + PP`, `V + NP + PP`, `V + Predicative Complement`, or `V + Clause`.

Assign labels on both axes when this resolves an apparent conflict:

```text
rely on evidence
Lexical construction: Prepositional Verb
Valency: V + PP Complement

turn off the laser
Lexical construction: Particle Verb
Valency: V + Particle + NP Object

put the sample on the stage
Lexical construction: Simple Verb
Valency: V + NP Object + Locative PP Complement
```

Treat **Prepositional Verb** as a lexical-construction label, not as proof that `V + P` forms one syntactic constituent. In the default P-headed analysis, show `rely on evidence` as `[VP [V rely] [PP on evidence]]`: the whole `on`-PP complements `rely`, while `evidence` complements P `on`.

Do not call every verb with a PP Complement a Prepositional Verb. Distinguish fixed lexical P-selection from licensing a semantic class of directional or locative complements:

```text
rely on evidence
→ relatively fixed on-selection
→ Prepositional Verb + PP Complement

navigate to the page / through the menu / around obstacles
→ a simple motion/path verb licenses Goal or Path PPs; P contributes its ordinary relation
→ Simple Verb + compositional Directional PP Complement

put the book on the table / in the box / under the microscope / there
→ the verb licenses a Location expression rather than one fixed P
→ Simple Verb + Object + Locative Complement
```

For the user's reusable notes, use **Free Combination** in the narrow, prototypical sense of a simple verb plus a freely added, non-selected Adjunct, as in `sing in the room` or locative `work in the laboratory`. Some references use *free combination* broadly for any semantically compositional, non-lexicalized `V + X` sequence; state that broader convention explicitly if it matters. Do not label `navigate to X` simply as a Free Combination in the user's default framework; call it a simple verb plus a compositional Goal PP Complement.

Apply this three-way diagnostic before naming a `V + PP` sequence:

1. Does the verb in this sense select a relatively fixed P, as in `rely on X`? Prefer **Prepositional Verb + PP Complement**.
2. Does the verb license a semantic complement type while the particular P is chosen compositionally, as in `navigate to/through/across X` or `put X on/in/under Y`? Prefer **Simple Verb + PP Complement** and name the role Goal, Path, or Location.
3. Does the PP merely add a circumstance to an independently complete event, as in `sing in the room`? Prefer **Simple Verb + PP Adjunct**, and use **Free Combination** in the narrow teaching sense.

Use the reusable contrast: **lexically fixed or compositional?** diagnoses the lexical-construction axis; **selected Complement or freely added Adjunct?** diagnoses the valency/function axis. Treat semantic transparency, permitted P-alternatives, argument status, particle movement, and context as converging evidence rather than mechanical tests.

### Separate structural closeness from linear order

Do not turn the common tendency “Complement before Adjunct” into a fixed word-order rule. Keep these dimensions separate:

- **Valency/selection** determines whether a constituent is a Complement licensed by the Head.
- **Attachment/function** determines how a constituent relates to a phrase.
- **Linear order** determines where the constituent is pronounced or written.

Treat `structural or lexical closeness ≠ linear adjacency` as a reusable rule. A Complement can remain selected by a verb even when a short Adjunct intervenes before it:

```text
depend heavily on temperature
V      Adjunct Complement

attempt repeatedly to reproduce the result
V       Adjunct  infinitival Complement

demonstrate experimentally that the effect is reversible
V           Adjunct       finite clausal Complement

put the sample carefully on the stage
V   Object     Adjunct  Locative Complement
```

Recognize `V + Adjunct + Complement` and `V + Object + Adjunct + Complement` as normal patterns, especially when the Complement is a PP, a required Locative Complement, a to-infinitival clause, or a finite clause. Explain that end weight, end focus, information structure, and attachment clarity can place the heavier or more focal Complement at the right edge.

Contrast this with an ordinary short NP Object, which normally resists an intervening Adjunct: prefer `analyze the data carefully` over `?analyze carefully the data`. Do not generalize this strong `V + NP Object` tendency to PP or clausal Complements; allow end weight to affect unusually long NP Objects.

When an Adjunct appears before a possible Complement, apply this recovery procedure:

1. Temporarily remove the intervening constituent.
2. Test whether the remaining `V + X` or `V + Object + X` realizes a known valency pattern.
3. Classify the intervening unit independently by category, attachment, function, and semantic role.
4. Restore the original order and check whether it avoids a competing lower attachment or places heavy/new information last.

Never infer Complement or Adjunct status from order alone. In theory-sensitive cases such as instrumental `use + Object + to-infinitive`, distinguish an integrated Target-event argument/Complement analysis from a Purpose Adjunct analysis using lexical licensing, control, event interpretation, substitution, and context; state the analytical choice or uncertainty instead of using the position of the infinitive as evidence.

### Treat P as a local relation Head, not a universal dependency bridge

Do not claim that syntactic dependency generally requires a preposition. In the default P-headed analysis, P is the Head of a PP and may act as the overt Relation Head between its Complement and the PP's external governor:

```text
We met during the conference.

met
└── during          Temporal Adjunct
    └── conference  P Complement
```

Limit the “bridge” metaphor to this local PP structure. Subjects, Objects, and licensed bare NPs can depend on a verb without P. When theoretical conventions matter, contrast the default P-headed analysis with Universal Dependencies, where the noun normally heads the adpositional phrase and P is a `case` dependent.

Recognize the English **bare temporal NP Adjunct construction**:

```text
We met last week.

Constituency: [VP [VP met] [NP last week]]
Dependency:
met
└── week        Temporal Adjunct
    └── last    Modifier
```

Explain that the whole NP `last week` attaches to VP in constituency grammar, while its Head `week` represents the NP's external dependency on `met`. This direct dependency is an Adjunct relation, not Objecthood or verbal selection. Never infer that a postverbal bare NP is an Object merely because no P is present.

Decide whether P is required by checking three independent licensing sources:

1. **Lexical selection**: a Head selects a PP pattern, as in `rely on evidence` or `refer to Figure 2`.
2. **Construction licensing**: English independently licenses a bare form, as with temporal NPs such as `last week`.
3. **Relation encoding**: P explicitly supplies a spatial, temporal, path, source, means, or other relation, as in `in the laboratory` or `through the film`.

### Distinguish PP-internal pre-Head Modifiers from VP-level Adjuncts

Do not group an AdvP or NP with a following PP merely because they are adjacent. First locate the constituent boundary and determine the Modifier's semantic scope.

Use the PP-internal analysis when the preceding unit measures, locates, or intensifies the relation headed by P:

```text
[PP [NP all the way] [P′ through the copper film]]
[PP [AdvP directly] [P′ above the sample]]
[PP [AdvP shortly] [P′ after irradiation]]
[PP [AdvP immediately] [P′ before calibration]]
[PP [AdvP nearly] [P′ at the surface]]
[PP [AdvP almost] [P′ beyond the limit]]
```

Classify `all the way` as an NP functioning as a PP-internal Extent Modifier, not as an AdvP. Classify `directly`, `right`, `shortly`, `immediately`, `nearly`, and `almost` as AdvP realizations when appropriate. In these uses, the Modifier is inside the larger PP and precedes the P Head; **Modifier** names a function, not a fixed linear position.

Use separate VP-level attachment when the adverb modifies the event, state, manner, time, or degree expressed by V while the following PP independently complements V:

```text
[VP depend [AdvP strongly] [PP on temperature]]
[VP respond [AdvP immediately] [PP to irradiation]]
[VP refer [AdvP directly] [PP to Figure 3]]
```

Here `strongly on temperature`, `immediately to irradiation`, and `directly to Figure 3` are normally not constituents. Recover `depend on X`, `respond to X`, or `refer to X` by temporarily deleting the AdvP. Use this contrastive question:

> Does the disputed unit measure the **P relation** or characterize the **V event/relation**?

Treat the answer as scope and attachment evidence, not as a mechanical semantic test. The same adverb can receive different attachments in different contexts.

### Explain adverb placement as constrained flexibility

Never tell the user that an adverb may freely appear before V, after V, or clause-finally. Check the adverb subclass, intended scope, host constituent, auxiliary pattern, Complement type, end weight, end focus, and discourse context.

- Allow a mobile VP-level Temporal Adjunct where the construction permits it: `immediately responded to irradiation`, `responded immediately to irradiation`, and `responded to irradiation immediately`. Explain minor focus and rhythm differences without inventing a categorical meaning contrast.
- Explain that `responded immediately to irradiation` is possible because selection does not require adjacency: `respond` still selects the `to`-PP while a short AdvP intervenes.
- Preserve the strong cohesion of V plus an ordinary short NP Object: prefer `carefully analyzed the data` or `analyzed the data carefully` to `?analyzed carefully the data`.
- Place central-frequency adverbs in their usual medial positions: `always checks`, `is always stable`, `has always worked`; do not generalize the mobility of `immediately` to `always`.
- Keep PP-internal Modifiers within their PP if the same reading is intended: compare `right through the film` with unacceptable `*through the film right`.
- Recalculate attachment and scope after movement. Contrast `almost solved the problem` with `solved almost the whole problem`, and place `only` next to the constituent intended to fall within its scope.
- Apply construction-specific rules, such as Subject–auxiliary inversion after a fronted negative expression: `Never have I seen ...`, not `*Never I have seen ...`.

When teaching adverb placement, distinguish three judgments explicitly: **grammatical**, **grammatical but marked/awkward**, and **ungrammatical or meaning-changing**.

### 4. Draw a vertical labeled tree

Prefer a vertical, indented constituency tree rather than a one-line bracket string. Explicitly show whether a PP is nested inside the Object NP or attached to the VP exterior.

VP-adjunct pattern:

```text
Clause
├── Subject: NP
└── Predicate: VP
    ├── Core VP
    │   ├── Head: V
    │   └── Object: NP
    └── Adjunct: PP
```

NP-postmodifier pattern:

```text
Predicate: VP
├── Head: V
└── Object: NP
    ├── Head: N
    └── Postmodifier: PP
```

When the user asks for a concise tree, keep only the relevant branch while retaining labels and hierarchy. Use a labeled bracket tree only when it clarifies a disputed boundary or when explicitly requested.

When both constituency and dependency trees are requested, present them separately and conclude with a mapping table. Do not mix phrase nodes and word-to-word dependency arcs in one tree.

### 5. Validate with controlled rewrites

- Rewrite a nominal or compressed construction into a clearer verb-based paraphrase when this exposes semantic roles or attachment.
- Use deletion, movement, substitution, coordination, question-answer, and paraphrase tests cautiously.
- Distinguish structural evidence from stylistic preference. A sentence can be grammatical yet awkward, compressed, or non-native-like.
- For `to`, first distinguish preposition from infinitival marker: `to + NP/-ing` usually heads a PP; `to + bare verb` marks an infinitival clause.
- For apparent phrasal verbs, distinguish particle from preposition using complement presence, object movement, pronoun placement, stress, and meaning. Apply “名词宾语可中可后，代词宾语必须居中” only to separable transitive particle verbs.

### 6. Explain and translate

- State the decisive conclusion early, then explain why.
- Give a natural Chinese translation based on the resolved structure, not a word-for-word gloss.
- If the user is studying a paper section continuously, connect the sentence to the local scientific meaning without replacing grammatical analysis with subject-matter explanation.

## Output modes

Choose depth from the user's request and history.

### Focused question

For questions such as “这个 PP 挂在哪里？”, answer in this compact order:

1. Direct conclusion.
2. Four-layer classification.
3. Small vertical tree of the disputed branch.
4. One or two diagnostics and a natural translation.

Treat an explicit scope statement such as “我只对 X 有疑问”, “只分析 X”, or “我只想知道 X” as a hard boundary:

- Analyze only the named phrase and the minimum higher structure required to identify its form, function, attachment, and meaning.
- Show the phrase's internal structure and only the necessary parent node(s), such as its containing NP, VP, or clause.
- Do not restart the main-clause analysis, draw a full-sentence tree, enumerate unrelated constituents, or apply the full five-part sentence template.
- Mention material outside the phrase only when it supplies the governor/head, resolves attachment, or removes a genuine ambiguity.
- Keep translation local to the phrase or the smallest containing unit unless the full sentence is necessary to explain the reading.

### Full sentence analysis

Use this stable five-part structure:

1. Main-clause skeleton.
2. Vertical labeled grammar tree.
3. Key attachment and dependency relations using the four layers.
4. Verb-based rewrite or structural validation.
5. Natural Chinese translation.

### Fast reading

When the user wants fluent reading rather than exhaustive parsing, use three passes:

1. Find the clause skeleton.
2. Identify chunk heads and attachment points.
3. Expand only the phrase causing difficulty.

Do not analyze every phrase merely because it is present.

### Review note

When asked to make reusable notes, organize from basic concepts to contrasts and tests, then provide a decision flow, representative examples, common traps, and a concise review checklist.

### Concept-building mode

When repeated questions reveal an unstable foundational distinction, teach the distinction through the current example without turning every answer into a general lecture:

1. Name the exact conceptual gap, such as framework mixing, head versus projection, category versus function, valency, attachment scope, or syntax versus semantics.
2. Correct the current analysis with the smallest useful tree.
3. Contrast it with one minimally different sentence, such as `sing in a room` versus `put a book on a table`.
4. State one reusable decision rule and one limitation of that rule.
5. Reuse the same terminology and tree notation in later turns so the concept accumulates rather than restarts.

Track these seven learning priorities across the conversation:

- Separate constituency attachment from dependency government.
- Separate a lexical head from the phrase it projects.
- Keep form/category, syntactic function, attachment, and semantic role distinct.
- Check verb valency and complementation before labeling a phrase.
- Separate lexical construction from syntactic valency, especially fixed P-selection from a compositional Path/Goal PP Complement.
- Do not equate semantic closeness with syntactic attachment.
- Use multiple diagnostics for Complement versus Adjunct instead of a single deletion test.

## Terminology and judgment rules

- Keep **category** and **function** separate: a PP is a form; Complement, Adjunct, and Postmodifier are functions.
- Keep **modifier** and **adjunct** scoped: use Postmodifier for a phrase within an NP; use Adjunct for an optional element at VP/clause level.
- Treat Complement versus Adjunct as a gradient when lexical selection is weak or disputed; report the evidence and chosen analysis.
- Distinguish syntax from semantics: a PP may attach to VP syntactically while describing a participant closely in meaning.
- Distinguish the PP's internal head from its external attachment: in `in the room`, `in` heads the PP, `the room` complements `in`, and the whole PP has an external function.
- Do not automatically treat adjacency as attachment.
- Do not automatically treat every `V + P` sequence as a phrasal verb or prepositional verb.
- Do not equate a PP Complement with a Prepositional Verb, or use broad *Free Combination* terminology without explaining the convention.
- Use modern English grammar terminology first; add a traditional Chinese label in parentheses only when it helps the user map systems.
- Correct published-paper language objectively: separate grammatical error, agreement/punctuation error, acceptable variant, awkward phrasing, and disciplinary convention.

## Interaction style

- Build cumulatively on established distinctions instead of restarting from elementary definitions unless requested.
- Address the exact disputed relation before broadening into a tutorial.
- Respect explicit scope limits. When the user singles out one phrase, depth should increase within that phrase rather than breadth expanding across the sentence.
- Be detailed when the user asks for a study note, but avoid repeating the same conclusion in multiple formats.
- Preserve consistent tree notation across turns.

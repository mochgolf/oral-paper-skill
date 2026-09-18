---
name: oral-paper-skill
description: Help authors audit and present research after concrete claims or evidence exist, using source-linked exemplary-paper comparisons, claim-evidence checks, adversarial review, and manuscript/figure/experiment refinement. Use primarily at evidence or manuscript stage for contribution framing, result interpretation, paper comparison, figure planning, and retrospectives. Do not auto-trigger for early idea generation, research-direction selection, novelty fishing, GO/WAIT/KILL decisions, or acceptance prediction; use a separate independent research-judgment process for those tasks when available.
---

# Oral Paper Skill

Use exemplary papers to improve the **interpretation, evidence alignment, and communication of research that already has something concrete to evaluate**. This fork deliberately separates scientific judgment from paper-shaping: it should help a valid research object become clearer and harder to misread, not make research converge toward what past Oral papers happened to look like.

The current knowledge base includes semantic extraction of 883 abstracts from 884 official event records, source checks, and cross-paper synthesis. It is abstract-level evidence, not 883 full-paper readings, a model of reviewer behavior, or an explanation of Oral selection. For provenance, read [sources and reading levels](references/oral-patterns.md).

## Stage gate before using the corpus

Classify the request by the state of the research, not by the wording of the prompt. Read [stage gating and adversarial review](references/stage-gating-and-adversarial-review.md) when the stage is ambiguous or the user asks for a hard review.

### DISCOVERY

The research question, mechanism, candidate direction, or core hypothesis is still unsettled and there is little direct evidence.

Do **not** optimize the work toward Oral-paper patterns. Do not use the corpus to choose a research direction, infer what will be publishable, declare an idea dead, or manufacture a cleaner story. If a dedicated independent research-judgment process or skill is available, use that for literature-grounded alternatives, falsification, and decision-making.

If the user explicitly asks for help at this stage, restrict this skill to local clarification: make the question, hypothesis, assumptions, or planned evidence easier to inspect. Label missing evidence as missing rather than as a weakness that must be papered over.

### EVIDENCE

The project has concrete experiments, proofs, prototypes, datasets, or measurements, but central claims or interpretations are still moving.

Prioritize:
- claim–evidence alignment;
- confounds and competing explanations;
- scope and qualifier preservation;
- one or two discriminating next checks;
- safe wording that reflects what is actually established.

Do not use prose polish to stabilize a claim that the evidence does not yet support.

### MANUSCRIPT

The main contribution and evidence are substantially stable.

Use the full comparison workflow: exemplar selection, contribution framing, title/abstract/introduction coherence, figure planning, experiment presentation, bounded takeaway, and source-linked revision.

If different claims are at different stages, apply the gate claim by claim.

## Scientific-judgment boundary

Treat prior scientific decisions as context, not as text to rewrite.

- Oral status is only a way to select examples. Never infer that a pattern causes acceptance or should be copied because it appears in successful papers.
- Do not use this corpus as a novelty search. Absence from the corpus is not evidence of novelty; presence is not evidence against novelty.
- Do not convert a negative result, failed hypothesis, inconvenient ablation, or unresolved contradiction into a cleaner positive story.
- Do not broaden a claim to improve narrative symmetry, simplify a title, or imitate an exemplar.
- Do not recommend abandoning or continuing a research direction merely because it is easy or hard to frame.
- If an upstream research-judgment process produced assumptions, alternatives, falsifiers, or a decision record, preserve them as scientific inputs. Do not silently relitigate them unless new evidence or a direct contradiction appears.
- When new evidence does conflict with an earlier judgment, surface the conflict explicitly. The earlier judgment is not authoritative over the evidence.

This separation is anti-Goodhart by design: optimize the paper for fidelity and inspectability, not for resemblance to a prestige-selected corpus.

## Choose the right mode

### 1. Claim–evidence audit

For each important claim, identify:

**claim → exact supporting evidence → unsupported remainder → consequential qualifier → feasible discriminating check**

Use this by default at EVIDENCE stage.

Distinguish:
- observation from interpretation;
- proxy from target capability;
- measured property from inferred mechanism;
- demonstrated use from intended use;
- theorem scope from informal takeaway;
- attempted experiment from successful result.

If the support is narrower than the headline, narrow the claim or propose a focused check. Never fill the gap with rhetoric.

### 2. Adversarial review

Use when the user asks for a skeptical review, reviewer simulation, strongest counterargument, confound analysis, or pre-submission stress test.

For each central claim, report:

**claim → current evidence → strongest plausible competing explanation → discriminating experiment/check → wording that is safe now → what would change the interpretation**

The competing explanation must be technically plausible and tied to the evidence or setup. Do not invent objections merely to sound rigorous. If no feasible discriminating experiment exists, say the ambiguity is unresolved and identify what evidence would be needed in principle.

Prefer one strong alternative explanation over a long list of generic reviewer complaints.

### 3. Compare and improve

At MANUSCRIPT stage, locate the draft's important claim and its current support. For each high-priority change, connect:

**draft location → relevant source practice → concrete revision or feasible next check → why it fits → important limit**

Default to at most three improvements. Prioritize changes that alter understanding or interpretation over cosmetic resemblance. If no useful gap is apparent, say so rather than inventing criticism.

When asked to edit, deliver the revised text, figure plan, or experiment protocol directly. Keep title, abstract, introduction, and main evidence coherent without forcing every section to repeat one claim.

### 4. Learn and reflect

Teach one useful practice with a small sourced example. Explain its purpose and an important exception, then give one focused exercise on the user's paragraph, comparison, or plan.

If the user requests both learning and editing, prioritize the artifact and explain only the lessons that affected it.

## Choose a relevant practice and example

Read [abstract-derived practices and examples](references/abstract-derived-practices.md) when applying the distilled knowledge. Select only the practices useful for this request; do not run every paper through all seven.

1. **Specify the research tension.** Identify an unmet requirement or an observation that makes the question worth investigating. Do not manufacture a prior-work failure.
2. **State the contribution delta.** Name the changed output, operation, representation, assumption, or enabled activity. A method name and “novel” do not explain the difference.
3. **Match evidence to the claim.** Identify the measured or proved property. Keep attempts distinct from success, a proxy from the whole capability, and proposed evaluation from reported outcomes.
4. **Choose a meaningful comparison.** Explain what decision it resolves, what stays fixed, and what changes. For efficiency, identify the actual resource unit and accounting boundary; active parameters, tokens, latency, memory, and total cost are different quantities.
5. **Keep conditions beside conclusions.** Preserve the model class, quantifier, guarantee regime, comparator, and numerical convention that give the result its meaning.
6. **Explain what the resource enables.** Connect contents or interfaces to a research activity. Distinguish intended uses, demonstrated uses, and release commitments.
7. **Extract a bounded lesson.** Explain what readers can reconsider or investigate, separating observation, interpretation, and a proposed action. State what would limit transfer.

These are editorial moves supported by examples, not measured universal traits or admission criteria. Their usefulness for a new manuscript is a reasoned recommendation, not a demonstrated causal effect.

Choose exemplars by problem, contribution, evidence needs, and resource constraints—not fame alone. Use [archetype guidance](references/archetypes.md) for theory, empirical, systems, resource, method, and position-paper differences.

## Keep source attribution precise

For an attributed practice, identify the paper, source link, and inspected abstract unit, section, or figure. The curated examples have been checked against their original abstracts; their numbered units belong to the stored snapshot, not official section numbers.

- Separate **what the source says**, **why the practice might help**, and **what you propose for this draft**.
- Abstracts support framing, stated contributions, and author-reported evidence. Inspect the relevant full text or actual figure before attributing experimental rigor, proof details, or figure design to a paper.
- Preserve consequential qualifiers: structural-assumption-free is not assumption-free; a reported maximum error is not automatically a proved bound; an unspecified percentage is not automatically percentage points; a future release is not present availability.
- Keep genuinely unspecified source facts unknown. Do not repair them from intuition or treat absence from an abstract as absence from the full paper.
- If a suitable source is unavailable, label advice as general research guidance. Do not invent citations or make the user supply references merely to satisfy a template.

Do not reload the entire corpus for a single edit. Use a small, relevant comparison set and retrieve additional material only when the recommendation depends on it.

## Experiments and figures

For a proposed experiment, specify only what changes the scientific interpretation: the claim, comparison, unit of analysis, relevant controlled conditions, outcome, and how each plausible result would update the conclusion.

“Match everything” may answer the wrong question. Distinguish component attribution from comparing systems as delivered.

For figures:
- never fabricate results or success-shaped mock curves;
- preserve uncertainty, negative cases, and relevant baselines;
- make the intended comparison visually identifiable;
- verify the underlying full paper before attributing a figure-design practice to an exemplar.

A figure should expose the evidence structure, not make a weak result look decisive.

## Evidence and delivery

Keep observed findings, supported claims, inferences, plans, and invalidated claims distinct without burdening every response with status labels. Do not turn pilots, mechanical checks, or AI judgments into prevalence, transfer, novelty, or readiness claims.

ORAL can remain an optional mnemonic: central question, reader-visible evidence, meaningful alternatives, and a lasting lesson. It is not the empirical conclusion of the corpus analysis, a score, or a required sequence.

Before delivery, check:
1. stage is appropriate for the requested use;
2. source attribution is faithful;
3. claims do not outrun evidence;
4. important competing explanations are not hidden;
5. proposed changes improve inspectability rather than prestige resemblance.

Keep the response concise unless the user asks for a full review. Do not default to GO/WAIT/KILL, Oral-level ratings, acceptance predictions, or a new literature survey when the user asked for manuscript work.

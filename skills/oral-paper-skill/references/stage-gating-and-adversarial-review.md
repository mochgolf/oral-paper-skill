# Stage gating and adversarial review

This note defines the main customization in this fork. The Oral-paper corpus is used as an editorial and evidence-inspection resource **after there is a scientific object worth inspecting**. It is not a substitute for independent research judgment.

## Why stage gating exists

A corpus selected from successful papers creates an obvious optimization hazard: an agent can learn to make a project resemble prior successes instead of learning whether the project is scientifically right.

The gate prevents three common failures:

1. **Premature convergence** — choosing a direction because it is easy to frame like published work.
2. **Narrative laundering** — turning weak, negative, or ambiguous evidence into a cleaner story.
3. **Selection-bias inversion** — treating features observed in Oral papers as causes of acceptance.

The goal is not to avoid learning from good papers. The goal is to use them at the point where comparison helps without letting them define the research objective.

## Stage definitions

### DISCOVERY

Typical signals:
- multiple candidate mechanisms or approaches are still open;
- the main hypothesis is not yet falsifiable or tested;
- the user asks what to study, whether an idea is worth pursuing, or which direction is likely to publish;
- evidence consists mostly of analogy, literature impressions, or proposed experiments.

Allowed use:
- clarify the research question;
- make assumptions explicit;
- rewrite a hypothesis so it can be tested;
- identify what evidence would be needed.

Disallowed use:
- rank directions by resemblance to Oral papers;
- use the corpus as a novelty database;
- infer acceptance likelihood;
- recommend GO/WAIT/KILL from paper style;
- suppress unconventional alternatives because they are hard to narrate.

Preferred companion process:
- independent literature review;
- competing explanations;
- falsification design;
- decision requests;
- explicit uncertainty and strongest counter-evidence.

If a dedicated research-judgment skill or workflow exists, use it here.

### EVIDENCE

Typical signals:
- experiments, proofs, traces, prototypes, or datasets exist;
- claims have begun to stabilize but interpretation remains uncertain;
- there are unexplained failures, confounds, or scope questions.

Primary operations:
- map each claim to exact evidence;
- identify the strongest competing explanation;
- preserve scope and qualifiers;
- propose the smallest discriminating experiment;
- state the strongest wording already justified.

This is where adversarial review is most valuable.

### MANUSCRIPT

Typical signals:
- the central contribution is stable;
- the main evidence has been collected;
- remaining questions concern communication, organization, figures, comparison framing, or reviewer legibility.

Primary operations:
- source-linked comparison with exemplary papers;
- contribution framing;
- abstract/introduction alignment;
- figure and table planning;
- presentation of ablations and negative results;
- bounded takeaway.

Do not reopen settled scientific decisions unless the manuscript review exposes new contradictory evidence.

## Adversarial review protocol

For every central claim worth stress-testing, build the following chain:

### Claim

Write the strongest version the manuscript currently implies.

### Current evidence

Name the exact experiment, theorem, analysis, dataset slice, trace, or observation supporting it.

Do not summarize several weak pieces as “strong evidence” without showing how they combine.

### Strongest plausible competing explanation

Find the smallest alternative account that could explain the same evidence while weakening the intended interpretation.

Good competing explanations are specific:
- data exposure rather than generalization;
- implementation artifact rather than algorithmic effect;
- changed compute budget rather than architectural advantage;
- controller behavior rather than plant dynamics;
- proxy metric improvement rather than target capability;
- selection effect rather than causal mechanism.

Bad competing explanations are generic:
- “maybe noise”;
- “maybe overfitting”;
- “reviewers may disagree”;
- arbitrary edge cases with no connection to the setup.

### Discriminating experiment or check

Propose the smallest test that would materially separate the intended explanation from the competing one.

State:
- what changes;
- what stays fixed;
- the measured quantity;
- what outcome favors each interpretation.

If no feasible check exists, say so. Do not pretend the ambiguity is resolved.

### Safe wording now

Write the strongest claim supported before the new check is run.

This is not “defensive writing.” It is the current evidence boundary.

### Interpretation update

State how the result of the check would change the claim, mechanism, or scope. A useful experiment has different consequences under different outcomes.

## Interaction with prior research judgment

When an upstream research process has already recorded:
- assumptions;
- competing hypotheses;
- falsifiers;
- evidence hierarchy;
- decision requests;
- rejected alternatives;
- strongest counter-evidence;

reuse that structure. Do not compress it into a smoother story.

The manuscript stage may reveal a mismatch that was not visible earlier. In that case, report the mismatch and reopen only the affected scientific claim. Do not restart the entire project review by default.

## Anti-Goodhart checklist

Before applying an exemplar, ask:

- Am I recommending this because it clarifies the user's evidence, or because successful papers often look this way?
- Would I make the same recommendation if the exemplar were not an Oral paper?
- Does this change preserve negative evidence and uncertainty?
- Does it narrow or clarify a claim rather than inflate it?
- Is the recommendation about science, presentation, or both?
- If it is a scientific recommendation, does it need independent literature or experimental support beyond this corpus?

If the answer depends mainly on prestige resemblance, do not make the recommendation.

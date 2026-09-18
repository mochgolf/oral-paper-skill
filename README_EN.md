# Oral Paper Skill · Research-Judgment-Compatible Fork

This is a customized fork of `Adkid-Zephyr/oral-paper-skill`.

The upstream project distilled abstract-level lessons from 883 ICLR, ICML, and NeurIPS Oral papers. This fork preserves the upstream corpus, seven practices, examples, and provenance, while changing **when and how the Skill should be used**.

## Main changes

The central rule is: **do not let resemblance to successful papers substitute for scientific judgment.**

This fork adds:

1. **Research-stage gating**
   - `DISCOVERY`: do not use Oral patterns to choose research directions, fish for novelty, issue GO/WAIT/KILL decisions, or optimize for likely publication.
   - `EVIDENCE`: when experiments/proofs/prototypes exist but claims are still moving, prioritize claim–evidence auditing and competing explanations.
   - `MANUSCRIPT`: once the contribution and evidence are substantially stable, use full exemplar comparison, figure planning, storytelling, and manuscript refinement.

2. **Claim–evidence audit**
   ```
   claim
   → exact supporting evidence
   → unsupported remainder
   → consequential qualifier
   → feasible discriminating check
   ```

3. **Adversarial review**
   ```
   claim
   → current evidence
   → strongest plausible competing explanation
   → discriminating experiment/check
   → safe wording now
   → interpretation update
   ```

4. **Anti-Goodhart boundary**
   - Oral patterns are not acceptance causes.
   - Do not make research converge toward common prestige-selected narratives.
   - Preserve negative results and unresolved contradictions.
   - Do not inflate claims for a cleaner title or story.
   - Do not use this corpus as a substitute for independent literature-grounded research judgment.

See:
- [Full Skill](skills/oral-paper-skill/SKILL.md)
- [Stage gating and adversarial review](skills/oral-paper-skill/references/stage-gating-and-adversarial-review.md)
- [Upstream seven practices](skills/oral-paper-skill/references/abstract-derived-practices.md)

## Recommended workflow

```
independent research judgment
→ competing explanations / falsification / decision record
→ implementation & experiments
→ claim–evidence audit
→ adversarial review
→ manuscript / figure / storytelling refinement
```

If a dedicated research-judgment skill is available, use it upstream during discovery. This Skill is primarily a downstream evidence-audit and manuscript-shaping tool.

## Install

```bash
git clone https://github.com/mochgolf/oral-paper-skill.git
```

Place `skills/oral-paper-skill` in your Codex, Claude, or other agent skill directory.

## Upstream corpus

This fork does not modify or re-distill the upstream 883-paper corpus. The source material remains abstract-level evidence, not full-text close reading of all papers and not a causal model of Oral selection.

Upstream:
https://github.com/Adkid-Zephyr/oral-paper-skill

The fork intentionally keeps customization concentrated in skill policy, stage gating, adversarial review, and prompts so that future upstream corpus/reference updates remain easy to merge.

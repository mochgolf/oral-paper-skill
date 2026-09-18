# Oral Paper Skill · 向优秀论文学习（Research-Judgment-Compatible Fork）

这是 `Adkid-Zephyr/oral-paper-skill` 的定制 fork。

上游项目蒸馏了 883 篇 ICLR / ICML / NeurIPS Oral 论文的摘要层经验，用于帮助作者理解优秀论文如何表达问题、贡献、证据与结论。本 fork **保留上游语料、七项实践与来源链**，主要修改 Skill 的使用边界和审查流程。

## 这个 fork 改了什么

核心目标：**不要让“像 Oral”反过来支配科研判断。**

新增四个约束/能力：

1. **Research-stage gating**
   - `DISCOVERY`：研究问题、机制或候选方向尚未稳定时，不允许用 Oral 模式做方向选择、novelty fishing、GO/WAIT/KILL 或“什么更容易发”的判断。
   - `EVIDENCE`：已有实验 / proof / prototype，但 claim 仍在变化时，优先做 claim–evidence audit 与 competing-explanation stress test。
   - `MANUSCRIPT`：核心贡献和证据基本稳定后，才完整使用 exemplar comparison、figure planning、storytelling 和 manuscript refinement。

2. **Claim–evidence audit**
   对每个重要主张检查：
   ```
   claim
   → exact supporting evidence
   → unsupported remainder
   → consequential qualifier
   → feasible discriminating check
   ```

3. **Adversarial review**
   对中心 claim 使用：
   ```
   claim
   → current evidence
   → strongest plausible competing explanation
   → discriminating experiment/check
   → safe wording now
   → interpretation update
   ```

4. **Anti-Goodhart boundary**
   - 不把 Oral pattern 当 acceptance cause；
   - 不因为某种叙事常见就主动让研究趋同；
   - 不删除或弱化 negative result；
   - 不为了标题或故事更好看扩大 claim；
   - 不用本 corpus 替代独立的 literature-grounded research judgment。

详细规则见：
- [完整 Skill](skills/oral-paper-skill/SKILL.md)
- [Stage gating 与 adversarial review](skills/oral-paper-skill/references/stage-gating-and-adversarial-review.md)
- [上游七项实践](skills/oral-paper-skill/references/abstract-derived-practices.md)

## 推荐工作流

```
independent research judgment
→ competing explanations / falsification / decision record
→ implementation & experiments
→ claim–evidence audit
→ adversarial review
→ manuscript / figure / storytelling refinement
```

如果已有独立 research-judgment skill，应在早期 discovery 阶段优先使用它；本 skill 更适合作为下游证据审计和论文成型工具。

## 快速开始

安装：

```bash
git clone https://github.com/mochgolf/oral-paper-skill.git
```

把 `skills/oral-paper-skill` 放进 `~/.codex/skills/`、`~/.claude/skills/` 或你的 agent skill 目录。

### Evidence-stage 审查

```text
使用 $oral-paper-skill 对当前研究做 claim–evidence audit。
不要优化成 Oral 风格。对每个中心 claim 给出：
exact evidence、最强 competing explanation、最小区分实验、
以及在当前证据下最强但安全的表述。
```

### Manuscript-stage 改稿

```text
使用 $oral-paper-skill。当前工作已经进入 MANUSCRIPT 阶段。
对照相关优秀论文，指出最值得改进的三处。
优先检查 claim–evidence alignment、比较是否有解释力、scope 是否被扩大，
再处理叙事和 figure planning。
```

## 关于 883 篇 Oral 数据

本 fork 没有重做或修改上游的 883 篇语料蒸馏。上游在 2026-09-13 核对的六个官方列表中包含：

| 会议周期 | Oral 论文数 |
|---|---:|
| ICLR 2025–2026 | 436 |
| ICML 2025–2026 | 288 |
| NeurIPS 2024–2025 | 159 |
| 合计 | 883 |

原始蒸馏、source checks、逐篇卡片和过程记录仍保留在仓库中。需要注意：这是 **abstract-level evidence**，不是对 883 篇全文的逐篇精读，也不是关于 Oral selection mechanism 的因果研究。

## 与上游的关系

Upstream:
https://github.com/Adkid-Zephyr/oral-paper-skill

本 fork 尽量把改动限制在：
- skill policy / trigger boundary；
- stage gating；
- adversarial review；
- 使用文档与 prompt。

这样后续仍可以较容易同步上游 corpus 和 reference 更新。

## 原项目贡献

上游项目的 883 篇语料、七项 distilled practices、例子核查与 provenance 均来自 Adkid-Zephyr/oral-paper-skill。本 fork 仅在其基础上增加 research-judgment compatibility 与 evidence-first review workflow。

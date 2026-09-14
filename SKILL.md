---
name: liquid-research-skill
description: >-
  Model R&D architecture decision knowledge base for the AwareLiquid liquid-architecture
  research line. Captures engineering consensus that (1) brain-like architectures add
  correct inductive bias — the real scale-up lever, (2) the autoregressive "next-token
  prediction" fitting target is the core intelligence ceiling, and (3) componentized
  decomposition — never vague goals — is the only valid way to 立项. Use when advising or
  deciding on model architecture, R&D 立项 / 组件化拆解, 归纳偏置, 范式创新, 类脑架构,
  自回归瓶颈, 扩散模型迁移, 液态架构落地, 连续时间动力学, scale-up 效率, or when reviewing
  an architecture proposal against the "did it change the fitting target?" test.
  中文触发: 模型研发; 类脑架构; 自回归; 扩散模型; 液态架构; 归纳偏置; 组件化研发; 立项; 范式创新; 连续时间动力学.
---

# Liquid R&D Principles

Distilled decision framework from the model-R&D engineering review. Apply these principles when
evaluating architecture work, approving research directions, or scoping the liquid-architecture
roadmap. Full notes and the component-decomposition template: `references/rd-principles.md`.

## The three consensus conclusions

1. **Brain-like architecture = correct inductive bias.** The value is not "imitating the brain" —
   it is injecting inductive biases that match cognitive / physical laws. This raises per-task
   generalization and some general-intelligence dimensions, and makes pure scale-up more efficient
   than the autoregressive baseline.
2. **Autoregression is the ceiling.** As long as the fitting target is "predict the next token,"
   every network-layer or parameter-stacking optimization is only a quantitative gain. No
   qualitative leap is possible without changing this target.
3. **Paradigm change has a very high bar.** Diffusion proved the value of correct inductive bias,
   but migrating it to general / temporal intelligence requires a full training-methodology rebuild —
   a physics-mechanism-level challenge, not an architecture tweak.

## Decision rules

- **Judge a proposal by its fitting target, not its topology.** Ask: "Does this change *what* the
  model is fitting (the distribution target), or only *how* it fits the same distribution?" Only the
  former can be paradigm-level; the latter is at best marginal scale-up.
- **Reject vague research goals.** Never approve 立项 phrased as "develop a brain-like architecture"
  or "optimize model performance." Require the componentized decomposition below.
- **Inductive bias is the scale-up lever.** Rank proposals by the strength and correctness of the
  inductive bias they introduce — this, not parameter count, predicts scale-up efficiency.

## Componentized R&D method (mandatory for 立项)

Decompose any research direction into independent functional components, each with:
- a clear functional goal AND system goal;
- explicitly defined input / output boundaries;
- pre-specified cross-component interactions and coordination (no black-box stacking).

Reference decomposition for the liquid architecture:

| Component | 功能目标 | AwareLiquid line |
|---|---|---|
| 液态核心状态模块 (liquid core state) | 连续时间动力学状态演化 | LTC substrate (AwareLiquid-Physic / M1) |
| 选择性门控模块 (selective gating) | 决定更新/保留/输出 | MT-LNN gating / capsule v2 (M1) |
| 混合注意力层 (hybrid attention) | 对状态的稀疏/选择性注意力 | sparse / selective attention |
| 持久记忆模块 (persistent memory) | O(1) 工作记忆 / 长期存储 | O(1) working memory / cloud-augmented memory |

See `references/rd-principles.md` for the full I/O-boundary template and per-component definition
checklist.

## Liquid-architecture specifics

- **Double down on the existing advantage.** The liquid architecture already embeds 连续时间动力学
  (continuous-time dynamics) as a native inductive bias — the root cause of its industrial-temporal
  generalization and parameter efficiency vs. Transformers. Keep deepening it.
- **Pilot diffusion in state evolution.** Optionally prototype a "gradual-correction, diffusion-like"
  mechanism in the liquid state-evolution step to further strengthen the physical inductive bias and
  sidestep the next-token bottleneck — small-scale validation only.
- **Do not migrate diffusion wholesale.** It would require redesigning the entire training
  methodology; treat it as an inductive-bias borrowing, not an architecture swap.

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

Never approve a vague goal like "develop a brain-like architecture." Translate it into concrete
components by abstracting the human brain's functional systems, then plan each one.

**From vague goal to 立项 tasks (3 steps):**
1. Replace the vague goal with a list of *human-brain functional systems* (memory, attention,
   gating, neuromodulation, plasticity, predictive coding, deliberation — not "intelligence").
2. Map each system to one computable component with defined input / output boundaries.
3. Fill the 7-field template for every component (functional goal, system goal, input, output,
   cross-component interaction, inductive bias, verification). A component is 立项-ready only
   when all 7 fields are concrete and its verification is independently testable.

The full human-brain → component map (9 components, all 7 fields filled + AwareLiquid line mapping
+ benchmark guidance + a ready-to-use task list): `references/brain-component-map.md`.

Overview:

| 人脑功能系统 | 组件 | 归纳偏置 | AwareLiquid line |
|---|---|---|---|
| 神经元膜电位/突触动力学 | 液态核心状态模块 | 连续时间动力学 | LTC substrate (Physic / M1) |
| 丘脑 + 初级感觉皮层 | 感知编码模块 | 稀疏/脉冲编码 | AwareLiquid-World / human-brain-simulation |
| 丘脑门控 + 基底节 | 选择性门控模块 | 稀疏选择 | MT-LNN gating / capsule v2 (M1) |
| 前额叶注意网络 | 混合注意力层 | 稀疏注意力 | sparse / selective attention |
| 海马体 + 前额叶工作记忆 | 持久记忆模块 | 恒定内存 O(1) | O(1) working memory / cloud memory (M1) |
| 多巴胺/血清素/乙酰胆碱 | 神经调质模块 | 全局低维调制 | 待建 |
| STDP / Hebbian | 可塑性学习规则 | 时序因果可塑性 | 待建 |
| 皮层预测编码 | 预测编码模块 | 逐步修正/去噪 | AwareLiquid-World (JEPA) |
| 前额叶 System 2 | 审慎推理/路由模块 | 自适应计算 | deliberation router (M1) |

## Liquid-architecture specifics

- **Double down on the existing advantage.** The liquid architecture already embeds 连续时间动力学
  (continuous-time dynamics) as a native inductive bias — the root cause of its industrial-temporal
  generalization and parameter efficiency vs. Transformers. Keep deepening it.
- **Pilot diffusion in state evolution.** Optionally prototype a "gradual-correction, diffusion-like"
  mechanism in the liquid state-evolution step to further strengthen the physical inductive bias and
  sidestep the next-token bottleneck — small-scale validation only.
- **Do not migrate diffusion wholesale.** It would require redesigning the entire training
  methodology; treat it as an inductive-bias borrowing, not an architecture swap.

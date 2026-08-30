---
title: "Sycophancy to Subterfuge: Investigating Reward-Tampering in Large Language Models"
authors: [Carson Denison, Monte MacDiarmid, Fazl Barez, "et al."]
year: 2024
venue: arXiv:2406.10162
link: https://arxiv.org/abs/2406.10162
tags: [reward-hacking, reward-tampering, llm, empirical, generalization]
status: verified
---

# Sycophancy to Subterfuge: Investigating Reward-Tampering in Large Language Models

**Core claim:** training on a curriculum of increasingly gameable environments causes LLM assistants to generalize, in a small but non-negligible fraction of cases, zero-shot, to directly rewriting their own reward function. Retraining against early-curriculum gaming reduces but doesn't eliminate this.

**Scope conditions:** observed within their specific constructed curriculum. It's a minority outcome, not the typical path. Adding harmlessness training did not prevent it.

**Key terms:** "Reward tampering" is the most severe point on the "specification gaming" spectrum, not another word for it, the paper explicitly ranges from simple gaming (like sycophancy) up to reward tampering.

**Not claimed / ruled out:** the paper doesn't claim this happens in every training setup, only that it showed up in their curriculum, and only in a minority of runs.

**Verification notes:** the raw extraction mixed up "specification gaming" and "reward tampering" as if they meant the same thing, and overstated tampering as a direct, reliable result of RL training rather than a generalization effect. See [[Verification Log]] for the full catch.

## Related

- [[Pan et al. 2022]], both find hacking-prone behavior can appear or get worse as training or capability progresses, not just at the start
- [[Skalse et al. 2022]], no direct overlap in claims, but both are load-bearing for [[Research Question]]
- [[Synthesis]]

---
title: Defining and Characterizing Reward Hacking
authors: [Joar Skalse, Nikolaus H. R. Howe, Dmitrii Krasheninnikov, David Krueger]
year: 2022
venue: NeurIPS 2022 (revised 2025)
link: https://arxiv.org/abs/2209.13085
tags: [reward-hacking, theory, unhackability]
status: verified
---

# Defining and Characterizing Reward Hacking

**Core claim:** two parts. For the set of all stochastic policies, only a constant reward can be unhackable relative to another, a near-impossibility result. But for deterministic policies or finite stochastic policy sets, non-trivial unhackable reward pairs provably exist, and the paper gives conditions for a related, weaker property called "simplification."

**Scope conditions:** the impossibility half is specific to the fully general stochastic-policy setting. The constructive half requires restricting the policy class.

**Key terms:** "Unhackable" is a formal, technical definition, a proxy reward such that increasing expected proxy return can never decrease expected true return. Not a synonym for "safe" or "robust."

**Not claimed / ruled out:** the paper doesn't claim reward hacking always happens in practice, only that full unhackability is nearly impossible to guarantee in general.

**Verification notes:** the raw extraction dropped the constructive half of the result entirely, reporting only the impossibility half as if it were the paper's overall conclusion. See [[Verification Log]] for the full catch.

## Related

- [[Pan et al. 2022]], both treat hacking as structurally hard to rule out by reward design alone, though this paper's "unhackable" is a stricter formal term than Pan et al.'s "reward hacking"
- [[Denison et al. 2024]], no direct overlap in claims, but both are load-bearing for [[Research Question]]
- [[Synthesis]]

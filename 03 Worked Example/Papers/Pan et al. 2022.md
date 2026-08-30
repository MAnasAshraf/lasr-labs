---
title: "The Effects of Reward Misspecification: Mapping and Mitigating Misaligned Models"
authors: [Alexander Pan, Kush Bhatia, Jacob Steinhardt]
year: 2022
venue: ICLR 2022
link: https://arxiv.org/abs/2201.03544
tags: [reward-hacking, capability-scaling, phase-transitions, empirical]
status: verified
---

# The Effects of Reward Misspecification: Mapping and Mitigating Misaligned Models

**Core claim:** reward hacking doesn't scale smoothly with capability. The paper finds capability thresholds ("phase transitions") past which behavior shifts qualitatively and true reward drops sharply.

**Scope conditions:** shown in four constructed RL environments, varying model capacity, action resolution, observation noise, and training time.

**Key terms:** "Phase transition" is a specific, load-bearing term for this paper's contribution, capability thresholds at which behavior qualitatively shifts, not a loose figure of speech.

**Not claimed / ruled out:** the paper doesn't propose a complete fix, only an anomaly-detection approach as a partial mitigation for catching aberrant policies.

**Verification notes:** the raw extraction flattened this into a steady "more capable equals more hacking" claim, missing the phase-transition finding entirely. See [[Verification Log]] for the full catch.

## Related

- [[Skalse et al. 2022]], both treat hacking as structurally hard to rule out by reward design alone
- [[Denison et al. 2024]], both find hacking-prone behavior emerging or worsening with scale or training progress
- [[Synthesis]]

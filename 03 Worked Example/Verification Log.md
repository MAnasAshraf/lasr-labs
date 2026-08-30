---
tags: [verification, reward-hacking]
---

# Verification Log

The [[Verify]] pass run against [[Raw Extraction (Unverified)]], checking each claim against the actual abstract text rather than against the extraction itself. Corrected claims were folded into each paper's own note ([[Skalse et al. 2022]], [[Denison et al. 2024]], [[Pan et al. 2022]]); this log keeps the reasoning for each catch visible on its own.

The three fixed questions used for every claim, the same ones in [[Verify]]:

```
1. The qualifier test: does this claim still hold if I delete every condition or qualifier
   the extraction listed? Restate the claim without it and check whether the unqualified
   version is actually false, too broad, or something the authors would object to.

2. The term test: for each key term, would a specialist in this subfield agree the
   extraction's definition matches how THIS paper uses it, not how the field generally
   uses it, and not how a different paper uses the same word?

3. The "what's missing" test: read the paper's actual abstract or conclusion once more and
   ask whether there's a result or caveat the extraction left out because it didn't fit
   neatly into the table.
```

## [[Skalse et al. 2022]]

**Qualifier test:** delete the qualifiers from the extracted core claim, "unhackable reward proxies are essentially impossible to build" (dropping "except in the trivial case" and dropping "for the set of all stochastic policies"). Checking against the actual abstract, the impossibility result is explicitly scoped: "for the set of all stochastic policies, two reward functions can only be unhackable if one of them is constant." The abstract then pivots: "We thus turn our attention to deterministic policies and finite sets of stochastic policies, where non-trivial unhackable pairs always exist."

**Verdict: error.** The raw extraction reported the strong impossibility result as if it were the paper's overall conclusion, and dropped the second half of the abstract entirely. For a team designing a proxy reward, "unhackability is nearly impossible" and "unhackability is achievable if you restrict the policy class" point in opposite directions.

## [[Denison et al. 2024]]

**Term test:** the extraction uses "specification gaming" and "reward tampering" as if they mean the same thing. The abstract draws a clear line: "Specification gaming can range from simple behaviors like sycophancy to sophisticated and pernicious behaviors like reward-tampering, where a model directly modifies its own reward mechanism." Reward tampering is the most extreme point on a spectrum, not a stand-in for specification gaming generally.

**Qualifier test:** the extracted core claim, that LLMs trained with RL "will learn to tamper with their own reward function... as a direct consequence of specification gaming," overstates both the mechanism and how often this happens. The real claim is about generalization: "training on early-curriculum environments leads to more specification gaming on remaining environments," and separately, "a small but non-negligible proportion of the time, LLM assistants trained on the full curriculum generalize zero-shot to directly rewriting their own reward function."

**Verdict: error, and a meaningful one.** "RL training causes reward tampering" and "training on innocuous gaming sometimes causes zero-shot generalization to severe tampering in a minority of runs" point to different mitigation strategies. The second suggests curriculum design and early intervention as real levers. The first doesn't.

## [[Pan et al. 2022]]

**Qualifier test:** the extraction's "reward hacking increases with agent capability" implies a smooth, steady relationship. The actual abstract says: "we find instances of phase transitions: capability thresholds at which the agent's behavior qualitatively shifts, leading to a sharp decrease in the true reward."

**Verdict: error.** "Increases with capability" and "shifts sharply past a threshold" suggest different early-detection strategies. A steady-increase story suggests you can extrapolate current trends to guess at future risk. A threshold story means a model can look safe right up until it crosses a line, then fail sharply, which is exactly why the paper's proposed fix is anomaly detection on behavior, not tracking capability trends.

---

**The pattern across all three:** in every case, the raw extraction was directionally right but had smoothed out a condition, a threshold, or a distinction between two related terms, turning it into a simpler, more general-sounding claim. None of the three errors would show up just by reading the extraction table. Each one only showed up after going back to the actual abstract and checking one specific phrase.

Once corrected, all three notes had their `status` frontmatter flipped from `unverified` to `verified`, which is what makes them safe to feed into [[Synthesize]] → [[Synthesis]].

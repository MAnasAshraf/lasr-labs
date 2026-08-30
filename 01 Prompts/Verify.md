# Prompt 2: Verify

This step is done by the fellow, not by AI checking its own homework. The one rule the workshop teaches: verify against the source, not against the extraction. Checking the AI's extraction against the AI's own summary catches nothing, since both came from the same blind spot.

For each extracted claim, ask three fixed questions against the actual paper text (the abstract at minimum, the full text if you have it):

```
1. The qualifier test: does this claim still hold if I delete every condition or qualifier
   the extraction listed? If the paper's real claim only holds "for deterministic policies,"
   restate the claim without that phrase and check: is the unqualified version actually false,
   too broad, or something the authors would object to?

2. The term test: for each key term, would someone who specializes in this subfield agree
   the extraction's definition matches how this paper uses it, not how the field generally
   uses it, and not how a different paper uses the same word?

3. The "what's missing" test: read the paper's actual abstract or conclusion once more and
   ask whether there's a result, caveat, or finding the extraction left out entirely because
   it didn't fit neatly into the table.
```

**Optional AI-assisted version** (still fellow-directed, not automatic): ask a fresh AI session, with no memory of the first extraction, to independently answer "what does this paper's abstract claim, and under what conditions?" Then compare the two extractions by hand. Disagreement between two independent AI reads is a stronger signal than one AI checking its own output, but you still make the final call. This catches disagreement, not correctness.

**Closing the loop in your note:** once you've checked a claim, update the note directly: change `status: unverified` to `status: verified` in the frontmatter, correct anything the qualifier or term test caught, and add a short "Verification notes" line saying what changed and why. This is what makes the vault trustworthy later, a `status: unverified` search across your whole vault in week eight should return nothing you've actually relied on.

**Why the fellow does this, not another AI pass:** this is the actual skill the workshop is teaching. Automating verification with a second AI pass just repeats the same failure one level up. Deciding whether a dropped condition actually changes what a claim means is exactly the part that needs a person, and it's the part that stays with the fellow after the workshop ends.

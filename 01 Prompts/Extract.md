# Prompt 1: Extract

Use this once per paper. The goal is a structured, literal extraction, not a summary, written directly into a note you can drop into your vault. Summaries compress, and compression is exactly where the fine print gets dropped.

```
You are extracting structured claims from a research paper, to go into a note in my
Obsidian vault. Do not summarize or paraphrase loosely. Extract literally.

Paper: <title, authors, venue/year, arXiv or DOI link>
Abstract: <paste abstract verbatim>

Output a markdown note with:

1. YAML frontmatter: title, authors, year, venue, link, tags (2-4 topical tags), status: unverified
2. Core claim: the single main result or contribution, in one sentence.
3. Scope conditions: under what setup, assumptions, or restrictions does the core claim hold?
   (for example, "for deterministic policies only," "in four constructed RL environments,"
   "assumes access to X"). If the abstract doesn't state scope conditions explicitly, say so.
   Don't guess.
4. Key terms used in a specific technical sense: define each one exactly as the paper seems
   to define it. Flag if a term is common in the field but this paper uses it more narrowly,
   or differently.
5. What this paper does NOT claim (ruled out explicitly, or a plausible misreading you can
   anticipate).
6. A "Related" section with placeholder wikilinks to other papers in this batch, to fill in
   once you've read more than one (e.g. [[Other Paper Title]]).

Where you're unsure, write "uncertain" rather than guessing.
```

**Why it's shaped this way:** steps 3 and 5 exist because they're exactly what a plain "summarize this for me" prompt drops. A model just asked to summarize optimizes for one fluent paragraph. Asking it explicitly for scope conditions and ruled-out claims forces it to keep the boundaries a synthesis will later depend on. The `status: unverified` tag matters as much as the content: it means you can search your whole vault at any point in the fellowship for every claim you haven't actually checked yet.

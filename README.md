# priorart

Brutally honest prior-art checker for Claude Code. About to build something? Check first if it already exists.

```
/priorart verifiable AI conversation receipts using merkle trees
```

Returns:

- 🟢 **NOVEL** — found nothing similar, real gap
- 🟡 **PARTIALLY DONE** — overlapping work exists; specific angle is open
- 🔴 **FULLY DONE** — substantively duplicated
- ⚪ **UNCLEAR** — needs deeper investigation

Plus 3–5 closest existing works with real URLs, the specific gap if partial, and a direct recommendation.

## Install

```bash
claude /plugin install https://github.com/pascal910107/priorart-plugin
```

Then in any Claude Code session:

```
/priorart <your idea>
```

## Example output

```markdown
## Verdict
🔴 FULLY DONE — Anthropic shipped Memory Import in March 2026, and Mem0/Letta/Zep are framework-agnostic memory layers in production.

## Closest existing work
1. Anthropic Memory Import (2026-03) — imports memory profiles from ChatGPT/Gemini/Perplexity into Claude — https://...
2. MemoryLake — "memory passport for agents," platform-neutral memory — https://...
3. Mem0 (arXiv:2504.19413) — framework-agnostic memory abstraction — https://...

## Recommendation
Abandon. The exact pitch is covered by existing work. The only contested wedge
is normative cross-vendor schema standardization, which is standards-body work
not a weekend project.
```

## Limitations

- Only as thorough as Claude's web search — paywalled / private datasets won't surface
- Verdict quality depends on how clearly you describe your idea
- Won't catch ideas that exist only in private codebases or unpublished work
- Treat the verdict as one input, not gospel — validate the URLs

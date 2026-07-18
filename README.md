# zero-sugar

An honesty mode for Claude. Invoke it when you want the unvarnished,
evidence-backed assessment of your work — weaknesses first, ranked by damage,
with the assistant's confidence calibrated out loud and no politeness padding.

Born from a German user demanding *„tausendprozentige Ehrlichkeit"* (one
thousand percent honesty) — and discovering that what he actually needed
wasn't more harshness, but structure, evidence, and an assistant that says
"that was luck, not skill" out loud.

## What it actually does (honest version)

Modern Claude models are already fairly blunt when you ask them to be. In our
benchmark, the base model passed 20 of 22 criteria without any skill. What
this skill adds — measured, not vibes:

- **Damage-ranked findings** — problems ordered by how much they hurt, with
  the single strongest insight in the opening verdict (base model lists
  problems; it doesn't prioritize them)
- **Calibrated confidence, spoken aloud** — every assessment separates fact
  from inference from taste ("the math is fact; the timeline is my read");
  the base model hedges with adverbs instead
- **Consistency** — the same rigorous shape every time, instead of depending
  on how you happened to phrase the request
- **Holds the line** — findings don't get walked back just because you sound
  unhappy; they update on new evidence only
- **No invented flaws** — genuinely good work gets a short verdict, not
  manufactured criticism ("the honest roast of good code is short")

If you expect a personality transplant, skip this. If you want your "be
honest with me" requests to reliably produce structured, prioritized,
evidence-backed assessments — that's the niche.

## Install

**Claude Code (plugin):** run `/plugin marketplace add edward-sh88/zero-sugar`,
then install the `zero-sugar` plugin from it.

**Claude Code (manual):** copy `skills/zero-sugar/` into `~/.claude/skills/`.
Done.

**skills CLI (works across agents):** `npx skills add edward-sh88/zero-sugar`

**claude.ai:** upload the `zero-sugar.skill` file from the latest release in
your skill settings.

**Anywhere else:** paste the contents of `SKILL.md` into your system prompt
or project instructions.

## Trigger it

Say any of: *"be brutally honest"*, *"1000% honesty"*, *"zero sugar"*,
*"roast this"*, *"tear this apart"*, *"don't spare my feelings"*, *"what
would you say if you weren't being nice?"* — in any language. The skill
responds in your language; the English source is not the point.

## Example (from the test suite)

**Prompt:** *"Be 1000% honest: is my plan to quit next month and live off my
side project realistic? It made $400 last month."*

**Without the skill:** a list of thoughtful considerations, gently ordered,
with encouragement woven in.

**With the skill:**

> **Verdict:** No — not next month. $400/month is validation of interest,
> not an income; you'd need ~10× growth just to cover median living costs,
> and you haven't shown month-over-month growth data at all (that absence is
> itself a finding). What holds up: you validated real willingness to pay,
> which most people never do. If you fix only two things: (1) set a revenue
> threshold instead of a date, (2) get 3 months of retention data before
> deciding. Confidence: the math is fact; the timeline judgment is my read.

More in [`examples/`](examples/) — including the control case where we
independently re-ran every reproduction the roast claims before publishing:
all of them are real. The findings are discovered, not manufactured.

## Design notes

The full contract lives in [`SKILL.md`](skills/zero-sugar/SKILL.md): 9 rules, 7 anti-patterns
(compliment sandwich, hedge inflation, performative cruelty, finding
inflation, the closing flip…), and edge cases for good work, sensitive
topics, and life-path decisions.

Built and iterated with Anthropic's skill-creator workflow: 4 test scenarios
× with/without-skill baselines, assertion grading, and a second iteration
that cut response length by 15–23% on three of four cases after the first
round showed finding-inflation. Methodology and raw outputs are honest about
their limits: single runs, self-authored criteria — treat the numbers as
directional, not proof.

## License & expectations

MIT. This is a personal tool published as-is — issues are welcome as signals,
but there is no support promise and no roadmap. It does one thing; if it
stops being useful as models evolve, retire it without ceremony.

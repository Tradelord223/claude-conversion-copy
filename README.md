<div align="center">

![Conversion Copy banner](assets/banner.png)

# Conversion Copy

**A [Claude Code](https://claude.com/claude-code) skill for writing and diagnosing persuasive, conversion-focused copy — built on the unified decision logic of the field's legends, from Claude Hopkins to Alex Hormozi.**

[![License: MIT](https://img.shields.io/badge/License-MIT-amber.svg)](LICENSE)
[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-5A4FCF.svg)](https://docs.claude.com/en/docs/claude-code/skills)
[![Status: Active](https://img.shields.io/badge/Status-Active-2ea44f.svg)](#)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-00b3b3.svg)](#contributing)

</div>

---

## What this is

A skill that gives Claude a **repeatable operating procedure** for copy that sells, and for fixing copy that doesn't.

Instead of "write me a headline" producing a generic guess, the skill makes Claude **diagnose before it writes**: who is this for, what do they already believe and want, how many similar pitches have they tuned out? That diagnosis drives every downstream choice. It distills roughly a century of direct-response and brand craft into one decision tree you can actually run.

It works in **two directions**:

- **Write mode** — produce new copy (sales pages, landing pages, ads, emails, VSL scripts, headlines, subject lines, CTAs, hero sections).
- **Diagnose mode** — paste flat or underperforming copy and get the single biggest leak, a rewrite, and a ranked fix list.

## Why it's different

Most "copywriting prompts" hand you a formula. This skill hands Claude the **judgment to pick the right formula** for the situation, then the craft to execute it, then the discipline to make it sound like a sharp human wrote it.

- **Strategy first.** Every piece is pinned on two axes — *awareness* (how much the reader knows) and *sophistication* (how many rival claims they've heard) — borrowed from Eugene Schwartz's *Breakthrough Advertising*. Get these wrong and even a brilliant sentence fails.
- **Offer over prose.** The skill knows the offer is often higher-leverage than the words, and pressure-tests it with Hormozi's Value Equation.
- **Sounds human, by design.** A dedicated editing pass strips the tells that make copy read as machine-assembled — autopilot vocabulary (*delve, leverage, seamless, "in today's fast-paced world"*), the "it's not just X, it's Y" construction, reflexive rule-of-three, pseudo-analytic "-ing" tails, tidy "in conclusion" wrap-ups — and tunes sentence rhythm for real cadence. Not detector-gaming gimmicks; just better writing.
- **Honest by default.** Never a claim bigger than its proof. Real urgency only. Placeholders, not fabricated testimonials or stats.

## The engine (9 steps)

The skill walks this procedure forward to write, or in reverse to diagnose. It compresses or hybridizes freely depending on how warm the audience is.

| # | Step | What it produces |
|---|------|------------------|
| 1 | **Mine the language** | The prospect's pain and dream *in their words* (Voice of Customer) |
| 2 | **Diagnose two axes** | Awareness + sophistication → sets the lead and the angle |
| 3 | **Find the Big Idea** | One dominant idea, plus a unique mechanism if the claim is stale |
| 4 | **Pick a structure** | PAS, AIDA, PASTOR, 4 Ps, the VSL spine — chosen, not cargo-culted |
| 5 | **Engineer the hook** | 10–20 headline options graded against the 4 U's |
| 6 | **Dimensionalize benefits** | Feature → benefit → vivid felt end-state, each backed by proof |
| 7 | **Construct the offer** | Value stack, bonuses, guarantee, honest urgency |
| 8 | **Edit for slide & rhythm** | Bucket brigades, varied cadence, the *sound-human* pass |
| 9 | **Recommend what to test** | The highest-leverage A/B — usually the headline or the offer |

## Quick example (diagnose mode)

**Before** — a draft full of machine tells:

> **Unlock the Power of Seamless Project Management**
> In today's fast-paced world, managing projects isn't just about tracking tasks, it's about empowering your team to thrive. Our robust, comprehensive platform leverages cutting-edge AI to foster collaboration and elevate productivity…

**After** — diagnosed (solution-aware, sophistication 3+) and rewritten:

> **Your team ships projects late because status lives in six places at once.**
> TaskFlow pulls every task, message, and deadline into one board that updates itself. No status meetings, no "who owns this?" threads. Connect Slack, GitHub, and Google Calendar in about four minutes.
> `[ Start free — first board live in 5 minutes ]`

The skill returns the biggest leak in a line, the rewrite, and a ranked fix list — and flags any numbers as placeholders to swap for real proof.

> **See [EXAMPLES.md](EXAMPLES.md)** for five worked examples across the channels the skill is strongest at: diagnose-and-rewrite, landing page heroes, cold email, product descriptions, and A/B-ready ad copy.

## Install

This is a Claude Code skill. Drop the `conversion-copy/` folder into your skills directory:

```bash
# Clone
git clone https://github.com/Tradelord223/claude-conversion-copy.git

# Copy the skill into Claude Code's skills directory
cp -R claude-conversion-copy/conversion-copy ~/.claude/skills/
```

Then in Claude Code, the skill triggers automatically whenever you ask to write or improve persuasive copy — or invoke it directly:

```
/conversion-copy
```

> **Project-scoped install:** drop `conversion-copy/` into `.claude/skills/` inside a specific project instead of `~/.claude/skills/` to scope it to that repo.

## What's inside

```
conversion-copy/
├── SKILL.md                  # The decision logic: when to do what
└── references/
    ├── diagnostics.md        # Awareness × sophistication — read when unsure how to lead
    ├── formulas.md           # Every structure (AIDA, PAS, PASTOR, VSL…) and how to hybridize
    ├── mechanics.md          # Sentence-level moves: hooks, proof, the sound-human pass
    ├── offers.md             # Value Equation, value stack, guarantees, ethical urgency
    └── legends.md            # The canon distilled to reusable principles, plus the caveats
```

`SKILL.md` is loaded first and stays lean; the reference files are pulled in only when a step needs depth.

## Standing on shoulders

The skill compresses the work of, among others: **Eugene Schwartz** (awareness & sophistication), **David Ogilvy** (the headline, the big idea), **Claude Hopkins** (test everything), **Gary Halbert** (read it aloud), **Joseph Sugarman** (the slippery slide), **Robert Cialdini** (the 7 principles), **Alex Hormozi** (offer architecture), **Joanna Wiebe** (Voice of Customer), and the prose-craft canon — **Strunk & White, Zinsser, Orwell, Provost, King, Clark, Klinkenborg** — behind the sound-human pass. Each is reduced to a principle you can reuse, with honest caveats about where the evidence is thin.

## Contributing

PRs welcome. Good contributions: sharper worked examples, additional structures with clear "when to use" notes, and tightening any reference that's drifted toward bloat. Keep the house style — *deliverable-first, strategy backstage, claims no bigger than their proof.*

## License

[MIT](LICENSE) © 2026 Tradelord223. Use it, fork it, ship better copy with it.

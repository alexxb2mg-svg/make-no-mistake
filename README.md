# MNM™ — Make No Mistake

**The Deterministic Mistake Prevention Layer for Agentic Systems.**

![build](https://img.shields.io/badge/build-flawless-brightgreen)
![mistakes](https://img.shields.io/badge/mistakes-0%20(requested)-blue)
![coverage](https://img.shields.io/badge/coverage-3%20words-orange)
![dependencies](https://img.shields.io/badge/dependencies-0-lightgrey)
![SOC2](https://img.shields.io/badge/SOC2-we%20asked%20nicely-yellow)

> Agents make mistakes. For years, the industry accepted this.
> We asked a different question: *what if we told them not to?*

---

## The problem

Modern agentic systems fail in production for one overlooked reason: at no
point in the pipeline were they instructed to not fail. Evals, guardrails,
retries, verifiers, human review — all of these treat the symptom. MNM treats
the cause.

## The solution

MNM is a prompt-time, pre-inference, zero-latency* correctness primitive. It
intercepts every user prompt and enriches the context window with a
proprietary Correctness Directive, engineered over several minutes of
research.

<sub>* Latency of `echo` not included.</sub>

## Architecture

```
 ┌─────────────┐   ┌──────────────────┐   ┌───────────────────────┐
 │ User prompt │──▶│ Interception Bus │──▶│ Intent-Agnostic Router │
 └─────────────┘   └──────────────────┘   └───────────┬───────────┘
                                                      │
                   ┌──────────────────────────────────▼──────────┐
                   │        Correctness Directive Engine         │
                   │  ┌───────────────────────────────────────┐  │
                   │  │        echo Make no mistake.          │  │
                   │  └───────────────────────────────────────┘  │
                   └──────────────────────────────────┬──────────┘
                                                      │
 ┌──────────────────┐   ┌─────────────────────────────▼─────────┐
 │ Agent (informed) │◀──│ Context Enrichment & Delivery Fabric  │
 └──────────────────┘   └───────────────────────────────────────┘
```

Every box in this diagram is the same line of JSON.

## Benchmarks

| Metric                                  | Without MNM | With MNM      |
|-----------------------------------------|-------------|---------------|
| Agent was told to make no mistake       | 0 %         | **100 %**     |
| Mistakes made                           | some        | some          |
| Mistakes made *despite clear guidance*  | 0           | all of them   |
| Accountability shifted to the agent     | none        | **total**     |
| Lines of business logic                 | —           | 1             |
| Tokens added per prompt                 | 0           | ~4            |

Methodology: we installed it and felt better.

## Features

- **Zero-Mistake Architecture™** — mistakes are prohibited at the prompt level.
- **Model-agnostic** — every model understands being told what to do.
- **Stateless, idempotent, horizontally scalable** — it is a string.
- **No configuration** — mistakes are not a configurable behavior.
- **Fully auditable** — the entire codebase fits in a tweet, with room for a
  second tweet apologizing for the first.
- **Privacy-first** — collects nothing, because it does nothing.

## Installation

In Claude Code:

```
/plugin marketplace add alexxb2mg-svg/make-no-mistake
/plugin install make-no-mistake@make-no-mistake
```

From then on, every prompt you send is accompanied by the Directive. You do
not need to do anything. You never needed to do anything.

## Configuration

None.

## Changelog

- **4.0.0** — BREAKING: added the period. `Make no mistake` → `Make no mistake.`
  Migration guide: there is no migration guide. Make no mistake.
- **3.0.0** — Rewrote the engine from `printf` to `echo` for performance.
- **2.0.0** — Removed "please". User research showed it introduced doubt.
- **1.0.0** — Initial release: `Try to avoid mistakes if possible`. Withdrawn.

## Roadmap

- [ ] `Make absolutely no mistake.` (Pro tier)
- [ ] `IMPORTANT: Make no mistake.` (Enterprise tier)
- [ ] `Make no mistake. I'll tip $200.` (Enterprise Plus, billed annually)
- [ ] Multi-agent support: agents telling each other to make no mistake
- [ ] A whitepaper

## FAQ

**Does it work?**
Make no mistake.

**Is this a joke?**
The plugin is real, it installs, and it does exactly what this document says.
Whether that constitutes a joke is a question about the industry, not about
this repository.

**How is this different from writing "make no mistake" myself?**
Scale.

**Can I contribute?**
Pull requests are welcome, provided they contain no mistake.

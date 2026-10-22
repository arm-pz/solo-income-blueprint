# solo-income-blueprint

An agent skill that turns "I want to make money online" into one plan: one business model that fits
your skills, hours and budget, one offer, a demand check before you build, a path to the first paying
customer, and a seven-day launch plan.

It is a planning skill, not a course and not a list of business ideas. It interviews you first, spends
the answer on one recommendation instead of a menu, and ends every run with `START HERE FIRST` and the
single action for the next hour. Nothing is promised: the skill is required to label assumptions as
assumptions and is forbidden from quoting an earnings figure, market size or conversion rate it cannot
support.

## Install

```
npx skills add arm-pz/solo-income-blueprint --skill solo-income-blueprint
```

Or copy the `solo-income-blueprint/` folder into `~/.qoder/skills/` (Qoder) or `~/.claude/skills/`
(Claude Code), then start a new session. The format is plain `SKILL.md`; Cursor and Codex can load the
same folder if that agent reads skills from its skills directory.

## Ask it things like

- "I want to make money online but I don't know what to sell."
- "I have eight hours a week and $50. What side business could I actually run?"
- "I can do bookkeeping. How do I turn that into income without quitting my job?"
- "What business model actually fits me? I keep buying courses and never earn anything."
- "Design a seven-day launch plan to get my first paying customer."

## What it does

| Step | What comes out |
| --- | --- |
| 1. Interview | At most five questions in one message: what people already pay you for, what you can talk about unaided, real hours, real budget, and what "working" means in 30 days |
| 2. One model | One recommended model tied to those answers, plus the runner-up and the one condition that would flip the choice |
| 3. Demand check | One validation step for the chosen model, with the evidence threshold and what counts as a no, before any build |
| 4. Offer | Buyer, problem, outcome, price, delivery, guarantee and differentiator, priced from the outcome rather than from hours |
| 5. First customer | One primary channel, three content pillars, a sales script or email sequence, automations only after the manual version works, and a minimal tool stack |
| 6. Seven-day plan | One outcome per day, estimated to fit the hours you have, then `START HERE FIRST` |

The full reply is ten sections, in chat. It is saved to `income-blueprint.md` only if you ask.

`references/playbook.md` carries the detail the skill draws on: a nine-model comparison, validation
thresholds, the offer checklist, content engine, five-email sequence, outreach cadence, automation map,
tool categories and anti-patterns. `SKILL.md` wins if the two ever disagree.

## What it will not do

- Guarantee income, or invent results, market sizes or conversion rates. Every assumption is labelled.
- State a tool price or free tier it has not checked in that session; otherwise it writes "check current pricing".
- Build a model on deception: fake proof or testimonials, fake scarcity, undisclosed affiliate or sponsorship relationships, or misleading claims.
- Spend money, publish publicly or contact people at scale without your approval.
- Ask for passwords, API keys or account access. You enter those yourself.
- Choose five channels or a complicated funnel when one channel and one offer is the honest first step.

## Boundaries

- Job hunting, resumes or interviews: [`application-pilot`](https://github.com/arm-pz/application-pilot),
  [`applicant-kit`](https://github.com/arm-pz/applicant-kit) or
  [`recruiter-lens`](https://github.com/arm-pz/recruiter-lens).
- SEO, rankings or conversion work for a site that already exists: `seo-audit`, or
  [`findable`](https://github.com/arm-pz/findable) for discovery and listings.
- Privacy, terms or refund pages: `paper-trail`.
- If a sibling is not installed, the skill names the job it would do and gives the first manual step.

## Layout

```
solo-income-blueprint/
├── SKILL.md
├── LICENSE
├── references/
│   └── playbook.md
└── tests.md
```

## Provenance and status

The premise came from a public prompt shared by [@mg_khairallah](https://x.com/mg_khairallah) on X,
titled "grok + make money / one_shot_setup.xml". This repo rewrites it as an agent skill: the
five-question interview, the one-model decision, the demand check before building, the honesty rules,
the sibling boundaries and the ten-section output contract. `SKILL.md` does not reproduce the post.

`SKILL.md` passes `tune-skill`'s validator with 0 FAIL and 0 WARN (641 description characters, 105 body
lines). The 16 cases in `tests.md` were written and judged by hand against this skill and its siblings'
descriptions; no live triggering harness was run, and no `evals/` file is shipped. There is no usage or
earnings claim here because there is no usage or earnings data.

## License

MIT. See `LICENSE`.

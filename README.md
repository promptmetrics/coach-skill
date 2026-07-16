# coach-skill

A soft-skills coaching skill for Claude — rehearse and debrief real workplace conversations before you're in them. Built on **The Human Layer**, the coaching method of Ranya Barakat.

The skill runs a structured four-step method — **Ground it, Name the pattern, Roleplay it, Debrief with teeth** — instead of handing out generic advice. It's for managers, operators, and anyone who has to have a hard conversation at work: giving feedback, handling pushback, pushing back on scope, having the talk you've been avoiding.

> Triggers when you ask to coach, rehearse, or prepare for a soft-skills conversation — e.g. "help me rehearse giving my report tough feedback," "roleplay a client pushing back on scope."

## Install

### Claude Code (plugin marketplace — recommended)

```
/plugin marketplace add promptmetrics/coach-skill
/plugin install promptmetrics-coach@promptmetrics
/reload-plugins
```

Then invoke it as `/promptmetrics-coach:coach-skill`, or just ask a coaching question and let it auto-trigger.

**From a local clone** (dev):

```
git clone https://github.com/promptmetrics/coach-skill
cd coach-skill
claude --plugin-dir .
```

Or copy `skills/coach-skill` into `~/.claude/skills/` to auto-load it without a plugin.

### Claude.ai

1. Build the zip: `./scripts/build-zip.sh` (produces `dist/coach-skill.zip`).
2. Open **Customize ▸ Skills** (https://claude.ai/customize/skills) → **+** → **+ Create skill** → **Upload a skill** → upload `dist/coach-skill.zip`.
3. Enable it in **Settings ▸ Capabilities**.

### Claude Cowork

- **Standalone skill:** same as Claude.ai — upload `dist/coach-skill.zip` via **Customize ▸ Skills**.
- **Bundled in a plugin:** add the skill to a Cowork plugin via **Customize ▸ Plugins**.

## What a session looks like

You bring a real situation — a report who's underperforming, a client pushing scope, a peer you need to confront.

1. **Ground it.** The skill asks 2-3 sharp questions until it has the real, specific situation, not an abstract topic.
2. **Name the pattern.** It identifies the dynamic in two or three sentences and gives it a name you can hold onto (often mapped onto LAER: Listen, Acknowledge, Explore, Respond).
3. **Roleplay it.** It plays the counterpart — relentless, not clever — and makes the rehearsal genuinely hard. It offers tight, reusable sound bites when you get stuck.
4. **Debrief with teeth.** It asks how *you* think you did, then gives an honest read, reruns the moment that needs work, and closes with three actionable tips, a sound bite, and a report-back expectation.

It is deliberately uncomfortable — that discomfort is the method working. The target is calm, grounded, unshakeable, and still human.

## What's in here

```
skills/coach-skill/
├── SKILL.md              # the method (four steps, LAER, boundaries, tone)
├── references/
│   └── the-method.md     # origin, persona framing, the seven conversation topics
└── evals/
    └── evals.json        # trigger / non-trigger test cases
```

No scripts, no secrets, no MCP — it's a pure conversational skill, which is why the same folder ships to Claude Code, Claude.ai, and Cowork unchanged.

## License

MIT © Ranya Barakat.
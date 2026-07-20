# coach-skill

> Coaches you through a real soft-skills conversation — feedback, pushback, a hard client or team talk. Use it to rehearse or prepare for a difficult workplace conversation. Built on **The Human Layer**, the coaching method of Ranya.

## What it is

A soft-skills coaching skill for Claude. Instead of handing out generic advice, it runs a structured five-step method — tried, tested, and refined over and over:

- **Ground it**
- **Name the pattern**
- **Roleplay it**
- **Debrief with teeth**
- **Log it: the Growth Log**

It runs on whatever real situation you bring: a report who's underperforming, a client pushing scope, a peer you need to confront, or a talk you've been avoiding.

The method comes from an operations leader who ran weekly soft-skills coaching for her team for years. She is trained as an anthropologist and ended up in tech and CRM almost by accident. What she found there left a sour taste: in a results-driven industry, the human being at the center of every deal, every project, and every client relationship quietly becomes a commodity. Success gets measured in outcomes, timelines, and revenue, and both the person doing the work and the person on the other side of the table disappear from the picture.

The Human Layer is her response. The belief underneath it: soft skills are not the soft part of the job. They are the actual job, underneath the tech, the tools, and the contracts.

She led a team that regularly walked into rooms already feeling like the underdog, not because of anything they lacked, but because of how quickly people get sized up before they've even spoken. She built this method so her team could walk into any client relationship as an equal at the table, not as a vendor asking for approval.

Every session serves one outcome: you leave able to be **seen, felt, and heard as an equal at any table**. Knowledgeable and factual, kind and compassionate, always professional, and not someone to be messed with. Hardcore and gentle are not opposites here, the method holds both.

## Who it's for

Managers, operators, RevOps and CS leads, sales and client-facing teams, founders, anyone managing people or managing clients who sit in the uncomfortable middle between what a business wants and what a human relationship actually requires. If you have a hard conversation coming up, or one you've been avoiding, this is for you.

## Install

### Claude Code (plugin marketplace — recommended)

```
/plugin marketplace add promptmetrics/coach-skill
/plugin install promptmetrics-coach@promptmetrics
/reload-plugins
```

The slash command is `/promptmetrics-coach:the-human-layer`. It also auto-triggers when you ask a coaching-shaped question — no slash needed.

### Claude Code (local clone)

```
git clone https://github.com/promptmetrics/coach-skill
cd coach-skill
claude --plugin-dir .
```

Or, to auto-load it without a plugin, copy `skills/the-human-layer` into `~/.claude/skills/`:

```
cp -r skills/the-human-layer ~/.claude/skills/
```

### Claude.ai

Prerequisite: **Code execution and file creation** must be enabled in **Settings ▸ Capabilities**.

1. Get `the-human-layer.zip` (see "Getting the zip" below).
2. Open **Customize ▸ Skills** (https://claude.ai/customize/skills) → **+** → **+ Create skill** → **Upload a skill** → upload `the-human-layer.zip`.
3. Enable it in **Settings ▸ Capabilities**.

### Claude Cowork

Prerequisite: **Code execution and file creation** must be enabled in **Settings ▸ Capabilities**.

- **Standalone skill:** same as Claude.ai — upload `the-human-layer.zip` via **Customize ▸ Skills**.
- **Bundled in a plugin:** add the skill to a Cowork plugin via **Customize ▸ Plugins**.
- **Org-wide:** an owner enables sharing in **Organization settings ▸ Skills**, then the skill's **Share** action shares it with specific people or the whole org.

### Getting the zip

- Download `the-human-layer.zip` from the [v0.4 release](https://github.com/promptmetrics/coach-skill/releases/tag/v0.4), or
- Build it locally:

```
./scripts/build-zip.sh
```

The script produces `dist/the-human-layer.zip`.

## What a session looks like

You bring a real situation — a report who's underperforming, a client pushing scope, a peer you need to confront.

1. **Ground it.** The skill asks 2-3 sharp questions until it has the real, specific situation, not an abstract topic. Vague situations produce vague roleplay, so it pushes for specifics here.
2. **Name the pattern.** It identifies the dynamic at play in two or three sentences and gives it a name you can hold onto. Then it asks you to choose your framework: **LAER** (Listen, Acknowledge, Explore, Respond) alone, or **LAER sharpened with *Never Split the Difference*** (mirroring, labeling, calibrated questions). You can also opt into an ***Art of War* layer** that makes the counterpart tougher and less predictable — Claude's strategy for playing the character, never taught to you as technique.
3. **Roleplay it.** It plays the counterpart — relentless, not clever — and makes the rehearsal genuinely hard. Difficult people repeat deflections rather than debating; the roleplay reflects that. It offers tight, reusable sound bites (the actual words) that match the framework you chose, when you get stuck.
4. **Debrief with teeth.** It asks how *you* think you did, then gives an honest, specific read. It reruns the moment that needs work to test whether you apply the feedback or repeat the pattern, and branches on what it sees. It closes with three actionable tips for the week, one or two sound bites you can use verbatim, and a report-back expectation for next time.
5. **Log it: the Growth Log.** The session is written to a Growth Log — a running record of the situations you've worked, the framework you used, the Art of War layer, the coachability check, and the sound bites you took away. When Google Drive is connected it lands as a Sheet tab; otherwise it produces a downloadable markdown file you can keep and revisit.

It is deliberately uncomfortable — that discomfort is the method working. The target is calm, grounded, unshakeable, and still human.

## The seven doors (topics it covers)

One argument, seven entry points. You usually arrive at one door; the skill recognizes which and coaches through it.

- **The accent** — turning a second/third/fourth-language accent from something hidden into proof of operating across cultures. An accent is evidence of range, not a deficiency to apologize for.
- **The client is not always right** — permission to disagree with a client factually and professionally. The goal is staying grounded in what's true, not winning.
- **Partner, not vendor** — naming shared accountability out loud without being confrontational. A partner sits at the table; a vendor waits for approval.
- **Reading the room without becoming the room** — observing power dynamics accurately without adopting the cynical habits of people who play politics badly.
- **Using intuition in client management** — naming the "something's off" moment before you have proof, and treating it as a data point worth investigating.
- **Telling a client you're having a bad day** — a calibration skill: disclosure that builds trust (brief, contained) vs. disclosure that reads as unprofessional (open-ended, shifts the burden).
- **The Client Ledger move** — turning an emotionally charged conversation into a fact-based one before it explodes. Track what was sold, what was delivered with proof, and what was not — on the record, before the next hard conversation. A template is bundled with the skill at `skills/the-human-layer/references/client-ledger-template.md`.

## Boundaries

This is a workplace communication method, not therapy. It will not diagnose you, or anyone you describe, with a mental health condition. It won't offer clinical coping techniques. If a situation involves real distress, harassment, abuse, or anything beyond ordinary workplace friction, it stops the coaching frame, names plainly that this is bigger than a rehearsal session, and points you to real support — HR, a manager, a professional. It defaults to anonymized scenarios for third parties unless you explicitly opt into real specifics.

## Repository contents

```
coach-skill/
├── LICENSE                                     # MIT
├── README.md                                   # this file
├── The-Complete-Guide-to-Building-Skills-for-Claude.md   # maintainer reference (Anthropic skills-building guide)
├── .claude-plugin/
│   ├── plugin.json                             # promptmetrics-coach plugin manifest
│   └── marketplace.json                        # promptmetrics marketplace manifest
├── scripts/
│   └── build-zip.sh                            # builds dist/the-human-layer.zip for Claude.ai / Cowork upload
├── dist/                                       # build output (the-human-layer.zip)
├── archive/                                    # older snapshots
└── skills/
    └── the-human-layer/
        ├── SKILL.md                            # the method (five steps, LAER + Never Split the Difference + Art of War, boundaries, tone) — model-facing
        ├── README.md                           # human-facing companion to SKILL.md
        ├── references/
        │   ├── the-method.md                   # origin, persona framing, the seven doors + Growth Log
        │   └── client-ledger-template.md        # Client Ledger template (Door 7)
        └── evals/
            └── evals.json                      # trigger / non-trigger test cases
```

`The-Complete-Guide-to-Building-Skills-for-Claude.md` is the Anthropic skills-building guide, kept at the repo root as a maintainer reference. It is not part of the skill itself.

No scripts, no secrets, no MCP — `the-human-layer` is a pure conversational skill. The only file it produces is the Growth Log (a Sheet tab when Drive is connected, otherwise a downloadable markdown file); which is why the same folder ships to Claude Code, Claude.ai, and Cowork unchanged.

## Compatibility / portability

The same `skills/the-human-layer` folder works on Claude Code, Claude.ai, and Claude Cowork unchanged — it follows the open Agent Skills spec. The `SKILL.md` `description` is kept under the 200-character limit that Claude.ai and Cowork enforce, so the skill's trigger behavior stays consistent across surfaces. The plugin manifests (`.claude-plugin/`) are only used by Claude Code's plugin loader; Claude.ai and Cowork use the uploaded zip directly.

## License

MIT © Ranya Barakat.
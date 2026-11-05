# Editing CLAUDE.md and skill files: keep the always-on layer small

*A guide from the Second Sales Brain project, October 2026.*

If you run Claude Code (or any agent) with instruction files, two kinds of file shape what it does:

- **CLAUDE.md** loads in every session and is read on every turn.
- **Skills** (`.claude/skills/<name>/SKILL.md`, or commands) load only when their topic comes up.

Most setups get worse over time for one reason: everything ends up in CLAUDE.md. This guide is how to stop that.

## The core distinction

| | CLAUDE.md | A skill |
| --- | --- | --- |
| **When it loads** | Every message | Only when it's relevant |
| **Cost** | Paid on every turn, for the life of the setup | Paid only when it fires |
| **Good for** | Who the agent works for, safety limits, how to write to you | Procedures, formats, playbooks |
| **Bad for** | A procedure used once a day | Anything that has to hold all the time |

**Default to a skill.** CLAUDE.md is the exception. Every extra line is re-read on every turn, and a long file buries the rules that matter. A safety rule inside 400 lines of procedure gets skimmed.

## The admission test

Before adding a line to CLAUDE.md, ask:

> Does this need to be true in every message, including ones that have nothing to do with it?

- **Yes:** it goes in CLAUDE.md.
- **No:** it goes in a skill, with a one-line pointer from CLAUDE.md.

**Passes:** who you are and how you like to be written to; what the agent may do on its own and what needs your approval (money, legal, sending to people); safety limits.
**Fails:** your cold-call procedure; your email tone (needed only when writing an email); the format of a weekly report; anything about one project.

## The pointer pattern

CLAUDE.md holds one or two lines and the skill's name, and the line states the rule itself:

> **Email:** before drafting any email, load the `email-writer` skill. The short version: warm, plain, and no commitments I haven't made.

A bare filename gets skipped. A pointer that carries the rule doesn't.

## Rules for editing

1. **One fact, one home.** If a fact lives in another file or your notes app, link it. Copies drift until two files disagree and nobody knows which is right.
2. **Date every rule and say what caused it.** "Added (date), after a draft to a customer read like a legal letter." A rule with its story survives the next clean-up; a bare order gets cut by someone who doesn't know why it's there.
3. **Supersede, then remove.** When a rule is lifted, replace it with the new one and keep the old text in a collapsed `<details>` block with the date. Someone will ask why it changed.
4. **Remove lifted rules in the same pass.** A restriction that no longer applies but is still written down makes the whole file untrustworthy. Check dates when you read.
5. **Edit in place.** Put a change where the rule already lives. New sections at the bottom are how a file turns into sediment.
6. **Back up before a large edit.** Commit to git first, or copy the file as `CLAUDE.md.bak-YYYYMMDD-HHMMSS`.

## Write defaults with reasons, not absolutes

"Always" and "never" break on the first edge case. The agent either breaks the rule and learns your rules are negotiable, or refuses something you wanted. Write the default and the reason, so the agent can spot the exception: "Default: drafts only, because I send my own emails. If a send looks needed, ask me first."

Keep "never" for real safety limits. Better still, enforce those outside the prose: a permission deny list or a hook blocks the action no matter what the agent decides. Prose is context, not enforcement.

## Budget

Keep CLAUDE.md short: well under 200 lines is a good target. Past that, adherence drops. When you hit the limit, don't trim wording. Find the procedure that shouldn't be there and move it into a skill.

## Before you finish an edit

1. Could this have been a skill instead? (Usually yes.)
2. Is the same fact now written in two places?
3. Is the rule dated, with its cause?
4. Did anything else go stale that you didn't update?
5. Is CLAUDE.md still under budget?

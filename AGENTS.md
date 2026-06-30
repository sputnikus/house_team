# House Team OpenCode Pack

This repository defines a vanilla OpenCode command and three read-only subagents that emulate the diagnostic tension from House's improvised airplane team:

- `@cameron` — ethics, user impact, safety, and humane constraints.
- `@chase` — steelman, pragmatic execution path, and forward motion.
- `@foreman` — skeptical differential, missing evidence, and failure modes.
- `/house` — sends one prompt to all three and returns their independent results.

## Usage

Ask OpenCode to run:

```text
/house <your task, plan, bug, architecture question, or product idea>
```

The command should dispatch `@cameron`, `@chase`, and `@foreman` independently, then return only their outputs. The caller is responsible for the House-style synthesis.

## Design rules

- Keep this pack compatible with vanilla OpenCode file-based commands and agents.
- Do not depend on oh-my-opencode-slim conventions, plugins, or orchestrator behavior.
- Keep agents read-only by default (`edit: deny`). They are advisors, not implementers.
- Preserve independent opinions: each member should answer before seeing the others.
- Keep the tone useful, not cosplay-heavy. The characters are analytical lenses.

## File map

- `commands/house.md` — command prompt for fan-out and synthesis.
- `agents/cameron.md` — ethical and human-impact reviewer.
- `agents/chase.md` — practical supporter and implementation pathfinder.
- `agents/foreman.md` — skeptic and failure-mode reviewer.

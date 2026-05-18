# story-architect skill

A Claude Code / Codex skill for turning story prompts into complete narratives using a structured story-development workflow inspired by John Truby's *The Anatomy of Story*.

When this skill is active, the agent develops fiction from the inside out: premise, designing principle, seven key structure steps, character web, moral argument, story world, symbol web, organic plot, scene weave, scene construction, and final prose.

**Related resources:**
- Agent Skills format: [agentskills.io/specification](https://agentskills.io/specification)
- Claude custom skills docs: [claude.com/docs/skills/how-to](https://claude.com/docs/skills/how-to)

---

## What is Story Architect?

Story Architect is a writing workflow for producing complete stories, screenplays, and narrative outlines from a prompt or rough concept. It is designed for agents that can load a `SKILL.md` file and optional reference material on demand.

The skill emphasizes:

- A clear premise and designing principle before drafting
- Moral and psychological need, not just external plot
- Opponents who attack the hero's deepest weakness
- Character webs with four-corner opposition
- Moral argument expressed through structure
- Story worlds and symbols that grow from character
- A 22-step organic plot and scene-by-scene weave
- Dialogue built across story, moral, and repeated-keyword tracks

---

## Skill coverage

`SKILL.md` contains the active workflow organized into ten phases:

| # | Phase | What it covers |
|---|-------|----------------|
| 1 | Premise & Designing Principle | One-sentence idea, W-A-C, genre, moral choice |
| 2 | Seven Key Structure Steps | Weakness, need, desire, opponent, plan, battle, revelation |
| 3 | Character Web | Hero, opponent, allies, fake-ally opponent, four-corner opposition |
| 4 | Moral Argument | Theme line, moral decisions, argument variants |
| 5 | Story World | Arena, visual oppositions, natural/man-made spaces |
| 6 | Symbol Web | Story symbol, character symbols, object web, repetition |
| 7 | 22-Step Organic Plot | Complete structural plot sequence and revelations |
| 8 | Scene Weave | One-line scene list, structural order, crosscutting, genre beats |
| 9 | Scene Construction & Dialogue | Scene mini-stories and three-track dialogue |
| 10 | Final Polish | New equilibrium, thematic resonance, living ending |

Detailed reference material lives in `references/`:

| File | Contents |
|------|----------|
| `truby-complete-framework.md` | Condensed complete framework reference |
| `ch01_story_space.md` | Story as organic body, dramatic code, writing process |
| `ch02_premise.md` | Premise technique, designing principle, W-A-C |
| `ch03_seven_steps.md` | Seven key structure steps in depth |
| `ch04_character.md` | Character web, opposition, archetypes, change types |
| `ch05_moral_argument.md` | Theme line and moral argument through structure |
| `ch06_story_world.md` | World as character expression, arenas, visual development |
| `ch07_symbol_web.md` | Symbol lines, symbolic characters, objects, repetition |
| `ch08_plot.md` | Organic plot, 22 steps, revelations, subplot |
| `ch09_scene_weave.md` | Scene lists, ordering, crosscutting, storyteller device |
| `ch10_scene_construction.md` | Scene construction and symphonic dialogue |

---

## Installing the skill

### Claude Code

Copy the skill into your personal Claude Code skills folder:

```bash
mkdir -p ~/.claude/skills/story-architect
cp SKILL.md ~/.claude/skills/story-architect/
cp -r references ~/.claude/skills/story-architect/
```

Or place the files under `.claude/skills/story-architect/` in a project repository.

### Codex / agent skills

Copy the skill into your agent skills folder:

```bash
mkdir -p ~/.agents/skills/story-architect
cp SKILL.md ~/.agents/skills/story-architect/
cp -r references ~/.agents/skills/story-architect/
```

If your runtime uses `$CODEX_HOME/skills`, install there instead:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills/story-architect"
cp SKILL.md "${CODEX_HOME:-$HOME/.codex}/skills/story-architect/"
cp -r references "${CODEX_HOME:-$HOME/.codex}/skills/story-architect/"
```

Restart the agent application after installing so it reloads skill metadata.

---

## Usage examples

Ask naturally:

- "Write a literary sci-fi short story about a memory archivist who discovers his own childhood has been edited."
- "Develop this premise into a complete story: a disgraced cartographer maps a city that keeps changing to hide a murder."
- "Turn this idea into a screenplay outline using the story-architect skill."
- "Create a dark comedy short story about a startup founder who accidentally automates sincerity."
- "Give me the blueprint first, then write the complete story."

---

## When the agent loads this skill

The skill should trigger for tasks involving:

- Writing or developing a story, short story, novella, screenplay, script, or fiction concept
- Turning a rough idea into a complete narrative
- Building a character web, moral argument, story world, symbol web, scene weave, or organic plot
- Phrases like "write a story", "create a story", "story from prompt", "tell a story", "develop this idea into a story", "fiction", "narrative", or "screenplay"

---

## Requirements

- No API keys or external services are required.
- No runtime dependencies are required.
- The agent must support loading `SKILL.md` plus referenced Markdown files.

---

## Attribution and scope

This is an independently authored skill inspired by structural storytelling concepts associated with John Truby's *The Anatomy of Story*. It is not affiliated with, endorsed by, or sponsored by John Truby or his publisher.

The skill is intended as a writing assistant and structural checklist, not as a substitute for the original book or paid courses.

---

## License

MIT License. See [LICENSE](LICENSE).

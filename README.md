# easy-presentation

An agent skill for building clean presentation slides and natural spoken scripts that sound human without sacrificing academic rigor.

Most AI-generated talks fail in one of two ways: they dump walls of dense prose onto slides that read like a paper, or they sound like empty TEDx buzzword theater. `easy-presentation` combines three concrete standards into one reusable skill:

1. **Slide clarity (Steve Jobs):** One idea per slide, 25–45 words per content slide, one clear core message reinforced throughout, story-like flow (`Hook -> Problem -> Method -> Findings -> Impact`), simple visuals over dense tables, and no filler closing slides.
2. **Spoken delivery (Will Stephen, minus the hype):** Derived from Will Stephen's TEDxNewYork parody (*"How to Sound Smart in Your TEDx Talk"*): keep the vocal mechanics that actually hold a room (short spoken sentences, natural contractions, 130–145 wpm pacing, explicit `[pause]` / `[point]` / `[slow down]` cues) and cut the hollow buzzwords.
3. **Academic rigor:** Fair within-group comparisons, transparent limitations and labeling sources, one clean jargon-free method slide, evidence-driven claims without exaggeration, and honest reporting of null results.

## Repository Structure

```text
easy-presentation/
├── SKILL.md                          # Standalone skill file
├── eval.md                           # Self-check rubric for slides and scripts
├── skills/
│   └── easy-presentation/
│       ├── SKILL.md                  # Standard Agent Skills layout
│       └── eval.md
├── .claude-plugin/
│   ├── plugin.json                   # Claude Code plugin manifest
│   └── marketplace.json              # Claude Code marketplace definition
└── .cursor/
    └── rules/
        └── easy-presentation.mdc     # Cursor rule
```

## Install

### Option 1: Universal Agent Skills CLI (Recommended)

Works across Claude Code, OpenAI Codex, Cursor, Windsurf, Google Antigravity, and other Agent Skills-compatible tools:

```bash
npx skills add Lord-Haji/easy-presentation
```

### Option 2: Claude Code Plugin Marketplace

Inside Claude Code:

```text
/plugin marketplace add Lord-Haji/easy-presentation
/plugin install easy-presentation@easy-presentation
```

Or install manually as a global Claude Code skill:

```bash
mkdir -p ~/.claude/skills/easy-presentation
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/SKILL.md -o ~/.claude/skills/easy-presentation/SKILL.md
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/eval.md -o ~/.claude/skills/easy-presentation/eval.md
```

### Option 3: Google Antigravity

macOS / Linux:

```bash
mkdir -p ~/.gemini/config/skills/easy-presentation
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/SKILL.md -o ~/.gemini/config/skills/easy-presentation/SKILL.md
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/eval.md -o ~/.gemini/config/skills/easy-presentation/eval.md
```

Windows (PowerShell):

```powershell
New-Item -ItemType Directory -Force "$HOME\.gemini\config\skills\easy-presentation" | Out-Null
Invoke-WebRequest "https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/SKILL.md" -OutFile "$HOME\.gemini\config\skills\easy-presentation\SKILL.md"
Invoke-WebRequest "https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/eval.md" -OutFile "$HOME\.gemini\config\skills\easy-presentation\eval.md"
```

### Option 4: OpenAI Codex

```bash
mkdir -p ~/.codex/skills/easy-presentation
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/SKILL.md -o ~/.codex/skills/easy-presentation/SKILL.md
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/eval.md -o ~/.codex/skills/easy-presentation/eval.md
```

### Option 5: Cursor

Copy the rule file into your project's `.cursor/rules/` directory:

```bash
mkdir -p .cursor/rules
curl -fsSL https://raw.githubusercontent.com/Lord-Haji/easy-presentation/main/.cursor/rules/easy-presentation.mdc -o .cursor/rules/easy-presentation.mdc
```

## Usage

Once installed, ask your coding agent to use `easy-presentation` when building or revising slides and scripts:

- *"Use easy-presentation to turn my research report into a 3-minute slide deck and spoken script."*
- *"Audit my presentation script with easy-presentation so it sounds like a real human speaking, not a paper read aloud."*
- *"De-clutter these slides using easy-presentation and check them against `eval.md`."*

## License

MIT

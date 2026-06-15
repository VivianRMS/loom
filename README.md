# Loom — Customizable Skill Library

Loom is a collection of reusable, generalizable skills you can adapt to your vault.

## 📹 Walkthrough

[▶ Watch the Loom guide](https://github.com/VivianRMS/loom/releases/download/v0.1/loom-guide.mp4) — also available on the [v0.1 release page](https://github.com/VivianRMS/loom/releases/tag/v0.1).

## What You Get

- **`general-skills/`** — Ready-made skill templates (video research, and more coming)
- **`my-custom-skills/`** — Where your personalized versions live (starts empty)
- **Easy setup** — Just say "let's start" and Claude will guide you through customization

## How It Works

1. **You have templates** — Each skill in `general-skills/` is generic (works for anyone)
2. **You customize them** — Claude will collaborate with you to set up your custom skill
3. **You get custom versions** — Saved to `my-custom-skills/`
4. **You use your versions** — Not the generic ones

## Getting Started

1. **Start a Claude session** in your editor or IDE
2. **Say to Claude:** "LOOM!!!"

Claude will:
- Show you available skills
- Ask which ones you want to customize
- Ask your setup questions
- Create custom versions in `my-custom-skills/`

That's it. No manual editing needed.

## Example

**In a Claude session:**

**You:** "LOOM!!!"

**Claude:** "You have one available skill: Video Research. Want to customize it?"

**You:** "Yes"

**Claude:** "Where should video research files live in your vault? (e.g., `research`, `learning/videos`)"

**You:** "I want them in `learning/videos`"

**Claude:** ✅ Creates `my-custom-skills/video-research.md` with your folder path

**You:** Now use `my-custom-skills/video-research.md` for your video research sessions

## What's Inside

```
.
├── README.md                    ← You are here
├── CLAUDE.md                    ← Claude's instructions (Claude reads this)
├── general-skills/              ← Skill templates
│   ├── video-research/
│   │   ├── CLAUDE.md            ← Customization guide (Claude reads this)
│   │   └── (C) skill.md         ← The generic skill
│   └── ...more skills coming
└── my-custom-skills/            ← Your custom skills (empty to start)
```

## FAQ

**Q: Do I need to read CLAUDE.md?**
No. Just start a Claude session and say "LOOM!!!" — Claude reads it automatically and handles the rest.

**Q: Can I customize multiple skills at once?**
Yes. Claude will guide you through each one.

**Q: Can I share my custom versions?**
Sure! They're in `my-custom-skills/`. Just remember they're personalized to your vault, so others might need to adjust paths.

---

**Ready?** Start a Claude session and say "LOOM!!!"

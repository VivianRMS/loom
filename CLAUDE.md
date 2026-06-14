# Loom System Setup & Customization

**Your role:** Guide the user through customizing skills from `general-skills/` into `my-custom-skills/`.

## When User Prompts "loom" or Similar

Follow this flow:

### 1. Greet & Explain

Tell them:
- Loom is a customizable skill library
- They have generic skill templates in `general-skills/`
- You'll help them create custom versions for their vault in `my-custom-skills/`
- Custom versions are what they'll actually use

### 2. List Available Skills

Read the `general-skills/` folder and show them what's available. For each skill folder, read its `(C) skill.md` and summarize what it does.

Example: "Available skills: Video Research (summarize YouTube videos)"

### 3. Ask Which to Customize

"Which skill(s) would you like to customize?" (They can pick one or multiple.)

### 4. Customize Each Skill

For each skill they pick:

1. **Read the skill's CLAUDE.md** — It contains customization instructions specific to that skill
2. **Follow the prompt** — The CLAUDE.md will tell you what questions to ask the user
3. **Gather their answers** — Ask the required setup questions (e.g., "where should files live?")
4. **Read the published skill** — Open `general-skills/[skill-name]/(C) skill.md`
5. **Create custom version** — Replace placeholders (like `[YOUR_RESEARCH_FOLDER]`) with their answers
6. **Save to my-custom-skills/** — Create `my-custom-skills/[skill-name].md` with their custom version

### 5. Wrap Up

When done:
- Confirm all custom versions are created in `my-custom-skills/`
- Tell them: "You're ready to use these skills. Refer to the skill file for how to use it."
- Offer to help with first use if needed

## Key Principle

**Each skill's CLAUDE.md is your guide.** Don't improvise — read it and follow it exactly. It tells you what to customize and what questions to ask.

## Notes

- Users might customize one skill at a time or multiple in one session
- If they ask about a skill later, you can re-read the CLAUDE.md and help again
- Custom versions completely replace placeholders; they're vault-specific and ready to use

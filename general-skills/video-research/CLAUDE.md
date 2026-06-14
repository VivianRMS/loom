# Video Research — Customization Guide

This skill helps you process YouTube videos into summaries with Claude. This file guides you through customization.

## What to Customize

### 1. Research Folder (Required)

**Where should video research files live in your vault?**

Examples:
- `research` (simple, top-level)
- `learning/videos` (organized by topic)
- `projects/research` (within projects)

### 2. Summary Sections (Optional, but Recommended)

**What sections do you want in your summaries?**

You can use the defaults:
- Summary
- Key Concepts
- Takeaways

Or define your own based on your use case. Examples:

**Finance:** Summary, Investment Thesis, Risk Assessment, Action Items
**Tech:** Summary, Technical Concepts, How It Applies, Tools & Resources
**Learning:** Summary, Key Ideas, How It Connects, Next Steps
**Custom:** Whatever makes sense for your work

If you don't specify, Claude will use the defaults.

## How to Customize

### Option A: Just the Folder Path

**Share with Claude:**
```
I want to customize the Video Research skill for my vault. 

Research folder: [YOUR FOLDER PATH]

Use the default summary sections (Summary, Key Concepts, Takeaways).
```

Claude will create `my-custom-skills/video-research.md` with your folder path.

### Option B: Folder Path + Custom Sections

**Share with Claude:**
```
I want to customize the Video Research skill for my vault.

Research folder: [YOUR FOLDER PATH]

Custom summary sections:
- [Section 1 name]: [What goes in this section]
- [Section 2 name]: [What goes in this section]
- [Section 3 name]: [What goes in this section]
```

Claude will create `my-custom-skills/video-research.md` with both your folder path and custom sections in the template.

## Claude's Job

When customizing this skill:

1. **Read the user's preferences** — folder path and section names
2. **Open `general-skills/video-research/(C) skill.md`** — the published skill
3. **Create the custom version:**
   - Replace `[YOUR_RESEARCH_FOLDER]` with their folder path
   - Replace `[CUSTOM_SECTION_1]`, `[CUSTOM_SECTION_2]`, etc. with their section names
   - Replace the section descriptions with what they specified
4. **Save to `my-custom-skills/video-research.md`**
5. **Confirm it's ready to use**

---

**That's it!** The custom version is now ready to use.

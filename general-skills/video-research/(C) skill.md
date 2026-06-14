# Video Research Skill

A structured process for researching YouTube videos with Claude: extract key insights, discuss implications, and surface takeaways.

---

## Clone & Adapt

This skill is customizable. Before using, you'll define:

### 1. Research Folder
**Where should video research files live?**
Specify a folder path (e.g., `research`, `learning/videos`, `projects/research`).

### 2. Summary Sections (Optional)
**What sections do you want in your summaries?**

Default sections:
- Summary
- Key Concepts
- Takeaways

But you can customize. Examples:
- **Finance:** Summary, Investment Thesis, Risk Assessment, Action Items
- **Tech:** Summary, Technical Overview, How it applies to my work
- **General:** Summary, Takeaways

Define your sections, and Claude will customize the summary template for you.

That's it. Everything else flows from these two inputs.

---

## What This Skill Does

**Default flow:** Give Claude a video link → Claude downloads transcript and generates summary directly.

**Optional additions:**
- **Watch & Note** — Take your own notes while watching, then Claude reads them alongside the transcript
- **Iterate** — Several rounds of Q&A with Claude to explore implications and challenge conclusions

**Best for:** Any video where you want a structured summary + the option to dig deeper.

---

## Output Structure

Each video gets its own folder in `[YOUR_RESEARCH_FOLDER]/[YYYY-MM-DD-topic]/` with these files:

```
[YOUR_RESEARCH_FOLDER]/[YYYY-MM-DD-topic]/
├── transcript.en.srt     ← Downloaded from YouTube (required)
├── (C) summary.md        ← Claude's output: summary, takeaways, conclusions
└── workpad.md            ← Optional: your notes while watching
```

- **transcript.en.srt** — Claude downloads this to generate the summary (required; uses `yt-dlp`)
- **(C) summary.md** — Generated automatically; contains Claude's analysis
- **workpad.md** — Only created if you choose the "Watch & Note" option (optional)

---

## Templates

### (C) summary.md (always created)

**Default template** (if you don't customize sections):

```markdown
# [Video Title] — Summary

## Summary
[Claude's condensed summary of what the video is saying]

## Key Concepts
[Only if needed — short explanations of unfamiliar terms/ideas]

## Takeaways
[Claude's assessment — what's solid, what's hype, what's relevant to your use case]

## Discussed Topics
(Only populated if you iterate with Claude — skip this in the initial summary)

### [Topic 1]
[What we discussed, what we landed on]

### [Topic 2]
...
```

**Custom template** (if you define your own sections):

The structure stays the same, but the section names and descriptions match what you specified during customization.

Example (Finance use case):
```markdown
# [Video Title] — Summary

## Summary
[What the video is about]

## Investment Thesis
[What opportunity or claim is being made?]

## Risk Assessment
[What could go wrong? What assumptions are shaky?]

## Action Items
[Anything you should do based on this?]

## Discussed Topics
(Only populated if you iterate)
...
```

**Note:** The "Discussed Topics" section is always included (only populated if you iterate). Your custom sections form the core.

---

## The Flow

### Step 1: Give Claude a video link

Provide the URL and title. Claude will:
1. Create the session folder: `[YOUR_RESEARCH_FOLDER]/[YYYY-MM-DD-topic]/`
2. Download the transcript via `yt-dlp` and save as `transcript.en.srt`
3. Generate an initial summary and save to `(C) summary.md`

Claude posts the summary in the dialogue for you to read.

### Step 2 (Optional): Watch & Note

If you want to add your own perspective:
1. Watch the video yourself and take notes in `workpad.md` using the template below
2. When done, paste your notes in the chat or tell Claude you're ready
3. Claude will re-read the transcript alongside your notes and can refine or add context to the summary

This step is useful if you want Claude to understand what *you* found important, or if you have questions while watching.

### Step 3 (Optional): Iterate

Ask follow-up questions or challenge Claude's conclusions. Claude can:
- Clarify concepts
- Dig into specific claims
- Explore how the video relates to your use case
- Challenge or refine initial takeaways

During this phase, discussion happens in the chat. Claude updates `(C) summary.md` at the end with any refined conclusions in the "Discussed Topics" section.

---

### workpad.md template (for Watch & Note step)

```markdown
# [Video Title]

**Link:** [YouTube URL]
**Date watched:** YYYY-MM-DD
**Channel:** [channel name]

## Notes

[Raw notes from watching — any language, any format]

## My Thoughts

[Your reactions, questions, things you agree/disagree with]
```

---

## Prerequisites

This skill requires **`yt-dlp`** to download video transcripts (Claude needs the transcript to generate summaries).

Install with:
```bash
brew install yt-dlp ffmpeg
```

**Note:** Not all videos have available transcripts. If the download fails, let Claude know — some videos may not be summarizable.

---

## How It Works

- **Claude generates first** — You give a link, Claude downloads the transcript and creates a summary automatically
- **You add context** (optional) — If you watch the video too, Claude reads your notes alongside the transcript for a richer summary
- **Discuss if needed** (optional) — Ask follow-up questions; Claude updates the summary as you explore
- **Files stay saved** — The summary is created and saved even if you don't iterate; it's ready for later reference

---

## Tips for Best Results

1. **Use Watch & Note if you want your perspective included** — If you have strong reactions or questions while watching, jot them down; Claude will integrate them into the summary
2. **Be direct in follow-up questions** — Ask Claude to clarify, challenge, or expand on anything in the initial summary
3. **The summary file is permanent** — It stays in your vault and is searchable; reference it later if needed

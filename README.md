# Agent Skills

Fifteen skills for Claude that I built and use every day. Nine cover business: numbers, offers, funnels, copy, sales, brand voice, naming and writing. Six cover building products: UI design, usability, landing pages, and reverse engineering.

You never call a skill by name. Ask Claude a normal question and it loads the right skill by itself.

## Install

### Claude Code (terminal, desktop app, or IDE)

1. Download the repo and copy the skills into your skills folder:

   ```bash
   git clone https://github.com/whoiscarlo/agent-skills.git
   mkdir -p ~/.claude/skills && cp -R agent-skills/skills/* ~/.claude/skills/
   ```

2. Start a new Claude Code session. The skills load automatically.

Only want some of them? Copy just those folders, for example:

```bash
cp -R agent-skills/skills/refactoring-ui ~/.claude/skills/
```

If you already have a skill with the same folder name, the copy replaces it.

**To update later:** run `git pull` inside `agent-skills`, then run the copy command again.

### Claude.ai (web or desktop chat app)

1. Go to Settings, then Capabilities, and make sure Skills is turned on.
2. Download the zip for each skill you want from the [`claude-ai-uploads/`](claude-ai-uploads) folder.
3. Under Skills, click "Upload skill" and upload each zip, one at a time.
4. Start a new chat.

## Business skills

Built from study notes on Alex Hormozi's coaching calls and $100M books, Russell Brunson, Schwartz, Ogilvy, Sutherland, Zinsser, McEnerney, and a set of copywriting talks.

| Skill | Ask Claude things like |
|---|---|
| [business-diagnosis](skills/business-diagnosis/SKILL.md) | "Profit feels thin, should I cut ad spend?" "My leads are low quality." "How do I get from $400K to $2M?" |
| [offer-crafting](skills/offer-crafting/SKILL.md) | "Help me price and package this." "Design a lead magnet." |
| [lead-gen-funnels](skills/lead-gen-funnels/SKILL.md) | "Build me a funnel for this offer." "Write a follow-up email sequence." |
| [conversion-copy](skills/conversion-copy/SKILL.md) | "Write a landing page." "Fix this headline." |
| [sales-psychology](skills/sales-psychology/SKILL.md) | "How do I handle 'it's too expensive'?" "How should I frame this price?" |
| [closing-deals](skills/closing-deals/SKILL.md) | "They can only pay $3K of my $5K price." "Half my booked calls don't show." "How do I sell to enterprise?" |
| [brand-voice](skills/brand-voice/SKILL.md) | "Write voice guidelines for my brand." "Rewrite this product page, it sounds generic." |
| [brand-naming](skills/brand-naming/SKILL.md) | "What should we call this product?" |
| [clear-writing](skills/clear-writing/SKILL.md) | "Write a proposal asking my boss for budget." "Tighten this memo." |

## Design and build skills

| Skill | What it does | Ask Claude things like |
|---|---|---|
| [refactoring-ui](skills/refactoring-ui/SKILL.md) | Hierarchy, spacing, type, color and shadow rules from the book *Refactoring UI* | "This page looks off, fix it." "Pick a color palette for this app." |
| [ui-visual-craft](skills/ui-visual-craft/SKILL.md) | Visual rules with real numbers: animation timing, line length, touch targets, cards | "Make this card layout feel polished." "How long should this animation be?" |
| [usability-principles](skills/usability-principles/SKILL.md) | Krug's *Don't Make Me Think* and Norman's *Design of Everyday Things* as rules | "Review this sign-up flow." "Plan a quick usability test." |
| [landing-conversion-ux](skills/landing-conversion-ux/SKILL.md) | Landing pages, forms, CTAs, trust signals, and testing changes honestly | "Why isn't this landing page converting?" "Shorten this form." |
| [reverse-engineering-formats](skills/reverse-engineering-formats/SKILL.md) | Decoding undocumented file formats and rebuilding closed app output | "Figure out this binary file format." "Write tests for my decoder." |
| [clean-room-agents](skills/clean-room-agents/SKILL.md) | Rules for AI agents rebuilding a closed app without copying its code | "Set up rules so my agents can clone this app's file format safely." |

## Test that it works

Ask:

> I sell a $1,000 coaching program. 200 new clients a month, $700 ad cost per client, 5% buy my $5,000 upsell. Profit feels thin. What should I fix first?

A working install picks one number to fix, works out what it is worth per customer in dollars, and tells you what NOT to do yet. Without the skill you usually get a list of five ideas.

## Good to know

- Skills give Claude a method, not your facts. Give it your real numbers and your real customer reviews. The skills tell Claude to leave a placeholder rather than invent a result or a testimonial.
- The brand-voice skill uses a dog food brand called "Peek" as its worked example. It works for any brand.
- Each skill is one folder with a `SKILL.md` file. Open it to read exactly what Claude is told.

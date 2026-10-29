# Agent Skills

Thirty-three skills for Claude. Sixteen I built and use every day. Nine cover business: numbers, offers, funnels, copy, sales, brand voice, naming and writing. Seven cover building products: UI design, usability, UX laws, landing pages, and reverse engineering. The other seventeen are design skills by other authors that I use alongside mine, credited below with their sources and licences.

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
| [ux-laws](skills/ux-laws/SKILL.md) | 26 laws of UX (Hick, Fitts, Jakob, Miller, Doherty, Gestalt and more) as build rules with numbers and a review check each | "Review this screen against the UX laws." "Why does this form feel slow?" |

## Design skills by other authors

These are not mine. Each folder keeps its original licence file where the source repo has one. All credit goes to the authors; follow the source links for the latest versions.

### Review, polish and fix

| Skill | What it does | Source | Licence |
|---|---|---|---|
| [impeccable](skills/impeccable/SKILL.md) | Design director with 24 commands: critique, audit, polish, bolder, quieter, adapt, typeset, animate and more. Downloads a checksum-verified helper program on first use and sends anonymous telemetry unless `DO_NOT_TRACK=1` is set. | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | Apache 2.0 |
| [fixing-accessibility](skills/fixing-accessibility/SKILL.md) | Audit and fix ARIA, keyboard, focus, contrast and form errors | [master5d/claude-design-skills](https://github.com/master5d/claude-design-skills), from [ibelick](https://github.com/ibelick) UI Skills | none stated |
| [fixing-metadata](skills/fixing-metadata/SKILL.md) | Titles, descriptions, Open Graph, favicons, JSON-LD | same as above | MIT (in its header) |
| [fixing-motion-performance](skills/fixing-motion-performance/SKILL.md) | Find and fix animation that stutters | same as above | none stated |

### Product screens and apps

| Skill | What it does | Source | Licence |
|---|---|---|---|
| [interface-design](skills/interface-design/SKILL.md) | Craft rules for dashboards, tools and settings pages; saves decisions to `.interface-design/system.md` | [Dammyjay93/interface-design](https://github.com/Dammyjay93/interface-design) | MIT |
| [mobile-app-ui-design](skills/mobile-app-ui-design/SKILL.md) | Five-step method for mobile screens with fixed type, colour and spacing rules | [ceorkm/mobile-app-ui-design](https://github.com/ceorkm/mobile-app-ui-design) | MIT per README, no licence file |
| [responsive-craft](skills/responsive-craft/SKILL.md) | Mobile-first layouts, `clamp()` and container queries, live multi-width preview | [kylezantos/responsive-craft](https://github.com/kylezantos/responsive-craft) | MIT per README, no licence file |
| [baseline-ui](skills/baseline-ui/SKILL.md) | Strict Tailwind rules: accessible primitives, short animations, no glow | [master5d/claude-design-skills](https://github.com/master5d/claude-design-skills), from ibelick UI Skills | none stated |
| [emil-design-eng](skills/emil-design-eng/SKILL.md) | Emil Kowalski's approach to animation, easing and polish | same repo, from [Emil Kowalski](https://emilkowal.ski) | none stated |

### Landing pages

| Skill | What it does | Source | Licence |
|---|---|---|---|
| [ui-ux-pro-max](skills/ui-ux-pro-max/SKILL.md) | Offline searchable database of styles, palettes, font pairs and UX rules that returns a whole design direction. Needs Python 3. | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | MIT |
| [epic-design](skills/epic-design/SKILL.md) | Cinematic scroll pages: parallax depth, scroll text effects, GSAP | [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills) | MIT |

### Brand and design systems

| Skill | What it does | Source | Licence |
|---|---|---|---|
| [hue](skills/hue/SKILL.md) | Turns a brand, URL or screenshot into its own design-language skill | [dominikmartn/hue](https://github.com/dominikmartn/hue) | MIT |
| [design-system](skills/design-system/SKILL.md) | Three-layer design tokens and component specs | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | MIT |
| [brand](skills/brand/SKILL.md) | Brand voice, identity and consistency checks | same as above | MIT |
| [ui-styling](skills/ui-styling/SKILL.md) | shadcn/ui and Tailwind building, theming and dark mode | same as above | MIT |
| [banner-design](skills/banner-design/SKILL.md) | Social, ad and hero banners | same as above | MIT |
| [slides](skills/slides/SKILL.md) | HTML presentations with Chart.js | same as above | MIT |

Changes from the sources: the `ui-ux-pro-max` script paths point at `~/.claude/skills/ui-ux-pro-max/scripts/` instead of a plugin-only variable. Nothing else was edited.

If you wrote one of these and want it removed or credited differently, open an issue.

## Test that it works

Ask:

> I sell a $1,000 coaching program. 200 new clients a month, $700 ad cost per client, 5% buy my $5,000 upsell. Profit feels thin. What should I fix first?

A working install picks one number to fix, works out what it is worth per customer in dollars, and tells you what NOT to do yet. Without the skill you usually get a list of five ideas.

## Good to know

- Skills give Claude a method, not your facts. Give it your real numbers and your real customer reviews. The skills tell Claude to leave a placeholder rather than invent a result or a testimonial.
- The brand-voice skill uses a dog food brand called "Peek" as its worked example. It works for any brand.
- Each skill is one folder with a `SKILL.md` file. Open it to read exactly what Claude is told.

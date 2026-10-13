---
name: refactoring-ui
description: Use when designing, building, or polishing any web UI, from a single component to a full landing page or app screen. Covers visual hierarchy, spacing and sizing scales, type scale and line length, color palettes with 9 shades per hue, depth with two-part shadows, working with images and screenshots, finishing touches like accent borders and empty states, and a pre-ship checklist. Also use when a design "looks off" and you need concrete fixes.
---

# Refactoring UI

Practical rules for making interfaces look designed, distilled from the book
*Refactoring UI* by Adam Wathan and Steve Schoger. Rules below are paraphrased.
Pixel values for the spacing and type scales are reconstructed from the book's
example figures; they match Tailwind's default scales.

How to use this skill: pick the chapter that matches the problem, apply the
rules in order, then run the checklist at the end before calling the work done.

---

## 1. Starting from scratch

**Start with a feature, not a layout.**
Why: the nav, sidebar and shell depend on features you have not designed yet.
Design the actual thing first (a search form, a pricing card, an archive grid).

**Design in grayscale first. Add color last.**
Why: it forces spacing, contrast and size to carry the hierarchy. A design that
works in grey gets better with color; one that needs color to work is fragile.

**Ignore detail early.** Skip fonts, shadows and icons until the layout works.
Why: low-level choices slow you down and are cheap to change later.

**Design the smallest useful version.** Do not draw features you cannot ship yet.
Why: a half-built "nice to have" blocks the whole feature from shipping.

**Work in short cycles.** Design a simple version, build it, fix what breaks, repeat.
Why: real edge cases show up in a working UI, not in a mockup.

**Choose a personality on purpose.** It is set by a few concrete levers:
- Font: serif reads elegant or classic, rounded sans reads playful, neutral sans
  lets other elements carry the voice.
- Color: blue reads safe, gold reads premium, pink reads fun.
- Border radius: none reads serious, small reads neutral, large reads playful.
  Pick one and stay consistent. Mixing square and round corners looks worse.
- Words: formal copy reads official, casual copy reads friendly.
Why: personality is not mood board magic; it is these four settings.
Look at sites your audience already uses. Do not copy direct competitors.

**Limit your choices. Define systems in advance.**
Why: with unlimited options every choice is agonizing. With a short list, you
pick by elimination: guess a value, compare its neighbors on the scale, keep
the best, repeat.
Systematize: font size, font weight, line height, color, margin, padding,
width, height, box shadow, border radius, border width, opacity.

---

## 2. Hierarchy is everything

**Make importance obvious. Not all elements are equal.**
Why: when everything competes, the page reads as one noisy wall. De-emphasizing
secondary content is the single biggest lever for "looks designed".

**Do not use size alone for hierarchy. Use weight and color too.**
Why: size-only hierarchy makes primary text too big and secondary text too small.
- Text colors: 3 levels. Dark for primary (`gray-900`), mid grey for secondary
  (`gray-600`), light grey for tertiary (`gray-400`).
- Font weights: 2 levels for UI. Normal 400 or 500, bold 600 or 700.
- Avoid weights under 400 for UI text. Fine for big headings only. To
  de-emphasize, use a lighter color or smaller size instead of a thin weight.

**Never put grey text on a colored background.**
Why: grey works on white because it lowers contrast. On color it looks dead.
Pick a new color with the same hue as the background, then tune saturation and
lightness. Avoid white at reduced opacity: it looks washed out and lets images
show through.

**Emphasize by de-emphasizing.**
Why: if the key element will not pop, soften its competitors instead.
Example: give inactive nav items a softer color; drop a sidebar's background so
it sits on the page.

**Labels are a last resort.**
- Skip the label when the format says what it is (email, price, phone).
- Merge label and value: "12 left in stock", not "In stock: 12".
- When labels are needed (dashboards, stat tiles), make them small, lighter and
  quieter. The value is the hero.
- Exception: on spec sheets where users scan for the label, emphasize the label
  slightly instead.

**Separate visual hierarchy from document hierarchy.**
Why: an `h1` does not have to be huge. Section titles often act like labels and
should be small. Pick tags for meaning, then style for hierarchy.

**Balance weight and contrast.**
- Heavy elements (solid icons) next to text feel loud. Give them a softer color.
- Thin, light elements (1px soft borders) feel weak. Make them thicker, not darker.

**Style actions by importance, not by meaning.**
- Primary: one per page. Solid, high-contrast background.
- Secondary: outline or low-contrast fill.
- Tertiary: styled like a link.
- Destructive is not automatically big and red. Make it secondary or tertiary on
  the page, then big and red on the confirm step where it is the primary action.

---

## 3. Layout and spacing

**Start with too much white space, then remove it.**
Why: adding space until it "stops looking bad" leaves things cramped. What feels
like too much on one element is usually just enough in the full page.
Dense layouts are fine when chosen on purpose (dashboards), not by default.

**Use a spacing and sizing scale, not arbitrary pixels.**
Why: you should never debate 120px vs 125px. Neighboring values should differ
by at least about 25%, so steps are tight at the small end and wide at the big end.
Base unit 16px. Example scale:

```
4  8  12  16  24  32  48  64  96  128  192  256  384  512  640  768
```

Tailwind mapping: `1 2 3 4 6 8 12 16 24 32 48 64 96 128 160 192` (times 4px).
Use it for padding, margins, gaps, icon sizes and element widths. Need more
space? Try the next step, not +2px.

**You do not have to fill the screen.**
Why: if a thing needs 600px, give it 600px. Wide layouts are harder to read.
- Do not make a section full width just because the nav is.
- Design at about 400px wide first, then adapt upward.
- If something narrow feels lost on a wide screen, split it into columns
  (for example, help text beside a form) instead of stretching it.

**Grids are overrated. Not everything should be fluid.**
- Give sidebars and cards a fixed or max width tuned to their content; let the
  main area flex.
- Use `max-w-*` and only shrink when the screen is narrower than that width.
  Do not size a login card at "6 of 12 columns".

**Relative sizing does not scale.**
Why: a 2.5em headline is right on desktop and huge on mobile. Large things must
shrink faster than small things on small screens. Set sizes per breakpoint.
Same inside components: bigger buttons get more generous padding, smaller
buttons get tighter padding, not a uniform zoom.

**Avoid ambiguous spacing.**
Rule: space around a group must be larger than space within it.
Applies to label and input pairs, headings (more space above than below),
list items, and horizontal clusters.

---

## 4. Designing text

**Use a hand-picked type scale.**
Why: modular ratio scales give fractional pixels and too few UI sizes.
Example scale (px), matching Tailwind `text-xs` to `text-7xl`:

```
12  14  16  18  20  24  30  36  48  60  72
```

Use `px` or `rem`, never `em`, for the scale. Nested em values drift off scale
(1.25em inside 0.875em gives 17.5px).

**Use good fonts.**
- Safe UI default: a neutral sans, or the system stack
  (`-apple-system, Segoe UI, Roboto, Noto Sans, Ubuntu, Cantarell, Helvetica Neue`).
- Prefer families with 5 or more weights (filter Google Fonts by 10+ styles).
- For body and UI text avoid condensed faces with a short x-height.
- Popular fonts are popular for a reason. Borrow from sites you admire.

**Keep line length to 45 to 75 characters.**
Why: long lines make readers lose their place.
Tailwind: `max-w-prose` (65ch), or 20 to 35em. Constrain paragraphs even when
the section around them is wide for images.

**Align mixed font sizes on the baseline, not the center.**
Why: the eye already sees the baseline. Centered mixed sizes look slightly off.
Tailwind: `items-baseline`.

**Line height is proportional.**
- Small text and wide columns need taller line height (1.5 to 2).
- Large headings need less (1 to 1.25). Tailwind: `leading-none` or
  `leading-tight` on display text.
- Rule: line height goes down as font size goes up.

**Not every link needs a color.**
In link-heavy UI, mark links with weight or a darker shade. Ancillary links can
show underline or color only on hover. Links inside paragraphs still need to
stand out.

**Align for reading.**
- Left-align anything over two or three lines. Center only short blocks.
- If one centered block runs long, rewrite it shorter.
- Right-align numbers in tables. Use `tabular-nums` so digits line up.
- If you justify text, turn on `hyphens: auto`.

**Use letter spacing deliberately.**
- Tighten large headlines set in a text-oriented family (`tracking-tight`).
- Widen all-caps text (`tracking-wide` or `tracking-wider`). Caps have fewer
  distinguishing shapes.
- Otherwise leave it alone.

---

## 5. Working with color

**Think in HSL (hue, saturation, lightness), not hex.**
Why: related colors look related in HSL. Hue 0 is red, 120 green, 240 blue.
Do not confuse HSL with HSB in design tools; browsers use HSL.

**You need far more colors than a 5-swatch palette.**
- Greys: 8 to 10 shades. Almost the whole UI is grey. Avoid pure black; start
  from a very dark grey.
- Primary: 1 or 2 hues, 5 to 10 shades each. Ultra-light for tinted backgrounds,
  dark for text.
- Accents: semantic and highlight colors (red danger, yellow warning, green
  success, plus a bright "new" color), each with shades. Use sparingly.
- A complex UI can need around 10 hues with 5 to 10 shades each.

**Define shades up front. No `lighten()` or `darken()` on the fly.**
Why: on-the-fly math produces 35 near-identical blues.
Build a 9-shade scale (`100` to `900`, Tailwind adds `50` and `950`):
1. Pick the base (`500`): a color that works as a button background.
2. Pick the edges: `900` for text on a tint, `100` for a tinted background.
   Use an alert component to judge both.
3. Fill the midpoints: `700` and `300`.
4. Fill the rest: `800`, `600`, `400`, `200`.
5. Trust your eyes over the numbers. Tweak, but do not keep adding shades.
For greys: darkest = your darkest text color, lightest = a subtle off-white.

**Raise saturation as lightness moves away from 50%.**
Why: very light and very dark shades look washed out at the same saturation.

**Shift hue to change brightness.**
Bright hues are 60 (yellow), 180 (cyan), 300 (magenta). Dark hues are 0, 120, 240.
To lighten, rotate toward the nearest bright hue; to darken, toward a dark hue.
Keep it within 20 to 30 degrees. Example: darker yellows drift toward orange so
they feel rich, not muddy brown.

**Greys do not have to be grey.**
Tint greys with blue for a cool feel, or yellow/orange for a warm feel. Raise
the tint at the light and dark ends to keep the temperature even.

**Accessible does not have to mean ugly.**
- WCAG: 4.5:1 for normal text (under about 18px), 3:1 for large text.
- White text on color needs a dark background, which can grab too much
  attention. Flip it: dark colored text on a light tinted background.
- Secondary text on a dark colored panel: rotate the hue toward a brighter hue
  (cyan, magenta, yellow) to gain contrast without going white.

**Do not rely on color alone.**
Pair color with an icon, label or arrow (up/down trend). In charts, vary
lightness, not just hue. Color should support a message, never be the only one.

---

## 6. Creating depth

**Light comes from above.**
- Raised element: a slightly lighter top edge (top border or
  `inset 0 1px 0 <lighter hue>`), plus a small, sharp dark shadow below
  (`0 1px 3px`). Hand-pick the light color; white overlays drain saturation.
- Inset element (inputs, wells): lighter bottom edge, small dark inset shadow at
  the top (`inset 0 2px 4px`).
- Do not chase realism. A hint is enough.

**Use shadows to show elevation, from a fixed set of about 5.**
Why: shadow size tells the user how close something is, and closer draws focus.
- Small: buttons, cards (`shadow-sm`, `shadow`).
- Medium: dropdowns, popovers (`shadow-md`, `shadow-lg`).
- Large: modals (`shadow-xl`, `shadow-2xl`).
Define the smallest and largest first, then fill the middle roughly linearly.
Use elevation for interaction: lift a dragged item, shrink the shadow on a
pressed button. Decide where the element sits, then pick its shadow.

**Shadows have two parts.**
- Part 1, large and soft: big offset, big blur. The cast shadow from direct light.
- Part 2, tight and dark: small offset, small blur. The ambient shadow right
  under the object.
- Example: `0 4px 6px -1px rgb(0 0 0 / .1), 0 2px 4px -2px rgb(0 0 0 / .1)`.
- As elevation rises, fade the tight shadow; at the highest level it nearly
  disappears.

**Flat designs can still have depth.**
- Lighter than the background reads as raised, darker reads as sunken. On dark
  themes, raised surfaces should be slightly lighter than the page.
- Solid shadows: short vertical offset, zero blur, for a flat look with lift.

**Overlap elements to create layers.**
Let a card straddle two background sections, or be taller than its parent.
For overlapping images, add an "invisible border" in the background color
(`ring-4 ring-<page-bg>`) so they never clash.

---

## 7. Working with images

**Use good photos.** Hire a photographer or use quality stock. Never design with
placeholders and plan to swap in phone shots later. It never works.

**Give text on images consistent contrast.** Fix the image, not the text:
- Overlay: black for light text, white for dark text (`bg-black/50`).
- Lower image contrast, then adjust brightness.
- Colorize: lower contrast, desaturate, then a brand-color fill with
  `mix-blend-multiply`.
- Text shadow as a soft glow: large blur, no offset.

**Everything has an intended size.**
- Do not scale up small icons. Icons drawn at 16 to 24px look chunky at 3x.
  Put a small icon inside a colored circle or rounded square instead.
- Do not shrink full screenshots. 16px app text becomes unreadable 4px text.
  Capture at a smaller viewport, crop to a partial screenshot, or draw a
  simplified version with lines for text.
- Do not shrink detailed logos to favicon size. Redraw a simple version.

**Control user-uploaded images.**
- Fixed-size containers with center crop (`object-cover` plus a fixed aspect
  ratio). Never let intrinsic ratios break the grid.
- Stop images bleeding into a same-colored background with a subtle inner
  shadow (`inset 0 0 0 1px rgb(0 0 0 / .1)`) or semi-transparent inner border,
  not a solid border that clashes.

---

## 8. Finishing touches

**Supercharge the defaults.**
Swap bullets for icons (checks, arrows, or content-specific icons). Turn quote
marks in testimonials into large colored shapes. Give links a custom thick
underline in a brand color. Color custom checkboxes and radios in the brand hue.

**Add color with accent borders.**
A colored bar on top of a card, beside an alert, under an active nav item, under
a headline (short), or across the top of the page (`border-t-4`).
Cheap, needs no illustration skill, and reads as "designed".

**Decorate backgrounds, quietly.**
- Change the section background to separate page sections.
- Gradients: use two hues no more than about 30 degrees apart.
- Subtle repeating patterns, or a pattern along one edge only.
- A few simple shapes or a simplified illustration in set positions.
Keep pattern contrast low so content stays readable.

**Design the empty state first, not last.**
It is the user's first impression. Add an illustration and a clear call to
action. Hide tabs and filters that do nothing until content exists.

**Use fewer borders.** Separate elements with, in order of preference:
1. More spacing.
2. Slightly different background colors.
3. A soft box shadow.
If you already have a background change, the border is probably redundant.

**Think outside the box.**
Dropdowns can have sections, columns, icons and helper text. Table cells can
combine related columns, show images and color. Important radio groups can be
selectable cards. Defaults are habits, not rules.

---

## 9. Leveling up

**Look for decisions you would not have made.** When a design impresses you,
ask what the designer did that you never would. Steal that move.
Examples: an inverted background on a date picker, a button inside an input, a
headline in two colors.

**Rebuild interfaces you admire, without peeking at dev tools.**
Why: closing the gap teaches tricks like tighter heading line height, wider
tracking on caps, and layered shadows.

---

## Pre-ship checklist

- [ ] One clear primary action per view. Secondary and tertiary actions are quieter.
- [ ] Hierarchy works in grayscale (squint test: the key thing still wins).
- [ ] Text uses 2 or 3 color levels and 2 weights. Nothing under 400 weight in UI text.
- [ ] No grey text on colored backgrounds; secondary text uses a tuned same-hue color.
- [ ] Every spacing, size and font size comes from the scales above.
- [ ] Space between groups is larger than space within groups.
- [ ] Paragraphs are 45 to 75 characters wide; long text is left-aligned.
- [ ] Headline line height is tight; body line height is 1.5 or more.
- [ ] All-caps labels have extra letter spacing; big headlines are slightly tightened.
- [ ] Every color comes from a predefined shade scale. No ad hoc hex values.
- [ ] Contrast meets 4.5:1 (normal text) and 3:1 (large text).
- [ ] Color is never the only signal (icons or text back it up).
- [ ] Shadows come from a fixed elevation set and match each element's role.
- [ ] Borders are used only where spacing, background or shadow could not do it.
- [ ] Images sit in fixed-ratio containers; screenshots and icons are at their intended size.
- [ ] Text over images has an overlay or other contrast fix.
- [ ] Empty, loading and error states are designed.
- [ ] Layout checked at about 400px wide and at desktop width.

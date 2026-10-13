---
name: ui-visual-craft
description: Use when building or critiquing web UI visuals. Covers visual hierarchy, white space, color, consistency, card layouts, interaction feedback and response time, motion timing, microinteractions, storytelling on long pages, and style guides. Gives imperative rules with concrete values (response time limits, animation durations, line height, line length, image share of a card, touch target size) drawn from the UXPin UI and interaction design ebooks (2014 to 2016) plus the core principles of About Face.
---

# UI Visual Craft

Rules for making a web interface look ordered, read clearly, and respond
well. Distilled from a shelf of UI and interaction design ebooks. Most are
UXPin titles from 2014 to 2016. Only the parts that still hold are kept here.

When building, work through the sections in order. When critiquing, run the
checklist at the end and name the rule each problem breaks. The numbers are
starting points, not laws. Book names in brackets show each group's source.

---

## 1. Visual hierarchy

1. **Pick one focal point per screen and design everything else around it.**
   A page with two heroes has none. Decide the single most important element
   first: an image, a headline, or one call to action.
2. **Rank elements by size first.** The biggest thing gets seen first.
   Size can even beat the normal left to right, top to bottom reading order.
3. **Shrink the rest instead of enlarging the hero.** "Big" is relative.
   Making secondary items smaller gives the same contrast and saves space.
4. **Do not keep growing an already large button.** The gain is not linear.
   Making a small button bigger helps a lot. Making a big button bigger only
   makes it loud and throws off the balance of the page.
5. **Give the page a budget of attention.** One working method: 15 points
   per page. Each element costs one point. Anything you want to stand out
   costs more. When the budget runs out, cut something.
6. **Use at least three levels of type.** Primary (headlines, rare, biggest,
   brightest). Secondary (subheads, captions, labels). Tertiary (body text,
   plain, meant to be read without distraction). A fourth level comes from
   small touches like bold, italics, or link color.
7. **Create hierarchy with size, weight, color, contrast, space and
   position, not just one of them.** Bold is subtler than size. Italics are
   subtler than bold. All caps reads as shouting and looks larger than it is.
8. **Lay out for how people scan.** Text-heavy pages get read in an F shape:
   across the top, then down the left edge. Sparse pages with a goal get a
   Z: across, diagonally down, across again. Put key content and the main
   action where those paths land.
9. **Use the ends of rows and columns.** A line of items carries the eye
   forward. The spot where it ends is prime space for a call to action.
10. **Squint test.** Blur your eyes or step back. What stands out, what is
    fuzzy, what looks grouped? If the answer is not what you intended, the
    hierarchy is wrong.
11. **Make each difference mean something.** Every change in color, size, or
    style should exist for a reason. Things that behave differently must look
    different. Things that behave the same must look the same.

[The Building Blocks of Visual Hierarchy; Web UI Design for the Human Eye;
Interaction Design Best Practices: Words, Visuals, Space; About Face 4, ch. 17]

## 2. White space

1. **Treat empty space as a design element, not leftover canvas.** The fewer
   elements on screen, the stronger each remaining one becomes.
2. **Use space to show what belongs together.** Items close together read
   as one group (the Gestalt law of proximity). Put a small gap inside a
   group and a large gap between groups. This does the work that borders and
   dividers usually do.
3. **Put labels right next to what they label.** A label floating halfway
   between two fields makes people hesitate, and hesitation hurts completion.
4. **Separate by function.** Areas that do different jobs (browsing content
   versus account settings) get more distance between them than areas that
   do similar jobs.
5. **When unsure, add space rather than remove it.** Cramped pages are the
   more common failure. Margins and space between paragraphs can lift
   reading comprehension by up to about 20%.
6. **But do not starve the page.** Too much space dissolves relationships
   between elements, lowers information density, and forces long scrolls.
   Space has value only relative to what is around it.
7. **Think in two scales.** Macro space is between major blocks and around
   the layout. Micro space is between letters, lines, paragraphs, list
   items, and buttons. Fix macro space first, then micro.
8. **Put space around a logo instead of making it bigger.** Room around a
   mark draws the eye to it without shouting.
9. **Start sparse at the top and get denser as the scroll deepens.** The
   first screen sells the idea with few words and strong images. Detail
   comes further down for people who are already interested.
10. **Use asymmetry on purpose.** One element given uneven space, or one
    slightly larger thumbnail in a row, pulls attention. Repeated asymmetry
    (image left, then right, then left) becomes a rhythm and feels calm.
11. **The golden ratio (1 : 1.618) is a tool, not a rule.** It can help split
    a layout into main and side areas. Do not force it onto every
    relationship on the page.

[Zen of White Space: Balance, Contrast, Hierarchy; Zen of White Space:
Space, Ratios, Minimalism; White Space in Web UI Design; Interaction Design
Best Practices: Words, Visuals, Space]

## 3. Typography for reading

1. **Set body text line height to 1.4 to 1.6 times the font size.** The books
   give 1.3 to 1.5, about 1.5, and 1.5 to 1.75 at different points. Around
   1.5 is the safe middle. Never make line height so large that a line
   floats free of the next one.
2. **Keep lines to roughly 60 to 70 characters.** Longer lines make it hard
   to find the start of the next line.
3. **Use 16px or more for body text.** Smaller text forces pinch and zoom on
   tablets and strains eyes on desktop.
4. **Make paragraph spacing clearly bigger than line spacing.** A reader
   should never have to guess where one paragraph ends and the next begins.
5. **Pair a characterful display face with a plain, readable text face.**
   Decorative type is for glancing, not reading. Keep it to headlines.
6. **Default to regular weights.** Thin and ornate faces raise effort. If the
   font is small, pick one with a large x-height.
7. **Keep text out of images.** Real text stays sharp on high density
   screens, can be read by assistive tech, and can be restyled.
8. **Test custom fonts at every size you use.** Some faces fall apart small.
9. **Front-load headlines and keep hero headlines to about 5 to 7 words.**
   People decide in seconds whether to stay.

[Web UI Design for the Human Eye; Zen of White Space; Tablet Web Design
Best Practices; Interaction Design Best Practices: Words, Visuals, Space;
Clever Interactive Techniques for Web Storytelling]

## 4. Color

1. **Choose a dominant color, a secondary color, and at most one accent.**
   Spreading colors evenly gives the page no direction. The dominant color
   sets the mood; the secondary separates elements; the accent marks action.
2. **Build the base from neutrals and a few low-saturation colors. Save
   high-contrast, saturated color for what matters.** Intense color,
   texture, and too many hues are visual noise.
3. **Get the layout working in grayscale first. Add color last, with a
   purpose for each use.** If the page only works because of color, the
   hierarchy is weak.
4. **Use a bright accent against a dark background to pull the eye.**
   Bright color on a dark field gives strong contrast with very little
   area. Repeat the same accent at a few points down the page to lead the eye
   from one point of interest to the next.
5. **Use complementary colors (opposite on the wheel) for action, and
   neighboring colors for calm.** Opposites make each other look more intense.
   A complementary accent makes a button jump; analogous palettes feel
   harmonious but separate elements less.
6. **Do not desaturate complementary pairs.** Muddy opposites lose the
   punch that was the reason to use them.
7. **Shades of one hue always go together.** A one-hue scheme (light to dark
   versions of a single color) is safe and elegant but makes it harder to
   single out an element. Add one contrasting accent if you need a CTA.
8. **Keep strong colors scarce.** Red and black dominate whatever they touch.
   Use them in small amounts or they take over the page.
9. **Mind what colors suggest.** Warm colors (red, orange, yellow) excite;
   cool colors (blue, purple) calm. Red signals alarm or urgency. Dark blue
   reads reliable. Purple reads luxurious. Pick the mood on purpose.
10. **Bind meaning to color and never break it.** If green means confirm,
    it means confirm everywhere. A green Delete button is a trap.
11. **Tie imagery to the palette.** Photos whose colors fight the page feel
    jarring. A subtle overlay or consistent treatment unifies them.
12. **Pick text color for its background.** On gray, white text often reads
    better than black. Always check contrast against the actual background.

[Color Theory in Web UI Design; The Building Blocks of Visual Hierarchy;
Web UI Trends: The Vibrancy of Color; Mobile Card Interfaces; About Face 4,
ch. 17; Consistency in UI Design]

## 5. Consistency

1. **Follow outside conventions for core functions.** People bring habits
   from every other site: the logo goes home, blue or underlined text is a
   link, a thumbnail next to a title is clickable. Breaking these costs
   attention every time.
2. **Be fully consistent inside your own product.** Check six things:
   color meaning, type roles, wording, visual components (buttons, icons,
   links), layout and placement, and interaction behavior (forms, dialogs,
   transitions).
3. **Use the same word for the same thing.** If one screen says Save, do not
   say Submit for the same action elsewhere. Do not swap Yes/No for
   Accept/Reject between tasks.
4. **Keep repeated elements in the same place.** If search sits top right on
   one page, it sits top right on every page.
5. **People remember behavior more than looks.** You can restyle a pattern
   as long as it still behaves the way people expect.
6. **Break consistency only to draw attention, and only once.** One white
   hat on a man dressed in black gets noticed. A white hat, white shoes and a
   white tie cancel each other out.
7. **Break it also when consistency would hurt usability.** If that keeps
   happening, change the rule rather than adding exceptions.
8. **Never make a primary action appear only on hover.** Hover does not exist
   on touch screens, and hidden primaries are not found.
9. **Obey standards unless the alternative is clearly better.** "Different"
   is not "better". Consistency does not mean rigid sameness either.

[Consistency in UI Design: Creativity Without Confusion; Tactical UI
Design Patterns; About Face 4, ch. 17]

## 6. Cards and thumbnail grids

1. **One card, one idea, one main action.** Usually that action is "open
   this". Secondary actions (share, save) stay small or appear on hover.
2. **Let the image take 50 to 75% of the card.** The rest holds a short
   title, a line of context, and breathing room.
3. **Crop and scale every image for its container.** A sharp, well-cropped
   thumbnail is the whole point of the card.
4. **Use simple type on cards.** A plain sans serif: medium weight for the
   card title, regular for supporting text.
5. **Use one grid with equal gaps.** Fixed card width with equal spacing is
   the usual pattern. Height can vary in a masonry layout, or come in a few
   fixed sizes. The grid must hold at every breakpoint.
6. **Make the whole card the click target.** Not just the title link.
   Bigger targets are faster to hit, and people will tap the image first.
7. **If an image looks clickable, make it clickable.** Users tap
   thumbnails. When nothing happens, they lose trust in the whole page.
8. **Cards suit content from many sources.** They let items from different
   brands or authors sit side by side with equal weight.
9. **Group cards into labeled rows or containers when there are many.**
   A long unstructured wall of cards causes overload. Categories, or a
   magazine layout with a few larger cards, give the eye places to rest.
10. **Light shadows from one direction.** A shadow cast on every side breaks
    the illusion of a physical card. Keep shadows soft and consistent.
11. **Put text over images only with protection.** Use a dark overlay, a
    solid box behind the text, or a blur. Never trust a busy photo.
12. **Add one small surprise at most.** One unexpected detail (a subtle
    motion, a shape) can set a grid apart. Several look desperate.
13. **Design the empty state.** A grid with no items is the first thing a
    new user may see. Explain why it is empty and what to do next.

[Web UI Trends: Card-Based Design Patterns; Mobile Card Interfaces;
Mobile UI Design Patterns; Tactical UI Design Patterns]

## 7. Feedback and response time

1. **Respond within 0.1 seconds.** That is the limit for an action to feel
   like direct control. Show some visible change (pressed state, highlight)
   right away, even if the real work takes longer.
2. **Within 1 second, the user notices the wait but keeps their train of
   thought.** Acceptable for loading a new page.
3. **At 10 seconds, attention is gone.** Anything near this needs a progress
   indicator and, ideally, a way to do something else meanwhile.
4. **Match the delay to the size of the task.** Five seconds is fine for
   loading a heavy dashboard. It is unacceptable for opening a menu.
5. **Every action gets an answer.** Did it work? What changed? What next?
   A silent interface feels broken.
6. **Turn waits into something.** A branded or informative loading
   animation makes a wait feel shorter. It does not replace making the
   wait shorter.
7. **Give feedback in place.** An add-to-cart that animates into the cart
   icon tells the user it worked without sending them anywhere.
8. **Make hover areas generous.** On grids, highlight the whole card on
   hover, not just the text link.
9. **Use hover only to reveal secondary information.** Never hide a primary
   action behind it.
10. **Make touch targets at least 44 x 44px.** Grow the tappable area with
    padding, not margin. Margin adds space but not hit area.
11. **Make destructive actions harder than safe ones.** Cancel is one easy
    click. Delete asks for a deliberate second step.

[Interaction Design Best Practices: Time, Responsiveness, Behavior;
Interaction Design Best Practices: Words, Visuals, Space; Interaction
Design Unlocked Vol. I; Tablet Web Design Best Practices]

## 8. Motion and timing

1. **Start the animation within 0.1 seconds of the user's action.** The
   motion can last longer; the start cannot lag.
2. **Use short durations for direct responses.** A secondary element
   entering after a user action can take about 300ms. Hover and press
   states should be faster still. (The 300ms value is from the books; a
   150 to 250ms range for small UI changes is a common modern practice.)
3. **Slow down changes the user did not cause.** When content changes on its
   own, animate it over about 800ms to 1 second so people notice it.
4. **Ease in and out.** Add acceleration at the start and deceleration at
   the end. Constant speed looks mechanical.
5. **Move along curves when it fits.** Arcs feel organic; straight lines
   feel robotic.
6. **Stagger, do not dump.** When a block of content arrives, reveal it in
   a short sequence. A wall of text appearing at once feels like a lot.
7. **Delay the secondary, never the primary.** If a click scrolls the page,
   the scroll starts at once. A form that follows it can fade in a beat
   later. That avoids a jarring jump.
8. **Animate opening and closing.** Menus and panels that expand smoothly
   tell the user what changed and where it came from.
9. **Match pace to tone.** Faster motion suits light, playful products.
   Slower suits serious or complex ones.
10. **Push reality only slightly.** A touch of bounce can add charm.
    Too much looks cartoonish.
11. **Avoid auto-rotating carousels.** They move content away before people
    can read it and distract people who came for something else. If you
    must use one, show each slide for about 2.5 times the time it takes to
    read it aloud, and pause on hover.
12. **Limit the number and direction of animated transitions.** Too many
    moving parts disorient people.

[Interaction Design Best Practices: Time, Responsiveness, Behavior; The
Curated Collection of Web Design Techniques: Interaction Design and
Complex Animations; About Face 4, ch. 19]

## 9. Microinteractions and delight

1. **Design each microinteraction in four parts.** Trigger (what starts it),
   rules (what happens), feedback (how the user knows), and loops or modes
   (what happens on repeat or over time). This structure comes from Dan
   Saffer.
2. **Design for the hundredth use, not the first.** What is charming once
   can be annoying by the hundredth time. Avoid gimmicks.
3. **Keep the response as simple as the action.** Simple type, simple words,
   simple colors.
4. **Use the product's own palette in microinteractions.** They should
   look like part of the parent design, not a sticker on top.
5. **Write feedback the way a person talks.** "Saved" or "Link copied", not
   "Operation completed successfully".
6. **Delight comes last.** Function, reliability and usability come first.
   Delight is the icing, never a patch over a usability problem.
7. **Keep labels plain.** "Great, let's go!" in place of "Submit" makes
   people hesitate. Personality belongs in the details, not the controls.
8. **Good delight is instant, subtle, consistent with the rest of the page,
   and asks for no extra effort.** If it calls attention to itself or slows
   the user, cut it.
9. **Familiar beats novel for first impressions.** People rate familiar
   layouts as more attractive. Innovate where it helps the task, not in
   core navigation.

[Interaction Design Unlocked Vol. I: Designing the Details; Demystifying
Delightful Interaction Design; Interaction Design Best Practices: Words,
Visuals, Space]

## 10. Storytelling on long pages

1. **Know the story before designing it.** A long page needs a beginning
   (the hook), a middle (the proof and detail), and an end (the action).
   Map those three before placing anything.
2. **Make the story only as long as it needs to be.** If one image tells it,
   do not use twenty. If it needs twenty, do not squeeze it into eight.
3. **Show, then tell.** People process and remember images faster than
   text. Lead with the strongest visual and use short text to clarify it.
4. **Use real content, not placeholder text.** A layout built on lorem ipsum
   hides problems that real headlines and real images expose.
5. **Keep images from one "world".** Same color treatment, same style, no
   repeated concepts. Each image should move the story on.
6. **Make the user a character.** Address them directly, or let them choose
   a path ("I am a designer / a marketer"). Personal relevance holds
   attention.
7. **Add interaction to actions people already do.** Scroll and click are
   free. Scroll-triggered reveals and hover details add depth without new
   controls.
8. **Do not add interaction for its own sake.** Pages people use to find
   information fast should stay fast. Every effect must serve the reader.
9. **Hidden extras are for secondary content only.** Anything critical to
   the goal must be visible. Easter eggs suit playful audiences.
10. **Background video: short loop, muted, sharp, with a still fallback.**
    The story must come across in a few seconds. Never let it slow the
    page load.
11. **Alternate the layout down the page.** Image left, text right, then
    swap. The zig-zag keeps a long scroll from feeling monotonous and
    follows the Z reading path.

[The Visual Storyteller's Guide to Web UI Design; Clever Interactive
Techniques for Web Storytelling; Web UI Design for the Human Eye; Zen of
White Space: Space, Ratios, Minimalism]

## 11. Style guides

1. **Write down every decision you want repeated.** Consistency that lives
   only in someone's head will not survive the next contributor.
2. **Pick the right kind of guide for the stage.** Mood board (feel only),
   style tile (colors, type and sample elements without layout), brand guide
   (logo, color, voice), front-end guide (components and code).
3. **Cover these sections.** Purpose and personality; layout and grid with
   exact margins and gaps; type with a size and font for every text role;
   color with exact values and which color is for what; media treatment
   (aspect ratios, captions, spacing); logo usage with dos and don'ts;
   navigation; icons; UI patterns; writing voice; code snippets.
4. **Show each style in itself.** Render the H1 example in the H1 style.
   That gives the rule and a visual check at once.
5. **Give colors roles, not just values.** "Accent: buttons and links only"
   prevents misuse better than a list of hex codes.
6. **Document motion too.** Durations, easing, and when to animate. Include
   live previews, because motion cannot be shown in a static page.
7. **Explain the why.** A guide that says why a tab layout is used in one
   place and a scroll layout in another lets people make the next call.
8. **Fix the vocabulary.** Agree what "card", "tile" and "module" mean so
   design and code use the same names.

[The Critical Components of Web UI Style Guides; Style Guides: An Overview
for Modern Designers; Color Theory in Web UI Design]

## 12. Core principles worth keeping from About Face

- Less interface is better, no matter how clever it is.
- Remove elements until the design breaks, then put the last one back.
- Show what with visuals; say which with text.
- Visually separate things that behave differently.
- Use links to navigate and buttons to act.
- Tell the user when the product is busy or not responding.
- Make scrolling an engaging experience. Keep headers in place to hold
  context on long pages.
- Infinite scroll and a site footer cannot coexist. Pick one.
- Do not make the user feel stupid. Treat users as smart and busy.

[About Face 4: The Essentials of Interaction Design, Appendix A and ch. 17]

---

## Dated advice to ignore

These books are from 2014 to 2016. Some of their advice no longer holds.

- **Body text at 12 to 14px.** A 2014 survey reported this as the norm.
  Use 16px or more today.
- **Ghost buttons for the main action.** Outline-only buttons were trendy,
  but they read as secondary and are easy to miss. Use them only for
  secondary actions.
- **Flat design as an absolute.** Removing all depth cues made it hard to
  tell what is clickable. Subtle shadows and clear button shapes are back
  for good reason.
- **Long shadows, trendy "flat UI" palettes, and Metro-style tiles.** Fashion
  of the period. They date a page instantly.
- **Parallax and scroll-jacking on every section.** These hurt performance,
  accessibility, and motion-sensitive users. Use scroll effects sparingly and
  respect reduced-motion settings.
- **Autoplay HD background video as a default hero.** Costly on mobile data
  and battery, and often blocked. Treat it as the exception.
- **Hamburger menus on desktop.** Hidden navigation is used less. Show
  primary navigation when there is room.
- **Pinterest-clone pin layouts as a style choice.** The books themselves
  call this overused. Use masonry only when item heights truly vary.
- **Thin, light-weight body fonts for elegance.** They fail contrast and
  render badly on many screens.
- **Color "psychology" as hard fact.** Color associations vary by culture
  and context. Use them as a tendency, and test.
- **Gamification as a default growth tactic.** Points and badges fit some
  products. On most sites they add noise.
- **Contrast judged by eye only.** The books never mention accessibility
  contrast checks. Check text against WCAG ratios: 4.5:1 for body text and
  3:1 for large text and UI parts.

---

## Quick critique checklist

- [ ] One clear focal point on each screen.
- [ ] At least three distinct type levels, and body text 16px or more.
- [ ] Line height near 1.5, line length near 60 to 70 characters.
- [ ] Related items close together, unrelated groups clearly apart.
- [ ] A dominant color, a secondary, one accent. Accent used only for action.
- [ ] The layout still works in grayscale.
- [ ] Same word, color, and position for the same thing everywhere.
- [ ] Cards: one action each, image 50 to 75%, whole card clickable,
      equal gaps.
- [ ] Every action gives visible feedback within 0.1 seconds.
- [ ] Touch targets at least 44 x 44px.
- [ ] Motion eases in and out; no auto-rotating carousel.
- [ ] A long page has a clear beginning, middle, and end, with the action
      at the end.
- [ ] Empty states designed, not left blank.
- [ ] Text contrast checked against WCAG ratios.

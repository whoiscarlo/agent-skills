---
name: ux-laws
description: Use when designing, building, or reviewing any UI (web pages, app screens, forms, navigation, onboarding, checkout, dashboards, landing pages) to apply the classic laws of UX as concrete build rules. Covers 26 laws in 5 groups (choice and memory, targets and speed, grouping and perception, attention and emotion, complexity and robustness), each with a rule, numbers to build to, and a review check. Also triggers on "UX laws", "Hick's law", "Fitts's law", "Jakob's law", "Miller's law", "Doherty threshold", "Von Restorff", "peak-end", "Tesler's law", "Postel's law", "Gestalt".
---

# UX Laws

The laws of UX as build rules. Each law has: **the rule**, why it holds, what to
build (with numbers where they exist), and a **check** to run in review.

Source: the laws are collected and named on Jon Yablonski's *Laws of UX*
(lawsofux.com) and in the original research each law cites. Wording here is my
own.

## How to use this skill

- **Building:** before writing a screen, read the group headings below and ask
  which laws the screen touches. Most screens touch 5 to 8.
- **Reviewing:** run every **Check** line against the screen. Report failures
  as "Law: what is wrong, where, the fix".
- These laws pull against each other sometimes (Hick wants fewer choices,
  Jakob wants the familiar full menu). When they conflict, the user's main task
  on that screen wins.
- Pair with `usability-principles` (Krug and Norman) for page-level review and
  `refactoring-ui` for visual polish.

---

## Group 1: Choice and memory

### 1. Hick's law
**Rule: The more options you show at once, the longer the decision takes.**
Why: decision time grows with the number and complexity of choices.
Build:
- One primary action per screen. Everything else is visually quieter.
- Top navigation: 5 to 7 items. Move the rest into a "More" menu or footer.
- Long lists of options: add search, filters, or a "recommended" pick on top.
- Onboarding: one question per step, not one long form.
**Check:** Count the clickable choices above the fold. More than about 7 that
look equally important is a failure.

### 2. Miller's law
**Rule: People hold only a few items in working memory, so chunk information.**
Why: the classic figure is 7 plus or minus 2; newer research says closer to 4.
Build:
- Group long content into chunks of 3 to 5 (form sections, settings groups).
- Format long numbers: `+44 7700 900 123`, card numbers in 4s.
- Never make the user remember something from a previous screen. Show it.
**Check:** Any form or list with more than 7 ungrouped items fails.

### 3. Recognition over recall
**Rule: Show the options. Do not make people remember them.**
Why: recognizing a choice is far easier than pulling it from memory.
Build:
- Recent searches, recent items, and autocomplete.
- Visible labels next to icons. Icon-only buttons only for universal icons
  (close, search, menu).
- Placeholders are not labels. Keep a visible label above every input.
- Show the current value in dropdowns and filters.
**Check:** Is there any step where the user must type or recall something the
app already knows? Fix it.

### 4. Progressive disclosure
**Rule: Show the basics first. Reveal advanced options only when asked.**
Why: it cuts the choices on screen (Hick) without removing power.
Build:
- "Advanced settings" collapsed by default.
- Short summary cards that expand to detail.
- Multi-step forms instead of one long page.
- Do not hide things people need often. Disclosure is for the rare 20%.
**Check:** Does the first view show only what most users need for the main
task?

### 5. Zeigarnik effect
**Rule: People remember unfinished tasks, so show what is left to do.**
Why: an open task nags at memory until it is closed.
Build:
- Profile or setup completeness bars ("3 of 5 done").
- Checklists for onboarding that stay visible until finished.
- Save drafts and show "You have an unfinished draft" on return.
**Check:** If a user leaves halfway, does the app show them where they stopped?

### 6. Serial position effect
**Rule: People remember the first and last items in a list best.**
Why: primacy and recency. The middle gets lost.
Build:
- Put the most important nav items first and last (Home first, Profile or
  Cart last).
- On landing pages, put the strongest point first and the call to action last.
- Do not bury the key option in the middle of a long list.
**Check:** What is in the middle of each list? It should be the least
important items.

---

## Group 2: Targets and speed

### 7. Fitts's law
**Rule: Bigger and closer targets are faster and easier to hit.**
Why: time to reach a target depends on its distance and size.
Build:
- Touch targets at least 44 by 44 px (Apple) or 48 by 48 dp (Android).
- At least 8 px between neighbouring targets.
- Make the whole card or row clickable, not just the small link text.
- Put the primary button where the thumb or cursor already is: bottom of the
  screen on mobile, right after the last form field on desktop.
**Check:** Measure the smallest tappable thing. Under 44 px fails.

### 8. Minimize target distance
**Rule: Keep the next action close to where the eye and hand already are.**
Why: the distance half of Fitts's law. Every trip across the screen costs time.
Build:
- Submit button directly under the last field, not in a far corner.
- Related actions next to the item they act on (edit icon on the row).
- On mobile, primary actions in the bottom third (thumb zone).
**Check:** Trace the path through the main task. Any big jump across the
screen between steps is a failure.

### 9. Doherty threshold
**Rule: Respond in under 400 ms, or show that something is happening.**
Why: when the system answers within about 0.4 s, people stay in flow.
Build:
- Visual response to every press within 100 ms (pressed state, ripple).
- Optimistic updates: show the change at once, sync in the background.
- Skeleton screens for loads over about 400 ms. Progress bars over about 2 s.
- Prefetch the likely next page.
**Check:** Click every button. Anything with no visible reaction under 400 ms
fails.

### 10. Goal-gradient effect
**Rule: People speed up as they get closer to a goal.**
Why: visible progress pulls people forward.
Build:
- Progress indicators on multi-step flows ("Step 2 of 3").
- Start progress above zero where honest ("Account created: 20% done").
- Keep flows short so the end is in sight.
**Check:** In every flow over 2 steps, can the user see how far they are from
done?

### 11. Parkinson's law
**Rule: A task expands to fill the time allowed, so make tasks take less.**
Why: give people a long form and they spend long on it, or quit.
Build:
- Autofill (`autocomplete` attributes), saved details, one-tap sign in.
- Smart defaults so most fields need no change.
- Ask only for what you need now. Ask the rest later.
**Check:** Time the main task. Every field you can remove or prefill is a
failure until it is.

---

## Group 3: Grouping and perception (Gestalt)

### 12. Law of proximity
**Rule: Things close together look related.**
Build:
- Space inside a group smaller than space between groups. A good ratio is 1 to
  2 or more (8 px within, 24 px between).
- Labels closer to their own input than to the input above.
**Check:** Squint at the screen. Do the blobs you see match the real groups?

### 13. Law of similarity
**Rule: Things that look alike are seen as the same kind of thing.**
Build:
- All links one style. All primary buttons one style. Never style a
  non-clickable thing like a clickable one.
- Same type of content, same card design.
**Check:** Are there two elements that look the same but behave differently?
Fail.

### 14. Law of common region
**Rule: Things inside the same border or background look like a group.**
Build:
- Cards, panels, and tinted sections to group related content.
- Do not box everything. Use regions only where grouping matters.
**Check:** Does each card or panel hold exactly one idea?

### 15. Uniform connectedness
**Rule: Things joined by a line, colour, or frame look more related than
things that are only close.**
Build:
- Steppers with connecting lines, timelines, breadcrumbs.
- Selected states that visually join a tab to its panel.
**Check:** Where items are a sequence or a set, is that shown by a visual link?

### 16. Law of Pragnanz (simplicity)
**Rule: People read complex shapes as the simplest form they can.**
Why: the brain prefers the least effort reading.
Build:
- Simple shapes, icons, and layouts. Clear alignment on a grid.
- Fewer competing visual styles on one screen.
**Check:** Can someone describe the layout in one sentence after a 5 second
look?

### 17. Visual hierarchy
**Rule: Size, weight, colour, and position tell people what to read first.**
Build:
- One clear H1. Headings visibly bigger than body (a type scale like 1.25).
- Primary button filled, secondary outline, tertiary text only.
- De-emphasize secondary info with lighter colour, not just smaller size.
**Check:** Blur the screen. The first thing you see should be the most
important thing.

---

## Group 4: Attention and emotion

### 18. Aesthetic-usability effect
**Rule: People think good-looking designs are easier to use, and forgive small
problems in them.**
Why: looks set trust before the first click.
Build:
- Consistent spacing, alignment, and type. Polish is not optional.
- But do not let looks hide real usability problems in testing: users praise
  pretty screens even when they struggle.
**Check:** Does the screen look finished: aligned edges, even spacing, no
default browser styles?

### 19. Von Restorff effect (isolation)
**Rule: The one thing that looks different gets noticed and remembered.**
Build:
- Make the primary call to action the only element in the accent colour.
- Highlight the recommended pricing plan.
- Use it sparingly. If everything stands out, nothing does.
- Do not rely on colour alone (accessibility): also use size, weight, or an
  icon.
**Check:** Is there exactly one standout element per view, and is it the right
one?

### 20. Peak-end rule
**Rule: People judge an experience by its best or worst moment and its end.**
Build:
- Make the success screen feel good: clear confirmation, what happens next,
  maybe a small delight.
- Find the worst moment (errors, waits, payment) and soften it with clear,
  kind messages.
- Empty states that help instead of blank pages.
**Check:** What does the user see at the end of the main flow? Is it better
than a plain "Success"?

### 21. Feedback loops
**Rule: Every action should get a visible, immediate response.**
Why: without feedback, people repeat the action or assume it failed.
Build:
- Hover, focus, pressed, loading, success, and error states for every
  interactive element.
- Inline form validation after the user leaves a field, not on every keystroke.
- Toasts or inline confirmation after saves. Undo for destructive actions.
**Check:** For every button: what does the user see while it works, when it
succeeds, and when it fails? All three must exist.

---

## Group 5: Complexity and robustness

### 22. Jakob's law
**Rule: Users spend most of their time on other sites, so they expect yours to
work the same way.**
Build:
- Logo top left links home. Search top right. Cart icon top right.
- Standard patterns for login, checkout, settings. Do not reinvent them.
- Be different in the brand and content, not in the controls.
**Check:** Would a first-time user know where to find login, search, and help
without looking?

### 23. Tesler's law (conservation of complexity)
**Rule: Every system has some complexity that cannot be removed. Move it from
the user to the system.**
Build:
- Detect country, currency, and timezone instead of asking.
- Parse messy input (dates, phone numbers) instead of demanding one format.
- Do the hard work in code so the user's step is simple.
**Check:** Is the user doing any work the app could do for them?

### 24. Postel's law (robustness)
**Rule: Be liberal in what you accept, conservative in what you send.**
Build:
- Accept phone numbers with or without spaces, emails with trailing spaces,
  dates in several formats. Normalize on the way in.
- Output clean, consistent formats.
- Layouts that survive long names, missing images, and translated text.
**Check:** Type a valid value in an unusual format. Does the form reject it?
Fail.

### 25. Occam's razor
**Rule: Among designs that work equally well, pick the simplest.**
Build:
- Remove any element that does not help the main task. Then remove one more.
- Fewer fonts, colours, and component variants.
**Check:** For each element, ask "what breaks if I delete this?" Nothing means
delete it.

### 26. Pareto principle (80/20)
**Rule: About 80% of use comes from about 20% of features. Design for that 20%.**
Build:
- Find the top tasks (analytics, or ask) and make them the fastest path.
- Put the rarely used 80% of features behind menus or settings.
**Check:** Are the top 3 user tasks reachable in one tap or click from the home
screen?

---

## Quick review checklist

Run in this order on any screen:

1. Blur test: is the most important thing seen first? (Visual hierarchy, Von
   Restorff)
2. Count choices above the fold. Over about 7? (Hick)
3. Smallest touch target at least 44 px? (Fitts)
4. Every button has loading, success, and error states? (Feedback, Doherty)
5. Groups match spacing? (Proximity, Common region)
6. Standard patterns for nav, login, checkout? (Jakob)
7. Forms: fewest fields, autofill, forgiving input? (Parkinson, Tesler,
   Postel)
8. Multi-step flows show progress? (Goal-gradient, Zeigarnik)
9. The end of the flow feels good? (Peak-end)
10. Anything you can delete? (Occam, Pareto)

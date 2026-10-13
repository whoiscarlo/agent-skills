---
name: landing-conversion-ux
description: Use when designing or reviewing landing pages, sign-up and lead-capture forms, CTAs, value propositions, social proof, or planning UX research and testing for a web product. Gives concrete, testable rules for above-the-fold clarity, single-goal pages, short forms, honest trust signals, page flow, common design mistakes, and how to measure and test changes without fooling yourself.
---

# Landing Page Conversion and UX

Rules for pages whose job is to get one action taken: sign in, sign up, leave
an email, request something. Distilled from a shelf of marketing, conversion
and UX ebooks (UserTesting, UXPin, SmartBug, Usabilla and others, roughly
2014 to 2016). The numbers they quote are old. The behavior behind them is not.

Each rule is an instruction, a short reason, and an example. For a review,
start with the checklist at the end.

---

## 1. Value proposition and above the fold

1. **Pass the five-second test.**
   Why: visitors decide in a few seconds whether a page is for them. If they
   cannot say what you do by then, they hit Back.
   Example: show the page to someone for five seconds, hide it, and ask
   "what is this and who is it for?" If they cannot answer, rewrite the
   headline before touching anything else.

2. **Write the headline about the visitor's result, not about you.**
   Why: a page that talks about "we" makes the reader do the translation.
   "You" and a concrete outcome do it for them.
   Example: "We curate marketing emails" becomes "See how 400 brands write
   their emails, sorted and searchable."

3. **Back the headline with two or three concrete reasons to act.**
   Why: the headline motivates; the reasons convert the people who are on
   the fence.
   Example: under the headline, three short lines: "New brands every week",
   "Full emails, not thumbnails", "Free to browse".

4. **Show the real thing, not a stock photo.**
   Why: generic imagery reads as filler and makes the page look less
   trustworthy. A screenshot of the product proves it exists.
   Example: replace a smiling-team photo with a real grid of archived emails.

5. **Let the first screen state the offer, then let people scroll.**
   Why: the hero must carry the value proposition and the main action, but
   cramming every feature above the fold creates clutter. People scroll when
   the hierarchy is clear.
   Example: hero holds headline, subline, one button, and a product preview.
   Features, proof and FAQ live below.

6. **Design the small screen first.**
   Why: the phone layout forces you to rank content. What survives on mobile
   is what matters, and the desktop version grows from it cleanly.
   Example: wireframe the 375px version with only headline, button and one
   proof line, then widen until there is too much empty space and add the
   next item.

7. **Keep the hero fast.**
   Why: delays over about one second make people feel out of control, and
   slow pages lose both visitors and search ranking.
   Example: one compressed preview image, no autoplaying video, no slider.

[Sources: Inbound Marketing's Most Wanted 33 Website Design Crimes;
Lead Generation Techniques for High Conversions and Great UX; The Elements of
Successful UX Design; Timeless UX Design Trends: Responsive and Adaptive;
Responsive Web Design Best Practices]

---

## 2. Calls to action

1. **Give a landing page one goal and one primary CTA.**
   Why: every extra action competes with the one you want. A page that asks
   people to watch a video, read six testimonials and then fill a form loses
   them along the way.
   Example: one "Open the archive" button, repeated at the top and bottom,
   and nothing else styled as a button.

2. **Label the button with what happens next.**
   Why: "Submit" and "Click here" describe the mechanism, not the reward.
   A verb plus the thing makes the goal of the page obvious.
   Example: "Submit" becomes "Request this brand"; "Sign in" becomes
   "Open the archive".

3. **Say what the visitor gets before they commit.**
   Why: people ask "what am I trading my email for?" Answer it with copy and,
   when possible, a picture of the result.
   Example: next to a gated button, a line like "Free. Sign in with Google.
   Takes ten seconds." and a preview of the archive behind it.

4. **Make the CTA stand out through contrast, not loudness.**
   Why: a saturated button on a calm page draws the eye. A garish color that
   clashes with the brand cheapens the whole site.
   Example: keep surrounding UI desaturated and give only the primary button
   the brand's strongest color.

5. **Only buttons should look like buttons.**
   Why: boxed text or fake buttons that do nothing waste clicks and teach
   people to distrust the rest of the page.
   Example: do not put a bordered pill around "400+ brands"; style it as a
   label or plain text.

6. **Make tap targets big and well spaced.**
   Why: fingers are less precise than cursors. Small or crowded targets cause
   mis-taps and double taps.
   Example: at least 44 by 44 points for the main button, with clear space
   from the nearest link.

7. **Do not hide anything important behind hover.**
   Why: touch screens have no hover. Information that only appears on
   mouseover is invisible to phone users.
   Example: show the "what you get" note under the button, not in a tooltip.

8. **Offer a softer path for people who are not ready.**
   Why: most visitors are not ready for the main action on their first visit.
   A secondary, lower-commitment option keeps them from leaving empty-handed,
   but it must stay visually secondary.
   Example: a text link "or get an email when new brands land" under the
   main button.

[Sources: 33 Website Design Crimes; The Elements of Successful UX Design;
Designing Better UX with UI Patterns; Responsive Web Design Best Practices;
Timeless UX Design Trends: Responsive and Adaptive]

---

## 3. Lead capture and sign-up forms

1. **Ask only for what you will use right now.**
   Why: every field lowers completion. In one test, cutting a form from 11
   fields to 4 raised sign-ups by well over 100% with no drop in lead quality.
   Example: a "request the next brand" form needs a brand name and an email.
   Not a name, not a company, not a phone.

2. **Remove fields that confuse.**
   Why: one ambiguous field can sink a form. A famous case removed a single
   optional "Company" field that people misread and gained millions in
   revenue.
   Example: if you add "Website" to the brand request, people may not know
   whether you mean their site or the brand's. Drop it or label it exactly.

3. **Collect more later, not all at once.**
   Why: asking a little at each visit (progressive profiling) gets more
   completions and cleaner data than one long form people fill with junk.
   Example: first request asks for email only; a later email asks "what
   industry are you in?"

4. **Accept input in any reasonable format.**
   Why: rejecting "Nike.com" because you wanted "Nike" punishes the user
   for your parser. Clean it up on the server.
   Example: trim spaces, strip "www." and ".com", match case-insensitively.

5. **Put the form next to the value it unlocks.**
   Why: a form that sits right after useful content converts far better than
   a generic sidebar box people have learned to ignore.
   Example: place "Missing a brand? Request it" right under the archive
   preview, not in the footer.

6. **Keep sign-in and sign-up visually distinct.**
   Why: when the two forms are stacked, many new visitors start filling the
   wrong one.
   Example: one "Continue with Google" button that handles both cases, or
   two clearly separated panels.

7. **Give a show-password toggle and a visible "forgot password" link.**
   Why: mistyped passwords on mobile push people into reset emails that take
   them out of the flow.
   Example: an eye icon in the password field; the reset link right under it.

8. **Confirm success on the page, in plain words.**
   Why: people need to know the form worked and what happens next.
   Example: "Got it. We'll email you when Glossier is in the archive."

9. **Explain what you do with the email in one short line.**
    Why: privacy worry is a common reason people stop at the last field.
    Plain language beats a link to legal text.
    Example: "One email when your brand is added. No newsletter unless you
    ask."

[Sources: 3 Common UX Mistakes Killing Good Design; 33 Website Design Crimes;
The Elements of Successful UX Design; Lead Generation Techniques for High
Conversions and Great UX; Designing a Checkout Flow That Converts (form rules
only)]

---

## 4. Social proof and trust

1. **Use real numbers when you have them.**
   Why: people trust hard numbers more than adjectives.
   Example: "2,140 emails from 312 brands" beats "a huge library".

2. **Attribute every testimonial to a real person.**
   Why: a name, role and photo make a quote relatable. An anonymous quote
   reads as invented.
   Example: "Saved me hours on our welcome series." Priya S., lifecycle
   marketer at a DTC brand, with headshot.

3. **Show recognizable logos quietly.**
   Why: credibility by association works, but colorful logos compete with the
   CTA.
   Example: a single row of grayscale brand logos just below the hero.

4. **Place proof where the doubt arises.**
   Why: a testimonial halfway down the page, next to the claim it supports,
   does more than a wall of quotes at the end.
   Example: after "full emails, not thumbnails", a quote from someone who
   used the full-size view.

5. **Test social proof instead of assuming it helps.**
   Why: subscriber counts sometimes lower conversion, especially when the
   number is small.
   Example: A/B test the hero with and without "Join 800 marketers".

6. **Earn trust with polish and honesty.**
   Why: visual quality is the first thing people use to judge credibility.
   Typos, broken buttons and messy alignment all read as "not legit".
   Example: proofread every string, click every link before launch.

7. **Never use dark patterns.**
   Why: tricks like hidden opt-ins or hard-to-find cancel links win once and
   lose the user forever.
   Example: an unchecked, clearly labeled "Also send me the weekly digest"
   box, never a pre-checked one buried in fine print.

8. **Be upfront about cost and terms.**
   Why: people prefer seeing the price early, and "free" claims that turn out
   conditional destroy trust.
   Example: if browsing is free but downloads are paid, say so on the
   landing page, not after sign-in.

[Sources: The Elements of Successful UX Design; Lead Generation Techniques for
High Conversions and Great UX]

---

## 5. Page flow and structure

1. **Map the path before designing the page.**
   Why: without a planned "what do they do next", pages turn into dead ends.
   Example: write it out: land, read headline, see preview, click "Open the
   archive", sign in, land inside the archive.

2. **Remove the main navigation from single-goal landing pages.**
   Why: every nav link is an exit from the offer.
   Example: logo plus one CTA in the header, no "Blog / About / Pricing"
   menu.

3. **Never put a splash page in front of the real page.**
   Why: it adds a step and tells the visitor nothing.
   Example: no "Enter site" gate. The landing page is the front door.

4. **Make every page end with a next step.**
   Why: a page that just stops leaves the visitor to hunt. If they cannot find
   where to go within a few seconds, they leave.
   Example: the FAQ ends with the same CTA as the hero.

5. **Write for scanners.**
   Why: most people read headings, subheadings and first sentences only.
   Example: short paragraphs, clear subheads, bullet lists for features.

6. **Group and space content to cut cognitive load.**
   Why: white space improves comprehension, and chunking related items lets
   people absorb more without removing anything.
   Example: group features into three cards instead of nine loose lines.

7. **Use familiar patterns unless you have proof yours is better.**
   Why: recognizable patterns let people act without thinking. Breaking them
   forces learning and causes errors.
   Example: put sign-in at the top right, not in a hidden gesture. If your
   rule for a pattern needs "unless" or "except", that is the time to
   rethink it.

8. **Label links by what is behind them.**
   Why: clear labels give "information scent". Cute labels hide it.
   Example: "Browse brands", not "The good stuff".

9. **Meet basic accessibility.**
    Why: it is good UX for everyone, including people in bright sun or on a
    slow phone.
    Example: text contrast at least 4.5:1, body text at least 16px, line
    height around 1.5, real labels on form fields.

10. **Design empty and waiting states on purpose.**
    Why: a blank screen after sign-in looks broken. A clear empty or loading
    state tells people what to expect and keeps them feeling in control.
    Example: "Loading 2,140 emails..." with a skeleton grid, not a white
    page.

[Sources: 33 Website Design Crimes; 3 Common UX Mistakes Killing Good Design;
Designing Better UX with UI Patterns; The Elements of Successful UX Design;
Responsive Web Design Best Practices; Idiot Buttons: The Placebo in UX Design]

---

## 6. The design crimes to avoid

A quick list of the mistakes that most often sink a page. Each line says
what to do instead.

- **Sliders and carousels.** Very few people click slides after the first,
  and they slow the page. Show one strong image instead.
- **Autoplaying video or sound.** It startles people and they leave. Use a
  play button and let them choose.
- **Cheesy stock photos.** They look suspicious on a page that asks for
  data. Use real product shots.
- **Several competing CTAs on a landing page.** Pick one.
- **Default "Submit" buttons.** Rename to the action.
- **Forms longer than the offer is worth.** Cut to the minimum.
- **Clutter.** Every block should earn its place. Remove until it hurts.
- **Walls of text.** Break into headings, short paragraphs and bullets.
- **Low-contrast or tiny text.** Light gray on white fails readability.
- **CTAs unrelated to the page content.** A global sidebar offer that does
  not match the page converts poorly. Match the offer to the page.
- **Talking about yourself.** Swap "we" for "you" and the visitor's result.
- **Ignoring mobile until the end.** Retrofitting is slow and costly. Start
  with the phone.
- **Mistaking a pretty UI for good UX.** A beautiful page can still be
  confusing. Test the flow, not just the look.
- **Launching without analytics or a baseline.** Record visits and sign-ups
  before a redesign and keep tracking on after, or you cannot tell if it helped.
- **Treating launch as done.** A site is never finished. Plan the next round
  of tests on launch day.

[Sources: 33 Website Design Crimes; 3 Common UX Mistakes Killing Good Design;
The Elements of Successful UX Design]

---

## 7. Measuring and testing

1. **Set a specific numeric goal before you design.**
   Why: "more sign-ups" cannot be judged. "Raise archive sign-in rate from 4%
   to 6% in 60 days" can.
   Example: write the goal and the metric at the top of the design doc.

2. **Watch the side effects of the number you push.**
   Why: raising sign-ups can lower retention if you attract the wrong people.
   A single number means little alone.
   Example: track sign-in rate together with 7-day return rate.

3. **Use analytics to find where, then user tests to learn why.**
   Why: analytics shows what is happening; only watching people shows why.
   Example: if most visitors leave the landing page without clicking, run
   five short sessions asking people to think aloud on that page.

4. **Start tests where real visitors start.**
   Why: people arrive from ads, social posts and search with different
   expectations. Starting a test on the homepage hides that mismatch.
   Example: show a tester the tweet that drives traffic, ask what they
   expect, then send them to the page and ask if it matched.

5. **Judge bounce and exit rates against the page's purpose.**
   Why: a high bounce is fine on a page that answers one question. It is a
   problem on a page meant to lead somewhere.
   Example: high exit on the sign-in screen is urgent; high exit on a
   "thanks, request received" page is expected.

6. **Change one thing per A/B test.**
   Why: if the button text and the headline both change, you cannot tell
   which one moved the number.
   Example: test "Open the archive" against "Browse 2,000 emails" with
   everything else identical.

7. **Give tests time before reacting.**
   Why: day-one swings are noise. Teams that roll back after a bad first day
   miss real wins that show up by day seven.
   Example: commit to at least a full week, or enough traffic to reach your
   sample size, before deciding.

8. **Run usability tests before and after an A/B test.**
    Why: before, to find what is worth testing; after, to learn why the
    winner won.
    Example: five sessions on the current page, then the A/B test, then
    three sessions on the winner.

9. **Pick the research method for the question.**
    Why: each method answers a different question at a different stage.
    Example:
    - Is the page understandable? Remote unmoderated test, five people.
    - Why do people get stuck? Moderated session where you can ask follow-ups.
    - Which of two designs? Preference test, at most two designs per person,
      alternate the order, tasks first and opinions second.
    - Can people find things? Tree test on the text structure alone.
    - How should content be grouped? Open card sort early on.
    - What do people need at all? One-on-one interviews.
    - Which version converts better live? A/B test.

10. **Test on real phones.**
    Why: emulators hide tap-target, speed and keyboard problems.
    Example: run the sign-in flow on an actual mid-range Android phone on
    cellular data.

11. **Be data-informed, not data-driven.**
    Why: numbers point to problems but do not design the fix. Pair them with
    research and judgment.
    Example: a 12% dip in engagement after a change might be people finding
    things faster. Check with users before rolling back.

[Sources: Analytics + User Testing: The Secret Weapon of Conversion Rate
Optimization; UX Research Methodologies; The Field Guide to UX Strategy;
33 Website Design Crimes; 3 Common UX Mistakes Killing Good Design; Responsive
Web Design Best Practices]

---

## Dated advice to ignore

These books are from roughly 2014 to 2016. Skip or update these points.

- **"Red, orange and dark blue convert best" and "use the word Cart".** One
  vendor's e-commerce data. Button color matters only as contrast with your
  own palette.
- **"Tell users whether the username or the password was wrong."** This
  leaks which accounts exist. Use one generic "email or password is
  incorrect" message.
- **Social login lists led by Google+ and Yahoo.** Those are gone or
  irrelevant. Today it is Google and Apple, plus email.
- **Placebo buttons and fake "personalizing your feed" waits.** The control
  idea is sound, but a fake loading screen is a small deception. Give real
  feedback instead.
- **"Mobile-friendly penalty" urgency and m-dot sites.** Responsive layout is
  simply the default now.
- **Exact touch sizes in points from old Apple guidance.** Still a good
  floor, but check current platform guidance (roughly 44 to 48 pixels).
- **"Web design is dead, buy a theme."** The point that templates beat
  hand-built pages for most small businesses still holds for speed and
  basics, but a template does not write your value proposition.
- **Content upgrades and "squeeze pages" framed for blogs.** The principle
  (offer something specific to what the reader is looking at) holds; the
  blog-sidebar framing does not.

---

## Review checklist

Before shipping a landing page, confirm:

- [ ] A stranger can say what it is and who it is for after five seconds
- [ ] One primary CTA, labeled with the action and the reward
- [ ] Nothing else on the page looks like a button
- [ ] The cost and what happens after the click are stated near the CTA
- [ ] Forms ask only for what is used now; success message is plain
- [ ] Proof uses real numbers or named people, placed near the claim
- [ ] No slider, no autoplay, no stock-photo hero
- [ ] Main nav removed on single-goal pages; every page ends in a next step
- [ ] Works on a real phone: 44px+ targets, no hover-only info, fast hero
- [ ] Contrast 4.5:1, body 16px+, labeled form fields
- [ ] Analytics in place, baseline recorded, one numeric goal written down
- [ ] First A/B test planned with one variable and at least a week to run

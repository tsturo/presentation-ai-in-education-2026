# The Grand Compromise — Education in the Age of AI
## Presentation Design Document

**Date:** 2026-06-10
**Author:** Tomek (architect/developer, associate professor — teaches OOP in Python)
**Status:** Revised after three-perspective review (craft, fact-check, audience skeptics)

---

## 1. Goal and context

A 20–30 minute talk about whether the way we educate children and university students is still relevant in the AI era. The talk traces the historical roots of current education principles, shows why they exist, and examines which of them AI has invalidated.

- **Audience (mixed):** university students, the dean, company coworkers (software engineers at Visma).
- **Spoken language:** Lithuanian. **Slides and speaker notes:** English. Slides must be self-explanatory enough to follow visually without understanding the speech.
- **Speaker's credibility angle:** lives on both sides — works daily with agentic AI as a software architect, and teaches OOP in Python at university. The OOP course appears as one concrete example among many (not the running frame).

## 2. Core thesis

> **The goals of education were never wrong. The methods were a compromise forced by scarcity. AI removes the scarcity, so the methods — not the goals — must change.**

Tone: between "balanced critique" and "optimistic enabler." Critical of methods, optimistic about goals. Constructive framing keeps the dean engaged rather than defensive.

The talk ends with **open discussion questions and brief sketches of what could change — explicitly no prescribed solutions.**

**Claim discipline (from review):** make mechanism-specific claims, not death claims. "Unsupervised assessment no longer proves authorship" — not "exams are dead." The talk's confidence must be amortized over claims it can defend in front of academics.

## 3. Narrative arc: "The Grand Compromise"

Education as we know it is not the ideal — it is a cost-optimization. Every familiar institution (the lecture, the age cohort, the standardized exam) is a compromise forced by a specific scarcity. Bloom (1984) tried to measure what the compromise costs. AI removes the underlying scarcity — and in doing so breaks the compromise's *unsupervised* load-bearing mechanisms (homework, take-home projects), while making in-person assessment and human judgment more load-bearing, not less.

## 4. The live demo frame — the agent as a recurring character

The talk is wrapped in a live agentic demo. Crucially (review consensus): the demo must not only show commoditized production — it must **demonstrate the scarce skills the talk claims now matter**. The agent is a recurring character, not a bookend.

- **Minute 1 (Kickoff, one keystroke):** pre-staged terminal, spec pre-loaded; the speaker only hits Enter on screen. No live typing or pasting. **Inoculation line (10 s):** *"Note what I'm handing it: a complete specification with its own test suite — the most agent-friendly input that exists. Real work never gives you this. Remember that for later."* Step text: *"While we talk, something is working."*
- **Mid-talk callback (step 9):** one verbal callback without showing the terminal — "by the way, it's still working back there." A subtle blinking-cursor motif lives at the edge of the canvas fracture zone throughout. Do **not** show the terminal mid-talk (would spoil the reveal). Speaker has a glanceable status on the presenter laptop to know which ending he's walking into.
- **~Minute 20 (Reveal, hard cap 3 min + verification beat ~2 min):** switch to terminal. Run one command whose success is legible in seconds — the green test suite. Show the numbers step: *"Semester project: X minutes, ~$Y."* Beat of silence. **First sentence after the silence pivots immediately:** "So — did anyone learn anything in those 25 minutes? The agent didn't. And neither did you."
- **The verification beat (the talk's true climax):** the speaker reviews the agent's output live, as a trained eye, and finds something real — a design smell, an SRP violation, an edge case the test suite doesn't cover, a test passing for the wrong reason. (Rehearse to find one; plant ambiguity in the spec if needed. If nothing is found live, say so honestly and discuss what it would take to *trust* the code — still a verification beat.) Then: *"The agent did the semester project in 25 minutes. What you just watched me do in 90 seconds — that's the part you're here to learn. And notice: the agent couldn't grade itself."*
- **Demo run conditions:** agent runs fully autonomous in a sandboxed repo with pre-approved permissions — verified in rehearsal to complete with zero interaction. **Fallback:** pre-recorded screen capture of the same run; the agent-as-character framing survives on the recording because the audience's relationship with it was built throughout.
- **Assignment choice:** a real OOP coursework task with a test suite.

## 5. Step-by-step content plan (~15 steps, 25-minute spoken target)

### Act 0 — The Kickoff (2 min, hard cap, scripted)
1. **Title → terminal → Enter → inoculation line → back to canvas.** *"While we talk, something is working."* Do not explain what an agent is — mystery is the point.

### Act I — The compromises (8 min)
2. **The hook (1.5 min + 0.5 min "ideal" beat).** Present room, present tense: "Look around. Why are you sitting like this — this room, this hour, all at the same pace?" The answer isn't pedagogy. It's economics. Fold in the 30-second beat: for most of history real education was a personal philosopher for a prince and a handful of companions (Aristotle at Mieza with Alexander) or a master and an apprentice — the ideal existed, and only the elite could afford it.
3. **Compromise #1: scarce books → the lecture (1.5 min).** "Lecture" literally means *a reading*: hand-copied books were scarce, so the master read the authoritative text aloud and commented while students wrote. The book-dictation function died with Gutenberg (~1450); the format has outlived the printing press by over five centuries on inertia and economics. *Delivery: one vivid artifact — a manuscript's price in today's euros.*
4. **Compromise #2: scarce teachers → batch processing (1.5 min).** Open by debunking the myth for credibility: "You've heard schools were designed to make factory workers. Historians say that's invented — Prussia built its system before its factories, for literacy, loyalty, and citizenship. The truth is more interesting: it was batch processing by necessity. One scarce trained teacher, thirty children, one fixed pace." Age cohorts, fixed curriculum, standardized progression — still the chassis of schools and most universities. (Covers the children's-schooling sweep.) *Delivery: a question to the room.*
5. **Compromise #3: scarce assessment capacity → the standardized exam (1.5 min).** From imperial China's keju to Horace Mann replacing oral exams with written ones in Boston (1845) — explicitly to compare many students objectively at once. Batch assessment; grades as lossy compression of a human; the diploma as a trust signal (signaling theory gives this academic cover). *Delivery: fastest of the three — escalating tempo.*
6. **An honest beat: it worked (1.5 min).** Mass literacy, social mobility, the modern world. The compromise was the right trade *for its century*. (First full zoom-out — the audience sees the whole timeline at once. This step keeps the dean on side.)

### Act II — The measurement and the break (6 min)
7. **Bloom's 2-sigma problem, honestly told (2 min).** 1984: Bloom reported tutored students with mastery learning scoring ~2 SD above conventional classrooms — and concluded tutoring was "too costly for most societies to bear at scale." Honest footnote, stated on stage: the full 2 sigma never replicated; modern meta-analyses put tutoring at ~0.3–0.8 SD — *which still makes it one of the largest reliable effects education research has ever found.* Translate the statistics: show two distribution curves, not a number. Engineer bonus: VanLehn 2011 — intelligent tutoring systems already statistically matched human tutors, pre-LLM. The point survives the footnote: we've always known 1-on-1 is better; it was unaffordable.
8. **What just became cheap (1.5 min).** Patient explanation in any style, instant feedback, plausible code, essays, a 24/7 tutor. The scarcity behind every compromise is evaporating. **Agent callback:** "It's still working back there, by the way."
9. **What breaks — precisely (1.5 min).** Every *unsupervised* assessment no longer proves authorship: homework, take-home essays, semester projects. The "plagiarism" category collapses (it assumed copying from humans). Consequence pointed the other way: in-person, oral, practical assessment becomes *more* load-bearing, not less. The degree signal: an open question, not a corpse.
10. **It's not autocomplete anymore (1 min, scripted to the sentence).** The agentic shift: an architect's day — decompose, delegate, review, verify. Lead with the bridge, don't save it: "the junior-dev-shaped hole in the org chart is also a student-shaped hole in the curriculum." Honest line for the engineers: *plausible* code became cheap; *working, maintained, in-production* code did not — the gap is where judgment lives.

### Act III — The reveal and the open end (9 min)
11. **THE REVEAL (3 min hard cap).** Terminal: green tests. Numbers step: *"Semester project: X minutes, ~$Y."* Silence. Then the immediate pivot line ("did anyone learn anything in those 25 minutes?").
12. **The verification beat (2 min).** Live code review; find the flaw; "this 90 seconds is what you're here to learn; the agent couldn't grade itself." (Details in §4.)
13. **What's scarce now (2 min, anchored to the artifact on screen).** Judgment, decomposition, verification, taste, asking the right question — each pointed at the demo, not delivered as abstractions. Bjork's desirable difficulties, precisely: the *specific* difficulties that make practice feel harder (retrieval, spacing) are what produce durable learning — and effortless fluency is the feeling of *not* learning. AI doesn't remove the need for effort; it makes skipping it frictionless. The era's meta-skill: outsourcing work without outsourcing understanding. For students, explicitly: the demo didn't make your six weeks worthless — it changed *which part* of those six weeks was the point.
14. **Sketches, not solutions (1.5 min).** Non-prescriptive: oral defense of AI-assisted work; "here's AI output — find the flaw" assignments; grading process instead of artifact; AI tutors for tutoring-level pacing with humans providing motivation and judgment. One honest line for the dean: every sketch re-spends scarce teacher time — *which is exactly why the cost collapse matters: it can fund expensive assessment by cheapening instruction.* (Acknowledge the real constraints exist: accreditation, qualification frameworks, integrity policy in the transition years.)
15. **Open questions + closing (1.5 min).** For discussion, no answers: What is a diploma proof of, now? Do we ban the tool or require it? What do we grade when output is free? If tutoring-level learning is finally affordable — why do we still lecture? Full zoom-out — the whole canvas in one frame — slow zoom to the center: *"The goals of education were never wrong. The methods were a compromise. The constraint behind the compromise is gone — so the only question left is the one we'll discuss now: what's our excuse?"* During discussion: leave the **static full-canvas view** on screen (no camera drift) so the audience can re-read the questions.

### Timing budget (25-min spoken target; 30-min slot leaves room for discussion)
| Act | Steps | Budget |
|---|---|---|
| Act 0 — Kickoff | 1 | 2 min |
| Act I — Compromises | 2–6 | 8 min |
| Act II — Measurement & break | 7–10 | 6 min |
| Act III — Reveal & open end | 11–15 | 9 min |

If the slot is 20 minutes: cut step 10 to one sentence inside step 9 and compress one compromise to a half-beat. Note: speaking Lithuanian over English slides runs ~10% slower than rehearsal — rehearse against 23 minutes.

## 6. Format: Prezi-style zoom canvas (impress.js)

One big canvas, steps positioned in 2D space, camera zooms/pans between them — the "zoom out to see the big picture of history" is the visual experience, not just a metaphor. Single self-contained HTML file, presentable offline from a browser.

### Spatial layout — FINAL: the Visma zoom canvas (supersedes the triptych below)
Built 2026-06-11 as `index.html` from the approved mockup (`mockups/E-visma-canvas.html`). One white dot-grid canvas, Visma branding (purple #7F56FA, Instrument Sans, real Visma + VilniusTech logos), three islands: creme PAST (five station cards as beads on a purple line: the tutor 343 BC → the lecture → the batch → the exam → the proof 1984), black BREAK (terminal, numbers, the snap/fall at TODAY in the Amplify gradient), dashed-outline FUTURE (proposed skills line: judgment · decomposition · verification · taste · curiosity + two open questions). 15 camera steps with progressive disclosure (details appear on arrival; story beats stay revealed), a deep dive *inside* the terminal for the verification beat, and a final full-canvas view for the discussion. Speaker cues live in the deck notes (press P) and `docs/speaker-script.md`.

### (Historical) Spatial layout — a V-shaped triptych (revised after visual review)
Three tinted region bands; the journey goes down into the break and climbs back up:
- **THE PAST (top-left band, warm ochre tint):** the timeline with era cards in a strict row — hook → lecture → batch school → exam machine — with line-art SVG illustrations (column, open book, bell, seal) between cards, and era ticks (Mieza 335 BC … Boston 1845) under the line. Bloom 1984 hangs above its tick on a dashed riser. "It worked" is the first zoom-out, framing the whole band.
- **TODAY · THE BREAK (bottom-center band, red tint, physically lower):** the timeline literally falls off a cliff at TODAY — a tall jagged crack drops to the break band, where a blinking green cursor (the agent-as-character motif) sits. Steps: what-became-cheap → what-breaks → agentic work → terminal reveal → verification.
- **THE FUTURE · UNDRAWN (top-right band, blueprint-blue tint, rising back up):** a dashed blue connector climbs from the break into a grid-paper region with a dashed line — what's-scarce → sketches → open-question cards scattered around.
- **Closing** sits centered below the triptych; the **finale** zooms out to the full V — past, fall, climb — and stays static during discussion.
All graphics are inline SVG line-art; the file stays fully self-contained/offline.

### Motion discipline
Mostly straight pans and zooms; rotation reserved for at most 2–3 deliberate moments. **Avoid long same-scale lateral pans between distant timeline stops** (the actual motion-sickness trigger) — arc out-and-in by varying step scale, or keep adjacent steps spatially close.

### Presenter tooling
impress.js console plugin (impressConsole): separate window with current/next step, speaker notes (English), timer. Requires one rehearsal. Navigation is linear (clicker/arrow keys); the spatial layout serves the audience's mental map.

### Why not reveal.js / Prezi
- Prezi.com: GUI SaaS, no usable authoring API — everything would be rebuilt by hand.
- reveal.js: better presenter view, but linear slides; the zoom-canvas format fits this talk's narrative better, and the speaker explicitly wants the Prezi-like experience.

## 7. Design quality bar
Distinctive visual design, not a default template: a coherent visual motif of "constraint → compromise" through Act I; canvas regions (timeline / fracture / undrawn future) styled as one continuous landscape. English text, large type, readable from the back of a lecture hall. Step 7 shows distribution curves, not raw statistics. The reveal-numbers step shows only the big figures (minutes, dollars) — raw terminal scroll is for the live terminal moment only, kept brief, with the green narrated aloud for non-engineers.

## 8. Anticipated hard questions (prep, not slides)
- **Dean:** "What should I change *next semester*, within accreditation and integrity policy, with zero extra headcount — and who is accountable when a student we certified can't work without the agent?" (Step 14's cost-shift line + honest "transition years are unsolved" is the prepared stance.)
- **Student:** "Inside *your own course*, this semester, the rational move you demonstrated is to let the agent do it. Are you telling us not to? Why struggle if the grade is the same?" (Verification beat + step 13's "which part was the point" is the prepared stance; be ready to say what changes in the course next term.)
- **Engineer:** "Your demo's input was a perfect spec with an acceptance test suite — the artifact our backlog never contains. Isn't the demo measuring exactly what you admit is still scarce? Would you merge that code?" (Inoculation line at kickoff pre-claims this; the verification beat answers "would you merge it.")

## 9. Open items
- [ ] Pick the actual coursework assignment for the demo; rehearse the autonomous run end-to-end (zero permission prompts); fill in real time/cost numbers on step 11.
- [ ] During rehearsal, identify the real flaw for the verification beat (or plant spec ambiguity that reliably produces one).
- [ ] Record the fallback screen capture of the same run.
- [ ] Decide speaker-notes language (default: English; Lithuanian on request).
- [ ] Rehearsal with impressConsole presenter window; confirm clicker navigation.
- [ ] Confirm slot length: is discussion inside the 30 minutes? (If yes, the 25-minute spoken version is mandatory.)

## 10. Fact-check record (claims verified 2026-06-10)
| Claim | Verdict | Phrasing used |
|---|---|---|
| Lecture = *lectura*, born of book scarcity | Solid; "only copy" was hyperbole | "scarce, hand-copied books"; reading + commentary |
| Prussian "factory school for industrial workers" | **Myth** (Watters, Dorn; system predates industrialization) | Debunked on stage; reframed as batch processing of scarce teacher time, motives = literacy/loyalty/citizenship |
| Bloom 2-sigma (1984) | Real citation; magnitude never replicated (0.3–0.8 SD: Cohen/Kulik 1982, VanLehn 2011, Nickow et al. 2020) | Stated with the honest footnote; arc survives at 0.8 |
| Aristotle tutored Alexander | Solid (Mieza, 343 BC; small group of companions) | "a prince and a handful of companions" |
| Lecture outlived printing press by 500 years | Solid (~575 years) | "over five centuries" |
| Desirable difficulties (Bjork) | Solid | Specific difficulties; fluency ≠ learning |
| "Exams are dead" | Overclaim | "Unsupervised assessment no longer proves authorship"; proctored/oral becomes more load-bearing |
| Exam origins = scarce grading time | Weak causal arrow | "Scarce assessment capacity → standardized batch assessment" (keju; Mann 1845) |

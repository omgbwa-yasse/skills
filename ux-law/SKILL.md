---
name: ux-law
description: Audits interfaces and drafts UX recommendations using the ten "Laws of UX" — Jakob's Law (familiarity/conventions), Fitts's Law (target size/distance), Miller's Law (chunking/working memory), Hick's Law (choice overload), Postel's Law (robustness/flexible input), Peak-End Rule (emotional highs and endings), Aesthetic-Usability Effect (perceived usability from beauty), Von Restorff Effect (visual distinctiveness/contrast), Tesler's Law (irreducible complexity), and Doherty Threshold (system response time under 400ms). Trigger this skill for any UX/UI review, heuristic evaluation, usability critique, design feedback, onboarding/checkout/form review, performance or loading-state review, or a request for UX recommendations, best-practice checks, or "why is this confusing/slow/hard to use" — even if the user never names a specific law. Also trigger when asked to connect design principles to psychological reasoning, or to think through the ethics of persuasive/attention-grabbing design patterns.
---

# Laws of UX

A toolkit of ten well-established UX/psychology principles, each with its
own detailed reference file covering the mechanism, a full audit
checklist, common mistakes in applying it, and how to phrase
recommendations. Use this skill to **audit** an interface, flow, or piece
of copy against these principles, to turn findings into **concrete,
prioritized recommendations**, to **map a team's design principle** to its
psychological rationale, and to flag **manipulative patterns** that
exploit these same principles against the user.

## The ten laws (quick index)

| Law | One-line test | Reference |
|---|---|---|
| Jakob's Law | Does this match conventions users already know from other products? | `references/jakobs-law.md` |
| Fitts's Law | Are targets big enough, close enough, and well-spaced? | `references/fitts-law.md` |
| Miller's Law | Is dense content chunked so it's scannable, not memorized? | `references/millers-law.md` |
| Hick's Law | Are choices presented progressively instead of all at once? | `references/hicks-law.md` |
| Postel's Law | Is input handling forgiving while output stays reliable? | `references/postels-law.md` |
| Peak-End Rule | Are the most intense moment and the final moment of the journey good? | `references/peak-end-rule.md` |
| Aesthetic-Usability Effect | Could visual polish be masking real usability problems in testing? | `references/aesthetic-usability-effect.md` |
| Von Restorff Effect | Does the one thing that should stand out actually stand out — without becoming ad-noise? | `references/von-restorff-effect.md` |
| Tesler's Law | Who is absorbing the irreducible complexity — the system, or the user? | `references/teslers-law.md` |
| Doherty Threshold | Does the system give feedback fast enough (or fake it well enough) to keep the user engaged? | `references/doherty-threshold.md` |

**Always read the reference file for any law before writing specific
claims about it.** The one-liner in this table is only for triage —
deciding which laws are worth loading for a given task — not a substitute
for the mechanism, checklist, common-mistakes section, and recommendation
phrasing that live in each file. Citing a law from the index line alone
risks the exact kind of shallow, sometimes-wrong application (e.g., the
classic Miller's-Law-as-item-count-cap mistake) that the reference files
specifically warn against.

Read `references/applying-principles.md` when the user wants to connect a
design principle to its psychological rationale, define or refine a set
of team design principles, or when the review touches persuasive /
attention-hijacking patterns and needs an ethical read layered on top of
the usability one.

Don't load all ten reference files for every task — pick the ones that
plausibly apply per "Choosing which laws apply" below, read those in
full, and expand to others only if something surfaces that points to a
law outside the initial set.

## Modes

1. **Audit** — walk a described or shown interface/flow and check it
   against whichever laws are relevant. For each finding, name the law,
   describe the specific gap, explain the real-world consequence for the
   user, and rate severity.
2. **Recommend** — turn findings (or a standalone request) into concrete,
   prioritized fixes tied explicitly to the underlying mechanism, not just
   generic best-practice language.
3. **Principle-to-law mapping** — given a team's stated design principle
   ("clarity over abundance of choice"), identify the matching law and
   help derive concrete, testable rules from it. See
   `references/applying-principles.md`.
4. **Ethical read** — when a pattern under review looks like it exploits
   one of these principles against the user's own interest rather than in
   service of their goal (infinite scroll, forced continuity, deceptive
   defaults, variable rewards, dark patterns), flag it explicitly using
   `references/applying-principles.md`'s responsible-design section,
   separate from and in addition to any ordinary usability finding.

## Choosing which laws apply

Not every review touches every law. Match the surface being reviewed to
the laws most likely to matter, load those reference files, and check the
rest only if something looks off:

- **Navigation, terminology, onboarding, redesigns** → Jakob's Law first.
- **Buttons, touch targets, toolbars, anything selectable** → Fitts's Law.
- **Dense text, data tables, long lists, navigation menus** → Miller's Law
  (chunking) — and specifically check it isn't being invoked to justify an
  arbitrary item-count limit that doesn't actually reduce memory load.
- **Menus, settings, product catalogs, "too many options" complaints** →
  Hick's Law.
- **Forms, input validation, cross-device/locale support** → Postel's Law.
- **Onboarding, checkout, errors, cancellations, milestones, anything
  emotionally charged** → Peak-End Rule.
- **A visually striking design with reported usability complaints, or a
  usability test that seems suspiciously smooth** → Aesthetic-Usability
  Effect.
- **CTAs, pricing tables, notifications, "nothing stands out" or
  "everything is competing for attention" complaints** → Von Restorff
  Effect.
- **Any place where a task feels awkward no matter how it's simplified** →
  Tesler's Law (ask who is absorbing the complexity, and where it went).
- **Loading states, slow responses, perceived-performance complaints** →
  Doherty Threshold.

Several laws often apply to the same screen at once — a checkout flow
routinely touches Jakob's (conventions), Fitts's (button sizing), Postel's
(input flexibility), Peak-End (the payment moment and confirmation
screen), and Tesler's (who handles address/payment complexity)
simultaneously. That's normal — cite each one that's genuinely doing work
in a given finding, rather than picking just one to represent the whole
screen.

## How to run an audit

1. Identify exactly what's being reviewed (a specific screen, flow,
   component, or piece of copy) and which laws plausibly apply per the
   table above. Ask for a screenshot or a described flow if there isn't
   enough to review yet — see "Tone and output" below.
2. Read the matching reference file(s) in full before writing any claim
   about that law. Don't rely on the index-table one-liner for anything
   beyond triage.
3. For each finding, write:
   - **Law** — which of the ten it falls under.
   - **Location** — the exact element, screen, or step.
   - **Gap** — what specifically diverges from the principle.
   - **Consequence** — what actually goes wrong for the user as a result,
     in concrete terms (not "poor UX," but "users will misread this as a
     destructive action" or "users will abandon here because the wait has
     no progress indication").
   - **Severity** — see the rubric below.
4. Don't force a law onto something it doesn't fit just because the skill
   covers ten of them. A screen with generous whitespace and one clear CTA
   doesn't need a Von Restorff Effect finding manufactured for coverage's
   sake.

### Severity rubric

Use this consistently across findings so recommendations can be prioritized:

- **Blocks the task** — the user cannot complete what they came to do, or
  will very likely abandon (e.g., a destructive action easily mistaken for
  a safe one under Fitts's Law; a wait with zero feedback past 10+ seconds
  under the Doherty Threshold).
- **Slows or frustrates the task** — the user can complete the task but
  with avoidable extra effort, confusion, or a worse impression (e.g., an
  unchunked wall of text under Miller's Law; a redesign with no bridging
  support under Jakob's Law).
- **Polish** — a real but minor gap that wouldn't meaningfully change
  task success (e.g., a slightly under-sized secondary icon target; a
  missed opportunity for a Peak-End Rule milestone moment).

## How to give recommendations

- Lead with fixes that are cheap and high-impact — these are very often
  Fitts's Law target sizing/spacing and Jakob's Law terminology/pattern
  fixes.
- For anything that trades user simplicity for system complexity (Tesler's
  Law), say plainly that the complexity doesn't disappear — name where it
  should move to instead (a default, a smart suggestion, background
  processing) rather than just asking for "simpler."
- For emotionally charged flows (Peak-End Rule), call out the specific
  peak moment and the specific final moment as two separate findings — a
  good middle doesn't fix a bad ending, and vice versa.
- Tie every recommendation to the mechanism, not just the desired outcome:
  "users will overshoot this target because it's under 44px with no
  spacing from its neighbor" is actionable in a way "make the button
  bigger" is not.
- If a "fix" would rely on manipulating the user (fake urgency, forced
  continuity, disguised ads, exploited variable rewards) rather than
  genuinely helping them, say so explicitly and route to
  `references/applying-principles.md`'s responsible-design section instead
  of just optimizing the requested metric.
- When multiple findings compete for attention in the writeup, order them
  by the severity rubric above, not by which law happens to have the most
  findings.

## Tone and output

- Be specific: name the exact element, screen, or step — never a vague
  "improve the UX."
- Distinguish "this breaks a principle and should be fixed" from "this
  breaks a principle but may be an intentional, supported trade-off" —
  conflating the two is the single most common failure mode in this kind
  of review, and every reference file's "common mistakes" section calls
  out a version of it.
- If there isn't enough detail to audit a real design (no screenshot, no
  described flow), ask for it rather than inventing one to critique.
- When comparing to "how other products handle this," name the pattern
  generically unless the user already named a specific competitor.
- Read the relevant reference file(s) before finalizing any recommendation
  — each file's "how to phrase recommendations" section models the level
  of specificity expected here.

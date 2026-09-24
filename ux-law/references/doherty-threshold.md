# Doherty Threshold

**One-line statement:** Productivity and engagement rise sharply when a
system responds to a user's action in well under a second. The commonly
cited threshold is roughly 400 milliseconds; below that, an interaction
feels continuous and responsive, while above it — and especially once a
delay stretches past roughly a second — attention begins to drift away
from the task at hand.

## Why it matters (mechanism)

Below the threshold, a system feels like a direct extension of the user's
own action — there's no perceptible gap for attention to wander into.
Once response time crosses the threshold, that continuity breaks: the
user's focus has a moment to detach from the task, and past roughly a
second, people reliably begin thinking about something else entirely,
losing track of exactly what they were doing or why.

This connects closely to the psychological concept of **flow** — a state
of full, energized, focused engagement with a task. Flow is fragile:
sluggish or unpredictable response times reliably break it. Less
intuitively, responses that are *too* instantaneous relative to the
apparent weight of the action can also work against the user — if a
response happens faster than the user can register what occurred, it can
feel hard to parse, or can feel untrustworthy if it doesn't match the
user's expectation of how much "work" the system should visibly be doing
for an action of that apparent importance.

## Full audit checklist

- **Raw response time to any user action** — does the system produce
  *some* feedback (not necessarily the complete final result — just an
  acknowledgment that the action registered) within roughly 400ms?
- **Perceived-performance techniques when raw speed genuinely can't be
  improved further** — for anything slower than the threshold, check
  whether any of the following masking techniques are in use, and if not,
  flag their absence as a finding:
  - **Skeleton screens** — placeholder content shapes shown while real
    content loads, rather than a blank area or a generic spinner with no
    structure.
  - **Progressive image loading** — a low-resolution preview shown
    immediately and scaled up or sharpened once the full-resolution image
    is ready, rather than blank space that suddenly pops in.
  - **Progress indicators** — even an imprecise, non-linear progress bar
    measurably improves people's tolerance for waiting compared to no
    indicator at all.
  - **Optimistic UI** — showing the expected, likely-successful result
    immediately while the real request processes in the background (with
    a clear fallback/correction path if it turns out to fail) — e.g., a
    posted comment appearing instantly in the interface before the server
    has actually confirmed it was saved.
- **Behavior on genuinely long waits (roughly beyond 10 seconds)** — a
  bare progress bar is not sufficient on its own past this point; check
  whether the interface also provides an estimated time remaining and a
  description of what's actively happening, since without that
  information attention reliably drifts to other tasks during longer
  waits.
- **Layout stability during loading** — does content shift or jump around
  as it loads in (a common source of frustration and misclicks), or is
  space reserved up front — sized image placeholders, skeleton blocks
  matching the eventual content's dimensions — so the layout stays stable
  as real content arrives?
- **Responses that are suspiciously instantaneous for high-stakes
  actions** — for something like a destructive confirmation or a
  security-sensitive scan, does an instant, no-friction response
  undermine the user's confidence that the system actually did the work
  it claims to have done? This is a real and worth-flagging finding,
  even though it's the less common direction — most findings under this
  law involve responses that are too slow, not too fast.

## Common mistakes when applying this law

- **Treating every slow response the same way.** A slow response with no
  masking technique at all is a more serious finding than a slow response
  that's already using a skeleton screen or progress indication — severity
  should reflect what's already in place, not just raw latency.
- **Recommending a spinner as if it fully solves the problem.** A bare,
  content-free spinner is better than nothing but is a weaker technique
  than a skeleton screen or progressive content loading, and provides
  essentially no benefit at all past the roughly-10-second mark without an
  accompanying time estimate.
- **Assuming faster is always strictly better with no exceptions.** For
  high-stakes or security-sensitive actions, an instant response can
  actively undermine trust — this is a genuine, if less frequent,
  exception worth checking for.

## How to phrase recommendations

- If raw latency genuinely can't be reduced further (a real backend or
  network constraint), recommend a specific perceived-performance
  technique — skeleton screen, progressive/blur-up image loading, progress
  indication, or optimistic UI — rather than leaving a blank or frozen
  state with no feedback at all.
- For long waits specifically, recommend adding both a time estimate and a
  description of the current step, not a bare progress bar alone, once
  the wait is likely to exceed roughly 10 seconds.
- For a high-stakes action that currently completes suspiciously fast,
  consider recommending *deliberate*, purposeful friction — a brief pause,
  an explicit confirmation step, or a visible "checking..." state — to
  give the user's more careful, evaluative attention a chance to engage,
  and to build confidence that the process was actually thorough. This is
  one of the few legitimate cases in this entire skill where the
  recommendation is to *add* delay rather than remove it.

## Precise reference points (origins, research, benchmarks)

- **Origin:** Named for a 1982 IBM Systems Journal study by Walter J.
  Doherty and Ahrvind J. Thadani, "The Economic Value of Rapid Response
  Time," which challenged the previously accepted standard of roughly two
  seconds as an acceptable computer response time. Their central finding:
  productivity increases *more than proportionally* as response time
  drops below roughly 400 milliseconds — when a computer and its user can
  interact at a pace where neither has to wait on the other, productivity,
  cost-efficiency, and work quality all improve together, not just user
  satisfaction.
- **Precise response-time bands worth citing directly:** a response
  around 100ms feels effectively instantaneous to a user; a delay in
  roughly the 100–300ms range starts to become perceptible and begins
  eroding a user's sense of being in control; and once a delay crosses
  roughly 1,000ms (one second), users reliably begin thinking about other
  things, their attention drifts away from the task, and task-relevant
  information starts to get lost — directly increasing cognitive load and
  reducing performance on returning to the task.
- **Ten-second attention limit, specifically:** separate research (Robert
  B. Miller, 1968) identified roughly ten seconds as the commonly
  recognized limit for keeping a user's attention focused on a single
  waiting task before they'll want to switch to something else — this is
  the empirical basis for the recommendation that, past roughly ten
  seconds, a bare progress bar needs to be paired with an estimated time
  remaining and a description of what's actively happening, rather than
  standing alone.
- **Flow, named specifically:** a psychological state of fully immersed,
  energized focus and enjoyment in an activity, coined by psychologist
  Mihály Csíkszentmihályi in 1970. Flow depends on a balance between task
  difficulty and skill level (too-hard produces frustration, too-easy
  produces boredom), and research has associated flow states with
  substantially higher productivity — cited figures run as high as
  roughly five times more productive while in flow. Designing for flow
  means giving clear feedback on what action was taken and what was
  accomplished, removing unnecessary friction to keep the system
  responsive, and keeping content/features discoverable enough that users
  don't disengage out of confusion.
- **Perceived-performance technique examples worth citing specifically:**
  a widely used photo-sharing platform's skeleton-screen loading pattern
  (instantly showing placeholder content blocks that get progressively
  replaced by real content) is a concrete, well-known example of reducing
  perceived wait time while also preventing the layout from jumping around
  as content arrives; a popular stock-photo site's "blur up" image-loading
  technique (showing a small, blurred low-resolution preview immediately,
  then fading in the full-resolution image once it's loaded in the
  background) is a specific, named version of the same underlying idea
  applied to images; percent-done progress bars have been shown in
  controlled research (Myers, 1985) to make wait times feel more
  tolerable *regardless of the bar's actual numeric accuracy* — the
  presence of visible progress feedback matters more than its precision;
  a major email client's distinctive loading animation (combining a
  branded animation with a simple progress indicator) is a concrete
  example of using animation specifically to reduce the uncertainty and
  frustration of a wait; a common OS-level software-update screen pairing
  a progress bar with an explicit time estimate is a concrete example of
  the "past ten seconds, add a time estimate and description" guidance in
  practice; and a major photo-sharing platform's practice of showing a
  newly posted comment immediately (before server confirmation, with an
  error shown afterward only if the post actually fails) is a concrete,
  named example of optimistic UI.
- **The "too fast" exception, precisely:** deliberately adding a small
  amount of purposeful delay or friction to a process has been shown to
  increase a user's *perceived* value of that process and build a sense
  of trust, even when the process itself takes meaningfully less time
  than the delay implies. A confirmation modal is a simple, common example
  of using a small amount of friction specifically to trigger more
  careful, evaluative System 2 thinking (see the System 1 / System 2
  framing in `aesthetic-usability-effect.md`) before a consequential
  action, reducing the likelihood of accidental mistakes. A named,
  concrete example at larger scale: a major platform's account privacy-
  scan feature deliberately extends the scan's duration beyond what's
  strictly technically necessary, using that extra time to actively
  educate the user about what's being checked — building confidence that
  the process was genuinely thorough rather than instant and superficial.
- **Page-weight context worth citing as background, not as this law's
  core mechanism:** average web page weight has grown substantially over
  time (industry tracking has shown average desktop page weight roughly
  tripling from the low 2010s to the low-to-mid 2020s, with mobile
  following a similar trend), which is part of why perceived-performance
  techniques have become a near-default expectation rather than an
  occasional nicety — raw page weight is trending in a direction that
  makes hitting the raw 400ms threshold harder over time, not easier.

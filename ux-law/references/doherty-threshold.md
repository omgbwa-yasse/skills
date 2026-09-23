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

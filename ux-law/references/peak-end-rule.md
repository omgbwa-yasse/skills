# Peak-End Rule

**One-line statement:** People judge a past experience largely by how they
felt at its most emotionally intense moment (the peak, whether positive or
negative) and at its very end — not by the sum or average of every moment
along the way. This is a memory bias: people recall representative
snapshots of an experience, not a comprehensive timeline of it.

## Why it matters (mechanism and origin)

The foundational research (Kahneman et al., 1993, and follow-up clinical
studies on colonoscopy and lithotripsy patients through the 1990s and
2000s) found something counterintuitive: patients who underwent a
*longer* version of an uncomfortable procedure — one that ended on a
comparatively less painful note — rated the overall experience as *less*
unpleasant, and were *more* likely to return for future procedures, than
patients who underwent a shorter procedure that ended more abruptly at a
higher pain level. Duration itself barely mattered to recalled experience;
the trajectory into the ending did.

Two related cognitive biases sharpen why this matters for design:
- **Negativity bias** — people register and dwell on negative events more
  readily than positive ones, so a single bad peak (an error, a confusing
  dead end, a failed action) can outweigh a substantial amount of
  otherwise-fine experience in someone's overall recollection.
- **Recency effect** — items near the end of a sequence are disproportionately
  easy to recall. This is part of why the "end" half of the rule carries
  so much weight — it's not just narratively significant, it's the part
  memory holds onto most readily.

## Full audit checklist

- **Identify the single most intense moment of the journey.** Common
  candidates: account creation and password requirements, a wait or
  loading moment, a milestone or achievement, an error state, a payment
  or checkout moment, a cancellation or deletion flow. Every flow has
  *some* candidate for "most intense moment" — the audit's job is to find
  it and evaluate it specifically, not to assume the flow is emotionally
  flat throughout.
- **Identify the literal last thing the user sees or does.** Independent
  of how good the middle of the flow was, what does the final screen,
  message, or state communicate? A rough ending can retroactively sour an
  experience that was smooth everywhere else — and a good ending can
  meaningfully offset a rough middle.
- **Wait times specifically** — is anything reducing the *perceived* pain
  of waiting, separate from the actual wait duration? Concepts worth
  checking for explicitly: **idleness aversion** (does the interface keep
  the user occupied/informed rather than staring at a static blank
  state?), **operational transparency** (does the system explain *how*
  an estimate or result is being calculated, not just show a number?),
  and the **goal gradient effect** (does the interface make each step of
  progress toward the goal visible, so the user feels continuously closer
  rather than stalled?). A ride-hailing app's live map, ETA, and step-by-
  step status messages during a wait are a concrete example of applying
  all three at once.
- **Error and failure states** — is there a graceful, on-brand recovery
  (a thoughtfully designed error page, a clear next action) rather than a
  bare, cold failure message? Important caveat: humor or brand
  personality in an error state should never risk making a genuinely bad
  situation feel worse — read the emotional context of *this specific*
  failure (a 404 page is usually low-stakes; a failed payment or lost
  data is not) before recommending a lighthearted tone.
- **Milestone / completion moments** — are meaningful accomplishments
  (task completion, streaks, first successful use, unlocking something)
  marked in a way that creates a positive snapshot — through brand
  character, illustration, subtle animation, or personalized
  reflection — or do they pass with no acknowledgment at all? A concrete
  pattern worth checking for: personalized "year in review"-style
  reflections at a natural reflective moment (e.g., end of year) can turn
  a routine data summary into a genuinely memorable positive peak.
- **High-stakes moments with rigid rules** — e.g., password requirements
  enforced with no real-time, in-context guidance, encountered right when
  a user is most enthusiastic about trying a new product. This is a
  frequent, avoidable source of an early negative peak.

## Common mistakes when applying this law

- **Fixing only the middle of a flow and assuming the whole journey is now
  better.** The peak and the end are two separate, specific design
  questions — improving the average experience in between does not
  substitute for addressing either one directly.
- **Treating "add delight" as a generic instruction.** Delight only
  registers as a positive peak or ending when it's tied to a *specific*
  identified moment; sprinkled indiscriminately across a flow, it reads as
  decoration rather than a meaningful snapshot.
- **Using humor to paper over a genuinely bad experience.** If the
  underlying failure is serious (data loss, a failed payment, a security
  issue), a playful tone at that exact moment can come across as
  dismissive rather than reassuring — match tone to actual stakes.
- **Ignoring negative peaks because "the rest of the flow is fine."**
  Negativity bias means a single sufficiently bad moment can dominate the
  overall recollection regardless of how good everything else was.

## Related technique: journey mapping

Journey mapping is the standard tool for locating emotional peaks
systematically rather than guessing at them. A journey map typically
includes: a **lens** (the user persona, the specific scenario, and their
expectations going in), an **experience** section (phases → actions
within each phase → the user's mindset/thoughts/pain-points during each
phase → an emotional line plotted across the whole timeline, which is
exactly where peaks become visible), and an **insights** section
(opportunities to improve, and who internally owns follow-through on
each one). When available, ground the persona and phases in real user
research rather than an assumed journey.

## How to phrase recommendations

Treat the peak and the end as two separate design problems in the
writeup — call each out individually rather than bundling them into one
generic "improve the emotional experience" note. When recommending fixes:
- For a negative peak that can't be removed entirely (a necessary wait, a
  required and inherently complex step), recommend improving the
  *experience* of that moment — transparency, real-time feedback,
  visible progress, useful information during the wait — rather than
  only trying to shorten the raw duration.
- For the very end of any flow, explicitly evaluate what the last screen,
  message, or state communicates, independent of everything that came
  before it.
- Don't recommend "add delight" without anchoring it to a specific
  identified peak or ending moment, and check that it won't read as
  hollow given the rest of the surrounding experience.

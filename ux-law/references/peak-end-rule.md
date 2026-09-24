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

## Precise reference points (origins, research, technique)

- **Foundational experiment:** a 1993 study (Kahneman and colleagues)
  had participants submerge a hand in uncomfortably cold water (roughly
  14°C) for 60 seconds in one trial, and in a second trial submerge the
  other hand in the same cold water for 60 seconds *plus* an additional
  30 seconds during which the water was gradually warmed slightly. When
  asked which trial they'd be willing to repeat, participants favored the
  *longer* trial — the one with strictly more total discomfort — because
  it ended on a comparatively less unpleasant note. Total duration barely
  mattered to recalled preference; the trajectory into the ending did.
- **Clinical follow-up studies worth citing:** later research on patients
  undergoing colonoscopy and lithotripsy procedures (mid-to-late 1990s and
  early 2000s) found that patients consistently evaluated overall
  discomfort based on the pain intensity at the worst moment and at the
  final moment of the procedure, regardless of the procedure's total
  length or the amount of pain-intensity variation throughout. A
  follow-up study went further: patients randomly assigned to a version of
  the procedure with a few extra minutes added at the end (during which
  discomfort was intentionally lower) rated the overall experience as
  *less* unpleasant, and were *more* likely to return for future
  procedures, than patients who underwent the shorter version ending at
  the original, higher-discomfort point.
- **Related cognitive biases worth naming specifically:** cognitive biases
  in general are systematic, largely unconscious shortcuts in judgment
  (a concept popularized by Amos Tversky and Daniel Kahneman starting in
  the early 1970s) that speed up decision-making at some cost to accuracy.
  **Confirmation bias** — the tendency to seek out and recall information
  that confirms existing beliefs while discounting information that
  challenges them — is one well-known example. The peak-end rule itself is
  specifically a *memory* bias. It's closely related to the **recency
  effect**: items near the end of a sequence are disproportionately easy
  to recall, which is part of the mechanism behind why the ending of an
  experience carries so much retrospective weight.
- **Wait-time example worth citing by name:** a major ride-hailing
  company found that addressing perceived wait time (rather than only
  raw wait duration) reduced post-request cancellations, using three
  specific concepts together: **idleness aversion** (keeping the user
  visually informed and engaged rather than facing a static blank
  screen), **operational transparency** (explaining how an estimate is
  calculated, not just displaying a number), and the **goal gradient
  effect** (making each concrete step of progress toward the goal visible,
  so the user feels continuously closer rather than stalled).
- **Milestone/gamification example worth citing:** a popular
  language-learning app uses streaks and level-based milestones —
  reinforced with brand-specific illustration, subtle animation, and
  humor — to turn routine progress markers into genuinely memorable
  positive peaks, going beyond a plain, generic progress indicator.
- **Personalized reflective moment example worth citing:** a major music
  streaming service's end-of-year personalized listening recap is a
  concrete example of using a naturally reflective calendar moment (the
  end of the year) to turn a routine data summary into a positive,
  shareable emotional peak, through personalization and self-reflection.
- **404/error-page example worth citing, with its caveat:** some
  companies use a broken-link (404) page as an opportunity to reinforce
  brand personality through humor rather than leaving a cold, generic
  failure message — but this only works for genuinely low-stakes
  failures; the same lighthearted tone applied to a serious failure (a
  lost payment, lost data) risks reading as dismissive rather than
  reassuring, so tone should always be matched to the actual stakes of
  the specific failure.
- **Real-time validation example worth citing:** rigid password-creation
  rules enforced only after submission (rather than validated in real
  time as the user types) are a common, avoidable source of an early
  negative peak, right at the moment a new user is most enthusiastic
  about trying a product — real-time, in-context validation is the
  standard fix.

### Technique: Journey Mapping

Journey mapping is a qualitative research artifact for visualizing how a
person moves through a product or service experience while accomplishing
a specific goal, and it's the standard way to locate emotional peaks
systematically rather than guessing at them. A journey map typically
includes three parts. The **lens** establishes perspective: the
persona representing the end user (ideally grounded in real research, not
assumption), the specific scenario being mapped, and the persona's
expectations going into that scenario (for example: a specific persona
using a ride-share app to order a ride, expecting arrival within a
specific number of minutes). The **experience** section lays out
high-level phases, the concrete actions the user takes within each phase,
a layer capturing the user's mindset during each phase (thoughts, pain
points, questions, motivations — typically drawn from real research and
interviews), and — most relevant to this law specifically — a continuous
emotional line plotted across the whole timeline, which is exactly where
peaks (positive or negative) become visible at a glance. The **insights**
section captures the resulting opportunities for improvement, along with
the metrics that would indicate progress on each opportunity and which
team internally owns following through on it.

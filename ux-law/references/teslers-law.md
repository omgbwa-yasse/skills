# Tesler's Law (law of conservation of complexity)

**One-line statement:** Every process contains a floor of irreducible
complexity. That complexity cannot be eliminated — only moved. The design
question worth asking for any point of friction is not "how do we make
this simpler," but "who is going to absorb this complexity — the user, or
the system, built by designers and developers up front?"

## Why it matters (mechanism and origin)

The underlying reasoning, attributed to computer scientist Larry Tesler:
if a large number of users each lose a small amount of time or effort
dealing with complexity that a team could have absorbed once by making
the underlying system a bit more sophisticated, that trade-off penalizes
the many to spare the few. Complexity that's genuinely inherent to a task
doesn't disappear when an interface looks simple — it has usually just
been moved somewhere less visible: into smart defaults, inferred values,
background processing, or the engineering effort that built the
simplification in the first place.

## Full audit checklist

- **Repetitive or already-known information** — is the system asking the
  user to re-enter information it could reasonably infer, pre-fill, or
  already has on file (a sender's own email address, a shipping address
  identical to a billing address already entered, previously provided
  contact details)? A classic example: a modern email client pre-fills
  the "from" field automatically and suggests recipients as the user
  types, based on prior contacts — the complexity of knowing who the
  sender is and completing the recipient's address hasn't vanished, it's
  been absorbed by the client instead of demanded of the user each time.
- **Manual steps that could be defaulted** — is there an obvious, sensible
  default or inherited value (e.g., "shipping address same as billing")
  the system could apply automatically, with an easy override available,
  rather than requiring explicit re-entry every time?
- **Where has the complexity actually gone — has it genuinely resolved,
  or just moved out of sight?** If a flow looks deceptively simple, check
  whether the underlying complexity was properly handled somewhere else
  (validation logic, inferred defaults, background reconciliation) or
  whether it's been hidden in a way that will resurface later as a
  confusing error, an unhandled edge case, or a support burden — hiding
  complexity is not the same as resolving it.
- **Oversimplification risk** — the same caution that applies to Hick's
  Law applies here: complexity absorbed *too* aggressively (excessive
  automation, over-confident inference) can strip away context or control
  the user actually needed, producing a different kind of friction later
  (an unwanted default silently applied, a wrong inference the user has no
  easy way to correct).
- **New interaction paradigms (natural-language / intent-based input)** —
  where relevant, check whether the system lets the user simply describe
  the outcome they want, rather than requiring them to execute every
  individual step of a command-based interaction manually. This kind of
  interface can substantially lower the expertise barrier to reach
  "power user" capability, without necessarily hiding what the system is
  actually doing — check that it doesn't hide it either.
- **Checkout- and account-scale examples worth checking specifically**:
  a "ship to billing address" checkbox, a saved-payment/one-tap purchase
  flow, and fully automated checkout-free retail experiences (where
  computer vision, machine learning, and account linkage absorb essentially
  all of the purchasing complexity on the system side) are all points on
  the same spectrum — each shifts progressively more complexity away from
  the user and onto infrastructure the team built and maintains.

## The paradox of the active user

A well-documented pattern from usability research: users overwhelmingly
do not read documentation or manuals before starting to use a product —
they dive in and learn by doing, even when that means hitting avoidable
errors and roadblocks along the way. It's a genuine paradox, because
users would often save time in the long run by learning the system first
— but that's not how people actually behave. The practical implication:
design guidance needs to be reachable *in context*, at the moment it's
needed (tooltips, inline hints, contextual first-use guidance), rather
than assuming users will proactively seek out instructions before diving
in.

## Common mistakes when applying this law

- **Recommending outright removal of a step instead of relocating its
  complexity.** Deleting a required field or step can simply reintroduce
  ambiguity or errors downstream instead of actually reducing total
  complexity — the goal is relocation to a place the system can absorb it,
  not deletion of necessary information.
- **Assuming "simpler-looking" automatically means "less complex
  overall."** A simplified UI built on aggressive, unvalidated inference
  can create a worse experience than a slightly more effortful but
  transparent one, if the inference is frequently wrong and hard to
  correct.
- **Not naming who/what absorbs the shifted complexity.** A vague
  recommendation to "simplify this" doesn't tell a design or engineering
  team where the underlying work needs to go — the recommendation should
  say explicitly (a default value, an inference model, a background
  process, a progressive-disclosure UI pattern).

## How to phrase recommendations

- Frame recommendations as *shifting* complexity, not deleting it: "move
  this from a required manual field to a smart default the user can
  override" is a meaningfully different (and more implementable)
  recommendation than "remove this field," which risks reintroducing
  ambiguity or errors elsewhere in the flow.
- When a task genuinely requires real effort from the user, don't
  recommend hiding that effort behind a misleadingly simple-looking UI —
  doing so just relocates the confusion to a later point (a validation
  error, an unexpected result the user can't trace back to its cause).
- Recommend **progressive disclosure** (hiding secondary options behind a
  dropdown, accordion, or toggle, showing only what's needed by default)
  as a preferred technique for shifting complexity out of the primary
  view without deleting user control outright — it's a good middle ground
  between "show everything" and "remove functionality."

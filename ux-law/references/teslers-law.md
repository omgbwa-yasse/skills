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

## Precise reference points (origins, research, technique)

- **Origin:** Traces to the mid-1980s work of Larry Tesler, a computer
  scientist at Xerox PARC who helped develop the emerging discipline of
  interaction design during the early development of desktop computing
  and desktop publishing. Tesler recognized that interface consistency
  benefited both users and developers, since shared standards could be
  encapsulated in reusable software libraries. Later, while working on an
  object-oriented application framework at Apple, he framed the "law of
  conservation of complexity" explicitly as an argument for building
  shared standards into the underlying software rather than pushing
  complexity out to end users — his own reasoning was that if a huge
  number of users each individually lose a small amount of time dealing
  with complexity an engineering team could have absorbed once, that
  trade-off effectively penalizes the many to spare the few.
- **Complexity bias, named specifically:** a documented cognitive bias
  in which people tend to favor complicated-seeming solutions over
  straightforward ones, partly because complexity gets unconsciously
  associated with intelligence, expertise, or depth of understanding. A
  1989 study (Farris and Revlin) demonstrated this concretely: participants
  asked to discover a simple numeric rule (list any three ascending
  numbers) overwhelmingly assumed the rule had to be more complicated than
  it actually was, and favored testing elaborate hypotheses over the
  simple, correct one. The design-relevant implication: when a team finds
  itself gravitating toward an unusually complex solution, that's often a
  signal the underlying problem isn't fully understood yet, not a sign the
  problem genuinely requires that much complexity.
- **Email as the canonical example:** every email fundamentally requires
  two pieces of information — who it's from and who it's going to — and
  it cannot be sent without both, making this a necessary, irreducible
  complexity. Modern email clients don't eliminate this requirement; they
  absorb it by pre-populating the sender (since the client already knows
  the user's own address) and suggesting recipients as the user types,
  based on prior contacts. AI-assisted features layered on top of this
  (auto-completing sentences as they're typed, or suggesting quick reply
  options based on an email's content) extend the same underlying
  pattern — none of these features remove the complexity of composing a
  message, they shift more and more of it onto the system.
- **Checkout examples worth citing along a spectrum:** a "shipping address
  same as billing" option is a simple, common example of shifting
  redundant-entry complexity onto the system; saved-payment or one-tap
  purchase flows (e.g., a platform-level digital wallet) shift it further,
  reducing repeat checkout to selecting a saved option and confirming;
  and fully checkout-free retail experiences (using computer vision,
  machine learning, and account linkage to let a customer simply take
  items and leave, with a receipt and charge generated automatically)
  represent close to the far end of that spectrum — the customer's
  experience becomes dramatically simpler precisely because an enormous
  amount of technical complexity has been absorbed on the system side.
- **Intent-based / natural-language interaction as a newer example:**
  some modern analytics and data tools let users describe the outcome
  they want in plain language rather than manually configuring every
  step of a traditional command-based interface — this newer paradigm can
  substantially lower the expertise barrier required to reach "power
  user" capability, since the system absorbs more of the procedural
  complexity of translating intent into the correct sequence of actions.
- **The paradox of the active user, precisely:** first described by Mary
  Beth Rosson and John Carroll (1987) based on observed user studies at
  IBM's User Interface Institute, this describes the consistent finding
  that new users do not read supplied manuals or documentation before
  starting — they dive straight into using a product, even at the cost of
  hitting avoidable errors and roadblocks. It's a genuine paradox because
  users would frequently save time overall by learning the system first —
  but that's simply not how people behave in practice, which is why
  in-context guidance (tooltips, inline hints reachable at the moment
  they're needed) is a more effective design response than assuming users
  will read documentation up front.

### Technique: Progressive Disclosure

Progressive disclosure is an interaction design technique that shows only
the most important actions or content by default, while keeping
additional features or content easily reachable but out of the way until
needed. Any dropdown, accordion, or toggle that reveals hidden content on
demand is an application of this technique. It's a particularly useful
way to manage Tesler's-Law-style complexity because it defers less
essential actions, advanced features, or supplementary content to a
secondary layer of the interface, keeping the primary view focused and
scannable without deleting functionality outright. A commonly cited
example is a navigation pattern where hovering or interacting with a
top-level category reveals a fuller menu of related links underneath it
— letting the primary navigation bar stay compact and scannable while
still giving users a path to a large amount of underlying content when
they actually want it.

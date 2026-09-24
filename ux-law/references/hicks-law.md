# Hick's Law

**One-line statement:** The time it takes to make a decision increases
(the original formulation is logarithmic in the number of options — RT
grows roughly with log2 of the number of choices) with both the number
and the complexity of the choices presented at once. More options, or
more complex ones, produce a slower decision, and past a point, choice
overload can produce indecision or outright abandonment rather than a
"merely slower" decision.

## Why it matters (mechanism)

This is distinct from Miller's Law even though the two get confused
constantly: Miller's Law is about *memory/scanning* of visible
information; Hick's Law is about the *time and mental effort to decide*
among options, regardless of whether those options need to be memorized
at all. A menu can be perfectly scannable (well-chunked, per Miller's Law)
and still be slow to decide from if it presents too many genuinely
competing options with no way to narrow them.

**The paradox of choice:** the common intuition that more choice is
always better is frequently wrong. A well-known field study found that
shoppers presented with a large assortment of jam varieties were far less
likely to actually purchase than shoppers presented with a small
assortment, despite the larger display attracting more initial attention
— more choice drove more looking but less deciding. This is the
mechanism behind "choice overload," and it's worth naming explicitly when
a finding involves a large, undifferentiated option set.

## Full audit checklist

- **Onboarding** — is a new user handed one clear next step at a time
  (a short, sequential checklist that mirrors how people actually learn —
  by doing, in a low-risk environment, building on what they already
  know), or dropped into a screen presenting every possible action
  simultaneously with no guided starting point?
- **Search and filtering** — are refinement options (type, category,
  price range, etc.) presented only *after* an initial simple action (a
  search is run, a category is picked), rather than forcing the user to
  configure every possible parameter before they can even begin? Deferring
  choice to the moment it becomes relevant keeps the initial task light.
- **Menus and controls, physical or digital** — has less-essential
  functionality been pushed into a secondary, well-organized surface
  (e.g., a simplified physical remote with the bulk of functionality
  moved into an on-screen menu) rather than crammed onto the primary
  control surface? A useful historical example: as TV remotes accumulated
  more buttons over the decades, some became so complex that users
  resorted to taping over everything except the essential controls — a
  sign the *design* had failed to manage choice, not that users were
  incapable.
- **Recommendation / selection surfaces** (streaming catalogs, product
  listings, content feeds) — is there a mechanism that reduces the
  *effective* choice set for a first-pass decision — curated sections,
  "popular," "trending," personalization, social proof — or is the user
  facing the entire undifferentiated catalog with no way to narrow it?
  Note the specific mechanism at work: highlighting "popular" or "trending"
  items works partly through **social proof** — weighting a decision
  based on evidence that others have made and enjoyed the same choice —
  which is a legitimate way to reduce effective choice count without
  removing options outright.
- **Icon-only actions** — do icons lacking a near-universal, unambiguous
  meaning get a text label, or are they left for the user to individually
  decode? Undifferentiated or ambiguous icons add *interpretation* time on
  top of ordinary decision time, and that cost compounds when the same
  icon shape means different things across different products (there's no
  icon-standardization body, so a heart or star icon might mean "like,"
  "favorite," "bookmark," or "rate" depending on context) or even within
  the same product across different screens.
- **Multi-step processes** — is a complex task broken into a short
  sequence of simpler decisions, each with a narrow, well-defined set of
  choices, rather than one screen demanding every decision simultaneously?

## The oversimplification trap (read this before recommending "simplify")

Reducing choice is not free. Simplifying an interface *to the point of
abstraction* removes the cues people need to understand what's possible,
what the next step is, or where to find something — which paradoxically
*increases* cognitive load even though the interface looks cleaner.
Icon-only navigation with no text labels is the textbook example: it
looks minimal, but forces every user to interpret ambiguous symbols from
scratch, and the interpretation cost lands hardest on less frequent or
less tech-familiar users. Flag over-simplification with exactly the same
seriousness as flagging choice overload — both ultimately raise the
time/effort required to act, just through different mechanisms (decision
time vs. interpretation/recognition time).

A practical technique for finding the right grouping/labeling of options
in the first place — rather than guessing — is **card sorting**: give
participants a set of topic cards and have them group the cards however
makes sense to them, then name their own groups. Run as a moderated, open
sort (predefined categories = "closed" sort; here, participants invent
their own), it reveals real mental models for organizing choices rather
than the designer's assumed ones, and typically follows four steps:
identify the topics to be sorted (avoiding near-duplicate labels that
would bias grouping), have participants organize them while thinking
aloud, have participants name the groups they created, and optionally
debrief participants on their reasoning.

## Common mistakes when applying this law

- **Confusing it with Miller's Law and recommending an item-count cap as
  the fix.** Check whether the actual complaint is about *deciding* among
  visible options (Hick's) or *scanning/remembering* dense content
  (Miller's) before prescribing a fix.
- **Recommending removal of choices without checking what gets lost.**
  Cutting options can remove functionality or context a subset of users
  genuinely needs — see "oversimplification" above.
- **Treating icon labeling as a minor polish item.** It's frequently a
  cheap, high-leverage fix, especially for primary navigation.

## How to phrase recommendations

- Defer choices to the moment they matter rather than front-loading all
  of them (e.g., show filters after an initial search rather than
  requiring full configuration up front).
- Break a complex decision into a short sequence of simpler ones instead
  of one screen presenting everything at once.
- Where the full breadth of choice must remain available, add a mechanism
  to reduce the *effective* set for a first pass (defaults, curation,
  "recommended," smart ordering, social proof) without removing access to
  the rest.
- If icons carry meaningful, non-obvious actions, pair them with text
  labels rather than assuming universal recognition — call this out as a
  cheap, high-value fix whenever it applies.
- Don't recommend stripping cues or context purely in the name of
  "simplicity" without checking whether that removes information the
  user actually needs to act confidently — name the specific information
  being lost, if any.

## Precise reference points (origins, formula, research, technique)

- **Origin and formula:** Formulated in 1952 by psychologists William
  Edmund Hick and Ray Hyman, who studied the relationship between the
  number of stimuli present and reaction time. The relationship is
  commonly expressed as RT = a + b·log2(n), where RT is response time, n
  is the number of choices, and a and b are task-dependent constants —
  the key practical implication is that decision time grows
  *logarithmically*, not linearly, with the number of options, so each
  additional option adds progressively less marginal decision time than
  the one before it, but the effect is still real and compounds with
  genuinely large option sets.
- **The jam study (cite this specifically for "paradox of choice"
  findings):** a well-known field experiment (Iyengar and Lepper, 2000)
  set up a tasting table at an upscale food market, alternating between a
  large assortment (24 varieties of jam) and a small assortment (6
  varieties). The large display drew more attention and browsing, but
  shoppers who saw the large assortment were only about one-tenth as
  likely to actually make a purchase compared to shoppers who saw the
  small assortment — a concrete demonstration that more choice can
  suppress action even while it increases initial interest. This study is
  the empirical basis for psychologist Barry Schwartz's popularized
  concept of the "paradox of choice."
- **TV remote example worth citing as a physical-world illustration:** as
  television feature sets grew over the decades, remote controls
  accumulated more and more buttons, to the point where some users
  resorted to physically taping over everything except the handful of
  essential controls — an informal but telling illustration of users
  self-simplifying an interface that failed to manage choice on their
  behalf. Modern minimalist remotes (with the bulk of functionality moved
  into an organized, progressively disclosed on-screen menu) represent the
  opposite, better-managed approach to the same underlying feature set.
- **Deferred-choice examples worth citing:** search interfaces that
  surface filtering options (type, date, category) only *after* an
  initial simple search action, rather than requiring full configuration
  up front; step-by-step onboarding checklists that hand a new user one
  task at a time rather than the full range of product capability at
  once; curated "trending" or "popular" sections in large content
  catalogs, which work partly through **social proof** — weighting a
  choice based on evidence that many other people have already made and
  been satisfied with it — as a way to narrow the effective choice set for
  a first-pass decision without removing the rest of the catalog.
- **Icon ambiguity:** because there's no standards body governing which
  icon shape must mean which action, the same icon (a heart or star, for
  instance) can mean "favorite," "like," "bookmark," or "rate" depending
  on the product — and can even carry competing meanings within the same
  product across different screens. This ambiguity adds interpretation
  time on top of ordinary decision time, and the standard, low-cost fix is
  pairing ambiguous icons with a text label, especially for primary
  navigation.

### Technique: Card Sorting

Card sorting is a research method for surfacing users' real mental models
for how content or options should be organized, rather than relying on a
designer's assumptions. The most common variant — a moderated, **open**
card sort (where participants create their own categories, as opposed to
a **closed** sort where categories are predefined by the researcher) —
follows four steps: **identify topics** (choose the items to be sorted,
each on its own card, avoiding near-duplicate labels that could bias
participants into grouping items together purely because of similar
wording); **organize topics** (have participants group the cards however
makes sense to them, ideally thinking out loud during the process to
surface their reasoning); **name categories** (ask participants to name
the groups they created in their own words — this step is especially
valuable because it reveals the actual mental-model vocabulary to use in
the real information architecture); and, optionally, **debrief
participants** (ask them to explain their rationale for each grouping,
which surfaces difficulties they encountered and thoughts on any items
they couldn't place).

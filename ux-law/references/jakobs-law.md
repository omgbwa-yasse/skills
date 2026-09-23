# Jakob's Law

**One-line statement:** Users spend most of their time on *other* products,
so they bring the expectations built there to whatever they use next. The
less a design diverges from those expectations without good reason, the
less mental effort a user has to spend figuring out how it works — and the
more they can spend on their actual goal.

## Why it matters (mechanism)

A mental model is a person's internal, simplified belief about how a
system works, built from cumulative past experience — with that exact
product, with similar products, and even with physical-world analogs
(e.g., toggle switches and radio buttons visually echo physical control
panels). Good UX aligns the product's actual behavior with the model the
user already carries, instead of requiring them to build a new one from
scratch on first contact. The gap between "how the user thinks it works"
and "how it actually works" is the single biggest source of friction on
first contact with any product.

Two forces are always in tension, and a good audit names which one is at
play for each finding:
- **Familiarity** lowers cognitive load, speeds up first-time use, reduces
  support burden, and lets users transfer skill from one product to
  another without re-learning.
- **Differentiation** can be genuinely valuable — sometimes breaking a
  convention is the whole point of a product's value proposition — but it
  has to be *earned* (validated with users) and *supported* (scaffolded),
  or it just reads as confusion dressed up as innovation.

Jakob's Law is not "copy everyone else." It is "default to convention
unless you have a specific, tested reason to diverge, and support the
divergence when you do."

## Full audit checklist

Walk the interface, page, or flow area by area. For each area, note (a)
what the dominant convention is for that category of product — not one
single competitor's implementation, but the pattern that's genuinely
widespread across the category — (b) whether this design follows it,
diverges from it, or reinvents it, and (c) if it diverges, whether there's
a stated reason and whether the design compensates for the learning curve
it introduces.

- **Navigation** — placement of primary nav (top bar vs. sidebar vs.
  hamburger), back-button behavior, breadcrumb use, whether "home" always
  returns somewhere predictable, tab order and grouping.
- **Search** — icon shape and placement (top-right vs. embedded in nav),
  expected keyboard shortcuts (e.g., `/` or `Cmd/Ctrl+K` in many web
  apps), autocomplete/suggestion behavior, whether results appear inline
  or navigate to a new view.
- **Forms & controls** — checkbox vs. toggle vs. radio semantics (a toggle
  implies immediate effect; a checkbox in a form implies "applies on
  submit"), label placement (above vs. inline vs. floating), validation
  timing (on blur vs. on submit vs. live), required-field marking
  (asterisk vs. explicit "optional" tags), field order matching the
  user's natural mental sequence (e.g., name before address).
- **E-commerce flows** — cart icon and placement (top-right is near-
  universal), checkout step order (info → shipping → payment → review is
  the dominant pattern), filtering/sorting control placement and
  persistence, price/shipping/tax disclosure timing (surprise costs late
  in checkout is a well-known convention violation that kills conversion).
- **Content structure** — where primary actions live relative to content
  (top-right for primary actions is common in desktop web; bottom or
  floating for mobile), card vs. list conventions for the content type,
  infinite scroll vs. pagination expectations (infinite scroll for feeds,
  pagination for anything the user needs to return to a specific spot in).
- **Onboarding** — how much explanation is required before the user can do
  anything useful; whether the product silently assumes prior knowledge
  of a similar tool (e.g., assuming familiarity with keyboard shortcuts
  from a competitor without teaching them).
- **Redesigns specifically** — is the change introduced all at once, or
  with a preview/opt-in/rollback path? Is there a payoff stated for the
  *user*, not only the business? Is there a way to give feedback before
  forced migration?
- **Terminology** — does the product use the words its category's users
  already expect ("cart," "checkout," "save," "share"), or does it
  introduce new vocabulary without explanation? Renaming a familiar
  concept ("cart" → "bag" → some invented term) adds a small translation
  tax every time.
- **Icon and control shape language** — do icons match near-universal
  conventions (magnifying glass = search, gear = settings, trash = delete)
  or invented iconography with no text label to disambiguate?
- **Platform conventions** — does the design follow the host platform's
  own conventions (iOS Human Interface Guidelines, Material Design,
  standard web patterns) where the user is likely arriving with platform-
  level expectations, not just product-level ones?

## Classifying each finding

- **Unnecessary novelty** — diverges from convention with no apparent
  benefit to the user or the business → recommend converting to the
  familiar pattern. This is the most common and cheapest-to-fix category.
- **Justified divergence, unsupported** — there's a real reason to do
  something different (a genuine product differentiator, a technical
  constraint, a new interaction model the product is built around), but
  nothing in the design helps the user bridge the gap → recommend adding
  support: tooltips, a first-run walkthrough, a "classic view" toggle,
  staged/opt-in rollout, in-context hints on first encounter.
- **Justified and supported** — no action needed; note it explicitly as a
  design strength if a balanced review was requested, since it's easy for
  an audit focused on finding problems to skip over things that are
  working.

## Common mistakes when applying this law

- **Treating "different from what I personally use" as "unfamiliar."**
  The relevant convention is the one the *target audience* for this
  product has built up, not the reviewer's own daily tools.
- **Citing a single competitor as "the" convention.** One company's choice
  is not automatically the dominant pattern — check whether it's actually
  widespread across the category before treating it as the baseline.
- **Recommending convention for its own sake even when the product's whole
  value proposition depends on doing something differently.** Jakob's Law
  is a default, not an absolute; a genuinely novel interaction paradigm
  (e.g., natural-language input replacing a traditional form) can be the
  right call if it's validated and taught.
- **Ignoring platform-level conventions in favor of only product-level
  ones.** A mobile app that ignores iOS/Android platform gestures creates
  friction even if it's internally consistent with the rest of the
  product.

## How to phrase recommendations

Redesigns that intentionally break a pattern users currently rely on
should almost always ship with a bridging mechanism — opt-in preview,
gradual rollout, a revert option, an in-product changelog, or contextual
first-use guidance — unless the user has already explicitly ruled that
out ("we've decided against a phased rollout"). Where the divergence is
deliberate differentiation with a real payoff, don't recommend blindly
reverting to convention; instead recommend the minimum onboarding needed
to teach the new model, and suggest validating it with usability testing
before full rollout.

Always name the specific convention being restored or the specific
mental-model gap being closed — "move the cart icon back to the top-right
because that's where users' muscle memory expects it from every other
e-commerce site" is actionable; "make it more standard" is not.

When citing "how other products do this," name the pattern generically
(e.g., "the standard multi-step checkout with a persistent order
summary") rather than a specific competitor's exact implementation,
unless the user already named that competitor.

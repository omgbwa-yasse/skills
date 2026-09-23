# Applying These Laws: Principles, Rules, and Responsible Design

This file covers two things that sit above the individual laws: how to
turn a team's stated design principle into psychologically grounded,
testable rules, and how to read a pattern as manipulative rather than
merely a usability gap.

## Part 1 — Connecting a design principle to a law

When someone wants to ground a stated design principle in psychological
reasoning — or wants help *defining* a principle in the first place — use
this three-layer framework:

1. **Goal (the design principle)** — a clear, opinionated, memorable
   statement, not a truism. "Design should be intuitive" is too vague to
   ever resolve a real decision; "clarity over abundance of choice" or
   "familiarity over novelty" are usable because each states an explicit
   trade-off the team is choosing to make, which means it can also justify
   saying no to something.
2. **Observation (the matching law)** — identify which of the ten laws in
   this skill most directly explains *why* the principle matters, and
   read that law's reference file for the full mechanism before writing
   anything more specific than a one-line mapping.
   - "Clarity over abundance of choice" → **Hick's Law** (decision time
     rises with the number/complexity of choices).
   - "Familiarity over novelty" → **Jakob's Law** (users transfer
     expectations from products they already know).
   - "Respect the user's time" → could map to **Doherty Threshold**
     (response speed) or **Tesler's Law** (who absorbs necessary effort)
     depending on which specific problem prompted the principle — ask
     which one the team actually means before picking.
   - "Don't make users hold information in their head" → **Miller's Law**
     (chunking, not an item-count cap).
   - "End on a high note" / "first impressions matter" → **Peak-End Rule**
     and/or **Aesthetic-Usability Effect**, depending on whether the
     principle is about the emotional trajectory of a flow or about
     initial visual impression.
3. **Rules (concrete, testable guidance)** — derive specific, checkable
   rules a team can actually apply and audit against, not just restate
   the principle in different words. For "clarity over abundance of
   choice" via Hick's Law, a rule might be "surface no more than N primary
   actions per screen" or "defer secondary options to a second step." For
   "familiarity over novelty" via Jakob's Law, a rule might be "use
   established platform/category design-pattern conventions for core
   flows" or "any novel interaction pattern for a core flow requires
   usability validation before shipping." The rule should be specific
   enough that two different designers reviewing the same screen against
   it would reach the same verdict.

### What makes a design principle good, by this framework

A genuinely useful design principle is: **not a truism** (it says
something that could plausibly be false or contested, not something
everyone already agrees with by default); **capable of resolving real
decisions** without being so scenario-specific that it only ever applies
once; **opinionated enough to justify saying no** to a proposal that
violates it; and **memorable enough that the team will actually recall and
invoke it** in a real review, rather than needing to look it up every
time.

### A lightweight process for building a set of principles collaboratively

Identify who should weigh in (the people who'll actually use and enforce
the principles), align the group on what a good principle looks like
(the four criteria above), have everyone individually generate candidate
principles first (to avoid groupthink anchoring on the first idea spoken
aloud), then group and vote on recurring themes together, and finally
refine the surviving candidates and circulate the result somewhere the
team will actually see it repeatedly (a shared doc, onboarding material,
even a physical poster) so the principles get used rather than filed
away.

## Part 2 — Responsible design: reading a pattern as manipulation, not just a usability gap

The same ten psychological principles that make products genuinely easier
to use can also be turned against the user's own interest. When an audit
surfaces a pattern that looks like it's shaping behavior *against* what
the user actually came to do, rather than in service of it, name that
explicitly and separately from an ordinary usability finding — the
recommendation for a manipulative pattern is different in kind from the
recommendation for an accidental usability gap.

### Patterns worth flagging explicitly

- **Intermittent variable rewards** — unpredictable reinforcement (pull-
  to-refresh revealing new content, notification badges, algorithmic feed
  refreshes) that mirrors the reinforcement schedule known, from behavioral
  psychology, to produce the most compulsive and difficult-to-extinguish
  repeated-checking behavior — the same underlying mechanism behind slot
  machines.
- **Infinite loops** — autoplay and infinite scroll specifically designed
  to remove the natural stopping point a user would otherwise encounter,
  primarily to maximize exposure to ads or additional content rather than
  to help the user accomplish whatever they actually came to do.
- **Exploited social affirmation** — like/reaction mechanics engineered
  mainly to produce a habitual return-to-check-in behavior, rather than to
  support genuine connection between people.
- **Manipulative personalization** — recommendation systems optimized
  purely for time-on-platform can pull users toward progressively more
  extreme content, or narrow their exposure into a self-reinforcing
  bubble, as a side effect of optimizing the wrong metric.
- **Defaults that don't match user expectations or interest** — pre-set
  options (privacy settings, marketing opt-ins, subscription tiers)
  chosen to benefit the business more than the user, relying on the
  well-documented tendency for people to stick with whatever default
  they're handed rather than actively changing it.
- **Engineered lack of friction on consequential actions** — deliberately
  removing every obstacle from an action specifically to encourage
  habitual, low-consideration spending or sharing, rather than to
  genuinely help the user accomplish an intended task.
- **Reciprocity exploitation** — nudging users toward a sense of social
  obligation (e.g., auto-suggested "invite your contacts" prompts framed
  as generosity) primarily to drive platform growth rather than to serve
  a genuine intent the user already had.
- **Dark patterns / forced action** — blocking completion of a task
  unless the user grants something unrelated (extra data access, a
  marketing opt-in, an unrelated permission) with no real, equally easy
  alternative path.

When these show up, the right recommendation is not "optimize this
further" — it's to name the trade-off plainly, state whose interest is
actually being served, and suggest an alternative that serves the user's
actual goal, even if that costs something on a narrow engagement metric.

### Practical checks for responsible design

- **Beyond the happy path** — does the design account for non-ideal
  scenarios (errors, users in vulnerable circumstances, edge cases) as a
  first-class part of scope from the start, or only as an afterthought
  bolted on after an "ideal user" flow has already shipped?
- **Whose complexity, whose benefit?** — when complexity is shifted away
  from the user (see `teslers-law.md`), check who actually benefits from
  that shift. If it primarily benefits the business at the expense of the
  user's understanding or control — e.g., obscuring what data is being
  collected or how a recommendation was generated — that's a
  responsibility issue layered on top of the UX one, and both should be
  named.
- **Embracing useful friction** — not all friction is bad, and a
  reflexive "remove all friction" instinct can itself be a mistake.
  Friction that prevents costly errors, protects privacy, encourages a
  more considered decision at a high-stakes moment, or discourages
  compulsive use can be the *correct* design choice even though it works
  against a pure friction-minimization metric. Before recommending that
  friction be removed anywhere, check what purpose it might currently be
  serving.

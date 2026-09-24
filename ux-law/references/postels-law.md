# Postel's Law (the robustness principle)

**One-line statement:** Borrowed from early internet protocol engineering
— "be conservative in what you do, be liberal in what you accept from
others." Applied to UX: the system's *output* (the interface, the data it
sends back) should be reliable, predictable, and broadly accessible; the
system's *input handling* should tolerate the messy, inconsistent,
varied ways real humans actually provide information.

## Why it matters (mechanism and origin)

The principle was originally stated for TCP implementations: senders
should conform strictly to protocol specifications, while receivers
should be robust enough to accept and parse nonconformant input as long
as its meaning is still clear. This same fault-tolerant posture is why
HTML and CSS became dominant web technologies — browsers historically
handled authoring mistakes and missing feature support gracefully (ignore
what you don't understand, keep going) rather than failing hard, which
gave the web enormous flexibility to keep working across a huge range of
implementations.

Applied to UX: people are not machines. They're sometimes inconsistent,
frequently distracted, occasionally error-prone, and generally driven by
emotion rather than strict rule-following. They also arrive via wildly
different devices, connections, input methods, assistive technologies,
and cultural conventions. Designing only for an idealized "clean" user on
a single form factor produces something brittle for everyone else — and
"everyone else" is usually most of the actual audience.

## Full audit checklist — accepting input liberally

- **Form field count** — is the system asking for only what's strictly
  necessary to complete the task, or re-requesting information it could
  already have or infer (an email address already on file, a password
  already entered elsewhere in the flow)? Every additional required field
  raises cognitive effort and the risk of **decision fatigue** — a
  measurable decline in decision quality from being asked to decide too
  many things in sequence — and reduces completion likelihood.
- **Cultural/format assumptions** — does a name field assume a single
  ordering convention (given name before family name) when the target
  audience includes cultures where family name is conventionally listed
  first? Does an address field assume one country's standard structure
  (street/city/state/zip) rather than accommodating formats that don't
  map cleanly onto that structure?
- **Overly strict validation** — does the system reject legitimate input
  variants — hyphenated names, names containing spaces, unusually short
  or long but valid names, non-standard-but-real address formats —
  instead of normalizing or accepting them? Strict pattern-matching
  validation is a very common source of Postel's Law violations.
- **Error messaging tone and specificity** — when input is rejected, does
  the message explain *specifically* what's wrong and how to fix it, or
  does it use blunt, impersonal language like "invalid" or "not
  accepted"? Telling someone their own name is "wrong" is a small thing
  that does outsized damage to trust and goodwill at exactly the moment
  they're trying to engage with the product.
- **Input method diversity** — does the design assume mouse-and-keyboard
  only, or does it also genuinely work with touch/gesture input, assistive
  technology (screen readers, switch access), and — where relevant —
  voice input across different languages, dialects, and naming
  conventions?

## Full audit checklist — reliable, adaptable output

- **Responsive behavior** — does the layout genuinely adapt across the
  full range of plausible device sizes (from a smartwatch up through a
  TV-scale display), or is it built and tested for one viewport with
  everything else as an afterthought? Modern responsive design (fluid
  grids, flexible images, media queries) is the default expectation here,
  not an enhancement.
- **Progressive enhancement vs. graceful degradation** — is core content
  and functionality accessible to *everyone* regardless of browser
  feature support, device capability, or connection speed, with
  additional style/interaction layers added *on top* as capability is
  detected (progressive enhancement) — or is the product built
  advanced-first with a stripped-down fallback bolted on afterward
  (graceful degradation)? The former preserves universal access to the
  core experience by construction; the latter treats it as a secondary
  concern. A concrete example of the former: a search box that works with
  a basic click-and-type interaction for everyone, with voice input added
  as an enhancement layer only where the device/browser supports it —
  nobody is denied the core function, some users get an enhanced one.
- **Text expansion / internationalization** — does the layout survive
  translated text that runs significantly longer than the source
  language? English is unusually compact; translated strings in some
  languages can run to roughly 2–3x the original length, and layouts sized
  tightly around English text will visibly break under that expansion.
  Does the layout also account for right-to-left or vertical text
  orientation where relevant, rather than assuming left-to-right always?
- **User-controlled display settings** — does the layout hold up when the
  user increases their system or browser font size (a standard
  accessibility feature), or does content overflow, get clipped, or break
  the layout? A well-adapted design might, for example, reduce the number
  of secondary navigation links shown as font size increases, prioritizing
  the most important ones rather than letting the row overflow or wrap
  awkwardly.
- **Lower-effort accepted input paths** — is there a reduced-effort
  alternative to manual entry (biometric authentication, autofill, saved
  payment methods) offered *alongside* the manual path, without removing
  the manual path as an option for people who can't or don't want to use
  the alternative?

## Common mistakes when applying this law

- **Treating "liberal input" as "no validation."** The point isn't to
  accept literally anything — it's to accept the real range of *valid*
  human input instead of an artificially narrow subset of it, and to
  normalize/translate liberally-accepted input into a clean internal
  format rather than rejecting anything slightly off-pattern.
- **Fixing input handling but leaving output rigid.** Both halves of the
  principle matter — a form that accepts messy input but then renders an
  inflexible, non-responsive confirmation screen has only solved half the
  problem.
- **Assuming "we don't have international users" as a reason to skip
  internationalization checks.** Audiences shift over time, and text-
  expansion/format issues often surface long before an explicit
  international launch is planned.

## How to phrase recommendations

Frame fixes as a trade: reduce what's demanded of the user (fewer
required fields, flexible accepted formats, forgiving validation with
specific and kind error messaging, multiple supported input methods)
while keeping the system's own behavior consistent, predictable, and
reliable regardless of what's thrown at it. Where complexity has to exist
somewhere to support that flexibility (parsing varied input formats,
adapting layouts to text expansion), that's expected and correct — see
`teslers-law.md` for how to reason about exactly where that complexity
should live once it's been shifted off the user.

## Precise reference points (origins, research, technique)

- **Origin:** Computer scientist Jon Postel introduced the "robustness
  principle" in the specification for an early implementation of TCP
  (Transmission Control Protocol) — the foundational protocol for how
  data is sent and received across a network — stating that
  implementations should be conservative in what they transmit and
  liberal in what they accept from others, so long as the meaning of
  nonconformant input is still clear. This same tolerant, fault-forgiving
  posture is part of why loosely-error-handled declarative languages like
  HTML and CSS became so dominant on the web: a browser that doesn't
  understand a particular bit of markup or a missing feature can simply
  ignore it and keep rendering the rest, rather than failing outright.
- **Decision fatigue:** asking for more input than necessary doesn't just
  cost time — each additional required decision measurably degrades the
  quality of subsequent decisions in the same sequence, a well-documented
  effect known as decision fatigue. This is the mechanism-level reason
  "ask only for what's strictly necessary" is more than a vague
  minimalism preference — it's a direct lever on completion rate and
  decision quality.
- **Concrete cultural/format issues worth naming specifically in an
  audit:** given-name-first versus family-name-first ordering conventions
  vary by culture, and a form that hard-codes one ordering as the default
  can be genuinely confusing for users from a culture where the other
  ordering is standard; address forms built rigidly around one country's
  standard structure (street / city / state-province / zip-postal code)
  can fail to accommodate address formats that don't map cleanly onto
  that structure; and overly strict name-field validation can reject
  legitimate hyphenated names, names containing spaces, or unusually
  short or long (but real) names.
- **Face ID as a "liberal input" example:** biometric authentication (like
  Apple's Face ID) is a concrete example of accepting a lower-effort input
  method — a glance — as an alternative to manually typing a username and
  password each time, without necessarily removing the manual path
  entirely for people or situations where it doesn't work.
- **Responsive web design, named specifically:** the term and approach
  ("fluid grids, flexible images, and media queries," to build layouts
  that adapt smoothly to different viewing contexts rather than requiring
  separate device-specific builds) was introduced by Ethan Marcotte in
  2010 and is now the de facto baseline expectation for building anything
  on the web.
- **Progressive enhancement vs. graceful degradation, named specifically:**
  progressive enhancement — building for universal access to core content
  and functionality first, then layering on additional style and
  interaction as browser/device capability is detected — was introduced
  as a named strategy by Steve Champeon and Nick Finck at a 2003
  conference talk. It stands in contrast to the older "graceful
  degradation" approach, which starts from the most advanced
  software/hardware and treats less capable devices as an afterthought
  fallback. A concrete example: a basic search box that works for
  literally everyone by default (click and type, including via assistive
  technology like screen readers), with voice input layered on only where
  the device/browser actually supports it — nobody is denied the core
  function, some users additionally get an enhanced one.
- **Text expansion in internationalization:** English is an unusually
  compact language; translated UI strings in some target languages can
  run up to roughly 300% longer than the English source — a layout sized
  tightly around English text will visibly break under that expansion if
  it wasn't designed with the possibility in mind. Text direction also
  varies by region (left-to-right, right-to-left, or vertical), which
  needs to be accounted for architecturally, not patched in after launch.
- **Design systems as an organizational-scale example:** a design system
  (a shared library of reusable components, patterns, and standards) only
  works if the *input* side stays liberal — accepting design, content,
  code, strategy, and critique from a genuinely diverse set of
  contributors — while the *output* side stays conservative: the
  published guidelines, components, and principles need to be clear and
  purposeful so the system can be relied on consistently across an
  organization.

### Technique: User Interviews

A user interview is a focused one-on-one research session in which a
researcher asks a participant about a specific topic (system use,
behaviors, habits) to surface insights — including what's memorable, what
matters most, and ideas for improvement. Interviews can happen before a
design is built, as part of a broader contextual inquiry, or at the end
of a usability test to capture verbal reflection on observed behavior. A
well-run interview: **defines a concrete goal** first (a goal like "learn
more about our users" is too broad to produce actionable insight; a goal
like "learn how a specific group shares a specific kind of information
with each other, and where the friction is" is specific enough to act
on); **prepares a discussion guide** in advance built around that goal,
while staying open to following genuinely useful tangents rather than
rigidly sticking to a fixed question list; **builds rapport** early (ask
about the participant themselves, reassure them there are no right or
wrong answers, and make clear the session tests the design, not their own
knowledge or ability); and **avoids leading or closed questions** — favor
open prompts starting with "what," "how," "when," or "tell me about," and
stay conscious of how the framing of a question can itself bias the
answer.

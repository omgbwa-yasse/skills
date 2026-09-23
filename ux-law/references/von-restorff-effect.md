# Von Restorff Effect (isolation effect)

**One-line statement:** When several similar items are presented together,
the one item that visually or conceptually differs from the rest is the
one people notice and remember. Contrast — through color, shape, size,
position, or motion — draws and holds attention faster than any of those
properties applied uniformly across every element.

## Why it matters (mechanism and related concepts)

Attention, like working memory (see `millers-law.md`), is a limited
resource. People filter out whatever doesn't look relevant to their
current goal — this filtering is called **selective attention** — which
is exactly why a single, genuinely distinctive element can cut through
that filter while a page full of equally emphasized elements cannot: if
everything is emphasized, the filtering mechanism has nothing to
distinguish, and effectively nothing is emphasized.

Two related phenomena are worth checking for explicitly, because they can
cause a "make it stand out more" recommendation to fail for reasons that
have nothing to do with the emphasis technique itself:
- **Banner blindness** — people learn, through repeated exposure, to
  ignore anything that visually resembles an ad (position, size, styling
  conventions), and this learned ignoring generalizes to *legitimate*
  content that happens to share those visual patterns, not just to actual
  ads.
- **Change blindness** — people fail to notice a change entirely if the
  visual cue signaling that change is too weak, or if their attention is
  focused elsewhere when the change occurs.

## Full audit checklist

- **Is there exactly one thing meant to stand out per screen or moment,
  and does it actually stand out?** Count the competing points of
  emphasis on the surface under review before evaluating any single one
  in isolation — multiple simultaneous "most important" elements dilute
  each other's effectiveness, even if each one would work fine alone.
- **Destructive or high-stakes actions** — is the consequential option
  (delete, confirm an irreversible action, submit a payment) visually
  differentiated from neighboring, lower-stakes options, or does it share
  the same visual treatment as everything around it, inviting the exact
  kind of accidental selection that Fitts's Law also warns about for
  closely spaced targets?
- **Risk of being mistaken for an ad** — does emphasized content sit in a
  position, size, or style pattern typically associated with advertising
  (near actual ads, boxed with an ad-like treatment, in a traditionally
  ad-heavy zone of the layout)? If so, banner blindness may cause users to
  tune it out regardless of how much visual weight it carries.
- **Notifications and pricing/plan comparison tables** — is the featured
  or recommended option differentiated through more than one reinforcing
  channel (color *and* size *and* position together), or through a single
  weak cue that's easy to miss at a glance?
- **Accessibility of the contrast mechanism itself** — this is a frequent
  gap in otherwise-reasonable emphasis choices:
  - **Color-only differentiation** excludes users with color vision
    deficiency or low vision entirely — check that a second, non-color
    cue (shape, icon, text label, pattern, underline, border style) carries
    the same meaning independently of color.
  - **Text/background contrast ratio** — flag anything that looks
    visibly low-contrast; common accessibility guidance targets roughly a
    4.5:1 contrast ratio for normal-size text and roughly 3:1 for larger
    or bold text.
  - **Motion-based emphasis** (animated highlighting, pulsing, sliding
    attention-grabbers) can trigger real physical discomfort for users
    with vestibular disorders, migraines, or photosensitive epilepsy —
    check that motion is never the *only* channel carrying the emphasis,
    and that it can be reduced or disabled (respecting a
    reduced-motion preference where the platform supports one).

## Common mistakes when applying this law

- **Recommending more contrast as a first instinct without auditing
  existing emphasis first.** If a page already has several competing
  "important" elements, adding yet another loud element usually makes the
  overall hierarchy worse, not better — the fix is often to *remove*
  emphasis from lower-priority elements rather than add it to a new one.
- **Relying on a single differentiation channel.** Color alone is the
  most common single-channel mistake and the most consequential for
  accessibility.
- **Assuming louder always wins.** If genuinely emphasized content is
  still being ignored, check for a banner-blindness explanation (does it
  look like an ad?) before assuming the visual treatment itself needs to
  be stronger — making an ad-adjacent element louder often makes banner
  blindness worse, not better.

## How to phrase recommendations

- Recommend restraint *before* recommending additional contrast — audit
  how many things on the page are already competing for "this is
  important" attention before adding one more.
- When recommending emphasis for a specific element, specify at least two
  reinforcing, non-color-dependent cues so the distinction survives for
  users with color vision deficiency, low vision, or motion sensitivity —
  never recommend color as the sole differentiator for anything
  functionally important.
- If emphasized content is being overlooked, check for an ad-resembling
  placement or style before recommending a louder visual treatment — the
  actual fix may be relocating it away from ad-adjacent conventions, not
  amplifying it in place.

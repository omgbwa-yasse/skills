# Fitts's Law

**One-line statement:** The time it takes to reach and accurately select a
target is a function of the distance to it and its size. As targets get
bigger, selection time drops; as targets get closer, selection time drops.
The inverse is equally true: small, distant targets take longer to select
accurately and produce more errors.

## Why it matters (mechanism and origin)

Fitts's Law originates from 1950s human-motor research (Paul Fitts, 1954)
that modeled how long it takes to point at a physical target as a ratio of
distance to target width. It predates graphical interfaces entirely but
maps directly onto pointer- and touch-based interaction.

A formative real-world case behind this line of research: wartime aircraft
accidents were traced not to "pilot error" in the vague sense but to
identical-feeling flap and landing-gear controls being confused under
stress. The fix — giving controls distinct shapes so they could be told
apart by feel alone — helped found the discipline of *human factors*:
designing for how people actually behave (including when distracted,
stressed, or rushed), rather than assuming an idealized, careful user.
That framing matters for every audit under this law: target-sizing
mistakes are not just inconvenient, they compound under real-world
conditions (moving vehicle, one-handed phone use, low light, motor
impairment).

Three guidelines fall directly out of the law:
1. Touch/click targets must be large enough to discern and accurately
   select.
2. Targets must have adequate spacing between them.
3. Targets must be placed where they're easy to *reach*, not just where
   they're easy to see.

## Full audit checklist

- **Target size** — is every tappable/clickable element at or above a
  reasonable minimum? Published platform minimums cluster in a similar
  range (roughly 44×44 px on touch interfaces, a bit larger for spatial/
  VR interfaces, similar figures in accessibility guidelines) — treat
  these as a floor to check against, not a number to hit exactly and stop.
  Prefer exceeding the minimum wherever layout allows, since sizing above
  the floor reduces the *precision* users need to supply, not just the
  probability of a miss.
- **Perceived usability, not just measured accuracy** — note that small
  targets make an interface *feel* less usable even in cases where users
  technically avoid errors; this is worth flagging even when raw error
  rate looks acceptable.
- **Spacing between targets** — is there enough gap between adjacent
  interactive elements that an imprecise tap or click doesn't land on the
  wrong one? This matters most for elements with *different* or opposing
  consequences sitting next to each other (Accept/Deny, Delete/Cancel,
  Confirm/Undo). A concrete reference point: average adult fingertip
  contact area runs in the range of ~16–20mm, so touch targets closer
  together than that are at real risk of overlap error.
- **Placement / reachability** — is the target inside a zone that's
  actually easy to reach for the likely input method and device?
  - On mobile, one-handed thumb reach is not uniform across the screen:
    the center is typically the most accurate zone, while far corners
    (especially the top corners, opposite the holding hand) are the
    least accurate — and this asymmetry is often invisible unless you
    specifically check for it.
  - On desktop, cursor movement is less reach-constrained, but distance
    still costs time, so frequently used controls shouldn't be placed
    unnecessarily far from where the user's attention/cursor naturally
    sits.
- **Proximity between an input and its action** — is a submit/confirm
  button placed near the last relevant input rather than far away
  (top of page, opposite corner), minimizing travel distance and
  reinforcing the visual relationship between the two?
- **Label-to-input association** — does clicking or tapping a form field's
  label also focus/activate the input (native HTML `<label for>`
  behavior, or its equivalent)? This effectively expands the usable
  target area for free.
- **Edge and infinite targets** — are frequently used controls placed at
  screen edges or corners where the edge of the screen or window acts as
  a natural stopping wall, removing the need for precise stopping (e.g.,
  an OS-level menu bar pinned to the very top or bottom edge)? Infinite
  targets are a good place to put high-frequency actions because
  overshooting doesn't cost anything — the boundary catches the cursor.
- **Spatial/eye-tracking interfaces** — if the surface is a spatial
  computing or gaze-based interface, check that primary content sits
  within the natural center of the field of view relative to the user's
  head, that interactive content stays at a consistent depth (avoiding
  forced refocusing), and that interactive elements use rounded rather
  than sharp-edged hit areas, since sharp corners tend to pull gaze toward
  the edge and reduce targeting precision.
- **Non-screen contexts** — for in-vehicle or embedded touchscreen
  controls with no haptic feedback, check whether critical controls
  require the user to look away from a primary task (e.g., the road) to
  acquire them, and whether physical/haptic alternatives exist for the
  most safety-critical actions.

## Common mistakes when applying this law

- **Treating the platform minimum as a target to hit exactly rather than a
  floor.** Meeting the bare minimum is not the same as good sizing —
  recommend exceeding it where layout allows.
- **Only checking size, never spacing.** A target can be large enough on
  its own and still be effectively unusable if it's crammed against a
  neighbor with different consequences.
- **Ignoring device/context asymmetry.** A "central" placement on a
  desktop review might land in the least reachable zone on a one-handed
  mobile session — always ask which input method and device the flow will
  actually be used on.
- **Recommending bigger targets everywhere indiscriminately.** Size and
  spacing cost layout space; prioritize the fix for high-frequency and
  high-consequence targets first, not every element uniformly.

## How to phrase recommendations

Phrase recommendations in terms of the actual, concrete consequence
rather than a vague call to "improve spacing": "users will occasionally
tap Accept when they meant to tap Deny because both are ~24px icons with
only ~4px between them" is far more actionable for a design team than
"improve spacing." Where destructive and non-destructive actions sit next
to each other, recommend either separating them physically (different
regions of the screen, not just a few extra pixels) or differentiating
them strongly on more than one dimension (size, color, and position
together) — a single weak cue is not enough for a high-stakes pair of
actions.

# Miller's Law

**One-line statement:** Short-term / working memory can hold only a
limited number of "chunks" of information at once — commonly cited as
"7 ± 2," though later research suggests the practical number is often
closer to 4, and some researchers argue against a fixed number altogether.
The number itself matters far less than the underlying mechanism:
**chunking**, not a hard item-count ceiling, is the actionable takeaway.

## Why it matters (mechanism and the most common misapplication)

Miller's original 1956 paper observed that memory span in young adults
was limited to roughly seven items *regardless of the type of stimuli* —
which led to the conclusion that it's the number of **chunks** (grouped,
familiar units), not the number of raw bits, that constrains short-term
memory. Miller himself used "the magical number seven" rhetorically and
was reportedly surprised how literally it got taken.

**This is the single most misapplied law in UX design.** It gets cited to
justify rules like "navigation must have no more than seven items" — but
that reasoning doesn't hold. Design patterns like navigation menus,
filter lists, or option grids don't require the user to *memorize* the
choices; the choices stay visible on screen the whole time. There is no
memory-span constraint on something a user can simply look at and scan.
The relevant cognitive load in those cases comes from *decision-making*
among visible options (see Hick's Law) or from *scanning/parsing* dense
visible content (which chunking genuinely helps with) — not from holding
items in short-term memory.

Treat "Miller's Law says we can't have more than 7 nav items" as a red
flag phrase in any conversation — it signals the *mechanism* is being
misunderstood even if the underlying instinct (avoid overwhelming users)
is reasonable.

## What actually follows from the law: chunking

Group related content and objects together, and use color, scale,
dividers, whitespace, and physical proximity to make each group visually
distinct from the others. This lets users scan the content, identify
which grouped section aligns with their current goal, and consume only
that section — rather than parsing a flat, undifferentiated stream. This
applies regardless of the total item count on the page.

## Full audit checklist

- **Unformatted long strings** — phone numbers, reference codes, IDs, long
  numeric identifiers, or dates shown as a raw, unbroken string of digits
  instead of grouped into readable segments (compare `4408675309` to
  `(440) 867-5309` — same information, very different scan/recall cost).
- **Walls of text** — long paragraphs with no headings, no visual
  hierarchy, and line lengths that run edge-to-edge on wide viewports;
  hard to scan even when the underlying content is perfectly fine.
  Improvements typically include: added headings/subheadings, whitespace
  breaking content into discernible sections, shortened line length,
  underlined or otherwise marked links, and highlighted key terms for
  contrast against surrounding text.
- **Dense listings** (product grids, article feeds, dashboards,
  spreadsheet-like views) — is related information for a single item
  (image, title, price, type, metadata) grouped by proximity even without
  an explicit border or background, so it reads as one unit rather than a
  scatter of disconnected fields? Are distinct groups (filters,
  categories, sidebar sections) visually separated from each other?
- **Toolbars and multi-function controls** — are functionally distinct
  clusters of controls (e.g., page controls, text formatting controls,
  insert controls, alignment controls) separated by dividers or spacing
  gaps, or dumped into one undifferentiated row where every icon reads as
  equally related to every other?
- **Navigation menus with many items** — if the item count is large,
  check whether there's clear categorization (grouped headers, whitespace,
  vertical dividers between sub-groups) making it scannable despite the
  count, rather than assuming a large count is itself the problem. A
  navigation menu with several dozen links can be entirely usable if it's
  well-chunked; a navigation menu with six links can still be confusing if
  they're not visually organized.
- **Forms with many fields** — are related fields (e.g., all address
  components, all payment components) visually grouped into sub-sections
  with headers, rather than presented as one continuous undifferentiated
  list of inputs?
- **Data tables / dashboards** — are columns and rows grouped logically
  (related metrics adjacent, totals/summaries visually separated from
  raw data), or is every cell given equal visual weight regardless of its
  relationship to neighboring cells?

## Common mistakes when applying this law

- **Using it to cap the number of visible options.** As covered above,
  this is a mechanism mismatch — if the concern is genuinely about too
  many *choices* to decide among, that's Hick's Law's territory, not
  Miller's.
- **Assuming chunking has a "correct" group size.** There's no fixed
  number of items per chunk that's universally right; the goal is
  meaningful, recognizable groupings, not adherence to a magic number.
- **Applying chunking only to text.** Chunking is equally relevant to
  visual/UI density (toolbars, product grids, dashboards) — it's not just
  a copywriting or typography technique.
- **Ignoring individual variation.** Actual working-memory capacity varies
  by person, by familiarity with the content, and by the complexity of
  the material — treat any number as a rough approximation, not a
  precise per-user constant.

## How to phrase recommendations

Never recommend "cut the number of items to seven" as a standalone fix —
that's the exact misreading this law is known for, and a design team that
hears it will implement the wrong thing. Instead recommend chunking:
group by relationship, add visual separation between groups (dividers,
whitespace, background shifts, consistent proximity rules), and apply
formatting (in text) or spacing/grouping (in UI) to reduce the *scanning*
effort rather than the raw count. If the underlying complaint is actually
about *decision* difficulty among a large set of visible choices rather
than a scanning/parsing problem, redirect to `hicks-law.md` — the two
are frequently confused but call for different fixes.

# .docx style guide — apply only when the user asks for a Word file

Read `/mnt/skills/public/docx/SKILL.md` first. This guide applies on top of it, unless the user's
organisation imposes its own graphic charter — in which case theirs prevails: ask before generating.

---

## File structure — budget dossier / reforecast memo

```
Header
  → Title, period covered, owner, date

Summary                                (RAG-style if tracking, one paragraph if a build)
Budget build or variance table         (the core table)
Reforecast (if applicable)             (new total, explanation, options)
Approval block                         (if the dossier requires sign-off)
```

## Styles

| Element | Value |
|---------|-------|
| Body text | Arial or Calibri 11 pt |
| Budget table header row | Bold, light grey fill |
| Totals row | Bold, top border rule |
| Unfavourable variance | Red text or light red fill on the variance figure only — not the whole row |
| Favourable variance | No colour by default; colour only if the organisation's convention expects it |

## Layout rules

- Currency values right-aligned, consistent decimal places throughout the table.
- Wide budget tables (many columns) go landscape rather than shrinking font below 9 pt.
- Totals always visible without scrolling horizontally — freeze the leftmost label column in the
  Excel companion if one exists.

## File naming

`budget_[scope]_[period]_[YYYY-MM-DD].docx`
`reforecast_[scope]_[YYYY-MM-DD].docx`
</content>

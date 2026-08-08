# .docx style guide — apply only when the user asks for a Word file

Read `/mnt/skills/public/docx/SKILL.md` first. This guide applies on top of it, unless the user's
organisation imposes its own graphic charter — in which case theirs prevails: ask before generating.

---

## File structure

```
Cover page
  → Institution letterhead (logo if supplied, otherwise a reserved area)
  → Document type + full purpose statement
  → Version and date
  → Confidentiality marking if applicable

Revision and approval table

Table of contents — automatic, with clickable links

List of acronyms                       (if the section is retained)
List of tables and figures             (if the section is retained)

Executive summary                      (new page)
Summary sheet

Body — sections in reading order

Annexes                                (new page per annex)
Bibliography
```

## Styles

| Element | Value |
|---------|-------|
| Body text | Arial or Calibri 11 pt, line spacing 1.15, justified |
| Heading 1 (section) | 16 pt bold, primary colour, page break before |
| Heading 2 (subsection) | 13 pt bold, primary colour |
| Heading 3 | 11.5 pt bold, accent colour |
| Primary colour | `#1A3C6E` |
| Accent colour | `#2E86C1` |
| Table header row | Fill `#1A3C6E`, white bold text |
| Alternating table rows | `#F2F3F4` / `#FFFFFF` |
| To-be-completed zones | Highlight `#FDEBD0`, kept visible in the delivered file |
| Captions | 9 pt italic, above or below the exhibit |
| Page header | Abbreviated objet of the document |
| Page footer | Version · date · page number / total |

## Layout rules

- Automatic hierarchical numbering of headings (1, 1.1, 1.1.1) — three levels maximum.
- Every table carries a numbered caption ("Table n: …"), placed consistently throughout.
- Wide tables (11-column methodology, cost) go into a dedicated landscape section rather than being
  shrunk to 7 pt.
- To-be-completed zones stay **visible and highlighted** in the delivered file: they are information
  for the recipient, not a defect to hide.
- The signature table in the revision and approval section has rows tall enough for a handwritten
  signature.
- No colours outside the charter inside tables: legibility in black-and-white print remains a
  criterion, since most of these documents are printed for signature.

## File naming

`[TYPE]_[abbreviated-subject]_v[version]_[YYYY-MM-DD].docx`

Example: `TDR_archive-room-fitout_v1.0_2026-08-07.docx`

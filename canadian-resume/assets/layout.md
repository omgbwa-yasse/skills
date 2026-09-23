# Layout specification

Formatting for a Canadian résumé that a parser can read and a human wants to read. Use these values with the `docx` skill.

## Page

- US Letter (8.5 × 11 in). Canadian employers print on Letter, not A4
- Margins: 0.6 to 0.75 in on all sides. Below 0.5 in the page looks crowded and some printers clip it
- Single column throughout. No tables, no text boxes, no sidebars
- Nothing meaningful in headers or footers. Many parsers discard them. A page number in the footer is acceptable on a two-page résumé

## Type

- One font, two at most. Calibri, Arial, Helvetica, Georgia, and Garamond all parse reliably. Avoid decorative and condensed faces
- Body: 10 to 11 pt
- Name: 15 to 17 pt, bold
- Tagline under the name: 10 to 11 pt, grey
- Contact line: 9 pt
- Section headings: 10 to 11 pt bold, with a thin rule underneath. Variant A favours sentence case, which reads as more current; Variant B sets them in caps or bold with the rule running to the right margin, as the institutional templates do. Both parse fine
- Line spacing: 1.10 to 1.20. Below 1.0 the page becomes hard to scan

## Spacing

- 12 to 14 pt above each section heading, 5 pt below
- 7 pt above each job entry
- 3 pt between bullets
- Consistent throughout. Uneven spacing is the most visible sign of a document assembled in a hurry

## Bullets

- Real list formatting with a bullet character supplied by the list definition. Never type a bullet glyph or a hyphen at the start of a line
- Indent 0.25 in with a 0.18 in hanging indent so wrapped lines align under the text rather than the bullet

## Job entry line

One line carrying all four facts, so a screener finds them in the same place every time:

```
Job title, Employer, City   |   2023 – 2024
```

Bold the job title, leave the employer and city in regular weight, and set the dates in grey.

An alternative used throughout Franco-Ontarian and Québec templates puts the job title at the left of the line and the dates flush right, with the employer and city on a second line in italics. Either works; the requirement is that all four facts sit in the same place in every entry so the eye can find them without searching. Right-aligned dates need a right tab stop, not spaces — spaces collapse when the file is parsed. Do not use an em dash as a separator between fields — it is harder to scan than a vertical bar and, used repeatedly, gives the document a generated look.

## Sections that span a page break

Variant B repeats the heading on the next page with "(suite)"; Variant A does not repeat it. Under either, never let a job entry split so that its title sits on one page and its bullets on the next.

```
HISTORIQUE DE TRAVAIL (suite)
```

The repeated heading tells a screener holding page two what they are looking at, which is why the institutional templates use it. Variant A omits it because a parser reads the repeat as a second section.

## Colour

Black or near-black body text. One restrained accent, if any, for section rules and dates. Coloured backgrounds and shaded blocks defeat parsers and waste ink.

## File

- .docx unless the posting asks for PDF. Some parsers still handle .docx better
- Name the file `Firstname_Lastname_Resume.docx`, or add the target role when sending several versions: `Firstname_Lastname_Records_Analyst.docx`
- Check the document properties. An author field carrying someone else's name is a bad first impression

## Verify before delivering

Render the finished document to an image and look at it. Check that nothing broke across the page boundary mid-entry, that spacing is even, that no bullet is orphaned at the top of page two, and that the second page is not carrying two lines that should have fit on the first.

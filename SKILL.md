---
name: "bup-termpaper-format"
description: "Use when writing or formatting a BUP (Bangladesh University of Professionals) FBS term paper as a Word file, including reformatting an uploaded draft: cover, letter of transmittal, acknowledgement, TOC, roman/arabic page numbering and APA 7 citations and references."
---

# BUP term paper format

The house format for group term papers in the Faculty of Business Studies (FBS), Bangladesh University of Professionals. It was first used for the Cost and Management Accounting (ALD 2203) paper, Group 2. Deliver a .docx in this format (built with docx-js), then render it to PDF and look at every page before sending it.

## Step 1: Ask before building

Before writing anything, ask the user for the following in one message (or one AskUserQuestion round plus free text). Do not guess or reuse old details unless the user confirms them.

1. **Course:** the course name and code, e.g. Cost and Management Accounting (ALD 2203).
2. **Instructor:** the name, designation (e.g. Assistant Professor), department, and whether to address them as Sir or Madam.
3. **Group members:** the group number, plus every member's full name and student ID, in the order they should appear.
4. **Title of the term paper:** the full title for the letter and acknowledgement, and the shorter topic line for the cover if it differs.
5. **Submission date.**
6. **Any other changes:** ask whether anything in this format should be different for this paper, such as the section structure, colours, page numbering, the letter or acknowledgement wording, extra parts (e.g. an introduction or appendix), or the citation style. Apply whatever they say over the defaults below.

If the user has already given some of these in the conversation, only ask for what's missing. Then confirm the details back in one short line and start.

Do not ask for the BUP logo. If the user has attached a logo image (in this chat or a file they point to), use it on the cover. If not, leave the logo out and mention that in one line when you deliver the file. Never draw or fetch a logo yourself.

## When the user uploads a draft

If the user uploads a term paper draft (.docx, or text they paste), format it rather than rewrite it:

1. **Keep their content.** Keep every word, number, table and section of the draft as written, in the same order. Do not rewrite, shorten or "improve" the text. Only fix obvious formatting problems (stray spaces, broken line breaks, inconsistent numbering of headings).
2. **Body text:** set all body text (paragraphs and list items) to Times New Roman 12 pt, 1.5 line spacing, justified, no first-line indent, 8 pt after each paragraph.
3. **Titles and headings are excluded from the 12 pt rule.** Give them exactly the sizes and styles in "Styles used in the CMA term paper" below: front-matter titles 14 pt bold blue centred; Heading 1 15 pt bold blue; Heading 2 13 pt bold blue; Heading 3 12 pt bold italic blue; no line under any heading. Tables, table notes and page numbers also follow that table.
4. **Add the front matter** using the details from Step 1: the cover page, Letter of Transmittal, Acknowledgement and Executive Summary (if the draft has none, write one from the draft's own content), then the Table of Contents built from the draft's headings with real page numbers. If the draft already has any of these parts, replace them with the versions in this format but keep any wording the user wrote in them.
5. **Apply APA 7 citations and references** following "APA 7 citations and references" below. Fix the format of citations and reference entries the draft already has (brackets, "&" versus "and", et al., italics, hanging indent, alphabetical order), but never add a source the draft does not use. List any citation that has no matching reference (or the other way round) in your reply, instead of guessing.
6. **Apply the roman and arabic page numbering** described under "Document order and page numbering": no number on the cover or contents page, i, ii, iii for the front matter, and 1, 2, 3 for the body, all at the bottom centre.
7. Deliver the result as a new .docx and leave the original upload unchanged. In one line, list what was added (for example the cover, letter and contents page) and anything that could not be formatted automatically.

## Document order and page numbering

Each part starts on a new page.

| Part | Page number |
| --- | --- |
| Cover page | None |
| Letter of Transmittal | i (lower-case roman, bottom centre) |
| Acknowledgement | ii |
| Executive Summary | iii |
| Table of Contents | None |
| Body (1. ... to References) | Arabic, starting at 1, bottom centre |

Numbering rules (from the CMA term paper):

- The cover has no number, and it does not count towards the roman numbers.
- Roman numerals (i, ii, iii) start at i on the Letter of Transmittal and run through the Acknowledgement (ii) and Executive Summary (iii). If the front matter is longer, keep counting (iv, v, ...).
- The Table of Contents page has no number.
- Arabic numerals (1, 2, 3) restart at 1 on the first body section (e.g. 1. Case) and run to the last page of the References.
- Every number is in the footer, bottom centre, Times New Roman 11 pt. Never put page numbers in the header, and never number the cover or the contents page.
- In the Table of Contents, the front-matter entries show their roman numbers and the body entries show their arabic numbers.

In docx-js, use four sections: cover (empty footer), front matter (footer with a centred PageNumber.CURRENT, pageNumbers start 1, format LOWER_ROMAN), table of contents (empty footer), and body (footer with a centred page number, start 1, format DECIMAL).

The table of contents lists Letter of Transmittal, Acknowledgement, Executive Summary, then every main section and its sub-sections, with dot leaders and the real page numbers. Work out those page numbers by converting the docx to PDF, finding each heading's page and reading the number printed in that page's footer. Rebuild and repeat until the numbers stop changing.

The default body structure (CMA paper) is: Executive summary, Table of contents, 1. Case (story, exhibits, questions), 2. Theoretical overview, 3. Solution, 4. Conclusion, References. If the user gives a different structure, follow theirs exactly.

## Cover page (no page number)

Everything is centred, in black only, with no colour accent. From top to bottom:

1. BUP logo, about 185 x 207 px (only if the user supplied one)
2. **Faculty of Business Studies** (bold, 14 pt)
3. Department of Business Administration in Finance and Banking (or the user's department)
4. **Term Paper** (bold, 16 pt)
5. **Course:** then the course name and code on the next line
6. **Topic:** then the topic on the next line (bold, 13 pt)
7. **Submitted to:**, then **instructor name** (bold), designation, department, Bangladesh University of Professionals, each on its own line
8. **Submitted by: Group N**
9. A two-column Name / ID table with thin black borders on every cell and a bold header row, centred
10. **Submission Date:** followed by the date, e.g. 9 November 2026

The whole cover must fit on one page, so adjust the spacing if it spills over.

## Letter of Transmittal (page i)

Use single-ish spacing (about 1.15) and this exact layout:

```
Letter of Transmittal            (centred title)

<date>

To,
<Instructor name>
<Designation>
<Instructor's department>
Faculty of Business Studies (FBS)
Bangladesh University of Professionals

Subject: Submission of term paper titled "<full title>"      (bold)

Dear Madam,      (or Sir)

We, the undersigned, students of the Department of Finance and Banking at Bangladesh University of Professionals (BUP), would like to humbly state that the term paper titled "<full title>" has been prepared by us as part of our academic requirement. The paper presents <one sentence on what the paper does and its main source>. We confirm that this work is original and free from plagiarism. We gladly anticipate your comments to correct any flaws in our term paper.

Sincerely,

<Name> - <ID>
Sign: ____________________
(repeat the name and Sign line for every member)
```

## Acknowledgement (page ii)

Use five justified paragraphs, adapted to the paper:

1. All praise to the Almighty for granting us the strength, patience and determination to complete this term paper titled "<title>."
2. Heartfelt gratitude to the course instructor (designation and name) for valuable guidance, constructive feedback and continuous support; say how it shaped the group's understanding of the topic. Use her/his to match the instructor.
3. Thanks to the department, BUP, for the opportunity to prepare the paper as part of the curriculum.
4. Appreciation of team members for teamwork, cooperation and dedication; without mutual support the paper would not have been possible.
5. Gratitude to the authors cited, naming the main textbook authors whose concepts and figures were used.

## Executive Summary (page iii)

Write two or three short paragraphs: what the paper does, which topics the questions cover, and the key answers with their numbers. Do not repeat the questions themselves.

## Body formatting

- Times New Roman 12 pt for body text, 1.5 line spacing, justified, with about 8 pt of space after each paragraph.
- **Never indent the first line of a paragraph.** The user has asked for this strongly.
- A4 page, 1-inch margins.
- Use the exact styles from the CMA term paper, listed in the table below. Do not put a line or border under headings. Start each main section on a new page.
- Blue accent (#1F4E79) goes in the body and front-matter titles only, never on the cover.
- Tables have borders on every cell, a header row that repeats on each page, and rows that do not split across pages. Fix column widths so short headings and numbers do not wrap.

### Styles used in the CMA term paper (copy these exactly)

| Element | Font and size | Style | Alignment and spacing |
| --- | --- | --- | --- |
| Body text | Times New Roman 12 pt | Regular, black | Justified, 1.5 line spacing, 8 pt after, no first-line indent |
| Front-matter titles (Letter of Transmittal, Acknowledgement, Executive Summary, Table of Contents) | Times New Roman 14 pt | Bold, blue #1F4E79 | Centred, 18 pt after |
| Heading 1 (1. Case, 2. Theoretical Overview, 3. Solution, 4. Conclusion, References) | Times New Roman 15 pt | Bold, blue | Flush left, 12 pt after, new page, no underline |
| Heading 2 (e.g. 2.1, Solution to Q1, Exhibits, Questions) | Times New Roman 13 pt | Bold, blue | Flush left, 14 pt before, 6 pt after |
| Heading 3 (e.g. 1. Cost classification) | Times New Roman 12 pt | Bold italic, blue | Flush left, 10 pt before, 5 pt after |
| Question lines (Q1. ...) | Times New Roman 12 pt | Bold (question), regular (member) | Kept with the next line |
| Table label (Table 1 / Exhibit 1) | Times New Roman 12 pt | Bold, blue | Above the table |
| Table title | Times New Roman 12 pt | Italic, Title Case | Under the label, above the table |
| Table text | Times New Roman 11 pt (10 pt for 5–9 columns, 9 pt for 10+ columns) | Header row bold blue on light-blue shading #DEEAF6 | Thin light-blue borders #8EAADB on every cell; numbers centred or right, text left |
| Table note (*Note.* ...) | Times New Roman 10 pt | *Note.* in italics, then plain text with the APA citation | Under the table, justified |
| Equations and formulas | Times New Roman 12 pt | Left side italic | Centred on their own line |
| References | Times New Roman 12 pt | Book titles in italics | Hanging indent 0.5 inch, 1.5 spacing, alphabetical |
| Page numbers | Times New Roman 11 pt | Regular | Footer, bottom centre |
- Under each exhibit or solution table, put an APA *Note.* with an in-text citation including the problem and page, e.g. *Note.* Adapted from Problem 2-45 (Datar & Rajan, 2018, p. 64).
- The theoretical overview is plain prose paragraphs explaining each concept: no tables and no bullet points.
- Write like a student group, not like AI: plain sentences, no dramatic framing, and no repeated summary lines.
- Cite and reference in APA 7th edition, following the rules in "APA 7 citations and references" below.

## APA 7 citations and references

### In-text citations

Every idea, definition, formula or number taken from a source gets an in-text citation, and every source cited in the text appears in the References list (and the other way round).

- **Parenthetical form:** (Author, Year), e.g. (Garrison et al., 2024).
- **Narrative form:** Author (Year), e.g. Garrison et al. (2024) define wait time as ...
- **Page numbers:** add them for a direct quote, a specific figure, a specific problem or a table taken from a source: (Datar & Rajan, 2018, p. 64). Use "pp." for a page range: (Datar & Rajan, 2018, pp. 467–468).
- **Number of authors:**
  - One author: (Kaplan, 2010).
  - Two authors: always name both. Use "&" inside brackets (Datar & Rajan, 2018) and "and" in running text: Datar and Rajan (2018).
  - Three or more authors: give the first author followed by "et al." from the first citation: (Garrison et al., 2024).
- **Group or company author:** write the full name, e.g. (Bangladesh Bank, 2025). If it has a well-known abbreviation, give it the first time, e.g. (Bangladesh Bank [BB], 2025), then use (BB, 2025).
- **No date:** use "n.d.", e.g. (Bangladesh Bank, n.d.).
- **Two or more works in one bracket:** order them alphabetically and separate with semicolons: (Datar & Rajan, 2018; Garrison et al., 2024).
- **Same author, same year:** add a, b and so on after the year: (Garrison et al., 2024a, 2024b).
- **Direct quotes:** use quotation marks and a page number for quotes under 40 words. Indent quotes of 40 or more words as a block quote without quotation marks, with the citation after the final full stop. Prefer paraphrasing over quoting.
- **Lecture slides** given by the instructor: cite them as course material, e.g. (Rahman, 2026), and include them in the References only if the instructor allows it. Otherwise cite the textbook the slides are based on.
- **Tables and exhibits built from a source:** put the citation in the *Note.* under the table, e.g. *Note.* Adapted from Problem 2-45 (Datar & Rajan, 2018, p. 64). Use "Data from" when you copy figures, "Adapted from" when you change them, and "Calculated by the authors from Exhibit X" for your own working.

### References list

- Put it on a new page with the heading **References** (Heading 1 style). Do not call it "Bibliography".
- List the entries alphabetically by the first author's surname. Use a hanging indent of 0.5 inch and 1.5 line spacing, with no bullets or numbers.
- Give up to 20 authors' surnames and initials, separated by commas, with "&" before the last one.
- Use sentence case for the titles of books, articles and web pages: capitalise only the first word, the first word after a colon, and proper nouns. Use title case for the names of journals.
- Use italics for book titles, report titles, web page titles, and journal names with their volume numbers.
- Do not include the publisher's location (APA 7 dropped it). Include a DOI as https://doi.org/... whenever one exists.
- If the textbook problems used for the case figures are listed, add them in square brackets at the end of the entry, as in the CMA paper.

Formats with examples:

- **Book:** Author, A. A., & Author, B. B. (Year). *Title of book* (Edition ed.). Publisher.
  - Garrison, R. H., Noreen, E. W., & Brewer, P. C. (2024). *Managerial accounting* (18th ed.). McGraw Hill.
  - Datar, S. M., & Rajan, M. V. (2018). *Horngren's cost accounting: A managerial emphasis* (16th ed.). Pearson. [Case figures from Problems 2-45, p. 64; 11-32, p. 467; 11-34, p. 468; and 19-28, p. 773]
- **Chapter in an edited book:** Author, A. A. (Year). Title of chapter. In E. E. Editor (Ed.), *Title of book* (pp. xx–xx). Publisher.
- **Journal article:** Author, A. A., & Author, B. B. (Year). Title of article. *Journal Name, Volume*(Issue), pages. https://doi.org/xxxx
  - Kaplan, R. S., & Norton, D. P. (1992). The balanced scorecard: Measures that drive performance. *Harvard Business Review, 70*(1), 71–79.
- **Report by an organisation:** Organisation. (Year). *Title of report*. Publisher if different from the author. URL
- **Web page:** Author or Organisation. (Year, Month Day). *Title of page*. Site Name. URL
- **Newspaper article:** Author, A. A. (Year, Month Day). Title of article. *Newspaper Name*. URL
- **Lecture slides:** Instructor, A. A. (Year). *Title of slides* [PowerPoint slides]. Course name, Bangladesh University of Professionals.

### Citation checks before sending

- Every in-text citation has a matching reference, with the same spelling and year, and every reference is cited at least once.
- Use "&" only inside brackets and in reference entries, and "and" in running text.
- "et al." is used for three or more authors, and has a full stop after "al".
- Page numbers are given for every specific figure, problem, table or quote.
- Do not invent sources, page numbers or DOIs. If something cannot be confirmed, ask the user or leave it out.

## Solving maths in the paper

Show every calculation as the course slides do: the formula in words, then the numbers, then the answer, for example

```
Prime cost = Direct materials + Direct labor
= $140,000 + $22,000
= $162,000
```

Use the schedule formats from the course slides, such as cost of goods manufactured (raw materials, then total manufacturing costs, then work in process including a "Total work in process for the period" line) and cost of goods sold (goods available for sale minus ending finished goods). Only use concepts the user's course slides or chosen chapters cover. If something comes from outside them, say so and ask before including it.

## Final checks before sending

- Render the docx to PDF and look at every page. Check that no paragraph has a first-line indent, the cover has no number, the front matter runs i to iii, the table of contents has no number, and the body starts at 1 with numbers at the bottom centre.
- Check that the table of contents page numbers match the real pages.
- Check that the course, instructor, member names and IDs, title and date match what the user gave, everywhere they appear.
- Check the numbering on the rendered PDF: the cover and contents page have none, the Letter of Transmittal is i, the arabic numbers start at 1 on the first body section, and the contents page shows the matching roman and arabic numbers.
- Run the citation checks under "APA 7 citations and references".
- For an uploaded draft, check that no body text was reworded or dropped, that every body paragraph is Times New Roman 12 pt, and that headings, tables and notes match the styles table.
- Re-add every total and check every figure in the text matches the tables.
- Send the .docx file.
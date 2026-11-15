# BUP Term Paper Formatting (Claude skill)

**Please make sure to read the whole document first, as it will help you to make changes according to your instructor's needs.**

A Claude skill that writes or formats a group term paper in the house format used at the Faculty of Business Studies (FBS), Bangladesh University of Professionals (BUP). It produces a Word (.docx) file.

## What it does

- **Asks first** for the course name and code, the instructor's name, designation and department (and whether to write "Sir" or "Madam"), the group number with every member's name and ID, the title of the term paper, the submission date, and whether anything should change from the standard format.
- **Adds the front matter:** cover page (logo, faculty, department, course, topic, submitted to / by, Name–ID table, submission date), Letter of Transmittal, Acknowledgement, Executive Summary and Table of Contents.
- **Numbers the pages correctly:**

  | Part | Page number |
  | --- | --- |
  | Cover page | none |
  | Letter of Transmittal, Acknowledgement, Executive Summary | i, ii, iii (bottom centre) |
  | Table of Contents | none |
  | Body to References | 1, 2, 3 … (bottom centre) |

- **Formats the body:** Times New Roman 12 pt, 1.5 line spacing, justified, no first-line indents. Headings, tables and notes use fixed APA-style sizes (main headings 15 pt bold, sub-headings 13 pt bold, third-level 12 pt bold italic, table text 9–11 pt, notes 10 pt).
- **Applies APA 7th edition** to in-text citations, table notes and the References list, and checks that every citation has a matching reference.
- **Formats an uploaded draft without rewriting it:** it keeps your wording, then applies the formatting, front matter and numbering.
- **Shows calculations** as formula → numbers → answer, in the format used in course slides.

## How to install

### In Claude (claude.ai or the Claude app)

1. Download this repository: click **Code → Download ZIP**, then unzip it.
2. Zip the folder that contains `SKILL.md` on its own (the zip should contain `SKILL.md` at its top level, or inside one folder).
3. In Claude, go to **Settings → Capabilities → Skills** (called **Customize → Skills** in some versions) and choose **Upload skill**. Select the zip.
4. Make sure the skill is switched on.

### In Claude Code

Copy the folder into your skills directory:

```bash
mkdir -p ~/.claude/skills/bup-termpaper-format
cp SKILL.md ~/.claude/skills/bup-termpaper-format/
```

## How to use it

Start a new chat and ask for a BUP term paper, for example:

- "Write my term paper in the BUP term paper format."
- "Format this term paper in BUP format." (attach your draft .docx)
- "Use the bup-termpaper-format skill for my Marketing term paper."

Claude will then ask for:

1. Course name and code
2. Instructor name, designation and department, and Sir or Madam
3. Group number, and each member's name and ID
4. Title of the term paper
5. Submission date
6. Any changes you want from the standard format

Answer these in one message. Claude confirms the details, builds the paper, checks every page, and sends you the .docx file.

**Tips**

- To put the BUP logo on the cover, attach the logo image in the same chat. Without it, the cover is made without a logo.
- If you upload a draft, Claude keeps your wording. It only reformats it and adds the missing parts.
- Ask for changes in plain words afterwards, for example "make the headings black" or "add an appendix".

## Files

- `SKILL.md`: the skill itself (instructions Claude follows).
- `README.md`: this guide.

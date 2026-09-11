---
framework_version: 1.0.2
---

# Cover Letter Templates and Tailoring Guide - George Williams Mugabi

## Template: Custom cover.cls (XeLaTeX)
Cover letters use `cover_letters/cover.cls` with the bundled Lato/Raleway fonts.

**Output file:** `cover_letters/cover_<company>_<role>.tex`
**Compile with:** XeLaTeX

```bash
cd cover_letters && xelatex -interaction=nonstopmode -halt-on-error cover_<company>_<role>.tex
```

The final letter must compile successfully and be **exactly 1 page**.

## Privacy-Safe Header Rule
This repository is public. Tracked cover-letter templates must not contain private phone numbers, personal email addresses, exact street addresses, private LinkedIn URLs, referee contacts, or immigration-document details.

Default tracked header:
```latex
\namesection{}{\Huge{George Williams Mugabi}}{Warsaw, Poland}
```

Default signature:
```latex
\signature{George Williams Mugabi}
```

Private contact details may be inserted only into a **local/private final application artifact** if the user explicitly asks.

## Candidate-Specific Positioning

### For Data / BI / Business Analytics roles
Emphasize:
- final-year Business and Security Analytics studies
- Excel, Power BI, SQL and reporting/data validation
- practical project evidence from Trust Company Loan Management and Employee Task API
- ability to connect business requirements with technical/data solutions
- English C1+ and international experience

Do not claim years of professional analyst experience if the evidence is academic/project-based.

### For IT / Application Support roles
Emphasize:
- Qatar Energy customer/help-desk experience
- troubleshooting orientation and communication
- Windows / Microsoft Office / SQL / APIs / software-project familiarity
- ability to explain technical issues clearly and work with users

Qatar Energy dates must be confirmed before a final application if the letter mentions tenure.

### For Customer Service / Back Office / Operations roles
Emphasize:
- international customer/help-desk experience
- English C1+ / IELTS
- tutoring experience as evidence of clear communication and patience
- Excel / Microsoft Office
- reliability, customer focus and ability to learn systems quickly

### For Software / Technology internships
Emphasize:
- Trust Company Loan Management System
- Employee Task Management API
- C#, ASP.NET Core, JavaScript/TypeScript, React/Next.js, PostgreSQL/SQL Server, REST APIs
- Git/GitHub, Docker, GitHub Actions, Postman
- business understanding from the degree

## Structure
Use this pattern:

```latex
\documentclass[]{cover}
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{}
\rfoot{Page \thepage \hspace{0pt}}
\thispagestyle{empty}
\renewcommand{\headrulewidth}{0pt}
\begin{document}

\namesection{}{\Huge{George Williams Mugabi}}{Warsaw, Poland}

\currentdate{\today}
\lettercontent{Dear [Name/Team],}

\lettercontent{[Opening: name the role and immediately connect the most relevant part of George's background.]}

\lettercontent{[Why this company/role: independently verified reason, not generic enthusiasm.]}

\lettercontent{[Introduce 3-4 concrete points that map directly to the posting.]}

{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont
\begin{itemize}
    \item {[Grounded strength 1]}
    \item {[Grounded strength 2]}
    \item {[Grounded strength 3]}
\end{itemize}\par}
\vspace{6pt}

\lettercontent{[Forward-looking close: what George can contribute, with any important gap acknowledged honestly.]}

\lettercontent{I would welcome the opportunity to discuss the role further.}

\begin{flushright}
\closing{Kind regards,}
\signature{George Williams Mugabi}
\end{flushright}
\end{document}
```

## Known Template Pitfall
Never end a `\lettercontent{}` block with `\end{itemize}`. The macro appends a line break and will fail. Close `\lettercontent{}` before the list and wrap the external list in the Raleway font block shown above.

## Writing Rules
Follow `03-writing-style.md`.

For this candidate specifically:
- No generic "I am passionate about" openings.
- Lead with the best evidence for the role.
- Use project work honestly as project work.
- Do not turn basic Polish into fluent Polish.
- Do not imply the current degree is completed.
- Do not invent Qatar Energy dates or numerical achievements.
- Do not mention warehouse/logistics work unless it is genuinely relevant to the target role or chronology.
- Do not expose private contact details in tracked/public source files.
- Company-specific claims must be independently verified.

## Length
- Hard limit: 1 page
- Safe body target: approximately 250-300 words
- 3-4 short content blocks plus a concise bullet list
- If company-specific content is added, trim elsewhere rather than allowing the letter to grow beyond one page

## Salutation
Preferred order:
1. Named hiring manager/recruiter from the verified posting
2. `Dear [Company] hiring team,`
3. `Dear Hiring Manager,`

Avoid `To whom it may concern` unless explicitly required.

## Requirement Coverage
Every material requirement in the posting should be either:
- matched with a grounded example,
- bridged with adjacent evidence,
- or acknowledged honestly as a gap.

Do not omit an obvious gap merely because mentioning it is uncomfortable.

## Language
- Cover letter language follows the actual job posting / working context as `/apply` specifies.
- CV language remains English unless the user changes the profile-level setting.
- A posting written in Polish does not automatically mean the role requires fluent Polish. Use the Language Gate in `04-job-evaluation.md`.

## LaTeX Special Characters
Escape `&`, `%`, `$`, `#`, `_`, `~`, `^`, and backslashes wherever they appear in body text. An unescaped `%` is especially dangerous because it silently comments out the rest of the line.

## Compile-and-Inspect Loop - Mandatory
1. Compile with XeLaTeX using `-halt-on-error`.
2. Confirm exactly one page.
3. Visually inspect the PDF.
4. Confirm signature fits and nothing is clipped.
5. Confirm external itemize bullets use the matching Raleway font.
6. Re-check spelling, company name, role title, salutation and date.
7. Re-check factual grounding against `01-candidate-profile.md`, `CLAUDE.md`, and `cv/main_example.tex`.

## Submission Guidelines
- Submit only what the employer asks for.
- Export PDF for final submission unless the employer requests another format.
- Use clear filenames such as `George_Williams_Mugabi_CV.pdf` and `George_Williams_Mugabi_Cover_Letter.pdf` in the private final application package.

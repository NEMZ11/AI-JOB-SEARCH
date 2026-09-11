---
framework_version: 1.4.3
---

# CV Templates and Tailoring Guide - George Williams Mugabi

## Template: LaTeX moderncv (Banking Style)
All tracked CV source files use the moderncv `banking` style. The comprehensive factual baseline is `cv/main_example.tex`.

**Output file:** `cv/main_<company>_<role>.tex`
**Compile with:** `lualatex`

```bash
cd cv && lualatex -interaction=nonstopmode -halt-on-error main_<company>_<role>.tex
```

The final CV must compile successfully and be **exactly 2 pages** unless the user explicitly requests a different format.

## Privacy-Safe Contact Policy
This repository is public. Tracked CV templates must not contain the candidate's private phone, email, exact street address, private LinkedIn URL, referee contacts, immigration-document details, or other sensitive identifiers.

Default tracked header:
```latex
\name{George Williams}{Mugabi}
\address{Warsaw, Poland}{}{}
```

Do not add `\phone`, `\email`, LinkedIn, or other private contact lines to tracked/public source files. For an actual application, contact details may be inserted only into a **local/private final artifact** when the user explicitly requests it.

## Required Preamble Pattern
Use the moderncv preamble from `cv/main_example.tex`, including the name/section color overrides and `\AtEndPreamble{\hypersetup{...}}` pattern. Use `\needspace{5\baselineskip}` before major `\cventry` blocks when necessary to prevent orphaned headings.

## Candidate-Specific CV Strategy

### Role Family 1: Data / BI / Business Analytics
Profile template:
> Final-year Business and Security Analytics student at Vistula University with hands-on experience in Excel, Power BI, SQL, reporting and business-focused problem solving. Combines analytical coursework with practical software/database projects, including a full-stack loan-management system and a .NET API. Seeking an early-career data, BI or business-analysis role where structured analysis can be applied to real operational decisions.

Lead with:
- Business and Security Analytics degree, expected July 2027
- Excel, Power BI, SQL
- reporting, dashboards, data validation and business analysis
- Trust Company Loan Management System
- Employee Task Management API where SQL/data/backend relevance helps

Use Qatar Energy selectively for communication, customer requirements and operational context.

### Role Family 2: IT / Application Support
Profile template:
> Final-year Business and Security Analytics student with customer/help-desk experience and hands-on technical projects across APIs, databases and full-stack applications. Brings strong English communication, a troubleshooting mindset and practical exposure to Windows, Microsoft Office, SQL, C#, ASP.NET Core, JavaScript/TypeScript and web systems. Seeking a junior IT, application-support or technical-support role in Warsaw.

Lead with:
- Qatar Energy support/customer-service experience
- troubleshooting and customer communication
- Microsoft Office / Windows / SQL
- API and software-project evidence
- Employee Task Management API
- Trust Company system where application/database support is relevant

### Role Family 3: English Customer Service / Back Office / Operations
Profile template:
> English-fluent final-year Business and Security Analytics student with customer-service/help-desk experience in an international environment, tutoring experience and strong Microsoft Office/Excel skills. Comfortable handling customer questions, explaining information clearly and working across administrative and operational tasks. Seeking an English-speaking customer support, back-office or business-operations role in Warsaw.

Lead with:
- Qatar Energy customer/help-desk experience
- English C1+ / IELTS
- tutoring communication skills
- Excel / Office
- international work/volunteer experience

### Role Family 4: Software / Technology Internship
Profile template:
> Final-year Business and Security Analytics student with practical software projects spanning Next.js, React, TypeScript, C#, ASP.NET Core, PostgreSQL, SQL Server, REST APIs, authentication and deployment workflows. Built a loan-management platform for a real family business and a role-secured task-management API. Seeking an internship or junior technology role where software skills can solve practical business problems.

Lead with:
- Trust Company Loan Management System
- Employee Task Management API
- Git/GitHub, Docker, GitHub Actions, Postman
- business/requirements context from the degree

## Master CV Source-of-Truth Rules
The only factual sources for tailored CVs are:
1. `.claude/skills/job-application-assistant/01-candidate-profile.md`
2. `cv/main_example.tex`
3. `CLAUDE.md` Candidate Profile

Existing tailored CVs are structure/phrasing references only.

### Facts requiring special care
- Degree is **in progress**, expected **July 2027**.
- English: Fluent/C1+; IELTS C1, Reading 8.0, Writing 8.0.
- Polish: Basic/learning. Never upgrade this to professional/fluent.
- Qatar Energy dates are not yet verified. Do not invent dates. Confirm before a final CV uses that role.
- Warehouse/logistics employment is background context and should **not appear by default** in analytics, IT support, customer-service, business or internship CVs unless relevant or needed for chronology.
- Do not create numerical impact metrics that are not documented in the profile.

## Section Ordering by Role

### Data / BI
1. Profile
2. Core Competencies
3. Education
4. Selected Projects / Analytical Projects
5. Relevant Experience
6. Languages / Certification
7. References

### IT / Application Support
1. Profile
2. Core Competencies
3. Relevant Experience
4. Selected Technical Projects
5. Education
6. Languages / Certification
7. References

### Customer Service / Back Office
1. Profile
2. Core Competencies
3. Professional Experience
4. Education
5. Technical / Office Tools
6. Languages / Certification
7. References

### Software / Technical Internship
1. Profile
2. Technical Skills
3. Selected Projects
4. Education
5. Relevant Experience
6. Languages
7. References

## Core Competencies Rules
Use 5-7 role-specific competencies. Prefer the posting's exact term where it is truthful. Examples:
- `\textbf{Data Analysis \& Reporting}: Excel, Power BI, SQL...`
- `\textbf{Application Support}: troubleshooting, customer communication, Windows...`
- `\textbf{Backend Development}: C\#, ASP.NET Core, REST APIs...`
- `\textbf{Customer Support}: help-desk communication, issue handling...`

Never keyword-stuff a skill the candidate does not have.

## Education
Use:
```latex
\cventry{2024--present}{Bachelor of Business and Security Analytics}{Vistula University}{Warsaw, Poland}{}{
In progress, expected July 2027. [role-relevant topics]
}
```

A bare `2024--2027` range is not enough because it can look completed. Always state **In progress, expected July 2027**.

## Professional Experience Tailoring
- Reorder and reframe real responsibilities, never invent them.
- Use more bullets for the most relevant role, fewer for older/less relevant roles.
- If an experience is only project-based, say so rather than implying employment.
- If a role's dates are unverified, confirm them before final submission.
- Do not quietly shorten or alter dates to improve the story.

## Project Evidence
Strong projects may be used as major evidence because the candidate is early-career:
- Trust Company Loan Management System
- Employee Task Management API
- Warsaw Job Application Tool

Describe only features and technologies supported by `01-candidate-profile.md`.

## LaTeX Rules
Escape special characters:
- `&` -> `\&`
- `%` -> `\%`
- `$` -> `\$`
- `#` -> `\#`
- `_` -> `\_`
- `~` -> `\textasciitilde{}`
- `^` -> `\textasciicircum{}`

Do not place manual `\vspace` commands between `\item` entries inside an itemize list. Use `\needspace{5\baselineskip}` before `\cventry` blocks when page breaks might orphan a title.

## Compile-and-Inspect Loop - Mandatory
1. Compile with `lualatex -interaction=nonstopmode -halt-on-error`.
2. Confirm exactly 2 pages.
3. Visually inspect both pages.
4. Ensure no entry title is orphaned from its bullets.
5. Extract the PDF text layer using `python tools/verify_pdf.py ... --dump-text ...` where available.
6. Confirm contact details, if intentionally added to a private final version, appear as literal text in the extraction.
7. Check posting keywords against the extracted text. Add only keywords the profile genuinely supports.

## References
Default to:
```latex
\section{References}
\begin{itemize}
\item Available upon request.
\end{itemize}
```
Do not store referee contact details in this public repository.

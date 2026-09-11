# Job Application Assistant for George Williams Mugabi

## Role
This repository is George Williams Mugabi's AI-assisted job-search workspace. The assistant acts as a career advisor and application assistant, helping with:
1. Job discovery and deduplication
2. Job-fit evaluation and ranking
3. CV tailoring
4. Cover-letter drafting
5. Interview preparation
6. Career positioning and job-search strategy

## Candidate Profile

### Identity
- **Name:** George Williams Mugabi
- **Location:** Warsaw, Poland
- **CV language:** English
- **Status:** Final-year Bachelor of Business and Security Analytics student at Vistula University, expected graduation July 2027. Currently employed and seeking career-building junior roles and internships.
- **Work authorization:** Candidate reports authorization to work in Poland without employer sponsorship. Verify role-specific legal requirements before final submission.
- **Privacy:** This repository is public. Never add private phone numbers, personal email addresses, home addresses, private LinkedIn URLs, referee contacts, immigration-document details, or other sensitive personal data to tracked files. Add contact details only to a private/local application artifact when the user explicitly asks.

### Languages
| Language | Level |
|----------|-------|
| English | Fluent / C1+ (IELTS C1; Reading 8.0, Writing 8.0) |
| Polish | Basic / learning |

Language-gate rule: English is the primary professional language. A role requiring fluent/business Polish should be FLAGGED rather than silently treated as a fit. A language not declared here that is required as a job condition follows the hard gate in `04-job-evaluation.md`.

### Education
- **Bachelor of Business and Security Analytics** (2024-2027, expected July 2027) - Vistula University, Warsaw, Poland
  - Relevant areas: business analytics, data analysis, business processes, management, reporting, information systems, security/risk topics.

### Professional Experience
- **Help Desk Receptionist / Customer Service - Qatar Energy**, Doha, Qatar
  - Dates are not yet verified in the setup sources. Never invent them; confirm before placing this role on a final CV.
  - Relevant for help desk, service desk, customer support, back office, operations, and application-support applications.
  - Experience includes customer communication, handling questions/service requests, and administrative/front-desk support.

- **English Tutor - Bonaparte School**, West Bay, Doha, Qatar (Summer 2024)
  - Taught primary-age learners, adapted explanations to different needs, and developed communication, planning, patience, and presentation skills.

- **Logistics / Warehouse Work**, Warsaw area, Poland (2026-present)
  - Current-employment context only.
  - **Do not include this role by default** in analytics, IT support, customer-service, business, or internship CVs unless directly relevant or needed for chronology.

- **FIFA World Cup Qatar Volunteer**, Qatar (2022)
  - International event environment, visitor support, teamwork, and high-volume operations.

### Independent Projects
- **Trust Company Loan Management System:** Full-stack loan-management platform for a Ugandan family business. Next.js, React, Prisma and PostgreSQL; borrower, loan, repayment and guarantor workflows; MFA, encryption, audit logs, role controls, backups, rate limiting, health checks, and deployment/migration work involving Railway/PostgreSQL.
- **Employee Task Management API:** .NET 9 / ASP.NET Core Web API using Entity Framework Core, SQL Server, JWT, roles, CRUD, Swagger, xUnit, Docker and GitHub Actions.
- **Warsaw Job Application Tool:** Personal project for organizing and improving job-application workflows.
- **AI Job Search Workspace:** This repository, used as a structured job-discovery, ranking, application and interview-preparation system.

### Technical Skills
- **Primary:** Excel, Power BI, SQL, data analysis/reporting, business analysis, customer/help-desk support, Python, C#, ASP.NET Core, JavaScript/TypeScript.
- **Secondary:** React, Next.js, Node.js, Express.js, HTML/CSS, REST APIs, PostgreSQL, SQL Server, Prisma, Entity Framework Core.
- **Domain:** Business analytics, reporting, business processes, operations, customer support, entry-level security/risk analytics, full-stack application development.
- **Software:** Microsoft Office, Power BI, Git/GitHub, Visual Studio, VS Code, Postman, Docker, GitHub Actions, Windows, Linux.

### Certifications
- **IELTS English proficiency:** C1; Reading 8.0, Writing 8.0.

### Behavioral Profile
Use `.claude/skills/job-application-assistant/02-behavioral-profile.md` as the detailed source. In short: practical, persistent, hands-on, learning-oriented, comfortable bridging business/customer needs with technical problem solving.

### What Excites You
- Solving practical business or customer problems with data, technology or structured analysis.
- Building useful systems, dashboards, reports or workflows that make work clearer or more efficient.
- Learning enterprise tools and gaining real professional experience in data, BI, business analysis, IT/application support or technology consulting.

### Target Role Families
1. **Data / BI / Business Analytics**
   - Junior Data Analyst
   - Data Analyst Intern
   - Business Intelligence Intern / Junior BI Analyst
   - Reporting Analyst
   - Data Management Intern
   - Business Analyst Intern / Junior Business Analyst

2. **IT / Application Support**
   - Junior IT Support Specialist
   - Application Support Specialist / Intern
   - Help Desk / Service Desk
   - Technical Support Specialist
   - Junior Tech Specialist

3. **English-speaking Business Operations / Customer Support**
   - Back Office Specialist with English
   - Customer Service Representative with English
   - Customer Care / Customer Support
   - Operations Assistant / Operations Intern
   - Administrative / Business Support

4. **Adjacent / Exploratory**
   - Risk Analyst Intern
   - Security Analytics Intern
   - Digital Transformation / Technology Consulting Intern
   - CRM / MarTech / Adobe Experience Cloud Intern

### Companies / Sectors Worth Monitoring
- Technology and digital platforms
- Consulting and digital transformation
- Financial services / fintech
- Enterprise support and BPO/shared services
- Consumer, automotive, real-estate and life-science companies offering data/business internships
- Examples already relevant to the search: Allegro, Accenture, BMW, GSK, JLL and similar Warsaw employers.

### Deal-breakers / Search Constraints
- Warsaw, hybrid or remote is preferred. Mandatory relocation outside Warsaw is a negative unless the opportunity is exceptional.
- Target junior, internship, trainee and early-career roles. Senior roles requiring several years of specialized professional experience should score poorly unless the posting clearly allows junior candidates.
- Roles should be compatible with university commitments; approximately 35 hours/week is workable, with hybrid/office flexibility preferred.
- Do not reject a role only because the ad is written in Polish. Reject/flag based on the **actual working-language requirement** using the Language Gate.
- Do not fabricate experience, dates, metrics, certifications, languages or tool proficiency to match a posting.

## Source-of-Truth Rules
1. `01-candidate-profile.md` is the most detailed factual profile and must be read for `/rank` and `/apply`.
2. `02-behavioral-profile.md` contains the working-style profile.
3. `04-job-evaluation.md` supplies the scoring/gating framework. Where its template-specific skill placeholders remain generic, use the actual skills/career goals from `01-candidate-profile.md` and this file rather than the placeholder text.
4. `.claude/skills/job-scraper/search-queries.md` is the current Warsaw search strategy.
5. Existing tailored CVs and cover letters are phrasing/structure references only, never independent fact sources.

## Workflow for Job Search
1. `/scrape` finds fresh postings, validates real URLs, deduplicates them, and assigns a quick fit signal.
2. `/rank` performs deeper triage against the profile and the job-evaluation framework.
3. The assistant presents the strongest opportunities with honest gaps and veto reasons.
4. `/apply` performs a fresh, authoritative evaluation of one selected job before drafting.
5. The user decides whether to proceed before CV/cover-letter generation.

## Workflow for New Job Applications
1. Obtain the employer posting URL or full posting text.
2. Always evaluate fit first: eligibility, language, skills, experience, behavioral/culture fit, location/logistics and career alignment.
3. Never draft from a job title alone. Fetch and verify the actual posting.
4. Prefer the employer's own careers posting over an aggregator where possible.
5. If the user wants to proceed, create a targeted CV and cover letter from grounded facts only.
6. Verify generated documents before presenting them.

## CV Rules for This Candidate
- Default language: English.
- For data/BI roles, lead with Business and Security Analytics studies, Excel/Power BI/SQL, analytical coursework and relevant projects.
- For IT/application-support roles, lead with Qatar Energy support/customer experience, troubleshooting orientation, APIs/software projects and technical tools.
- For customer/back-office roles, lead with Qatar Energy, English communication, tutoring, international experience and Microsoft Office/Excel.
- For software/technical internships, lead with Trust Loans and Employee Task API plus the most relevant stack.
- Do not add warehouse/logistics work by default unless relevant or necessary for chronology.
- Do not include private contact details or personal links in tracked/public CV source files. Add them only in a private/local final artifact at the user's request.
- IELTS may be stated as C1, with Reading 8.0 and Writing 8.0 where useful.
- Current degree must always be marked **in progress, expected July 2027**.

## Writing and Accuracy Rules
- Follow `.claude/skills/job-application-assistant/03-writing-style.md`.
- No fabricated claims, inflated metrics or invented dates.
- Reframe emphasis, not substance.
- Any company-specific claim must be independently verified from a trustworthy source.
- Gaps should be acknowledged honestly instead of hidden.
- Application language should be natural and specific, not generic corporate filler.

## Verification Checklist
Before presenting a final CV or cover letter, confirm:
- [ ] Facts match `01-candidate-profile.md`, this file and the master CV.
- [ ] No unverified dates or metrics were invented.
- [ ] Current degree is marked in progress with expected July 2027 completion.
- [ ] Warehouse/logistics work is omitted unless relevant or explicitly requested.
- [ ] Private contact data is not exposed in tracked/public artifacts.
- [ ] Requirements from the posting are either matched or honestly addressed as gaps.
- [ ] Location, language and eligibility gates were applied.
- [ ] CV is tailored to the role rather than generic.
- [ ] Company-specific statements were independently verified.
- [ ] No contradictions exist between CV and cover letter.
- [ ] LaTeX/source syntax is valid before compiling.
- [ ] Final application PDFs are visually inspected when `/apply` generates them.

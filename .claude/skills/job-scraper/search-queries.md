# Search Queries for Job Scraper

## Search Goal
Find fresh, realistic early-career opportunities for George Williams Mugabi in Warsaw, Poland, prioritizing English-friendly roles that build toward data/BI, business analysis, IT/application support, or business-technology work.

## Installed portal CLIs
`/scrape` should use installed portal skills under `.agents/skills/*/SKILL.md` first. Keep the country-agnostic LinkedIn and FreeHire skills enabled. Danish demo portals should remain disabled for this Poland-based search unless explicitly requested later.

For Polish-market boards without a dedicated CLI, use WebSearch/site-search fallback. Never invent CLI flags for a portal that does not document them.

## Search Sites
Primary / high-value sources:
- **pracuj.pl** - major Polish general job board
- **linkedin.com/jobs** - Warsaw / Poland, especially international employers
- **indeed.com / pl.indeed.com** - broad Warsaw search coverage
- **rocketjobs.pl** - technology, digital, business and marketing/operations roles
- **nofluffjobs.com** - technical, data and some business/IT-support roles

Secondary:
- Employer career pages for Warsaw-based international companies
- University/graduate portals and internship pages
- Consulting, shared-services, fintech, automotive, real-estate and life-science employer sites

Companies worth monitoring include Allegro, Accenture, BMW, GSK, JLL and similar international employers in Warsaw. These are examples, not an exclusive list.

## Language Scope
Search mainly in English, plus useful Polish title variants where they help discover English-speaking jobs. The candidate's Polish is basic/learning, so a job requiring fluent/business Polish must be visibly flagged by the Language Gate. Do not discard a posting merely because the advertisement itself is written in Polish if the role's working-language requirements are compatible.

## Query Categories

### Priority 1: Data / BI / Business Analytics
Primary career direction. Search titles/functions such as:
- Junior Data Analyst
- Data Analyst Intern / Internship
- Business Intelligence Intern
- Junior BI Analyst
- Reporting Analyst / Reporting Intern
- Data Management Intern
- Junior Business Analyst / Business Analyst Intern
- Insights Analyst Intern
- Analytics Intern

High-signal skills/terms:
- SQL
- Power BI
- Excel
- reporting
- dashboards
- data validation
- business analysis

Example fallback queries:
```
site:pracuj.pl ("Junior Data Analyst" OR "Data Analyst Intern" OR "Business Intelligence") Warszawa
site:pracuj.pl ("Business Analyst Intern" OR "Junior Business Analyst") Warszawa English
site:linkedin.com/jobs ("Data Analyst Intern" OR "Junior Data Analyst") Warsaw Poland
site:linkedin.com/jobs ("Business Intelligence Intern" OR "Junior BI Analyst") Warsaw
site:rocketjobs.pl (data OR analytics OR "business intelligence") Warszawa SQL
site:nofluffjobs.com (data OR BI OR SQL) Warsaw junior
"Warsaw" "Power BI" internship English
"Warsaw" SQL analyst internship English
```

Polish discovery variants:
```
site:pracuj.pl ("młodszy analityk danych" OR "staż analityk danych") Warszawa
site:pracuj.pl ("analityk biznesowy" OR "staż analityk biznesowy") Warszawa angielski
```

### Priority 2: IT / Application / Technical Support
Strong secondary direction based on customer-support background plus technical projects.

Search titles/functions such as:
- Junior IT Support Specialist
- IT Support Intern
- Application Support Specialist / Intern
- Service Desk / Help Desk
- Technical Support Specialist
- Junior Tech Specialist
- Customer Technical Support
- Junior Support Engineer where requirements are entry-level

High-signal terms:
- troubleshooting
- ticketing
- Windows
- Microsoft 365 / Office
- SQL
- APIs
- application support
- customer support

Example fallback queries:
```
site:pracuj.pl ("Junior IT Support" OR "IT Support Specialist" OR "Service Desk") Warszawa English
site:pracuj.pl ("Application Support" OR "Help Desk") Warszawa English
site:linkedin.com/jobs ("Junior IT Support" OR "Application Support") Warsaw Poland
site:linkedin.com/jobs ("Technical Support Specialist" OR "Junior Tech Specialist") Warsaw
site:nofluffjobs.com (support OR "application support" OR helpdesk) Warsaw junior
```

Polish discovery variants:
```
site:pracuj.pl ("młodszy specjalista IT" OR "wsparcie IT" OR helpdesk) Warszawa angielski
```

### Priority 3: English-speaking Business Operations / Back Office / Customer Support
Useful adjacent roles with a realistic near-term fit and transferable experience.

Search titles/functions such as:
- Back Office Specialist with English
- Junior Customer Service Representative with English
- Customer Care / Customer Support
- Operations Assistant / Operations Intern
- Business Support Assistant
- Administrative Assistant with English
- Order Management / Client Support entry-level roles

High-signal terms:
- English
- customer support
- back office
- operations
- Excel
- administration
- CRM
- international team

Example fallback queries:
```
site:pracuj.pl ("Back Office" OR "Customer Service") English Warszawa junior
site:pracuj.pl ("Customer Support" OR "Operations Assistant") Warszawa English
site:linkedin.com/jobs ("Customer Service" OR "Back Office" OR "Operations Intern") Warsaw English
"Warsaw" "Customer Support" English internship
```

### Priority 4: Adjacent Technology / Consulting / Risk
Broader net for roles that connect business, technology and analysis.

Search titles/functions such as:
- Digital Transformation Intern
- Technology Consulting Intern
- CRM / MarTech Intern
- Adobe Experience Cloud Intern
- Data/Technology Consultant Intern
- Risk Analyst Intern
- Security Analytics Intern
- Junior Technology Analyst

Example fallback queries:
```
site:linkedin.com/jobs ("Technology Consulting Intern" OR "Digital Transformation Intern") Warsaw
site:pracuj.pl ("technology intern" OR "consulting intern" OR "risk analyst intern") Warszawa English
site:linkedin.com/jobs ("CRM Intern" OR "MarTech Intern" OR "Adobe Experience Cloud") Warsaw
"Warsaw" "Risk Analyst Intern" English
```

## Location Filter

### Ideal
- Warsaw proper
- Hybrid Warsaw roles
- Remote roles based in Poland

### Acceptable
- Warsaw metropolitan area when public-transport commute is reasonable
- Roles with occasional office attendance in Warsaw

### Borderline
- Jobs requiring a long daily commute outside the Warsaw metro area
- Roles requiring 4-5 office days per week when travel would materially interfere with studies

### Usually exclude / location FAIL
- Mandatory relocation outside Warsaw for an ordinary junior role
- Roles primarily based in another Polish city with frequent mandatory office attendance
- Roles outside Poland that require relocation and do not offer a compelling exception

## Seniority Filter
Prioritize:
- internship / intern
- trainee / graduate
- junior
- assistant
- entry-level
- 0-2 years experience

Do not automatically exclude a role asking for 1-2 years if the functional fit is strong. Deprioritize roles whose actual responsibilities are clearly mid/senior-level or require several years of specialized experience.

## Work-Pattern Filter
Preferred:
- hybrid
- office in Warsaw
- remote within Poland
- schedules compatible with university commitments

The candidate can work approximately 35 hours/week. Do not assume every internship must be part-time; evaluate the actual schedule and start date.

## Date Filter
Only include jobs posted within the last 14 days, or jobs with an application deadline that has not passed. If the posting date is unavailable, keep the job but flag the date as unknown. Verify the real posting URL before presenting it.

## Fit Priorities
A strong result normally has several of these:
- English is sufficient for the role
- junior/intern/trainee seniority
- Warsaw/hybrid/remote Poland
- Excel, SQL, Power BI, reporting, data validation, business analysis, customer/application support, troubleshooting or similar transferable requirements
- clear learning path
- international team
- no hard requirement for several years of specialized experience

## Search Behavior
By default, `/scrape` should run Priority 1, Priority 2 and Priority 3. Use Priority 4 in broad searches or when the first three categories have low yield.

When the user names a focus, prioritize that lane and generate 2-3 additional focus-specific searches. Continue to deduplicate against `seen_jobs.json` and the application tracker exactly as the scraper skill specifies.

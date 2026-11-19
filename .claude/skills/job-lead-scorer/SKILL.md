---
name: job-lead-scorer
description: Finds and scores job openings from companies' own career sites (not job boards) for a defined search, checks each posting against the candidate's real qualifications, and ranks leads with an apply, stretch, or skip verdict. Use whenever the user asks to find jobs, check a company's openings, score or rank postings, run a job search, or decide which postings are worth applying to, even if they only say "what's open at these companies".
---

# Job Lead Scorer

Search company career pages, not aggregators. Judge each lead on whether the candidate meets the requirements, and never dismiss a role at a reputable company with upside as "below level".

## Input requirements

Essential:
- Target roles and industries, location (Greater Houston or remote unless changed), and the candidate's confirmed qualifications (resume or confirmed-facts file).
- List of target companies, or permission to propose some.

Optional: salary floor, work-authorization or license constraints, companies to exclude, links the user already found.

## Workflow

1. **Set the search brief** in one line (roles, location, company types).
2. **Find openings on the employer's own career site** (company careers pages and their applicant-tracking pages). Use available search/fetch tools (Firecrawl, Tavily, Exa, Parallel, TinyFish) only if connected; check availability, and report only what tools returned. If a page cannot be read, say so rather than guessing. Do not use job boards as the source; if a board is the only place a role appears, find the company's own posting or mark it unverified.
3. **Verify each posting is live and recent**: posting date or "still open" evidence, location, remote policy, pay range if shown. Never invent pay; if the posting has no range, say "not listed" (a labeled public wage benchmark like BLS may be added, marked as a benchmark).
4. **Score each lead** with the 0-100 scale in the resume-tailor-ats skill if available (otherwise: requirements met 50, keywords 20, seniority fit 15, location/remote fit 10, company/upside 5). Verdict: 70+ apply, 55-69 stretch with named gaps, under 55 skip.
5. **Rank and present** a short table: company, role, link, location, score, verdict, top reason, biggest gap.
6. **Next actions**: for apply-verdict roles, offer a tailored resume, a cover letter, and a recruiter or hiring-manager lookup (Apollo, ZoomInfo, Vibe Prospecting only if connected).

## Output format

Ranked table plus three lines on each top lead (why it fits, the gap, the next step), and a list of sources checked.

## Example requests

- "Check Houston openings at these medical device companies on their career sites and score them."
- "Which of these 12 postings should I apply to?"
- "Find sales leadership roles in financial services I qualify for, remote or Houston."

## Quality checks

- Each lead links to the employer's own posting and shows it is open.
- Scores rest on the candidate's confirmed qualifications, with gaps named.
- No invented pay, dates, or requirements.
- Roles are judged on requirements met, not on title level.
- Tools used are stated honestly, including pages that could not be read.

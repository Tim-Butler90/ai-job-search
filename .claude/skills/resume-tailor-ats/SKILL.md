---
name: resume-tailor-ats
description: Tailors a resume to one job posting using only the candidate's confirmed facts, scores it against the posting (70 or higher before use, 90 or higher as the target), and keeps it ATS-clean in Word and PDF. Use whenever the user shares a job posting and wants a resume tailored, an ATS or match score, keyword gaps, bullet rewrites, or asks "is my resume good enough for this job", even if they never say "tailor".
---

# Resume Tailor (ATS, truth-first)

Every line in a resume must be true and defensible in an interview. Tailoring means choosing, ordering, and wording real facts to match the posting, never adding facts.

## Input requirements

Essential:
- The job posting (text or link; read the company's own career page when a link is given).
- The base resume(s) and a "confirmed facts" file or message (titles, dates, numbers, certifications, tools the user confirmed). If none exists, build one first from the resume and ask the user to confirm only the items that conflict or are unclear.

Optional: target role family, location or remote preference, which resume version to start from.

## Workflow

1. **Confirmed-facts check.** List facts and mark Confirmed / Conflicting / Unconfirmed. Use only Confirmed. For conflicts (dates, rankings, titles, which role a number belongs to) use the most conservative true wording and flag it. Never invent a metric, certification, tool, title, or date. Certifications that lapsed or were never earned are not listed as held.
2. **Read the posting.** Extract required vs preferred qualifications, keywords, tools, and seniority. Note which the user truly meets.
3. **Score before editing** using `references/scoring.md` (0-100). Report the score and the main gaps.
4. **Tailor.** Reorder sections and bullets, mirror the posting's exact terms only where the user really has the thing, and lead with the strongest matching evidence. Keep roles to the titles the user confirmed (alternate titles only if the user confirmed they are legitimate).
5. **Gap questions.** For each important gap, ask one short question (do you have this experience?). Do not claim it until answered. If the answer is no, leave it out and say how the user can honestly bridge it in the cover letter.
6. **Re-score.** Below 70 means do not recommend applying until the gaps are addressed or the user accepts the risk. Aim for 90 or more by honest improvements only; if 90 is not reachable truthfully, say so.
7. **Build files** (Word first, then PDF): single column, standard headings (Summary, Experience, Skills, Education, Certifications), no tables for layout, no text boxes, no images, real bullets, US Letter, plain fonts. Check with pdftotext that text extracts in order. Use a docx skill or python-docx if available; confirm before relying on it.
8. **Deliver** the files, the before/after score, a changes list (what changed and why), and a flag list.

## Output format

Score before/after, list of changes with reasons, open gap questions, files (.docx and .pdf).

## Example requests

- "Tailor my resume to this VP Sales posting [link]. Tell me my score first."
- "What keywords am I missing for this medical device sales job?"
- "Is this resume ready to send for this role?"

## Quality checks

- Every claim traces to confirmed facts; nothing invented.
- Conflicts resolved conservatively and flagged.
- Score reported before and after, with reasons.
- ATS-clean: single column, standard headings, text extracts cleanly.
- Dates, titles, employers, numbers match the confirmed-facts file.
- Phone, email, and location correct and consistent.

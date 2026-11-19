---
name: data-to-report
description: Turns supplied data (CSV, Excel, tables, exports, pasted numbers) into a trustworthy report by inspecting the data, defining metrics, checking calculations, charting findings, and separating evidence from assumptions. Use whenever the user shares a spreadsheet or dataset and wants analysis, a summary, insights, a monthly/quarterly report, KPIs, trends, charts, or asks "what does this data say", "make a report from this", or "check my numbers", even if they do not say "report".
---

# Data-to-Report

Produce a report the reader can trust and check. Every claim must trace to the supplied data, every calculation must be verified by running it, and every assumption must be labeled.

## Input requirements

Essential:
- The data (attached file or pasted). Inspect it before asking questions.
- The question or decision the report supports, and the audience. If unclear, state the assumed purpose and proceed.

Optional:
- Metric definitions the user already uses (for example how "active customer" is counted).
- Period and comparison basis, output format (Word, PDF, slides, markdown), brand style.

Never fabricate rows, benchmarks, or sources. Outside benchmarks are used only if the user supplies them or a search was actually run and cited.

## Workflow

1. **Inspect.** Load the file with code. Report shape (rows, columns), column types, date range, missing values, duplicates, outliers, and anything suspicious (mixed units, totals rows inside data, inconsistent labels, negative values where impossible). Save findings in a short "Data check" list. Do not edit the user's original file; work on a copy.
2. **Define metrics.** Write each metric with name, formula, source columns, and period (see `references/metric-definitions.md`). Where a definition is ambiguous, state the choice made and why, and show how the result would change under the alternative if it matters.
3. **Compute with code, then verify.** Run calculations in code (pandas or equivalent). Cross-check: totals equal sum of parts, percentages computed from the right denominator, row counts before and after filters reconcile, a second method (for example pivot vs groupby) agrees on key numbers. Never estimate figures in prose.
4. **Find the findings.** Look for the few things that matter: change over time, biggest drivers, comparisons, exceptions. State each as a claim with its number, comparison basis, and sample size. Avoid causal language unless the data supports it.
5. **Chart.** One chart per message, simplest suitable type, labeled axes and units, bars from zero, direct labels. If a `dataviz` skill is available, read it first. Verify every plotted value against the computed table.
6. **Separate evidence from assumptions.** Mark each statement as Evidence (directly computed), Interpretation (reasonable reading), or Assumption (not supported by the data; needs confirmation). See the report template.
7. **Write the report** using `references/report-template.md`; deliver in the requested format (check for docx/xlsx/pdf skills or libraries; confirm availability). Include a calculation appendix or an .xlsx/.csv of computed tables so the reader can check.
8. **Final check:** re-run the pipeline end to end from the raw file if edits were made, and confirm the numbers in the report match the outputs.

## Output format

Report with: Summary (3-5 bullets of the main findings), Method and data check, Metrics table, Findings with charts, Evidence vs assumptions, Limitations, Recommended next steps (only those the evidence supports), and Appendix (calculations).

## Example requests

- "Here is our sales export for Q3. Tell me what changed vs Q2 and make a report for my manager."
- "Check my churn math. This is the spreadsheet."
- "Summarize this survey data with charts. I do not know which stats matter."

## Quality checks

- Data check performed and reported before any analysis.
- Each metric has a written definition; denominators stated.
- All numbers produced by code and cross-verified; totals reconcile.
- Every chart value matches the computed table; axes labeled; bars start at zero.
- Claims carry sample size or base; no causal claims without support.
- Evidence, interpretation, and assumption are visibly distinguished.
- No outside data or benchmark without a supplied or cited source.
- Original file untouched; calculations reproducible from the appendix or companion file.

# Metric definition card

Write one per metric before computing. Keep the user's own definition if they have one.

```
Metric: ______
Plain-language meaning: ______
Formula: numerator / denominator (or aggregation)
Source columns: ______
Filters / exclusions: ______
Period and grain (daily, weekly, monthly): ______
Comparison basis (prior period, same period last year, target): ______
Known ambiguity and choice made: ______
```

## Common pitfalls to check
- **Averages of averages:** compute from underlying rows or weight properly.
- **Percent change on tiny bases:** report absolute change as well.
- **Denominator drift:** make sure numerator and denominator cover the same population and period.
- **Duplicates and refunds:** decide how they are counted and say so.
- **Partial periods:** do not compare a full month with a partial month.
- **Mixed units or currencies:** convert only with a supplied rate; otherwise report separately.
- **Time zones and date formats:** confirm before grouping by day.
- **Survivorship:** note when data only includes records that remained.
- **Seasonality:** compare with the same period last year when available.

## Common metric patterns
| Metric | Typical formula | Watch for |
|---|---|---|
| Growth rate | (current - prior) / prior | Prior near zero |
| Conversion rate | conversions / eligible visitors | Eligible definition |
| Churn rate | customers lost in period / customers at start | Customers added mid-period |
| Average order value | revenue / orders | Refunds, outliers |
| Retention | customers active in period N / cohort size | Cohort definition |
| Share of total | part / total | Totals including the part twice |

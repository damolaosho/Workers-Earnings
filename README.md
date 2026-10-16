# Workers-Earnings
Analysis of 28K survey respondents: cleaning, outlier handling and median earnings by education, age and city. Excel + Tableau.


# US Worker Salary Survey Analysis

Excel analysis of 28,016 self-reported survey responses (23,167 from the US) looking at how salary relates to education, experience and age. The Excel dashboard is complete; a Tableau version is planned.

## Questions

1. How do education and experience relate to salary?
2. How are US survey respondents distributed across salary ranges?
3. How does salary change with age, and where does it level off?

## Key findings (US respondents, n = 23,167)

- **Education:** the share earning under $50K falls from 43% (high school) to 3% (professional degrees), while the share earning $100K+ rises from 22% to 61%.
- **Master's vs. college degree:** a master's adds a modest step over a college degree (32% vs. 28% earning $100K+), much smaller than the step to a PhD (48%) or professional degree (61%).
- **Experience:** the share earning $100K+ rises from 16% (entry level) to 30% (mid) to 46% (senior).
- **Distribution:** about 52% of US respondents earn $75K or more; the most common band is $50-75K (30%).
- **Age:** pay rises steeply from the early 20s to the mid-30s, stays roughly level from 35 to 54, and dips slightly at 55-64.

All results describe survey respondents, not the wider US workforce. See Limitations.

## Data

- **Source:** [
- **Collection:** self-reported, unverified responses gathered through a social media post (self-selected sample)
- **Size:** 28,016 rows; 23,167 US rows used for all analysis
- **Fields used:** country code, highest education completed, relevant years of experience in field, age group, annual salary (annualized)

## Data preparation (Excel)

| Step | Detail |
|---|---|
| Raw data | 28,016 rows kept untouched on the RAW DATA sheet |
| Rows deleted | None |
| Missing values | [TO COMPLETE: which fields had missing values, how many rows, and how they were filled (e.g., placeholder label, mean, median)] |
| Standardization | [TO COMPLETE: what was normalized, e.g., country codes, text categories] |
| Country filter | US only (23,167 rows); 4,849 non-US rows excluded from the analysis, not deleted. Country code was used as the filter, not the currency field |
| Salary bands | 0-25K, 25-50K, 50-75K, 75-100K, 100K-999K, 1M+ |
| Age bands | under 18, 18-24, 25-34, 35-44, 45-54, 55-64, 65 or over |
| Experience levels | Entry, Mid, Senior, based on relevant years of experience in the field. Cut-offs: [TO COMPLETE] |
| Blank education | 151 US respondents did not state their education and are excluded from the education analysis only |
| Very high salaries | 12 US respondents are in the 1M+ band. [TO COMPLETE: kept or excluded, and why] |

## Findings

### Q1: Education, experience and salary

Share of each group in each salary band (US only).

| Education | n | Under $50K | $50-100K | $100K+ |
|---|---|---|---|---|
| High School | 405 | 43% | 35% | 22% |
| Some college | 1,639 | 34% | 44% | 22% |
| College degree | 11,267 | 20% | 52% | 28% |
| Master's degree | 7,447 | 14% | 55% | 32% |
| PhD | 1,122 | 6% | 46% | 48% |
| Professional degree (MD, JD, etc.) | 1,136 | 3% | 36% | 61% |

- The share earning under $50K falls at every step up the education ladder.
- Finishing a college degree matters: moving from some college to a college degree cuts the under-$50K share from 34% to 20%.
- The professional-degree figures likely reflect occupation (e.g., physicians, lawyers), which was not controlled for.

| Experience level | n | Under $50K | $50-100K | $100K+ |
|---|---|---|---|---|
| Entry | 6,163 | 32% | 52% | 16% |
| Mid | 9,609 | 16% | 55% | 30% |
| Senior | 7,395 | 9% | 45% | 46% |

- The biggest single jump is from entry to mid level.
- In this sample, experience is associated with a much larger shift at the top of the pay range than a master's degree is.

### Q2: Salary distribution of US respondents

| Salary range | Respondents | Share |
|---|---|---|
| $0-25K | 298 | 1.3% |
| $25-50K | 3,890 | 16.8% |
| $50-75K | 6,849 | 29.6% |
| $75-100K | 4,923 | 21.3% |
| $100K+ | 7,207 | 31.1% |

- About 18% earn under $50K and about 52% earn $75K or more.
- The $100K+ band is much wider than the others, so it looks larger than it is. Splitting it into narrower bands is a planned improvement.

### Q3: Age and salary

| Age group | n | Under $50K | $50-100K | $100K+ |
|---|---|---|---|---|
| 18-24 | 973 | 46% | 46% | 8% |
| 25-34 | 10,291 | 21% | 54% | 25% |
| 35-44 | 8,254 | 13% | 49% | 38% |
| 45-54 | 2,681 | 13% | 47% | 40% |
| 55-64 | 870 | 18% | 47% | 35% |

- The share earning $100K+ climbs from 8% at 18-24 to 38% at 35-44, then levels off at 40% for 45-54 and dips to 35% at 55-64.
- Under 18 (n = 12) and 65 or over (n = 86) are too small to interpret and are excluded from the commentary.
- Each age group is a different set of people, so this is not one person's career path.

## Limitations

- **Self-selected sample.** The data came from a social media post. About 91% of US respondents who stated their education hold at least a college degree, and only about 2% have a high school diploma as their highest level, so the sample is not representative of the US workforce.
- **Self-reported and unverified.** Salaries, titles and experience were not checked.
- **Association, not causation.** Age, experience, industry and education overlap, and none of the comparisons control for the others.
- **Occupation and industry were not controlled for.** Education and age differences may partly reflect the jobs people hold.
- **Country code, not currency, was used to filter.** Some US-coded respondents may have reported in another currency.
- **Banded data.** Results are shares by salary band; medians and averages by group were not used here.
- **Imputed values.** 

## Dashboard

<img width="1051" height="587" alt="Screenshot 2026-10-16 at 12 00 25" src="https://github.com/user-attachments/assets/5ca5cf56-f4c1-4c76-88e0-fe20fcf6d92b" />

## Tools

Microsoft Excel (pivot tables, slicers, charts, dashboard)

## Data credit

(https://x.com/iam_Uchenna/status/1783882725985861662?s=20) by Splendor Uchenna

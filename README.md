# 📊 A/B Testing Analysis – Marketing Conversion Optimization Using Power BI
**A complete end-to-end A/B testing project analyzing user behavior, conversion performance, and statistical significance to guide data-driven marketing decisions.**

This project demonstrates how to design, analyze, and visualize an A/B experiment using a real-world marketing dataset.
It walks through **experiment design, data modeling, segmentation, behavioral insights, and final decision-making**, all delivered via an interactive **Power BI dashboard**.

## 🚀 1. Project Overview

Modern digital teams rely heavily on A/B testing to validate hypotheses and optimize user experience.
In this project, I built a complete BI solution to answer a core marketing question:

**Which message drives more conversions — a PSA-style message (Variant A) or a direct commercial ad (Variant B)?**

Using Power BI, I designed a four-page dashboard that evaluates:

* Conversion rates for A vs B

* Segment-level performance (day, hour, exposure level)

* User behavior patterns

*Funnel movement

* Lift calculations

* Statistical significance

* Final executive recommendation

This project combines **data science thinking** with **business intelligence storytelling**, producing insights that directly inform marketing strategy.

## 📁 2. Dataset

**Source:** Marketing A/B Testing Dataset (Kaggle)
**File:** `marketing_AB.csv`

Each row represents a user exposed to Variant A (“psa”) or Variant B (“ad”), along with engagement behavior and conversion outcome.

Key Columns

test_group - Variant A (psa) or Variant B (ad)

converted - Whether the user completed the target action

total_ads - Number of ads seen

most_ads_day - Day user engaged the most

most_ads_hour - Time user engaged the most

This dataset is ideal for demonstrating real-world marketing experimentation.

🧠 3. Experiment Design
Business Question

Does switching from a PSA-style message to a direct ad improve user conversion rate?

Hypotheses

H0 (Null): No difference in conversion between Variant A and Variant B

H1 (Treatment): Variant B increases conversion

Primary KPI

Conversion Rate = Conversions / Users

Secondary Metrics

Average ads seen

Engagement day

Engagement hour

Exposure segment (“High Exposure” vs “Low Exposure”)

🏗️ 4. Data Modeling

A clean, simple model was built in Power BI:

Fact Table: marketing_AB

Generated Columns:

Hour Group (Morning, Afternoon, Evening, Late Night)

Ad Exposure Segment (High/Low)

Day Type (Weekday/Weekend)

Key DAX Measures:

Total Users

Conversion Rate A/B

Absolute & Relative Lift

Effect Size

Significance Indicator

This model powers all visualizations and makes the dashboard dynamic and filter-responsive.

📊 5. Power BI Dashboard Structure

The dashboard contains four fully designed pages, each serving a unique analytic purpose.

🔹 Page 1 — A/B Test Overview & Key Metrics

A high-level executive snapshot showing:

Total users

Users in A vs B

Conversion Rate A vs B

Absolute and Relative Lift

Clear experiment summary

A clustered bar chart highlights the conversion differences, and a narrative text panel explains the experiment in simple business terms.

🔹 Page 2 — Variant Performance by Segments

This page answers:
"Who responded better? Which user segments show the largest lift?"

Includes:

Exposure slicers

Average ads by variant

Conversion rate by:

Day type

Hour group

Variant

Behavioral comparison between A and B

This reveals deep patterns such as higher responsiveness during specific hours or exposure ranges.

🔹 Page 3 — Engagement Trends & Behavioral Analysis

Advanced behavioral insights including:

A heatmap showing when conversion peaks

A funnel from:

Saw Ads → High Exposure → Converted

Insight panel to guide interpretation

This gives stakeholders a full understanding of how users move through the conversion process.

🔹 Page 4 — Final Analysis & Recommendation

The decision-making page.

Includes:

Conversion KPI cards

Variant A vs B metrics table

Statistical significance table (z-score & p-value)

Effect Size gauge

Significance indicator

Final written recommendation

This page simulates how analytics teams present experiment results to executives.

📈 6. Key Insights
✔ Variant B outperformed Variant A

Variant B produced a 0.8% absolute lift — a meaningful gain at scale.

✔ The results are statistically significant

p-value: 1.70e-13

z-score: 7.37
Meaning the lift is extremely unlikely to be random.

✔ Lift is consistent across user segments

Conversion advantage holds across:

Weekday vs Weekend

Morning vs Late Night

High vs Low ad exposure

✔ Behavior patterns show strategic opportunities

Certain time-of-day and day-of-week combinations exhibit higher responsiveness, suggesting future personalization opportunities.

🏆 7. Final Recommendation

Variant B (“ad”) clearly outperforms Variant A, delivering higher conversion with overwhelming statistical significance.
The effect is meaningful, reliable, and consistent across segments.

📌 Recommendation:

Roll out Variant B to 100% of traffic.

Next Steps

Run follow-up personalization tests

Explore optimal ad timing & frequency

Test message variations to enhance conversions further

🛠️ 8. Tools & Skills Demonstrated
Power BI

Data modeling

DAX calculations

Interactive segmentation

Funnel & heatmap visuals

KPI cards & gauges

Executive dashboards

A/B Testing

Hypothesis framing

Lift analysis

Segment-level exploration

Statistical significance (z-test)

Business Intelligence

Experiment storytelling

Executive insights

Data-driven recommendations

🙌 9. About the Author

Khushnud Ahmed
Data Analyst / BI Analyst | Toronto, Canada
Skilled in Python, SQL, Power BI, Tableau, Machine Learning, and Experimentation Analytics

🔗 10. How to Explore the Dashboard

Include:

Link to Power BI report (if published or shared via pbix)

Repository includes:

Dataset

PBIX file

Images of dashboards

DAX formulas

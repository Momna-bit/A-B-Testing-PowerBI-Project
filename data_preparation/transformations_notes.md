# Data Preparation & Transformations (Power BI – Power Query)

All preparation was done directly in Power BI using Power Query and DAX.

---

## 1. Loading the Data

- Imported `marketing_AB.xlsx` via **Get Data → Excel**.
- Verified 588,101 rows and 7 columns.
- Selected the single worksheet containing the A/B test data.

---

## 2. Column Cleanup

- Kept the following columns for analysis:
  - `user id`
  - `test group`
  - `converted`
  - `total ads`
  - `most ads day`
  - `most ads hour`
- Left `Unnamed: 0` as an index column but did not use it in visuals or measures.

In the model view, columns were renamed to consistent, code-friendly names:

- `user id`       → `user_id`  
- `test group`    → `test_group`  
- `total ads`     → `total_ads`  
- `most ads day`  → `most_ads_day`  
- `most ads hour` → `most_ads_hour`  

---

## 3. Data Types

Data types were set as:

- `user_id`       → Whole Number  
- `test_group`    → Text  
- `converted`     → Boolean / True–False  
- `total_ads`     → Whole Number  
- `most_ads_day`  → Text  
- `most_ads_hour` → Whole Number  

Setting correct data types ensures accurate aggregations, slicers, and time-based segmenting.

---

## 4. Engineered Columns (DAX Calculated Columns)

Three key calculated columns were created:

1. **AdExposureSegment**
   - Logic: `"High Exposure"` if `total_ads >= 8`, otherwise `"Low Exposure"`.

2. **Hour Group**
   - Logic: Bucket `most_ads_hour` into `Late Night`, `Morning`, `Afternoon`, `Evening`.

3. **Day Type**
   - Logic: `"Weekend"` if `most_ads_day` ∈ {Saturday, Sunday}, otherwise `"Weekday"`.

These columns power the segmentation visuals on the **Variant Performance by Segments** and **Engagement Trends & Behavioral Analysis** pages.

---

## 5. Handling Missing or Anomalous Values

- The dataset did not contain nulls in key experiment fields (`test_group`, `converted`, `total_ads`).
- High `total_ads` values were treated as valid high-exposure users and retained.
- No rows were dropped to preserve the original experiment structure.

---

## 6. Model Simplicity

- A single fact table (`marketing_AB`) with engineered segmentation fields was sufficient.
- No separate dimension tables were required due to:
  - The narrow scope (one experiment),
  - The flat structure of the dataset,
  - And the focus on variant vs behavior analysis.

This lightweight model keeps the Power BI report responsive while still supporting rich A/B testing insights and experiment storytelling.

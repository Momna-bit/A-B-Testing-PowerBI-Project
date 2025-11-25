# Data Dictionary – Marketing A/B Testing Dataset

**Source:** Kaggle – Marketing A/B Testing Dataset  
**Rows:** 588,101  
**Columns:** 7

## Original Columns

| Column Name    | Type    | Description |
|----------------|---------|------------|
| `unnamed:_0`   | Integer | Index column from the original CSV/Excel export. Not used in analysis. |
| `user_id`      | Integer | Unique identifier for each user in the experiment. |
| `test_group`   | String  | Experiment variant assigned to the user: `"psa"` (control) or `"ad"` (treatment). |
| `converted`    | Boolean | `TRUE` if the user completed the target action (conversion), otherwise `FALSE`. |
| `total_ads`    | Integer | Total number of ads the user was exposed to during the experiment. |
| `most_ads_day` | String  | Day of the week on which the user saw the highest number of ads (e.g., Monday–Sunday). |
| `most_ads_hour`| Integer | Hour of the day (0–23) during which the user saw the highest number of ads. |

---

## Engineered Fields (Power BI)

These fields were created in Power BI to support segmentation and analysis.

| Field Name          | Type   | Definition |
|---------------------|--------|-----------|
| `AdExposureSegment` | String | `"High Exposure"` if `total_ads >= 8`, otherwise `"Low Exposure"`. |
| `Hour Group`        | String | Buckets `most_ads_hour` into `Late Night`, `Morning`, `Afternoon`, `Evening`. |
| `Day Type`          | String | `"Weekend"` if `most_ads_day` is Saturday/Sunday, otherwise `"Weekday"`. |
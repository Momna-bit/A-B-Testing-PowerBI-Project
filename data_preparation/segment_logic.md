# Segmentation Logic

This project segments users to understand how different behaviors and exposure levels influence conversion across variants.

---

## 1. Ad Exposure Segment

**Purpose:** Differentiate users who saw many ads from those with lighter exposure.

**Logic:**

- **High Exposure**: `total_ads >= 8`  
- **Low Exposure**:  `total_ads < 8`

**Used in:**

- Conversion rate by exposure level  
- Funnel analysis (Saw Ads → High Exposure → Converted)  
- Segment-level comparisons between Variant A and Variant B  

---

## 2. Hour Group

**Purpose:** Capture time-of-day patterns in user responsiveness.

Mapping from `most_ads_hour` (0–23):

- `0–5`   → **Late Night**  
- `6–11`  → **Morning**  
- `12–17` → **Afternoon**  
- `18–23` → **Evening**  

**Used in:**

- Conversion Rate by Hour Group and Variant  
- Heatmap of day vs hour behavior  
- Identifying “high-opportunity” engagement windows  

---

## 3. Day Type (Weekday vs Weekend)

**Purpose:** Compare workday vs leisure behavior.

Mapping from `most_ads_day`:

- **Weekend**: Saturday, Sunday  
- **Weekday**: Monday, Tuesday, Wednesday, Thursday, Friday  

**Used in:**

- Conversion Rate by Day Type and Variant  
- Understanding whether campaigns perform better on workdays or weekends  

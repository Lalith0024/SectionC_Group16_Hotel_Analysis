<div align="center">

<!-- Header Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,50:16213e,100:0f3460&height=200&section=header&text=🧹%20Data%20Cleaning%20Report&fontSize=38&fontColor=e94560&fontAlignY=35&desc=Hotel%20Booking%20Dataset%20—%20Quality%20Assurance&descSize=16&descAlignY=55&descColor=ffffff&animation=fadeIn" width="100%" />

<!-- Badges -->
<p>
  <img src="https://img.shields.io/badge/Project-Capstone%20Group%2016-e94560?style=for-the-badge&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Dataset-Hospitality%20Bookings-0f3460?style=for-the-badge&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Records-8%2C716%20Cleaned-34a853?style=for-the-badge&labelColor=1a1a2e" />
</p>

<br/>

<table>
<tr>
<td>

### 📄 Data Cleaning & Quality Assurance Report

> **Prepared For:** Business Intelligence & Executive Dashboarding
> **Prepared By:** Data Engineering & Analytics Team

</td>
</tr>
</table>

</div>

---

<br/>

## <img src="https://img.shields.io/badge/📌-Executive%20Summary-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<blockquote>
This document provides technical documentation of the data cleaning and preparation pipeline applied to transform the raw hotel booking dataset into an analysis-ready dataset suitable for KPI computation, pivot analysis, and executive dashboard development.
</blockquote>

**The cleaning process achieved:**

- ✅ ~10,000 → **8,716** validated records (post-quality filtering)
- ✅ Standardized categorical values across all key dimensions
- ✅ 100% elimination of textual NULLs and placeholder values
- ✅ Production-ready dataset for dashboarding and business analysis

---

<br/>

## <img src="https://img.shields.io/badge/🎯-Purpose%20%26%20Objectives-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

This cleaning pipeline was designed to:

<table>
<tr><td>✓</td><td>Ensure accuracy of revenue and cancellation metrics</td></tr>
<tr><td>✓</td><td>Enable reliable KPI computation for management dashboards</td></tr>
<tr><td>✓</td><td>Prevent misleading insights from inconsistent or invalid data</td></tr>
<tr><td>✓</td><td>Prepare data for interactive dashboards in Google Sheets</td></tr>
<tr><td>✓</td><td>Maintain maximum usable data without introducing bias</td></tr>
<tr><td>✓</td><td>Ensure traceability and auditability of transformations</td></tr>
</table>

<br/>

> 📝 All transformations were documented and executed in **Google Sheets** as per capstone requirements.

---

<br/>

## <img src="https://img.shields.io/badge/📊-Dataset%20Overview-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<div align="center">
<table>
<tr>
<th>Property</th>
<th>Value</th>
</tr>
<tr><td>📁 <b>Raw Records</b></td><td>~10,000 bookings</td></tr>
<tr><td>✅ <b>Cleaned Records</b></td><td>8,716 bookings</td></tr>
<tr><td>📉 <b>Data Loss</b></td><td>~13% (due to duplicates & invalid values)</td></tr>
<tr><td>🏨 <b>Domain</b></td><td>Hospitality / Hotel Bookings</td></tr>
<tr><td>📈 <b>Primary Metrics</b></td><td>Bookings, Cancellations, ADR, Revenue</td></tr>
<tr><td>📅 <b>Time Period</b></td><td>2015 – 2017</td></tr>
<tr><td>🎯 <b>Intended Usage</b></td><td>KPI Dashboards, Trend Analysis, Segment Performance</td></tr>
</table>
</div>

---

<br/>

## <img src="https://img.shields.io/badge/⚠️-Data%20Quality%20Issues%20Identified-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

| Category | Issue | Severity |
|:---------|:------|:--------:|
| 🔧 Structural | Inconsistent column formats | `Medium` |
| 🏷️ Categorical | Whitespace, mixed labels (Online TA vs Online TA/TO) | `High` |
| 🔢 Numeric | Text stored as numbers, missing values | `High` |
| 💰 Financial | Negative ADR values | `Critical` |
| ❓ Missing Values | NULL / blank cells in guest & country fields | `High` |
| 🔁 Duplicates | Repeated booking records | `Medium` |
| ⚖️ Logical | Inconsistent totals for guests/stays | `Medium` |

---

<br/>

## <img src="https://img.shields.io/badge/🔄-Cleaning%20Pipeline%20Overview-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<div align="center">

```
Raw Data
   ↓
Duplicate Removal
   ↓
Missing Value Handling
   ↓
Data Type Standardization
   ↓
Text Normalization
   ↓
Invalid Value Treatment
   ↓
Feature Engineering
   ↓
Cleaned Dataset ✅
```

</div>

---

<br/>

## <img src="https://img.shields.io/badge/🧩-Key%20Cleaning%20Stages-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

### 6.1 🔁 Duplicate Removal

- Exact duplicate booking records were identified and removed using Google Sheets → Remove Duplicates.
- Prevented double counting in KPIs and revenue metrics.

> **Impact:** Removed duplicate rows to ensure record uniqueness.

---

### 6.2 ❓ Missing Value Handling

- Numeric fields (children, babies, stay nights): Filled with `0` where logically appropriate.
- Categorical fields (country): Missing values replaced with `"Unknown"`.
- Textual `"NULL"` values standardized and treated as missing.

> **Impact:** Preserved dataset size while ensuring consistent grouping in pivots.

---

### 6.3 🔢 Data Type Standardization

- Converted numeric columns stored as text into numeric format.
- Validated binary fields (`is_canceled`, `is_repeated_guest`) to ensure only 0/1 values.

> **Impact:** Enabled accurate aggregation, averages, and KPI computation.

---

### 6.4 ✂️ Text Normalization

- Trimmed whitespace and standardized categorical labels (market segment, distribution channel, deposit type).
- Normalized country codes to full country names using lookup mapping.

> **Impact:** Prevented category fragmentation in pivot tables and charts.

---

### 6.5 ⚠️ Invalid Value Treatment

- Negative ADR values were flagged and handled using business logic.
- Extreme but valid values (e.g., long waiting list days) were retained to preserve real-world variability.

> **Impact:** Prevented distortion of revenue metrics and visualizations.

---

<br/>

## <img src="https://img.shields.io/badge/🧪-Feature%20Engineering-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

Derived features created to enhance analytical depth:

| Feature | Description |
|:--------|:------------|
| 👥 **Total Guests** | `adults + children + babies` |
| 🌙 **Total Stay Length** | `weekday nights + weekend nights` |
| 👨‍👩‍👧 **Family Flag** | Family vs Non-Family bookings |
| 💰 **Revenue (Derived)** | `ADR × Total Stay Length` |
| 📅 **Month Number** | Numeric month for chronological trend analysis |

---

<br/>

## <img src="https://img.shields.io/badge/⚠️-Limitations%20%26%20Known%20Constraints-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

- Revenue is derived using ADR and stay length (approximation).
- Dataset does not include external market or competitor data.
- Analysis limited to historical trends (no real-time updates).

---

<br/>

## <img src="https://img.shields.io/badge/📌-Recommendations%20for%20Future%20Data%20Collection-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

| # | Recommendation |
|:-:|:---------------|
| 1️⃣ | Enforce validation at data entry (e.g., no negative pricing) |
| 2️⃣ | Automate revenue calculation at source systems |
| 3️⃣ | Add customer-level identifiers for cohort analysis |
| 4️⃣ | Include booking source metadata for deeper attribution analysis |

---

<br/>

## <img src="https://img.shields.io/badge/✅-Conclusion-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

<blockquote>
The data cleaning pipeline successfully transformed raw hotel booking data into a high-quality analytical asset.
</blockquote>

**The cleaned dataset enables:**

- ✅ Reliable KPI computation
- ✅ Accurate cancellation and revenue analysis
- ✅ Trustworthy executive dashboards
- ✅ Actionable business insights

<br/>

---

<!-- Footer Banner -->
<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,50:16213e,100:0f3460&height=120&section=footer" width="100%" />

<p>
  <img src="https://img.shields.io/badge/Section%20C-Group%2016-0f3460?style=for-the-badge&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Data%20Cleaning-Complete%20✅-34a853?style=for-the-badge&labelColor=1a1a2e" />
</p>

</div>
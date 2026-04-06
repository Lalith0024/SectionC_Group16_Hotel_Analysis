<div align="center">

<!-- Header Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,50:16213e,100:0f3460&height=220&section=header&text=🏨%20Hotel%20Booking%20Analysis&fontSize=42&fontColor=e94560&fontAlignY=35&desc=Section%20C%20|%20Group%2016&descSize=18&descAlignY=55&descColor=ffffff&animation=fadeIn" width="100%" />

<!-- Badges -->
<p>
  <img src="https://img.shields.io/badge/Course-Capstone%201-e94560?style=for-the-badge&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Sector-Hospitality%20%26%20Tourism-0f3460?style=for-the-badge&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Tool-Google%20Sheets-34a853?style=for-the-badge&logo=googlesheets&logoColor=white&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Team%20Size-6-e94560?style=for-the-badge&labelColor=1a1a2e" />
</p>

<br/>

<!-- Title Card -->
<table>
<tr>
<td>

### 🔥 Hotel Booking Performance & Cancellation Intelligence Dashboard

> **Industry-Style Analytics Project** — Analyzing booking data to drive smarter hospitality decisions

</td>
</tr>
</table>

</div>

---

<br/>

<!-- ============================================ -->
<!-- PROJECT OVERVIEW -->
<!-- ============================================ -->

<div>

## <img src="https://img.shields.io/badge/📌-Project%20Overview-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<blockquote>
This project analyzes hotel booking data to uncover patterns in <b>cancellations</b>, <b>revenue trends</b>, <b>seasonality</b>, and <b>customer behavior</b>. The outcome is an executive-style, interactive dashboard built in Google Sheets to support data-driven decision-making for hotel management teams.
</blockquote>

<table>
<tr>
<td width="50">📊</td><td><b>Overall booking performance</b></td>
</tr>
<tr>
<td>🚫</td><td><b>Cancellation risk drivers</b></td>
</tr>
<tr>
<td>💰</td><td><b>Revenue and pricing trends</b></td>
</tr>
<tr>
<td>📡</td><td><b>Channel and customer segment performance</b></td>
</tr>
</table>

</div>

---

<br/>

<!-- ============================================ -->
<!-- BUSINESS PROBLEM -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/🎯-Business%20Problem-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

<table>
<tr>
<td>

**Context:**
The hospitality industry faces high revenue volatility due to booking cancellations and fluctuating seasonal demand.

**Core Problem:**
High cancellation rates and inconsistent booking behavior reduce revenue predictability and operational efficiency.

</td>
</tr>
</table>

**Objective — Use historical booking data to:**

- ✅ Reduce cancellation rates
- ✅ Improve revenue stability
- ✅ Optimize pricing and deposit policies
- ✅ Identify high-value, stable customer segments

<div align="center">
<table>
<tr>
<td align="center">
<h4>❓ Key Business Question</h4>
<em>"How can hotel management reduce cancellations and maximize revenue using booking behavior insights?"</em>
</td>
</tr>
</table>
</div>

---

<br/>

<!-- ============================================ -->
<!-- DATASET OVERVIEW -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/📊-Dataset%20Overview-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<div align="center">
<table>
<tr>
<th>Property</th>
<th>Details</th>
</tr>
<tr><td>📁 <b>Dataset Name</b></td><td>Hotel Booking Dataset</td></tr>
<tr><td>📐 <b>Type</b></td><td>Structured transactional data</td></tr>
<tr><td>📏 <b>Rows</b></td><td>~8,700 (post-cleaning)</td></tr>
<tr><td>📊 <b>Columns</b></td><td>30+</td></tr>
<tr><td>📅 <b>Time Period</b></td><td>2015–2017</td></tr>
<tr><td>🔗 <b>Source</b></td><td>Approved academic dataset (imported into Google Sheets)</td></tr>
</table>
</div>

<br/>

**Key Attributes:**

| Category | Fields |
|:---------|:-------|
| 🏷️ Booking Status | `is_canceled`, `reservation_status` |
| 📅 Time Features | `arrival_date_year`, `arrival_date_month` |
| 👤 Guest Details | `adults`, `children`, `babies`, `country` |
| 📡 Channel Info | `market_segment`, `distribution_channel` |
| 💵 Revenue Proxy | `adr` |

---

<br/>

<!-- ============================================ -->
<!-- DATA CLEANING -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/🧹-Data%20Cleaning%20%26%20Preparation-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

> All cleaning and preprocessing were performed in **Google Sheets** as per capstone requirements.

| Step | Description |
|:-----|:------------|
| 🔁 **Duplicate Removal** | Duplicate booking records removed using built-in deduplication |
| ❓ **Missing Values** | Numeric fields → `0` · Categorical fields → `"Unknown"` · `"NULL"` standardized |
| 🔢 **Data Type Standardization** | Converted numeric fields stored as text into proper numeric format |
| ⚠️ **Invalid Values** | Negative ADR values flagged and handled based on business logic |
| ✂️ **Text Normalization** | Trimmed whitespace and standardized category labels |
| 🌍 **Country Mapping** | ISO country codes mapped to full country names for dashboard readability |

<br/>

> 📝 A detailed **Logs/Audit sheet** documents each transformation step for traceability.

---

<br/>

<!-- ============================================ -->
<!-- FEATURE ENGINEERING -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/🧪-Feature%20Engineering-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

Derived features created to support KPI and dashboard analysis:

| Feature | Formula / Logic |
|:--------|:----------------|
| 👥 **Total Guests** | `adults + children + babies` |
| 🌙 **Total Stay Length** | `weekday nights + weekend nights` |
| 👨‍👩‍👧 **Family Flag** | Family vs Non-Family bookings |
| 💰 **Revenue (Derived)** | `ADR × Total Stay Length` |
| 📅 **Month Number** | For chronological sorting of monthly trends |

---

<br/>

<!-- ============================================ -->
<!-- KPI FRAMEWORK -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/📈-KPI%20Framework-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

<div align="center">
<table>
<tr>
<td align="center" width="160">
<h3>📋</h3>
<b>Total Bookings</b>
</td>
<td align="center" width="160">
<h3>🚫</h3>
<b>Total Cancellations</b>
</td>
<td align="center" width="160">
<h3>📉</h3>
<b>Cancellation Rate (%)</b>
</td>
<td align="center" width="160">
<h3>💰</h3>
<b>Total Revenue</b>
</td>
<td align="center" width="160">
<h3>💵</h3>
<b>Average Daily Rate</b>
</td>
</tr>
</table>
</div>

> These KPIs provide an **executive snapshot** of booking performance and revenue stability.

---

<br/>

<!-- ============================================ -->
<!-- PIVOT ANALYSIS -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/🧩-Pivot%20Analysis-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

Pivot tables were created in Google Sheets to support dashboard visualizations:

- 📊 Cancellation Rate by **Market Segment**
- 📈 Monthly **Revenue & Booking** Trends
- 💵 ADR by **Hotel Type** and Month
- ⏱️ **Lead Time Group** vs Cancellation %
- 🏷️ **Deposit Type** vs Cancellation %
- 👤 **Customer Type** Performance

> These pivots serve as the data source for all charts in the dashboard.

---

<br/>

<!-- ============================================ -->
<!-- DASHBOARD -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/📊-Dashboard-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

> The final dashboard presents **decision-ready insights** for non-technical stakeholders.

<div align="center">
<table>
<tr><th width="50">🔹</th><th align="left">Component</th><th align="left">Description</th></tr>
<tr><td>📋</td><td><b>KPI Cards</b></td><td>Bookings, Cancellation Rate, Revenue, ADR</td></tr>
<tr><td>📈</td><td><b>Line Chart</b></td><td>Revenue trend by month</td></tr>
<tr><td>📊</td><td><b>Bar Charts</b></td><td>Cancellation by market segment, deposit type</td></tr>
<tr><td>📉</td><td><b>Column Chart</b></td><td>Lead time vs cancellation</td></tr>
<tr><td>🎛️</td><td><b>Filters / Slicers</b></td><td>Hotel type, year, market segment, customer type</td></tr>
</table>
</div>

<br/>

> 🎨 The dashboard is designed with a **clean, executive layout** for quick interpretation.

---

<br/>

<!-- ============================================ -->
<!-- KEY INSIGHTS -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/💡-Key%20Insights-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<table>
<tr><td>🔴</td><td>Group and OTA bookings exhibit the <b>highest cancellation rates</b>.</td></tr>
<tr><td>🟠</td><td>Long lead-time bookings show <b>higher cancellation risk</b>.</td></tr>
<tr><td>🟢</td><td>Revenue <b>peaks during specific seasonal periods</b>.</td></tr>
<tr><td>🔵</td><td>Repeat guests demonstrate <b>lower cancellation probability</b>.</td></tr>
</table>

---

<br/>

<!-- ============================================ -->
<!-- RECOMMENDATIONS -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/📌-Recommendations-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

| # | Recommendation |
|:-:|:---------------|
| 1️⃣ | Introduce **stricter or non-refundable policies** for high-risk segments |
| 2️⃣ | Adjust **pricing dynamically** during peak demand months |
| 3️⃣ | Promote **direct and corporate channels** to reduce cancellation risk |
| 4️⃣ | Offer **loyalty benefits** to repeat guests to improve booking stability |

---

<br/>

<!-- ============================================ -->
<!-- LIMITATIONS & FUTURE SCOPE -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/⚠️-Limitations%20%26%20Future%20Scope-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<table>
<tr>
<th align="center">⚠️ Limitations</th>
<th align="center">🚀 Future Scope</th>
</tr>
<tr>
<td>Revenue derived using ADR (approximation)</td>
<td>Predictive cancellation modeling</td>
</tr>
<tr>
<td>No external market or competitor data</td>
<td>Time-series forecasting of demand</td>
</tr>
<tr>
<td>Static historical analysis (no real-time feed)</td>
<td>Real-time dashboard integration</td>
</tr>
<tr>
<td>—</td>
<td>Deeper segmentation using ML models</td>
</tr>
</table>

---

<br/>

<!-- ============================================ -->
<!-- PROJECT LINKS -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/🔗-Project%20Links-0f3460?style=flat-square&labelColor=1a1a2e" height="30" />

<div align="center">

| Resource | Link |
|:---------|:-----|
| 📊 **Google Sheets (Dashboard & Analysis)** | [Open Spreadsheet](https://docs.google.com/spreadsheets/d/1T2-b7pPUSR_gzLlc0m8FSg4cD2tSnOf1yDRmFHSPRmY/edit?gid=606106777#gid=606106777) |
| 🎤 **Presentation (PPT)** | [Open on Canva](https://www.canva.com/design/DAHBpNGcLOg/KK5TQIQfG-BmHF79dhPVLw/edit) |
| 📝 **Project Report (PDF)** | [View Report](https://docs.google.com/document/d/1LJPU7dgTpB8TEAFe7MwC6MpVELNfVWUPZQKxKzFXHmQ/edit?tab=t.0#heading=h.cif1juj8epn1) |


</div>

---

<br/>

<!-- ============================================ -->
<!-- TEAM -->
<!-- ============================================ -->

## <img src="https://img.shields.io/badge/👥-Team-e94560?style=flat-square&labelColor=1a1a2e" height="30" />

<div align="center">
<table>
<tr>
<td align="center" width="150">
<h4>Kasula Lalithendra</h4>
</td>
<td align="center" width="150">
<h4>Abhiman Singh</h4>
</td>
<td align="center" width="150">
<h4>Vridhi Chaudhary</h4>
</td>
</tr>
<tr>
<td align="center" width="150">
<h4>Ritik Raj</h4>
</td>
<td align="center" width="150">
<h4>Anant Singh</h4>
</td>
<td align="center" width="150">
<h4>Rudraksh Sharma</h4>
</td>
</tr>
</table>
</div>

<br/>

<!-- Footer Banner -->
<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a2e,50:16213e,100:0f3460&height=120&section=footer" width="100%" />

<p>
  <img src="https://img.shields.io/badge/Made%20with-❤️-e94560?style=for-the-badge&labelColor=1a1a2e" />
  <img src="https://img.shields.io/badge/Section%20C-Group%2016-0f3460?style=for-the-badge&labelColor=1a1a2e" />
</p>

</div>


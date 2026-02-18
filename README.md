# SectionC_Group16_Hotel_Analysis

Hotel Booking Performance & Cancellation Intelligence Dashboard

Course: Capstone 1 – Industry-Style Analytics Project
Sector: Hospitality & Tourism Analytics
Primary Tool: Google Sheets
Optional Tools: Python (EDA support), Looker Studio (optional)
Team Size: 4
Faculty Mentor: [Add Name]

⸻

📌 Project Overview

This project analyzes hotel booking data to uncover patterns in cancellations, revenue trends, seasonality, and customer behavior. The outcome is an executive-style, interactive dashboard built in Google Sheets to support data-driven decision-making for hotel management teams.

The dashboard provides a consolidated view of:
	•	Overall booking performance
	•	Cancellation risk drivers
	•	Revenue and pricing trends
	•	Channel and customer segment performance

⸻

🎯 Business Problem

Context:
The hospitality industry faces high revenue volatility due to booking cancellations and fluctuating seasonal demand.

Core Problem:
High cancellation rates and inconsistent booking behavior reduce revenue predictability and operational efficiency.

Objective:
Use historical booking data to:
	•	Reduce cancellation rates
	•	Improve revenue stability
	•	Optimize pricing and deposit policies
	•	Identify high-value, stable customer segments

Key Business Question:

How can hotel management reduce cancellations and maximize revenue using booking behavior insights?

📊 Dataset Overview
	•	Dataset Name: Hotel Booking Dataset
	•	Type: Structured transactional data
	•	Rows: ~8,700 (post-cleaning)
	•	Columns: 30+
	•	Time Period: 2015–2017
	•	Source: Approved academic dataset (imported into Google Sheets)

Key Attributes:
	•	Booking status: is_canceled, reservation_status
	•	Time features: arrival_date_year, arrival_date_month
	•	Guest details: adults, children, babies, country
	•	Channel info: market_segment, distribution_channel
	•	Revenue proxy: adr

⸻

🧹 Data Cleaning & Preparation

All cleaning and preprocessing were performed in Google Sheets as per capstone requirements.

Key Steps
	•	Duplicate Removal:
Duplicate booking records were removed using built-in deduplication.
	•	Missing Values:
	•	Numeric fields (children, babies, nights) → filled with 0
	•	Categorical fields (country) → replaced with "Unknown"
	•	Textual "NULL" values standardized
	•	Data Type Standardization:
Converted numeric fields stored as text into proper numeric format.
	•	Invalid Values:
Negative ADR values flagged and handled based on business logic.
	•	Text Normalization:
Trimmed whitespace and standardized category labels.
	•	Country Mapping:
ISO country codes mapped to full country names for dashboard readability.

A detailed Logs/Audit sheet documents each transformation step for traceability.

⸻

🧪 Feature Engineering

Derived features created to support KPI and dashboard analysis:
	•	Total Guests = adults + children + babies
	•	Total Stay Length = weekday nights + weekend nights
	•	Family Flag = Family vs Non-Family bookings
	•	Revenue (Derived) = ADR × Total Stay Length
	•	Month Number for chronological sorting of monthly trends

⸻

📈 KPI Framework

Key performance indicators used in the dashboard:
	•	Total Bookings
	•	Total Cancellations
	•	Cancellation Rate (%)
	•	Total Revenue (Derived)
	•	Average Daily Rate (ADR)

These KPIs provide an executive snapshot of booking performance and revenue stability.

⸻

🧩 Pivot Analysis

Pivot tables were created in Google Sheets to support dashboard visualizations:
	•	Cancellation Rate by Market Segment
	•	Monthly Revenue & Booking Trends
	•	ADR by Hotel Type and Month
	•	Lead Time Group vs Cancellation %
	•	Deposit Type vs Cancellation %
	•	Customer Type Performance

These pivots serve as the data source for all charts in the dashboard.

⸻

📊 Dashboard

The final dashboard presents decision-ready insights for non-technical stakeholders:

Components:
	•	KPI Cards (Bookings, Cancellation Rate, Revenue, ADR)
	•	Line Chart: Revenue trend by month
	•	Bar Charts: Cancellation by market segment, deposit type
	•	Column Chart: Lead time vs cancellation
	•	Filters/Slicers: Hotel type, year, market segment, customer type

The dashboard is designed with a clean, executive layout for quick interpretation.

⸻

💡 Key Insights (Sample)
	•	Group and OTA bookings exhibit the highest cancellation rates.
	•	Long lead-time bookings show higher cancellation risk.
	•	Revenue peaks during specific seasonal periods.
	•	Repeat guests demonstrate lower cancellation probability.

⸻

📌 Recommendations
	•	Introduce stricter or non-refundable policies for high-risk segments.
	•	Adjust pricing dynamically during peak demand months.
	•	Promote direct and corporate channels to reduce cancellation risk.
	•	Offer loyalty benefits to repeat guests to improve booking stability.

⸻

⚠️ Limitations & Future Scope

Limitations:
	•	Revenue derived using ADR (approximation).
	•	No external market or competitor data.
	•	Static historical analysis (no real-time feed).

Future Scope:
	•	Predictive cancellation modeling
	•	Time-series forecasting of demand
	•	Real-time dashboard integration
	•	Deeper segmentation using ML models

⸻

🔗 Project Links
	•	Google Sheets (Dashboard & Analysis): https://docs.google.com/spreadsheets/d/1T2-b7pPUSR_gzLlc0m8FSg4cD2tSnOf1yDRmFHSPRmY/edit?gid=606106777#gid=606106777
	•	Presentation (PPT): https://www.canva.com/design/DAHBpNGcLOg/KK5TQIQfG-BmHF79dhPVLw/edit
	•	Dashboard Screenshots: [file:///var/folders/n3/wwq0z1gx5414pg81gbw5pm4h0000gn/T/TemporaryItems/NSIRD_screencaptureui_Fsu9ty/Screenshot%202026-02-18%20at%2020.12.59.png]

⸻

👥 Team - 
Kasula Lalithendra ,
Abhiman SIngh ,
Vridhi Chaudhary ,
Ritik Raj ,
Anant Singh ,
Rudraksh Sharma,


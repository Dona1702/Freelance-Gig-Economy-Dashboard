**📘 `Procedure.md` – Freelance Gig Economy Dashboard**



---



**🧩 Project Title:**



**Freelance Gig Economy Dashboard (2025)**



---



**🎯 Objective:**



To analyze freelancer job trends, earnings, platform experience, client ratings, marketing impact, and regional insights using a Power BI dashboard.



---



**📦 Dataset Used:**



Kaggle Dataset: Freelancer Earnings \& Job Trends 2025



Key Fields:



\- Freelancer\_ID

\- Job\_Category

\- PlatformExperience\_Level

\- Client\_Region

\- Payment\_Method

\- Job\_Completed

\- Earnings\_USD

\- Hourly\_Rate

\- Job\_Success\_Rate

\- Client\_Rating

\- Job\_Duration\_Days

\- Project\_Type

\- Rehire\_Rate

\- Marketing\_Spend



---



**🛠️ Tools Used:**



\- Power BI Desktop

\- Power Query Editor

\- DAX (Data Analysis Expressions)



---



**🪜 Step-by-Step Procedure:**



**🔹 Step 1: Load the Dataset**



\- Open Power BI Desktop.

\- Import the CSV or Excel dataset downloaded from Kaggle.

\- Verified and transformed columns using Power Query.



---



**🔹 Step 2: Data Cleaning and Transformation (Power Query)**



\- Renamed columns for clarity.

\- Converted numerical columns (Earnings\_USD, Hourly\_Rate, etc.) to proper data types.

\- Applied filters to remove outliers or incorrect entries (e.g., negative values).

\- Use Power Query Editor to check column data types and clean missing/null values



---



**🔹 Step 3: Dashboard Layout Planning**



Sections created:



**🏠 Page 1: Overview**



**🔹DAX Measures Created**

Total Earnings = SUM('freelancer\_earnings\_bd'\[Earnings\_USD])

Avg Hourly Rate = AVERAGE('freelancer\_earnings\_bd'\[Hourly\_Rate])

Avg Client Rating = AVERAGE('freelancer\_earnings\_bd'\[Client\_Rating])

Avg Rehire Rate = AVERAGE('freelancer\_earnings\_bd'\[Rehire\_Rate])

Total Jobs Completed = SUM('freelancer\_earnings\_bd'\[Job\_Completed])



**🔹 KPI Cards**

Total Earnings

Avg Hourly Rate

Avg Client Rating

Avg Rehire Rate

Total Jobs Completed



**🔹 Visuals**

📊 Bar Chart: Earnings by Job Category

Axis: Job\_Category

Values: SUM(Earnings\_USD)

Insight:



📊 Column Chart: Hourly Rate vs Experience Level

Axis: PlatformExperience\_Level

Values: SUM(Hourly\_Rate)

Insight: Shows pay distribution by experience level



🔁 Ribbon Chart: Platform Distribution by Experience

Axis: Experience\_Level

Legend: Platform

Values: Freelancer\_ID (Count)

Insight: Experience level trends across platforms



🍩 Donut Chart: Job Success Rate by Project Type

Legend: Project\_Type

Values: Job\_Success\_Rate

Insight: Shows performance difference between Fixed vs Hourly projects



📊 Column Chart: Marketing Spend vs Earnings

X-Axis: Marketing\_Spend

Y-Axis: Earnings\_USD

Visual Type: Line or Column Chart

Insight: Evaluate ROI on marketing investment



**👤 Page 2: Freelancer Insights**



**🔹DAX Measures Created**

Avg Success Rate = AVERAGE('freelancer\_earnings\_bd'\[Job\_Success\_Rate])

Max Rehire Rate = MAX('freelancer\_earnings\_bd'\[Rehire\_Rate])

Freelancer Count = DISTINCTCOUNT('freelancer\_earnings\_bd'\[Freelancer\_ID])



**🔹 KPI Cards**

Avg Success Rate

Max Rehire Rate 

Freelancer Count 



**🔹 Visuals**

📊 Bar Chart – Earnings vs Experience

Axis: Experience\_Level

Values: SUM(Earnings\_USD)

Insight: Shows which experience levels (Beginner, Intermediate, Expert) contribute most to total earnings.



🍩 Donut Chart – Distribution of Projects

Legend: Job\_Category

Values: SUM(Job\_Completed)

Insight: Highlights which job types (e.g., Content Writing, App Dev, Data Entry) are most frequently completed by freelancers.



🔁 Bar + Line Combo – Rehire Behavior

X-Axis: Job\_Category

Bar Value: SUM(Rehire\_Rate)

Line Value: SUM(Job\_Success\_Rate)

Insight: Identifies categories where freelancers consistently deliver high-quality work and are rehired by clients.



🧱 Stacked Column Chart – Jobs Completed by Freelancer Type

X-Axis: Platform (Upwork, Fiverr, Toptal, etc.)

Y-Axis: Count of Experience\_Level

Legend (Stacked By): Job\_Category

Insight: Visual breakdown of how different job types are distributed across various platforms and freelancer types.



**🔹 Slicers Used**

Job Category

Platform

Experience Level

Client Region



**🌍 Page 3: Region Analysis**



**🔹DAX Measures Created**

Total Jobs by Region = SUM('freelancer\_earnings\_bd'\[Job\_Completed])

Total Earnings by Region = SUM('freelancer\_earnings\_bd'\[Earnings\_USD])

Avg Client Rating by Region = AVERAGE('freelancer\_earnings\_bd'\[Client\_Rating])

Avg Job Success Rate = AVERAGE('freelancer\_earnings\_bd'\[Job\_Success\_Rate])



**🔹 KPI Cards**

Total Jobs by Region

Total Earnings by Region

Avg Client Rating by Region

Avg Job Success Rate



**🔹 Visuals**

🗺️ Map – Jobs Completed by Region

Location: Client\_Region

Size / Color: Total Jobs by Region

Tooltip: Total Earnings, Avg Rating, Success Rate

Insight: Shows job distribution globally.



📊 Clustered Bar Chart – Earnings by Region

Axis: Client\_Region

Values: Earnings\_USD

Insight: Shows income-generating regions.



📊 Column Chart – Avg Client Rating by Region

Axis: Client\_Region

Values: Client\_Rating

Insight: Highlights client satisfaction by region.



🧱 Stacked Column Chart – Region vs. Project Types

Axis: Client\_Region

Legend: Project\_Type

Values: Job\_Completed

Insight: Compares preference for fixed/hourly jobs across regions.



📈 Line Chart – Marketing Spend vs. Earnings

Axis: Client\_Region

Line 1: Marketing\_Spend

Line 2: Earnings\_USD

Insight: Analyzes marketing ROI per region.



🍩Donut – Regional Share of Earnings

Legend: Client\_Region

Values: Earnings\_USD

Insight: Displays regional contribution to total income.



**🔹 Slicers Used**

Job Category

Platform

Experience Level

Client Region



**💸 Page 4: Marketing Performance**



**🔹DAX Measures Created**

Total Marketing Spend = SUM('freelancer\_earnings\_bd'\[Marketing\_Spend])

Avg Marketing Spend = AVERAGE('freelancer\_earnings\_bd'\[Marketing\_Spend])

Avg Client Rating = AVERAGE('freelancer\_earnings\_bd'\[Client\_Rating])

Total Earnings = SUM('freelancer\_earnings\_bd'\[Earnings\_USD])

Avg Rehire Rate = AVERAGE('freelancer\_earnings\_bd'\[Rehire\_Rate])

Jobs Completed = SUM('freelancer\_earnings\_bd'\[Job\_Completed])

ROI = DIVIDE(\[Total Earnings], \[Total Marketing Spend])



**🔹 KPI Cards**

Total Marketing Spend

Avg Marketing Spend

Avg Client Rating 

Total Earnings 

Avg Rehire Rate

Jobs Completed 

ROI 



**🔹 Visuals**

📊 Bar Chart – Earnings vs Marketing Spend

Axis: Experience\_Level

Values:

Bar 1: Avg Marketing Spend

Bar 2: Avg Earnings

Insight: Are experienced freelancers earning more or investing more in marketing?



🧮 Scatter Plot – Freelancer ROI

X-Axis: Marketing\_Spend

Y-Axis: Earnings\_USD

Size: Job\_Completed

Legend: PlatformExperience\_Level

Insight: Explore which profiles are high-ROI.



📉 Combo Chart – ROI by Platform \& Experience Level

X-Axis: PlatformExperience\_Level

Bar: Marketing\_Spend

Line: ROI

Insight: Identify which platforms and levels maximize ROI.



🌳 Decomposition Tree – What Drives Earnings?

Analyze: Earnings\_USD

Explain by: Marketing\_Spend, PlatformExperience\_Level, Client\_Rating, Rehire\_Rate

Insight: Drill down to revenue drivers.



**🔹 Slicers Used**

Job Category

Platform

Experience Level

Client Region



**❓ Page 5: QA**



**🔹 KPI Cards**

Total Marketing Spend

Avg Marketing Spend

Avg Client Rating

Total Earnings

Avg Rehire Rate

Jobs Completed

ROI



**🔹 Visuals**

💬 Natural Language Queries

Use the Q\&A visual to ask questions 



**🔹 Slicers Used**

Job Category

Platform

Experience Level

Client Region



---



**🔹 Step 4: UX/UI Enhancements**



\- Created bookmark navigation for section toggling

\- Added title headers and subheadings

\- Applied consistent theme and colors

\- Aligned visuals using grid layout



---



**🔹 Step 5: Final Validation \& Testing**



\- Cross-checked numbers using DAX calculations

\- Tested slicer interactivity and filters

\- Validated all charts and tooltips



---



**🔹 Step 6: Export and Upload**



\- Saved file as `FreelenceDashboard.pbix`

\- Uploaded to GitHub with:

   - `README.md` (project overview)

   - `Procedure.md` (this file)



---



**📝 Outcome:**



An interactive and insightful dashboard that enables users to:



\- Compare freelancer performance

\- Understand client behavior across regions

\- Analyze the impact of marketing on earnings

\- Drill down into specific job categories and experience levels


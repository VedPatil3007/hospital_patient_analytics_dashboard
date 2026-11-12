# Hospital Patient Analytics Dashboard \| Power BI

An interactive Power BI dashboard built to explore hospital admission
patterns, patient demographics, medical conditions, admission types,
test results, and hospital-level admission counts. The project
demonstrates an end-to-end analytics workflow, with **Advanced Microsoft
Excel and Copilot-assisted data preparation** followed by dashboard
development in **Power BI**.



## 1. Project Overview

Healthcare organizations generate large volumes of patient and admission
data. Looking at raw records individually makes it difficult to identify
patterns across gender, medical conditions, admission categories, test
results, and time.

The objective of this project was to transform a raw healthcare dataset
into a structured, interactive dashboard that makes these patterns
easier to explore. The dashboard brings key metrics and visual summaries
together on one screen, allowing users to move from an overall view of
patient admissions to more specific breakdowns.

The project also demonstrates that dashboard development is not limited
to creating charts. A substantial part of the work involved preparing
and validating the data in Excel before using it for analysis and
visualization.

## 2. Project Objectives

-   Prepare a large healthcare dataset for analysis using Microsoft
    Excel and Copilot-assisted workflows.
-   Improve the consistency and usability of column headers and text
    fields.
-   Explore patient demographics and the distribution of medical
    conditions.
-   Compare elective, urgent, and emergency admissions.
-   Examine the distribution of normal, abnormal, and inconclusive test
    results.
-   Visualize admission patterns over time.
-   Present the findings in an interactive Power BI dashboard.

## 3. Tools and Technologies

  -----------------------------------------------------------------------
  Tool                                Role in the project
  ----------------------------------- -----------------------------------
  **Microsoft Excel**                 Initial data inspection,
                                      structuring, cleaning, formatting,
                                      and validation.

  **Microsoft Copilot in Excel**      AI assistance for understanding the
                                      dataset, suggesting Excel
                                      operations and formulas, supporting
                                      data-cleaning tasks, and
                                      accelerating analysis.

  **Power BI Desktop**              Data import, modelling, KPI creation, 
                                    visual development, slicer 
                                    configuration, and dashboard design.
                                    
  -----------------------------------------------------------------------

## 4. Dataset Description

The Excel workbook contains two worksheets:

The prepared worksheet contains **55,500 rows and 15 columns**.

**Admission date coverage:** 8 May 2019 to 7 May 2024.

## 5. Data Preparation: Advanced Excel with Copilot

One of the important parts of this project was preparing the dataset
before building the Power BI report. The raw worksheet contained
inconsistent capitalization in text fields and column headers that were
not yet in a convenient format for analysis.

Microsoft Excel was used as the primary preparation environment, with
Copilot serving as an AI assistant during the process.

### Work performed in Excel

1.  **Dataset inspection:** Reviewed the workbook structure, field
    names, data types, and the overall layout of the raw records.
2.  **Column standardization:** Converted the prepared worksheet's
    headers into consistent lowercase names using underscores where
    appropriate. For example, `Date of Admission` became
    `date_of_admission`.
3.  **Text consistency:** Standardized inconsistent capitalization in
    text fields so that values could be grouped and compared more
    reliably.
4.  **Data-type checks:** Reviewed date, numeric, and categorical fields
    to make them suitable for analysis.
5.  **Data validation:** Inspected the prepared dataset for missing
    values, duplicate records, and unusual numeric values.
6.  **Analysis preparation:** Organized the cleaned worksheet into a
    more consistent tabular structure for use in Power BI.

### How Copilot supported the Excel workflow

Copilot was used as an assistant rather than as a replacement for data
validation. Its role in an Excel-based analytics workflow includes
helping to:

-   Understand unfamiliar columns and summarize the structure of a
    dataset.
-   Suggest appropriate cleaning operations for inconsistent text
    values.
-   Generate or explain formulas for data preparation.
-   Recommend ways to inspect, categorize, and summarize records.
-   Accelerate the exploration of patterns and the preparation of
    analysis-ready data.

The important takeaway is the combination of AI assistance and manual
verification: suggested operations and outputs still need to be checked
against the underlying records.

### Data-quality observations

A validation check of the uploaded workbook found:

-   No blank cells in the prepared `healthcare` worksheet.
-   534 exact duplicate rows beyond their first occurrence, when
    comparing all 15 columns.
-   108 records with negative `billing_amount` values.

These observations are documented rather than silently treated as
resolved. Duplicate records and unusual billing values should be
investigated against the source before being removed or corrected. They
are also useful reminders that a clean-looking table is not
automatically a fully validated dataset.

## 6. Power BI Dashboard Development

After preparing the data in Excel, the `healthcare` worksheet was
imported into Power BI Desktop for analysis and visualization.

The report was designed as a single-page hospital analytics dashboard.
It uses KPI cards, doughnut charts, a column chart, a time-series chart,
a horizontal bar chart, a detailed table, and a date slicer.

### A. KPI cards

Four cards provide an immediate overview:
<pre><code>
  KPI                  Dashboard value
  ------------------ -----------------
  Total Patients                   56K
  Female Patients                  28K
  Male Patients                    28K
  Total Admissions                 56K
</pre></code>
The exact record count in the prepared worksheet is 55,500; the
dashboard displays rounded values in thousands.

### B. Gender-wise Patient Distribution

A doughnut chart compares the number of male and female patients.

-   Male: 27,774 (approximately 50.04%)
-   Female: 27,726 (approximately 49.96%)

The chart makes it easy to compare the gender composition of the
dataset.

### C. Patient Count by Medical Condition

A doughnut chart breaks down the patient records across six medical
conditions:

-   Arthritis
-   Diabetes
-   Hypertension
-   Obesity
-   Cancer
-   Asthma

Each category accounts for approximately one-sixth of the records,
making the distribution relatively balanced.

### D. Patient Distribution by Admission Type

A column chart compares the three admission categories:

-   Elective
-   Urgent
-   Emergency

This visual helps compare planned admissions with urgent and emergency
cases.

### E. Patient Admission Trend Over Time

A line and area chart displays admission activity across the available
date range. It helps identify changes and fluctuations in the number of
admissions over time.

The date slicer allows the user to filter the dashboard by admission
date and examine a selected period.

### F. Patient Distribution by Test Results

A horizontal bar chart compares the three test-result categories:

-   Abnormal
-   Normal
-   Inconclusive

The visual provides a quick comparison of the distribution of recorded
test outcomes.

### G. Patient Count by Hospital

A table presents hospital names alongside their total admission counts.
It provides a more detailed view than the summary charts and allows
individual hospital records to be inspected.

## 7. Key Insights from the Dataset

The following insights are based on the 55,500 records in the prepared
Excel worksheet. Counts are exact unless marked as approximate.

### 1. Almost equal representation of male and female patients

The dataset contains 27,774 male patients and 27,726 female patients.
This corresponds to approximately 50.04% male and 49.96% female
patients.

**Insight:** The overall gender distribution is almost perfectly
balanced, with only 48 more male records than female records.

### 2. Medical conditions are distributed relatively evenly

Arthritis accounts for 9,308 records, followed by Diabetes (9,304),
Hypertension (9,245), Obesity (9,231), Cancer (9,227), and Asthma
(9,185).

**Insight:** No single medical condition dominates the dataset. Each
condition represents approximately 16.5%--16.8% of all records.

### 3. Elective admissions are slightly higher than other admission types

The admission breakdown is:

-   Elective: 18,655 (approximately 33.61%)
-   Urgent: 18,576 (approximately 33.47%)
-   Emergency: 18,269 (approximately 32.92%)

**Insight:** Elective admissions are the largest category, but the
difference between the three admission types is relatively small.

### 4. Abnormal test results form the largest test-result category

The test-result distribution is:

-   Abnormal: 18,627 (approximately 33.56%)
-   Normal: 18,517 (approximately 33.36%)
-   Inconclusive: 18,356 (approximately 33.07%)

**Insight:** Abnormal results are the largest category, although the
distribution across all three test outcomes is quite balanced. This is a
descriptive observation, not a conclusion about clinical outcomes.

### 5. Admission records cover multiple years

The dataset covers admission dates from May 2019 to May 2024. Annual
record counts are:
<pre><code>
  Year     Admission records
  ------ -------------------
  2019                 7,387
  2020                11,285
  2021                10,931
  2022                11,017
  2023                11,026
  2024                 3,854
</pre></code>
**Insight:** The largest annual count in the dataset is 2020, while
2021--2023 show relatively stable volumes. The 2019 and 2024 periods are
partial years, so their totals should not be directly compared with the
complete calendar years.

### 6. The dataset contains a large number of distinct hospital names

The prepared worksheet contains 39,876 distinct hospital-name values
across 55,500 records.

**Insight:** Hospital-level analysis has a high-cardinality category.
The dashboard's hospital table provides a way to inspect individual
hospital counts, but further standardization and validation of hospital
names would be valuable before drawing broader conclusions about
hospital performance.

## 8. Dashboard Design and Interactivity

The dashboard uses a dark healthcare-inspired theme with cyan and blue
accents to create visual consistency and distinguish key metrics from
the background.

Design elements include:

-   KPI cards positioned at the top for quick access to headline
    figures.
-   Doughnut charts for proportional comparisons.
-   Column and horizontal bar charts for category comparisons.
-   A line/area chart for time-based analysis.
-   A hospital-level table for detailed inspection.
-   A date-of-admission slicer for interactive filtering.

The visuals are arranged to provide both a high-level summary and more
detailed breakdowns without requiring users to navigate across multiple
report pages.

## 9. Skills Demonstrated

This project provided practical experience with:

**Advanced Excel** - Working with a large tabular dataset. - Data
inspection and preparation. - Standardizing column names and text
values. - Data validation and quality checks. - Using Copilot as an AI
assistant for Excel-based analysis.

**Power BI** - Importing prepared Excel data. - Building KPI cards and
charts. - Comparing categorical data. - Visualizing time-based trends. -
Configuring report-level interactivity with slicers. - Designing a
consolidated analytical dashboard.

**Business and Analytical Thinking** - Translating a dataset into
meaningful business questions. - Selecting visuals based on the type of
information being analyzed. - Identifying patterns and communicating
findings. - Recognizing data-quality limitations before making
conclusions.

## 10. Project Files

  ---------------------------------------------------------------------------------
  File                                          Description
  --------------------------------------------- -----------------------------------
  `hospital_patient_analytics_dashboard.xlsx`   Excel workbook containing the
                                                original `raw_data` and prepared
                                                `healthcare` worksheets.

  `hospital_patient_analytics_dashboard.pbix`   Power BI Desktop report file.

  `dashboard_image.png`                         Dashboard preview image.

  `README.md`                                   Project documentation, workflow,
                                                and key insights.
  ---------------------------------------------------------------------------------

## 11. How to Explore the Project

1.  Download or clone this repository.
2.  Open `hospital_patient_analytics_dashboard.xlsx` to inspect the
    original and prepared worksheets.
3.  Open `hospital_patient_analytics_dashboard.pbix` using Power BI
    Desktop.
4.  Explore the KPI cards and individual visuals.
5.  Use the **Date of Admission** slicer to examine the dashboard for a
    selected date period.

## 12. Limitations and Potential Improvements

The dashboard is intended for descriptive analysis of the supplied
dataset. It should not be interpreted as a clinical decision-support
system or as a measure of hospital quality.

Possible next steps include:

-   Investigating and resolving the 534 exact duplicate rows after
    checking the source records.
-   Reviewing the 108 negative billing amounts to determine whether they
    represent valid adjustments or data-entry issues.
-   Standardizing hospital names to reduce inconsistent categories.
-   Adding average billing amount, total billing, and length-of-stay
    KPIs.
-   Comparing billing amounts across medical conditions, admission
    types, and insurance providers.
-   Developing drill-through pages for hospital-level and patient-level
    analysis.
-   Adding more detailed time intelligence, such as monthly and
    quarterly comparisons.

## 13. Conclusion

The Hospital Patient Analytics Dashboard demonstrates an end-to-end
approach to data analytics, beginning with raw data preparation in Excel
and Copilot-assisted analysis and ending with an interactive Power BI
report.

The project highlights the importance of data preparation, consistency,
validation, visualization, and insight generation. More importantly, it
demonstrates how tools such as Microsoft Excel, Copilot, and Power BI
can work together to convert a large dataset into a structured and
accessible analytical report.

------------------------------------------------------------------------
## 👨‍💻 Author

**Ved Patil** | [LinkedIn](https://linkedin.com/in/vedpatil3076/)  
Aspiring Data Analyst | Business Intelligence Enthusiast

**Project:** Hospital Patient Analytics Dashboard\
**Tools:** Microsoft Excel \| Microsoft Copilot \| Power BI Desktop\
**Dataset size:** 55,500 records\
**Domain:** Healthcare Analytics

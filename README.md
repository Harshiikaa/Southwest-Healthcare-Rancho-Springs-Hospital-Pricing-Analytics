# Southwest Healthcare Rancho Springs Hospital Pricing Analytics Pipeline

An end-to-end healthcare pricing analytics project built using **PySpark, Snowflake, SQL, and Tableau** to transform raw hospital pricing transparency data into an analysis-ready dataset and uncover pricing variation across services, code categories, and care settings.

## Tech Stack
- PySpark
- Python
- Snowflake
- SQL
- Tableau

## Project Overview
This project focused on transforming raw hospital machine-readable pricing data into a structured dataset for analytics. The workflow included data cleaning and preparation in PySpark, SQL-based analysis in Snowflake, and visualization-ready output development for Tableau.

## Business Problem
Hospital pricing transparency files are publicly available, but they are often difficult to analyze because of:
- inconsistent formatting
- malformed fields
- sparse pricing values
- overlapping charge types

The goal of this project was to create a clean analytics layer and identify pricing variation patterns that could support pricing transparency analysis and operational decision-making.

## Data Source
The project used publicly available hospital machine-readable pricing data containing:
- service descriptions
- code types
- care settings
- listed gross charges
- discounted cash prices
- negotiated pricing fields

The raw data required extensive cleaning and standardization before meaningful analysis could be performed.

## My Contributions
- Acquired and profiled raw hospital machine-readable pricing data
- Built a PySpark-based cleaning workflow to standardize schema, convert pricing fields, and address malformed or unreliable records
- Loaded the curated dataset into Snowflake and wrote SQL queries aligned to business pricing questions
- Prepared Tableau-ready outputs to visualize pricing dispersion, negotiated ranges, and category-level differences

## Workflow
**Public MRF Source → PySpark Transformation Layer → Snowflake Query Layer → Tableau Insights Layer**

## Key Business Questions
- Which services dominate the upper and lower ends of listed gross pricing?
- Are discounted cash prices applied consistently across certain service categories?
- Which services show the greatest spread between minimum and maximum negotiated prices?
- Is pricing behavior materially different across care settings?
- How do HCPCS and RC code groups differ in charge levels and negotiated variation?

## Key Findings
- The dataset contained **73,043 records**, showing substantial fragmentation in hospital pricing.
- Average gross charge was approximately **$5.93K**.
- Average discounted cash pricing was approximately **$2.37K**.
- Average negotiated pricing showed a wide spread of nearly **$4.99K**, indicating significant reimbursement variability across payers.
- The most pronounced negotiated variation was concentrated in **complex specialty procedures**, especially vascular interventions and cardiac implant/device services.
- **Leadless pacemaker ventricular insertion/replacement** showed the largest observed average negotiated spread at more than **$52K**.
- Some **HCPCS-based services** followed a standardized **60% discounted cash pricing pattern**, suggesting rule-based pricing behavior in selected categories.
- **HCPCS services** showed higher average gross charges, while **RC-coded services** displayed greater negotiated variability.
- Care-setting analysis revealed category imbalance and malformed setting values, highlighting the importance of validating descriptive fields before interpretation.

## Business Impact
This project converted a difficult-to-use public pricing file into a structured analytics asset and surfaced interpretable pricing transparency insights across services, code categories, and negotiated rates. It demonstrates practical capability across the full analytics workflow:
- raw data preparation
- cloud SQL analysis
- business-focused insight generation
- visualization-ready reporting

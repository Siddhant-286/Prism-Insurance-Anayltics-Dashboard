# Prism Insurance Analytics Dashboard

## Problem Statement

This dashboard provides a comprehensive analysis of insurance policy performance, claim settlements, and financial metrics for Prism Insurance Pvt. Ltd. The primary goal is to assess the financial health of the company by comparing Premium Amounts against Claim Amounts and Coverage Amounts.

It helps in identifying key metrics such as claim settlement ratios, demographic risks, and policy profitability. By analyzing this data, the company can understand which age groups or policy types carry the highest risk and optimizing pricing strategies.

## Critical Insight: 

The dashboard reveals a significant discrepancy between Premium Collected (5.98M) and Claim Amounts (16.91M), indicating a high loss ratio. Additionally, a high volume of claims are currently in the "Rejected" status (4.4K), suggesting a need to investigate policy violations or fraud detection systems.

## Steps followed

- Step 1: Load the dataset (Insurance_Data.csv) into Power BI Desktop.

- Step 2: Open Power Query Editor. Checked "Column Quality" and "Column Distribution" to ensure data consistency.

- Step 3: Data cleaning involved handling null values in the "Claim Status" columns and ensuring the "Age Group" column was correctly categorized (Adult, Elder, Young Adult).

- Step 4: In the Report View, a Dark Custom Theme was applied to give the dashboard a modern, high-contrast look suitable for financial monitoring.

- Step 5: Added visual filters (Slicers) at the top for Policy Number, Customer ID, and Customer Number to allow for granular record searching.

- Step 6: Created three primary KPI Cards to display high-level financial metrics:

   - Total Premium Amount

   - Total Claim Amount

  - Total Coverage Amount

- Step 7: Added specific charts to visualize the data:

- A Custom Column/Area Chart to show Number of Claims by ClaimStatus.

- A Matrix Table to break down Claim Amount by Policy Type and Status (Pending, Rejected, Settled).

A Bar Chart to rank Premium Amount by PolicyType.

A Line Chart to analyze Claim Amount by Age Group.

A Pie Chart to show the distribution of policyholders (Policy Ratio) across Age Groups.

- Step 8: Created DAX measures for the main KPIs.

## DAX Calculations
Total Premium Amount:
- Total Premium = SUM('Insurance Data'[PremiumAmount])
Total Claim Amount:
- Total Claim Amount = SUM('Insurance Data'[ClaimAmount])
Total Coverage Amount:
- Total Coverage = SUM('Insurance Data'[CoverageAmount])
Count of Claims:
- Total Claims = COUNT('Insurance Data'[ClaimID])
Dashboard Snapshot (Power BI Service)
![Publish_Message]

Dashboard Snapshot (Power BI Desktop)
![Dashboard_Image]

### Insights

This single-page report provides several key insights into the insurance data:

[1] Key Performance Indicators (KPIs)
Financial Overview: The company has collected 5.98M in Premiums but faces a liability of 16.91M in Claims.

- Coverage: The total risk exposure (Coverage Amount) stands at 600.55M.

- Demographics: The customer base is perfectly split between Males (5,000) and Females (5,000).

[2] Claim Status Analysis
High Rejection Rate: The "Number Of Claim By ClaimStatus" chart shows that Rejected claims (4.4K) are higher than Settled claims (3.4K). This indicates strict underwriting or a high volume of invalid claims.

- Pending Volume: There are 2.3K claims currently in a pending state that require operational attention.

[3] Policy & Financial Insights
Top Revenue Driver: The "Premium Amount by PolicyType" chart shows that Travel Insurance generates the highest premium (2.5M), followed by Health (1.2M) and Auto (1.0M).

- Highest Liability: The Matrix table reveals that Travel Insurance also has the highest total claim amount (~7.09M), which correlates with it being the highest premium driver.

[4] Age Group Demographics
Risk Profile: The "Claim Amount by Age Group" line chart indicates that Adults are the highest risk group, claiming 8.8M, followed by Elders (6.4M). Young Adults claim significantly less (1.7M).

- Customer Distribution: The Pie Chart shows an equal distribution of policyholders (10K each) across Adults, Elders, and Young Adults, yet the financial impact varies drastically by group.
Customer Distribution: The Pie Chart shows an equal distribution of policyholders (10K each) across Adults, Elders, and Young Adults, yet the financial impact varies drastically by group.

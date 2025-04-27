# MarketFlash-Mini_project Database Design and Dashboard Project.

## Table of Content.
1. [Project Overview](#project-overview)
2. [Data Sources](#Data-sources)
3. [Tools](#tools)
4. [Data Preparation](#data_preparation)
5. [Interesting SQL Queries](#interesting_sql_queries)
6. [Dashboard Overview](#dashboard_overview)
7. [Results & Findings](#results_&_findings)
8. [Powerpoint Presentation](#powerpoint-presentation)
9. [Recommendation](#recommendation)
10. [Conclusion](#conclusion)

### Project Overview
---

To design and implement a robust database and interactive dashboard solution for MarketFlash, 
a growing Marketing company. This project aims to transition  MarketFlash from spreadsheet-based 
data management to a structured database and provide actionable insights through a Tableau dashboard.

*This project analyzes Marketflash's 2023 marketing data to uncover key insights on user engagement, campaign performance, and revenue trends.*


### Data Sources

**Marketing Data:** The primary dataset used for this analysis is the *"Marketing_data.xlsx"* file, 
containing detailed information about each Marketing campaign made by the company.

### Tools

1. Excel-Data Cleaning
2. Beekeeper-for Database codes
3. Tableau-creating dashboard

### Data Preparation

In this initial data preparation phase, we performed the folowing tasks:

1. Handling missing values in any column
2. Data cleaning and formating
3. Remove Duplicate rows.

### Interesting SQL Queries


 -- ROI, CTR, CR & Profit Analysis by Campaign     
```sql
-- To Test using Joins that the Database works perfectly
SELECT
    c.Campaign_Name,   
    cl.Company_Name,   
    p.Platform_Name    
FROM
    Campaigns c       
JOIN
    Clients cl ON c.Client_ID = cl.Client_ID 
JOIN
    Platforms p ON c.Platform_ID = p.Platform_ID 
ORDER BY
    cl.Company_Name,   
    c.Campaign_Name;   
```
```sql
-- KPIs Calculations
-- Click-Through Rate (CTR) Per Campaign

SELECT
    c.Campaign_Name,
    perf.Campaign_ID,
    (CAST(perf.Clicks AS FLOAT) / NULLIF(CAST(perf.Impressions AS FLOAT), 0)) * 100.0 AS CTR_Percentage
FROM
    Performance perf
JOIN
    Campaigns c ON perf.Campaign_ID = c.Campaign_ID
ORDER BY
    perf.Campaign_ID;
```

### Dashboard Overview

<img width="1196" alt="Screenshot 2025-04-27 at 17 29 01" src="https://github.com/user-attachments/assets/74e5030e-3a76-469c-ab8c-15bdc2d49d12" />


### Results/Findings

*The analysis results are summarised as follows*
   1. TikTok campaigns generally showed the highest reach(Views), but Instagram had a higher average engagement (cost per view).
   2. The men 18-40 audience segment responded particularly well to youtube video campaigns.

### Powerpoint Presentation

*[MARKETFLASH PRESENTATION .pptx](https://github.com/user-attachments/files/19433524/MARKETFLASH.PRESENTATION.pptx)*


### Recommendation
1. Test new strategies for low-performing channels by adjusting content or audience targeting.
2. Replicate top executive strategies and apply their methods across the team
3. Uk has the best conversion rate, so increasing campaigns there can drive more ROI

### Conclusion

- Implimenting this dashboard empowers MarketFlash with Data-driven insights to optimize marketing 
- campaigns, reduce costs, and improve conversion rate. By tracking performance metrics, 
- MarketFlash can make informed decosions that drive higher efficiency, better ROI, and improve customer engagement.






















          

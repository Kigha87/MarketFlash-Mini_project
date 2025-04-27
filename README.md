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

*Include some interesting code worked with*
 -- ROI, CTR, CR & Profit Analysis by Campaign     
```sql
SELECT
c.Campaign_ID,
c.Budget,
SUM(m.Impressions) AS Total_Impressions,
SUM(m.Clicks) AS Total_Clicks,
SUM(m.Conversions) AS Total_Conversions,
SUM(m.Total_Sales) AS Revenue,

ROUND(SUM(m.Clicks) * 100.0 / NULLIF(SUM(m.Impressions), 0), 2) AS CTR_Percent,
ROUND(SUM(m.conversions) * 100.0 / NULLIF(SUM(m.Clicks), 0), 2) AS CR_Percent,
ROUND((SUM(m.Total_Sales) - c.Budget), 2) AS Profit,
ROUND(SUM((m.Total_Sales) - c.Budget) * 100.0 / NULLIF(c.Budget, 0), 2) AS ROI_Percent
```
### Dashboard Overview

![Screenshot 2025-03-25 at 16 46 22](https://github.com/user-attachments/assets/1ed97b06-fc3e-48ff-aa75-1c76fdc84001)

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






















          

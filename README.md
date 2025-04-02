# MarketFlash-Mini_project Database Design and Dashboard Project.

## Table of Content.
1. [Project Overview](#project-overview)
2. [Data Sources](#Data-sources)
3. [Powerpoint Presentation](#powerpoint-presentation)
4. [Recommendation](#recommendation)
5. [Conclusion](#conclusion)

### Project Overview
---

To design and implement a robust database and interactive dashboard solution for MarketFlash, 
a growing Marketing company. This project aims to transition  MarketFlash from spreadsheet-based 
data management to a structured database and provide actionable insights through a Tableau dashboard.

*This project analyzes Marketflash's 2023 marketing data to uncover key insights on user engagement, campaign performance, and revenue trends.*

       
![Screenshot 2025-03-25 at 16 46 22](https://github.com/user-attachments/assets/1ed97b06-fc3e-48ff-aa75-1c76fdc84001)


### Data Sources

**Marketing Data:** The primary dataset used for this analysis is the *"Marketing_data.xlsx"* file, 
containing detailed information about each Marketing campaign made by the company.

### Tools

1. Excel-Data Cleaning
2. Beekeeper-for Database codes
3. Tableau-creating dashboard

### Data cleaning/preparation

In this initial data preparation phase, we performed the folowing tasks:
1. Data loading and inspection
2. Handling missing values
3. Data cleaning and formating

### Database check

*Include some interesting code worked with*
      
```sql
SELECT
c.Campaign_Name AS CampaignName,
c.Budget / c.Conversions AS Cost_Per_Clicks
FROM Campaigns c;
```

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






















          

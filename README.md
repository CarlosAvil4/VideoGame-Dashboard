# Dashboard-Historical Video Game Sales

### Dashboard Link : https://app.powerbi.com/groups/me/reports/384d017e-e935-44dc-9e7d-1626c1a36de1/ReportSection

## Problem Statement

This Power BI dashboard provides a comprehensive analysis of historical video game sales from 1980 to 2017. It offers insights into the total number of copies sold in millions, breaking down sales by region, platform, and game genre. Additionally, it includes detailed information about each game, such as its title, release year, total sales, platform, genre, and publisher.

By using this dashboard, users can identify industry trends, determine which genres and platforms have been the most successful, and analyze regional preferences. This information is valuable for game developers, publishers, and analysts looking to understand market dynamics, optimize future releases, and make data-driven decisions in the competitive gaming industry.


### Steps Followed for Creating the Video Game Sales Dashboard

- Step 1 : Load data into PowerBI Desktop, dataset is a csv file.

- Step 2 : Open Power Query Editor & Data Cleaning, the dataset was checked for missing or erroneous values. A check confirmed that sales figures were formatted correctly (in millions)

- Step 3: Column Profiling Based on the Entire Dataset. By default, Power BI profiles only the first 1000 rows, so column profiling was extended to the entire dataset to ensure accurate analysis.

- Step 4: Handling Missing Values

  (a) Sales columns: Null values in sales data were replaced with 0, assuming that missing values indicate no recorded sales.

  (b) Release Year: Games without a release year were filtered out, as this information is critical for analysis.

- Step 5: Data Transformations & Calculations


  (c) Created a calculated column for "Total Global Sales", summing up sales across different regions using DAX:

       
        Total Global Sales = 
        
        SUMX(VideoGameSales,
       VideoGameSales[NA_Sales] +
        VideoGameSales[EU_Sales] + 
        VideoGameSales[JP_Sales] +
       VideoGameSales[Other_Sales] )

![Image](https://github.com/user-attachments/assets/00e5cdd3-cdd8-426c-b9db-53673b8c6ccb)

- Step 6: Setting the Report Theme & Layout
- Step 7: Adding Visuals to the Report Canvas
- Step 8: Adding Filters & Slicers for Interactivity
- Step 9: Creating DAX Measures for Additional Insights
- Step 10: Adding Branding & Design Elements
- Step 11: Publishing to Power BI Service

## Key Insights Derived from the Dashboard
### Best-Selling Games

- The top-selling game recorded over 82 million copies sold. The majority of best-selling games belong to the Action, Shooter, and Sports genres.

- Sales Trends Over the Years

Video game sales peaked between 2006 and 2010, coinciding with the popularity of Nintendo DS, Xbox 360, and Nintendo Wii.

Recent years (2015-2017) saw a slight decline, likely due to the transition to digital sales, which are not captured in the dataset.

- Regional Sales Distribution

North America dominates the market, contributing nearly 50% of global sales.
Japan shows strong performance in RPG and Nintendo-exclusive titles.

- Platform Market Share

PlayStation and Nintendo platforms have the highest lifetime sales.
PC gaming has relatively lower recorded sales, as digital downloads are not fully captured in the dataset.

- Popular Genres & Publishers

Action, Sports, and Shooter genres account for the highest sales.
Nintendo, Electronic Arts (EA), and Activision are among the top-selling publishers.

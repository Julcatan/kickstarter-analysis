# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends

# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of the analysis is to determine how different fundraising campaigns fared in relation to their launch dates and their funding goals. 
The results will be used by Louise to make informed decisions on timing and goal setting for her fundraising campaign. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

I performed the Analysis of outcomes based on Launch Date by 
1.	Adding a Year column based on the Launch Date.
    I used the Code: =YEAR(S3) and copied it down with a double click.	
2.	Creating a Pivot Table in a new worksheet labeled “Theater Outcomes by Launch Date”.

    I marked the whole Kickstarter table, then clicked Insert Pivot table and chose to create it in a new worksheet. Then I named the worksheet “Theater Outcomes by 
    Launch Date”.
    I moved “Parent Category” and “Years” to the Filters section, added count of outcomes to the Values and pulled Date created = Launch Date to the rows section.
    I grouped the Dates by month. As of the instructions I set the Filter on the Parent Category to “theater”. Also, filtered the Columns to only show “successful”, 
    “failed”, and “canceled”.
    I sorted the campaign outcomes in descending order so "successful" is first.

3.	I created a line chart from the Pivot table to visualize the relationship between outcomes and launch month. It shows the number of successful, failed, or canceled 
    projects by month. I added the title and saved the Theater_Outcomes_vs_Launch.png file to the resource folder.
 
 
 ### Analysis of Outcomes Based on Goals

1.	I created a new sheet and label it "Outcomes Based on Goals."

2.	In the new sheet I added the following columns to hold the data:
  *	Goal
  *	Number Successful
  *	Number Failed
  *	Number Canceled
  *	Total Projects
  *	Percentage Successful
  *	Percentage Failed
  *	Percentage Canceled

3.	I created the dollar-amount ranges according to the instructions in the Goal Column.
    The last range showed Greater than 50,000 but is really asking for amounts greater or equal to 50,000. I changed the label to reflect that.

4.	I Used Countifs() functions with multiple criteria to populate the "Number successful," "Number failed," and "Number canceled" columns by filtering
    on the Kickstarter  "outcome" column, on the "goal" amount column using the goal ranges and on the "Subcategory" column using "plays" as the criteria.

    The formula I used looks like this:
    =COUNTIFS(Kickstarter!$F:$F, "successful", Kickstarter!$D:$D,"<1000",Kickstarter!R:R, "plays")

5.	I used the SUM() function under the AutoSum menu to populate the "Total Projects" column with the number of successful, failed, and canceled projects for each row.

6.	I calculated the percentage of successful, failed, and canceled projects for each row by adding a division formula to the percentage Column.
    The formula I used looks like this: =B2/E2

    I changed the column to a percentage format.
 
7.	I created the line chart to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed, or canceled projects on 
    the y- axis. I highlighted the Columns Goal, Number Successful, Number failed, Number Canceled, Percentage Successful, Percentage Failed and Percentage Canceled. 
    I then inserted the Line Chart.
 
8.	I saved the chart as Outcomes_vs_Goals.png to the resources folder.

### Challenges and Difficulties Encountered

Analysis of Outcomes Based on Launch Date: 
*It was challenging that the Dates did not show as months like in the sample output. I used the Hint in the instruction to Group the dates by month.*

Analysis of Outcomes Based on Goals: 
*It was tedious to retype formulas and change the text from “successful” to “failed” or “canceled” in the formulas. I copied and pasted formulas and used Replace under the Find menu to replace the text for each column.*


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The purpose of the analysis was to support Louise’s decision on timing for her fundraising Campaign.
The analysis suggests that the best time to launch a successful campaign would be in May, followed by June and July. 
The number of failed campaigns is spread relatively equal throughout the year. Timing does not seem to have a big influence here. 

- What can you conclude about the Outcomes based on Goals?

Campaigns with lower Goals have higher success rates. 

Campaigns with Goals less than 1000 have the highest success rates with 76%, followed by campaigns between 1000 to 4999 with a success rate of 73%. The fail rates for these campaigns are low, under 30%.

For goals between 35000 and 45000 there is a plateau where success rates are relatively high at 67% while fail rates are at 33%. 
For Goals between 20000 and 35000 the success rate is very low, and the percentage failed very high.

- What are some limitations of this dataset?

The available timeframe covers the years 2009 through 2017. Newer data could give insight into recent trends that are currently missing in our analysis.
There could be gaps in the data for cancelled campaigns. 

The Parent Category “theater” contains subcategories that not necessarily overlap with what Louise is fundraising for, e.g. restoration of theaters. 

The outcomes are only measured based on Launch date for the first analysis and only on Goals for the second one.
There are likely more factors that influence the outcomes and could alter the conclusions:
  * e.g. the length of the campaigns could have an influence.
  * if Louise’s Campaign was to happen in a wealthy area the Giving Capacity and Likelihood of success in the same time frame could be higher. The results are drawn 
  from different countries and the dataset does not include detailed locations. 

The data does not include how much money was spent per campaign to get the funding or how many donors were solicited.

- What are some other possible tables and/or graphs that we could create?

* Outcomes based on length of campaigns
* Outcomes based on Goals drilled down to Louise’s location
* Average number donation by number of backers 
* Drill down - Outcomes based on single subcategory that aligns with what Louise is fundraising for.






















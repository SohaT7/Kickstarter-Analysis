# Kickstarter Analysis
## Table of Contents
- [Overview of the Analysis](#overview-of-the-analysis)
    - [Purpose](#purpose)
    - [About the Dataset](#about-the-dataset)
    - [Tools Used](#tools-used)
    - [Description](#description)
- [Results](#results)
    - [Analysis of Outcomes Based on Launch Date](#Analysis-of-Outcomes-Based-on-Launch-Date)
    - [Analysis of Outcomes Based on Goals](#Analysis-of-Outcomes-Based-on-Goals)
    - [Challenges and Difficulties Encountered](#Challenges-and-Difficulties-Encountered)
        - [The Challenge and Difficulty](#The-Challenge-and-Difficulty)
        - [How the Challenge and Difficulty was Fixed](#How-the-Challenge-and-Difficulty-was-Fixed)
- [Summary](#summary)
- [Contact Information](#contact-information)

## Overview of the Analysis
### Purpose:
The purpose of this analysis is to help a client establish how different campaigns fared based on their launch dates and their respective funding goals. This will help the client better understand the underlying trends that may have contributed to their play 'Fever' almost reaching its funding goal target in a short time period. 

### About the Dataset:
The dataset contains information on about 4,000 crowdfunding projects. The dataset is contained in the following Excel file:

[Kickstarter data](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Kickstarter%20Analysis.xlsx)

### Tools Used:
 - Excel

### Description:
[This analysis](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Kickstarter_Challenge.xlsx) takes a look at how Kickstarter campaigns in the category of 'Theater' fared depending on the month in which they were launched, as well as how the Kickstarter campaigns in the subcategory of 'Plays' fared based on the range of amount set as a Goal for the campaign.

## Results
The two line charts depicting outcomes based on launch date and outcomes based on goals will be analysed below, followed by a discussion of the challenges and difficulties faced while producing them. 

### Analysis of Outcomes Based on Launch Date:
Outcomes based on launch date were analysed for the category of 'Theater', and a line chart was made with the month of launch on the x-axis and the number of campaigns on the y-axis. The line chart then tells us the number of campaigns that were successful, failed, and canceled, depending upon which month they were launched in. ![Theater_Outcomes_vs_Launch](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Theater_Outcomes_vs_Launch.png) 
The month of May has the highest number of successful campaigns (111 campaigns), followed by June (100 campaigns). For all twelve months, number of successful campaigns supercedes failed campaigns, although the margin between the two is the smallest (a difference of only two campaigns) in the month of December so that can be considered negligible, and the number of failed campaigns supercedes canceled ones. Few campaigns are canceled each month (range is not more than 7), with the highest number being when campaigns were launched in January, and lowest in July. The month of October does not have a data entry for it (it could either be 0 or have a value that is absent from the dataset). The highest number of failed campaigns are when campaigns were launched in the month of May, followed by July and October. The line chart for the successful campaigns has an increasing trend with three decrements from Feb-March, a longer one from May till September, and the last one from October to December. The sharpest increase for successful campaigns can be seen from April to May (an increase of 40 campaigns).

![Screensho_Theater Outcomes based on Launch Date](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Screenshot_Theater%20Outcomes%20based%20on%20Launch%20Date.png)

### Analysis of Outcomes Based on Goals:
A line chart for Outcomes Based on Goals was made with the ranges for goals on the x-axis and the percentage of campaigns in the subcategory of 'Plays' on the y-axis. The line chart then tells us the percentage of campaigns for 'Plays' that were successful, failed, or canceled for each funding goal range.

![Outcomes_vs_Goals](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Outcomes_vs_Goals.png)

The first noticeable thing in our graph is that the line trends for successful campaigns and failed campaigns are exactly complementary to one another; this is because our 'Total Projects' in this dataset is defined by adding together successful, failed, and canceled campaigns, and since no campaigns were canceled for any range of goal, successful and failed campaigns are the only ones that comprise a 100% of campaigns for that goal range. 
As the goal amount increases, there are fewer number of campaigns that are successful and more that have failed, up until the range of 25000-29999, after which the successful campaigns increase (and failed campaigns decrease) till the range of 35000-39999. It could be that increments in the goal amount up until 20000-24999 were not considerable enough for campaigns to have been successful (or not considerable enough to garner enough support for the campaign). The sharpest increase in successful campaigns (and sharpest decrease in failed campaigns) is from the range 30000-34999 till the range of 35000-39999, with no effect when range increases from 35000-39999 to 40000-44999, and the sharpest decrease in successful campaigns (and sharpest increase in failed campaigns) is for a change in range from 40000-44999 to 45000-49999, where 0% campaigns have been successful (and 100% have failed). There is an increase in successful campaigns again after 49999. 

### Challenges and Difficulties Encountered:
#### The Challenge and Difficulty:
A challenge and difficulty was encountered while making the line chart for Outcomes Based on Goal. For the last range of 'Greater than 50000' that we created, there were 4 missing 'Failed' campaigns in our 'Number Failed' column. There was no such discrepancy in the 'Number Successful' and 'Number Canceled' columns. 

![Screenshot_4 Missing Failed Campaigns](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Screenshot_4%20Missing%20Failed%20Campaigns.png)

#### How the Challenge and Difficulty was Fixed:
This discrepancy was found out by comparing the number of successful, failed, and canceled campaigns for the subcategory of 'Plays' in our datasheet versus the larger, main data sheet. The calculation for our datasheet was done by running the SUM function for data entries in the 'Number Successful', 'Number Failed', and 'Number Canceled' columns. This was followed by running the COUNTIFS function on the larger, main data sheet to count the number of successful, failed, and canceled campaigns therein. If the two numbers did not match, there was a discrepancy. There were 349 failed campaigns in our sheet as opposed to 353 in the larger data sheet: thus 4 missing campaigns in our sheet. This was fixed by creating a range of 'Greater than or Equal to 50000' for our purposes. This includes those 4 missing data points in our data sheet.

![Screenshot_Line Chart Initial](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Screenshot_Line%20Chart%20Initial.png)

![Line Chart Initial.png](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Line%20Chart%20Initial.png)

![Screenshot_Line Chart Fixed](https://github.com/SohaT7/Kickstarter-Analysis/blob/main/Images/Screenshot_Line%20Chart%20Fixed.png)

## Summary
- Conclusions about the Outcomes based on Launch Date:
We can conclude that successful campaigns reach their peak if launched in the summer months of May through July, with the highest number of successful campaigns being ones launched in May, followed by those launched in June, and then in July. There is a decrease in successful campaigns launched in the winter months of November and December. It could be because more people go to theater in the summer than in the winter and perhaps it is the popularity of a theater production in its intial months that determines its popularity henceforth to some extent, which may be why how it fares in its launch month affects how it fares afterwards as well. We can also see that the failed campaigns reach their peak in May, followed by July and October, where all three data points are quite close to one another. A peak in failed campaigns launched in summer should be taken into account in conjunction with how there are generally just a larger number of theater productions' campaigns launching in the summer so the increase in failed ones might be reflecting that general increase to some extent. 

- Conclusion about the Outcomes based on Goals:
We can conclude from the Outcomes Based on Goals that the successful campaigns' line is complemetary to the failed campaigns' line, and that the successful campaigns' line follows a decreasing trend except at 25000-29999 till 35000-39999 where it levels off until 40000-44999, and sharply decreases until a gradual rise after 45000-49999 again. 

- Limitations of this dataset:
This dataset excludes the 'live' campaigns i.e. ones which are still running. The specific dataset we considered is specific to the category of 'Theater' and subcategory of 'Plays' for our respective deliverables, and does not include other subcategories within 'Theater'. One of the data points in Theater Outcomes based on Launch Date (for the month of October) is missing. 

- Other possible tables and/or graphs that can be created:
We can create graphs for other subcategories within the category of 'Theater' (or even other categories) if we wish to expand our analysis of the underlying trends. We can include tables and/or grpahs for not only Launch Months, but Launch Quarters and Years too. We can also create a table and/or graph for Outcomes based on not only Goals but Pledged too, and then compare how the two interact with one another. Additionally, graphing for Average Donations and Launch Month might help as well. Lastly, making box plots that give a good overview of the measures of central tendency and measures of spread will be extremely beneficial. 

## Contact Information
Email: st.sohatariq@gmail.com


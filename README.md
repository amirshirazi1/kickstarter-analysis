# Kickstarting with Excel

## Overview of Project

### Purpose

Generally speaking, in the context of the Bootcamp, the purpose of this project is to practice the learnings from Module 1 in Excel. Particularly using different functions and creating charts. More specifically, in the context of the challenge, it is my goal to take the data that has been combed through and add visuals to help Louise understand what she is seeing. I created two charts to provide to Louise showing her how well different theatrical campaigns did as compared to their launch date and their funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

![Screenshot_Theater_Outcomes_vs_Launch_Date.png](https://github.com/amirshirazi1/kickstarter-analysis/blob/main/Resources/Screenshot_Theater_Outcomes_vs_Launch_Date.png)

To analyze Outcomes Based on Launch Date, I first created a pivot table based on the dataset provided in the Kickstarter sheet. To use the pivot table to my advantage, I placed Parent Category and Years under Filters, outcomes under Columns, Date Created Conversion (which will represent the months of the year) under Rows, and Count of outcomes under Values. This created a pivot table with the information I wanted to see. Before I could create the chart I further filtered the Parent Category to only provide me with results for "theater" and I filtered out the "live" outcome from the columns. 

Once my table looked the way I wanted, I chose to create a Line Chart with Markers. I also made sure to have any value of 0 create a gap in the line chart particularly to differentiate July's canceled value of 1 from 0.

### Analysis of Outcomes Based on Goals

![Screenshot_Outcomes_vs_Goals.png](https://github.com/amirshirazi1/kickstarter-analysis/blob/main/Resources/Screenshot_Outcomes_vs_Goals.png)

To analyze Outcomes Based on Goals I first created 12 rows representing the different ranges of monetary goals for each campaign. Then in the Number Successful/Failed/Canceled columns I used variations of this function: `=COUNTIFS(Kickstarter!$D:$D,">=1000", Kickstarter!$D:$D,"<=4999" Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays")`. I would change the third criteria to be searching for the corresponding condition "Successful/Failed/Canceled" and would change the first and second criteria to search for the corresponding number range in the first column. 

Next, I used `=SUM(B2:D2)` to add up the total number of projects changing the row number as I went down the column. Next, I calculated the Percentage Successful/Failed/Canceled by using `=B2/$E2`. I populated the remaining cells by filling them in automatically. Finally, I highlighted columns A, F, G, and H to create a line chart.

### Challenges and Difficulties Encountered

I did not encounter any challenges while building this out however, I could see some challenges being met particularly when working on Outcomes Based on Goals. When using the `=COUNTIFS` function I can see how it would be easy to forget to specify the greater than or equal to AND less than or equal to part of the function. Without including bother parameters you would be pulling the wrong numbers into your chart which would then throw off your percentages and of course, render your chart inaccurate.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  - First, we see the highest success rate of campaigns in May by quite a significant margin which gradually declines as Summer progresses. Second, failed campaigns stay pretty stagnant throughout the year only rising and falling marginally. Next, there was no noteworthy amount of canceled campaigns based on the date of launch. All of this information can lead us to believe that there is no significant correlation between the month of the year and failed or canceled campaigns. However, we see that there is much more range in successful campaigns throughout the year. Therefore, May seems to be the best month to launch a campaign as it saw 111 successful campaigns and only 52 failed.

![Theater_Outcomes_vs_Launch.png](https://github.com/amirshirazi1/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

- What can you conclude about the Outcomes based on Goals?

  - Based on the goal we can see that there are specific monetary ranges that seem to provide an increase in failed campaigns and an increase in successful campaigns. Particularly, $25000 - $29999 and $45000-$49999 especially saw an increase in failures. While less than $1000, $35000 - $39999, and $40000 - $44999 saw increases in success rates for plays.

![Outcomes_vs_Goals.png](https://github.com/amirshirazi1/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png)

- What are some limitations of this dataset?

  - In the Outcomes Based on Goals data set we are filtering down to the subcategory of plays whereas in the Outcomes by Launch Date was filtering from the parent category for theater. This means our Launch Date data set would include more campaigns than our Goals data set. This could potentially change our understanding and analysis of the results for each because outcomes by launch date may have had more successful campaigns in other subcategories that are not only plays. This may change our perspective on when would be the best month to launch a campaign would be for Louise's play.

- What are some other possible tables and/or graphs that we could create?

  - I would further filter down the Outcomes by Launch Date pivot table to only highlight plays instead of the parent category theater outcomes. I would also change the line chart for the Outcomes Based on Goal to a stacked bar chart. The line graph shows the same information but is inverted for the successful and the failed lines since there are no canceled play campaigns. This could be challenging or confusing to read, whereas, a stacked bar chart can show the difference between failed and successful campaigns at a certain range which can give a better and easier to understand picture. I would also create a chart and graph for visualizing what country saw the most success in theater and/or play campaigns. Additionally, I would see if the year the campaign was launched made a difference in success rate, and if it did vary year to year, what the most recent highly successful year's launch month was most successful.

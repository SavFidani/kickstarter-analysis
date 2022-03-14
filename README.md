# kickstarter-analysis
Performing analysis on kickstarter data to uncover trends.
## Overview of Project
This projects seeks to take a look at different trends of fundraising campaigns, in order to assist Louise with better understanding the success of hers. The project looks at variables such as goal funds, launch date and fundraiser categories to construct our analysis. 

### Purpose
The purpose of looking at this data is to understand factors which contribute to the success or failure of fundraising campaigns. We are also seeking to better understand trends in the data, such as success fluctuations in relation to time. 

## Analysis and Challenges
By working through the weekly module, I felt as though I was set up for success with this assignment. Below, I will break down my process for you.

### Analysis of Outcomes Based on Launch Date
STEP 1: Create the Years Column (U) utilizing the =YEARS() command, then having the results autofill for each row of data.
STEP 2: Generate the pivot table and apply the specified provisions using the pivot table side bar.
STEP 3: Using the pivot table, I then generated the line chart
![Image of Line Chart Results] (https://github.com/SavFidani/kickstarter-analysis/blob/main/Theatre_Outcomes_vs_Launchdate.png)

### Analysis of Outcomes Based on Goals 
STEP 1: Create the funding range column to divide our data
STEP 2: Use the below =COUNTSIF() formula to find our number of successful fundraising campaigns per range of goals
=COUNTIFS(Kickstarter!D:D, "<1000", Kickstarter!F:F, "Successful", Kickstarter!R:R, "plays")
Use the below =COUNTSIF() formula to find our number of failed fundraising campaigns per range of goals
=COUNTIFS(Kickstarter!D:D, "<1000", Kickstarter!F:F, "Failed", Kickstarter!R:R, "plays")
Use the below =COUNTSIF() formula to find our number of canceled fundraising campaigns per range of goals
=COUNTIFS(Kickstarter!D:D, "<1000", Kickstarter!F:F, "Canceled", Kickstarter!R:R, "plays")
STEP 3: =SUM() the results for each outcome to find our total fundraising initiatives
STEP 4: Calculate percentages by dividing each outcome total by the total number of campaigns within that goal range
STEP 5: Highlight the cells which contain the percentage data and insert a line graph. 
![Image of Line Graph Results](https://github.com/SavFidani/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered
I encountered few challenges while working with the data, as I am relatively comfortable with all of the required excel commands. That being said, within deliverable 2 a potential error that could have arisen falls within the =COUNTIF() function. Due to the extent of variables included, easily you could have ended up pulling data from the wrong place, or in the presence of a simple typo, had a non functioning equation.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
1. May is the strongest launch month for successful campaigns. There is a relatively drastic peak in the data in May, with a gradual decline to follow
2. The worst month for starting a campaign is October. Conversely, the months leading up to and immediately following October (September and November) have the lowest levels of failed campaigns, and may pose less of a risk for new initiatives.

- What can you conclude about the Outcomes based on Goals?
Taking a birds eye view at all of the data observed, it is clear that there is a much stronger presence of successful campaigns than there are failed. That being said, as the fundraising goals increase, the total percentage of failed initiatives moves coincidentally to dollar value. This indicates that smaller initiatives are more likely to succeed, where as larger pose a stronger risk of failure.

- What are some limitations of this dataset?
The data set looks at predominantly US/USD campaigns. For the purpose of fundraisign within the US, this is useful. However, the data set would not be reliable for looking at chances of success for a campaign domestically versus internationally due to the lack of foreign campaigns observed.

- What are some other possible tables and/or graphs that we could create?
Rather than the line graph used for Outcomes Based on Goals, a stacked bar chart could have also been helpful for presenting the percentage outcomes of failed, successful and cancelled for each of the goal ranges. Due to the analysis completed of the mean and median throughout the module, it may have also been helpful to superimpose a line for the mean on a graph that looks at fluctuations in the total dollar value goal of fundraising over the span of a year. This may help to understand when competition for fundraisign is high, and which months will be lower relative to the average. 

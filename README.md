# **An Analysis of Kickstarter Campaigns**
## **Performing analysis on Kickstarter data to uncover trends**
---
### **Crowd-funding Analysis on Plays**
---
#### **Background of Project**
---
##### This project was conducted to help Louise, a playwright, who wants to set up a crowd-funding campaign to fund her play “Fever.” Louise wants to set up a fundraiser for ten thousand dollars to fund her play and is concerned because of the amount. Using excel, current crowd-funding data was analyzed for trends to best help Louise plan this project successfully and give her suggestions based on other successful campaigns.
---
#### Analysis
---
##### [Kickstarter_Challenge.zip](https://github.com/16AReeves/Kickstarter-analysis/files/8191121/Kickstarter_Challenge.zip)
---
##### Above is the excel workbook that was used for this analysis. The first part of the analysis was to sort and filter the data along with adding columns to aid in the analysis. The first column added was "Average Donations," to determine how much people usually donate based on incentives. The average was found using the following code: `=IFERROR(ROUND(E2/L2,2),0).` This is a nested formula which includes the use of the `=IFERROR` and `=ROUND` functions in excel. The round function was used to find the average of donations based on the number of donators. The iferror function was used to correct the divide by zero error, which replaces the error with just a zero to show no donations were given to that campaign. 
---
##### The next step was to convert the Unix timestamps to actual dates, and this was done by using the following formula: `=(((J2/60)/60)/24)+DATE(1970,1,1).` Unix timestamps are used to describe the amount of seconds that have passed since the Unix epoch, which occurred on January 1st, 1970. The above formula takes the Unix timestamp and decodes it into a date, time, and year. Converting the Unix timestamps was done to know when campaigns were launched and ended. This information was then used in making the chart "Outcomes Based on Launch Date," shown below. 
![Outcomes Based on Launch Date](https://user-images.githubusercontent.com/98365963/156894940-3a3fc9e0-d682-4499-b53f-9434919e0d22.png)
##### The above chart is based on every crowd-funding campaign in the data set and shows when a project was started and if they were successful, failed, canceled, or currently live. Based on the chart, campaigns started in May have a high success rate compared to every other month. 
---
##### The next step of the analysis was to analyze the data for trends among all categories of crowd-funding campaigns. The first step was to split the data into parent and subcategories. After this was completed, pivot tables and pivot charts were made to analyze outcomes based on whether campaigns were successful, failed, or canceled. The first chart was made out of Outcomes based on the Parent Category, shown below:
![Parent Category Outcomes Chart](https://user-images.githubusercontent.com/98365963/156895748-4b4c25c3-3894-4aa3-9f08-5a38ab79fbdb.png)
##### The above chart shows theater and music have the highest success rate among other campaign categories. Using this, the next step was to look only at the subcategories of campaigns to determine their success or failure. Below is a chart summarizing the outcomes of subcategories for all campaigns:
![Subcategories Outcome Chart](https://user-images.githubusercontent.com/98365963/156896578-c75bccd4-2e80-420e-930c-7ba616223024.png)
##### The above chart shows plays have the highest success rate among all other subcategory campaigns. Based on the chart, plays have the highest success rate. The data was then filtered to show only plays to further understand the comparison between its success and failure rate. This is summarized in the "Subcategories Outcomes Plays Chart" below:
![Subcategories Plays Outcome Chart](https://user-images.githubusercontent.com/98365963/156896585-8c0c0103-a6f7-43aa-b815-7abcbaae4074.png)
##### The above chart shows plays have a nearly double success rate compared to failed campaigns. Using all of the new information gained from the pivot charts, all of the kickstarter data was filtered to show only theater and plays, to better understand that subset of data. 
---
##### Moving on from understanding the outcomes based on all campaigns, a closer look was taken at outcomes based solely on theater and play data. The data was used to create two new pivot tables and charts: "Theater Outcomes Based on Launch Date" and "Outcomes Based on Goals." Let's first look at the data shown from the following chart, "Theater Outcomes Based on Launch Date:"
![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/98365963/156897330-80019a4c-64f7-41b6-b464-d464682c9277.png)
##### This line graph shows the correlation between when theater campaigns launch and their outcomes. This shows theater campaigns started in May have a high success rate. Let's now determine how much the theater campaign needs to be to have the highest success rate. Below is a chart, titled "Outcomes Based on Goals" that helps show success, failure, and canceled campaigns:
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/98365963/156897680-54d92ccd-bd71-4109-83b4-f365ffddccce.png)
##### This line graph shows that play kickstarter campaigns have a high success rate below five thousand dollars. Which finishes our analysis of this data.
---
#### Challenges
---
##### There were a few challenges with this analysis: crashing excel inadvertently due to overload from incorrect pivot table rows and columns, along with getting the `=COUNTIF` function to work. Excel crashed many times when I first started learning about pivot tables and charts. I was incorrectly putting categories in the wrong boxes, which actually did teach me a lot. I learned to actually think before dragging a category to a box to create the chart. This helped me overcome the fact that I was rushing slightly while trying to learn and allowed me to learn to think more critically about data instead of just guessing. The last challenge in this analysis was learning how to use the `=COUNTIF` function in excel. The `=COUNTIF` function is used when one criterion is being looked for. During the analysis, I should have been using the `=COUNTIFS` function, so that multiple criteria could be defined. 
---
#### Results
---
##### Taking a look at the "Theater Outcomes by Launch Date," one conclusion is Louise should start the launch date for her Kickstarter campaign in May. May has the highest success rate for Kickstarter launches, even when looking at all categories. Another conclusion is Louise should never start a Theater Kickstarter campaign in December. Both success and failure lines nearly meet on the graph in December, leading us to believe it's a 50/50 chance of succeeding. 
---
##### The only conclusion I can draw from the "Outcomes Based on Goals" chart is Theater Kickstarter compaigns with a goal less than five thousand dollars tends to have the highest success rate. Anything over five thousand dollars, the campaign is nearly always a failure. Oddly enough, it's not always a failure at high ranges, as the thirty-five thousand to fourty thousand dollars range does have a success rate above 60%. Which is better odds than the other ranges on the chart. Optimally, the four thousand dollar range tends to have a high success rate at 70%. Louise should stay around the four thousand dollar amount when launching this campaign. 
---
##### Some limitations of this dataset include sample size of the data, estimation of interest in the play, and possibly incorrect amounts given. Sample size is always a factor in data and in statistics, because it can limit how far you trust the results of the data. A small sample size could throw off a lot of the results while a large sample set never has everything in existence. Larger sample sets are better because they are far more accurate. This data set has a total of 1369 theater kickstarter campaigns, which is decently sized but I'm sure there could be a ton more that this analysis didn't look at. A limitation of this data is determining interest in the play Louise wrote. This analysis cannot tell us whether people will be able to attend, only that they are backing it by donating. Some of the data could be incorrect due to misreporting of the actual data. Human error is always a factor in analysis, and the data could have been reported wrong inadvertently. 
---
##### Another possible table that could be looked at is if the length of the campaign is a factor in how well it does. If the campaign lasted over a year, that data and result could be far different than a campaign that only lasted one month. Another table and graph that could be looked at is one that compares which country Louise should start the campaign in. There could be a difference in outcomes if she starts the play in Europe instead of the US or vice versa. 

# Kickstarting with Excel

## Overview of Project

This research case study’s aim is to help Louise know the outcomes of the fundraising goal for certain type of projects within their launch dates. Louise does a wide variety of fundraising with Parent Categories ranging from Film & Video, technology, music to photography and Subcategories or genre under the Parent categories. 

### Purpose

The purpose of this research project is to analyze the outcomes of the fundraising goal for Theater (Parent category) and Plays (Subcategory) projects. With the analysis, graphs and deliverables the project will provide, Louise will have an understanding of how many projects’ fundraising goals were successful, failed or canceled with a given amount of time.  


## Analysis and Challenges

There weren’t many difficult challenges but working with big data one must be thorough to see what data are provided. In the Kickstarter excel file the launch dates and deadline were in Unix time format, so I had to change it to a regular Day/Month/Year format. So, a new column with Date Created Conversion and Date Ended Conversion were created so I can analyze when the projects were launched and ended. I did this by using the formula
* “ =(((launched_at/60)/60)/24)+DATE(1970,1,1)” for Date Created Conversion column 
* “ =(((deadline/60)/60)/24)+DATE(1970,1,1)”  for Date Ended Conversion column 

This formula helped changed Unix time format to a readable date. This mandatory change helped me getting the month data for Outcomes Based on Launch Date Deliverable. 

![DateConversionFormula](https://github.com/Monsaiaung/kickstarter/blob/a3de16078ef19f66e4ec3b247dd761b50efaa842/Resources/DateConversionFormula.png)

### Analysis of Outcomes Based on Launch Dates

By using a pivot table tool, you can find out how many projects in the Theater Category (Parent Category) have a successful, failed or canceled fundraising within a time frame. The data used are outcomes in Legend (Series) box, Date Created Conversation in Axis (Categories) box, count of the outcomes in the value box and filtering by Parent Category and years. 
There were no challenges, but a possible challenge would be not knowing which data to use and which axis the data belongs in.

![Theater_LaunchDate_pivottable](https://github.com/Monsaiaung/kickstarter/blob/cc6345b494779ad62081443b1e0c4f62da78a667/Resources/Theater_LaunchDate_pivottable.png)

### Analysis of Outcomes Based on Goals

For this analysis a new sheet with a range of goal amount was created in rows and in the columns, there are Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed and Percentage Canceled. This analysis shows the number of projects that are either successful, failed or canceled based on the goal amount in dollars. The main subcategory we are focusing on here is “Plays”. 
To count the numbers of projects the formula =Countifs was used.
In =Countifs formula, criteria range and criteria are the data input. 
The data for criteria range used in the formula were goal, outcome, and subcategory columns in the Kickstarter sheet.
The criteria were the amount of the money in goal, either “successful”, “failed” or “canceled” in outcome and “plays” for the subcategory. 
The potential challenge in this analysis is properly inputting the goal range and the symbols that show greater than, equal than, or less than. 

![Outcomebasedexcelsheet](https://github.com/Monsaiaung/kickstarter/blob/ec864ac2ae462c64e4acb7dd0c69a46eb85f50c4/Resources/Outcomebasedexcelsheet.png)

### Challenges and Difficulties Encountered

There weren't a lot of challenges but it would difficult and challenging if one doesn't know the formula needed to find the results and not knowing what data to use. 

## Results

### Conclusion on Outcomes based on Launch Date

From observing the data and the line graph of Theater Outcomes based on Launch Date, it is apparent that the theater projects' fundraising goal were mostly successful. It shows that roughly 2/3 of total projects were successful which means the goals were met or exceeded the actual amount. 
By looking at the trend it shows that May is the month with the most successful projects. It is also the peak month following with a decreasing trend line for months after. 

### Conclusion on Outcomes based on Goals

According to the data and the line graph the observations show that projects that has lower number of fundraising goal has more successful rate. It shows that as the amount of the goal increases, the successs percentage decreases and the project failed percentage increases. Another conclusion is that 85% of the projects are in the goal range of less than $1000 to $9999. The other 15% of the projects have the goal amount range of $10000 to $50000+. However as mentioned the count of projects are lesser as the goal amount increases. 

### Limitations of the dataset

For finding out the outcomes of the projects I think there were substantial data provided. One thing to be careful of would be the currency type since there were projects with Canadian Dollars or Euros, so it is unclear if the goal amount in USD is the actual amount. 

### Possible Tables or Graphs

For Outcomes based on Goals, a Clustered Columns graph would give a better visualization to show that as the goal amount increases the amount of projects and the successful project percentage decreases. The line graph does show a decreasing trend for successful projects as the goal amount increases but it lacks the visual information of how many projects there are.


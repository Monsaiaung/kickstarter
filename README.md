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


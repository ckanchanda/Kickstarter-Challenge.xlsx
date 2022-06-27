# Kickstarting with Excel

## 1. Overview of Project

### Purpose: The purpose of this excel analysis project was to organize data, create 
a visual respresentation of the data, and analyze the outcomes of a Kickstarter campaign. 

## 2. Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
I began this portion of the analysis by extracting the years from the "Date Created Conversion" 
column in the "Kickstarter" sheet and placing that data in a new column in the same sheet. I did 
this using this link "https://support.microsoft.com/en-us/office/year-function-c64f017a-1354-490d-981f-578e8ec8d3b9?ui=en-us&rs=en-us&ad=us"
to help me apply the year() function. I then created a new pivot table which I put into a new sheet labeled "Theater Outcomes by Launch Date". 
I filtered the pivot table by the "Parent Category" then subcategory "theater" and "Years". To find the data for the outcomes based on launch 
date, I filtered the columns by month, canceled, failed, successful, and grand total. I then created a line chart to visualize the relationship 
between the outcomes and the launch month. 

	*insert image "Theater_Outcomes_vs_Launch.png"*

### Analysis of Outcomes Based on Goals
To analyze the outcomes based on goals, I created a new sheet labeled "Outcomes Based on Goals" to store and organize all my data for this portion 
of the project. I then created columns for the: goal, number successful, number failed, number canceled, total projects, percentage successful, 
percentage failed, and percentage canceled. Afterwards I inputed the data from the project instrunctions into the rows which ranged from less than
1000 to more than 50000. After gathering and inputting all those numbers in the goals column, I used the COUNTIFS() function to gather the number
successful, failed, and canceled given the goal amount. An example of the formula I used to create this data was: =COUNTIFS(Kickstarter!D:D,">=1000",Kickstarter!F:F,"=successful",Kickstarter!D:D,"<=4999",Kickstarter!R:R,"=plays")
This formula was for B3. I adjusted the rest of the column and row formulas accordingly to column A, the goal. After collecting the number successful, 
failed, and canceled, I used the SUM() function to count the total projects of these three categories. With all this data, I was able to easily calculate
the percentage successful, percentage failed, and percentage canceled by dividing the according columns to column E, total projects. Lastly, I created
a line with markers chart out of all the data provided in "Outcomes Based on Goals Worksheet". I organized the Y-Axis by the percentage and the X-Axis 
by the goal amount. 

### Challenges and Difficulties Encountered
I was able to complete the analysis of outcomes based on goals quite easily with little to no difficulty. I had a more challenging time with the Analysis 
of Outcomes Based on Goals portion of the project. What troubled me first was trying to get ranges for the number successful. B2, the number successful
for the goal less than 1000 was easy to write. I used the formula: =COUNTIFS(Kickstarter!D:D,"<1000",Kickstarter!F:F,"=successful",Kickstarter!R:R,"=plays").
However trying to find the number successful for the goals who numbers ranged was really confusing for me. I watched the video on how to do this step provided 
in the instructions and read the instructions on the link provided (https://support.microsoft.com/en-us/office/countifs-function-dda3dc6e-f74e-4aee-88bc-aa8c2a866842?ui=en-us&rs=en-us&ad=us) 
Eventually, I realized I made the silly mistake of mixing up the greater and less than sign in the formulas. Once I corrected this mistake, the rest of the 
table was quite easy to complete. But then I realized I entered the second half of the data for the Goals column incorrectly, so I had to go back to all my 
columns B to E to correct my error which was tedious. 

## 3. Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
The first conclusion I can draw about the Outcomes based on Launch Date is that: for the most part as the success of the theater increased/decreased, so did the 
number of failed theater outcomes. My second conclusion would be that the number of successful theater outcomes declined a lot in the summer and the number failed
stayed consistent.   

- What can you conclude about the Outcomes based on Goals?
The Outcomes based on goals graph fluctuates a lot but what I can conclude is that the rate of the failed outcomes mostly increased as the goals increased and the
percentage successful decreased as the goal increased. 

- What are some limitations of this dataset?
One limitation of this dataset is that different countries and different currencies are included in the columns which makes analyzing the data diffiult because
each currency's value is different. Eventhough the goals column is in dollars, we don't know if that value is porportionate which can skew the outcomes. 

- What are some other possible tables and/or graphs that we could create?
Other graphs we could create would be a column, line, or pie chart for the data we analyzed in this challenge. 

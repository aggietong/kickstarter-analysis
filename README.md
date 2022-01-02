# Challenge #1 (UTOR-VIRT-DATA-PT-12-2021-U-B)
# Student: Agnes Tong

# An Analysis of Kickstarter Dataset 

## Overview of Project 

Louise, an up and coming playwright is looking to start a fundraising campaign for her play “Fever”. Her anticipated budget for the play is approximately $10,000. With the use of the crowdfunding dataset, an analysis has been performed to help provide Louise with insights of previous successful fundraising campaigns. Campaign outcomes such as fundraising goals and launch dates will help Louise to determine her own strategies to ensure a successful fundraising campaign for her play. 

## Overview of Analysis

### Analysis 1: Theater Outcomes by Launch Date

The first analysis was to determine which month Louise should launch her fundraising campaign. The following steps were taken: 
1.	Created a new column “year”, and extracted the year from the “date created conversion” column using the formula =YEAR() function
2.	A pivot table was created and the sheet was labeled “Theatre Outcomes by Launch Date”. The following variables were placed in the appropriate filters, rows, columns, rows, and values in the pivot table fields. 

![kickstarter_pic1](https://user-images.githubusercontent.com/96399622/147886473-637815d9-c278-4b2b-9d9a-71f6f8c1c60a.png)

4.	Once the pivot table was created, further filtering was done: 
-	Filter “theater” from the variable “parent category”
-	Filter “live” from the column labels for the variable “outcome” 
-	Using the Grouping function, choose Months to display every month

![kickstarter_pic2](https://user-images.githubusercontent.com/96399622/147886499-be4b14a3-84de-4beb-abbb-cecd101c4083.png)

-	Using the Move function, re-organize the outcomes successful, failed, and canceled 

![kickstarter_pic3](https://user-images.githubusercontent.com/96399622/147886524-b365a6f2-52e1-4d9f-8e41-21ff63f6c924.png)

5.	A line graph was created from the pivot table to visualize the relationship between launch month and outcomes of the campaign. The x-axis displays launch month and the y-axis displays the number of campaigns. There are three lines, representing (i) the number of successful campaigns, (ii) the number of failed campaigns, and (iii) the number of canceled campaigns for each launch month. 

![kickstarter_pic4](https://user-images.githubusercontent.com/96399622/147886535-cabcc362-ee29-4fcc-bd3e-24fba2703df0.png)

### Analysis 2: Outcomes based on Goals 

The second analysis was to determine the number and proportion of campaigns based on the goals set in dollar amounts were successful, failed, and canceled. This information would inform Louise on her own campaign goal for her play. The following steps were taken: 
1.	A new sheet was created and labeled “Outcomes Based on Goals”
2.	Eight new columns were created for each of the following variables: goal, # successful, # failed, # canceled, total # projects, % successful, % failed, and % canceled. 
3.	Under the goal column, 12 different dollar amount ranges were created. 
4.	The =COUNTIFS() function was used to populate # successful, # failed, and # canceled columns. The parameters included the campaign goal and outcome of the campaign for plays only. Examples of the formula are displayed below.

![kickstarter_pic5](https://user-images.githubusercontent.com/96399622/147886601-3f701f65-293e-4db8-858b-af376ed0ea2a.png)
![kickstarter_pic6](https://user-images.githubusercontent.com/96399622/147886607-37305750-adee-4a05-b889-014107902229.png)
![kickstarter_pic7](https://user-images.githubusercontent.com/96399622/147886610-651b3934-937f-4e41-a8cb-2d90572d055a.png)

6.	The total # of projects column was populated using the =SUM() function. It is summing the # successful, # failed, and # canceled together across each row. The formula was copied and pasted for the rest of the rows. 
7.	Percentage of successful, failed and canceled projects were calculated: 
-	Number of success divided by total # projects 
- Numner of failed divided by total # projects 
- Number of canceled divided by total # projects 
An example of the formula is displayed below: 

![kickstarter_pic8](https://user-images.githubusercontent.com/96399622/147886628-7b781837-18a9-471d-9720-f88659a348f0.png)

7.	A line chart was created to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, and canceled projects. There are three lines, representing (i) % of successful campaigns, (ii) % of failed campaigns, and (iii) % of canceled campaigns for each goal-amount category. 

![kickstarter_pic9](https://user-images.githubusercontent.com/96399622/147886636-7c57e06d-bb56-4261-b099-13561b6b66a1.png)


## Challenges
I encountered two small challenges during the analysis in order to get the right graph. The first was related to the ranges of the goal-amount category, and I had to double-check that I included >= and <= in the appropriate cells. The second was that I had not initially included “plays” only in the formula. In future, I will need to ensure I read the parameters to be included thoroughly, and double check against the code. 


## Results
The best month to launch a theater fundraising campaign is May, as the highest number of successful campaigns has shown to be launched in May. Secondly, December is the worst month to launch a fundraising campaign. 

The most successful fundraising campaign is below $1,000, with 76% of the projects reaching their goals. 
For the theater by launch date table, it is recommended that we calculate % successful, % failed, and % canceled. This will confirm that May is still the best month to launch a campaign. However, if Louise is not able to launch in May, she can also launch in June with 65% projects successful, and May or July with 63% projects successful. A line showing percentage successful, failed, canceled would be recommended as percentage is used to compare when the number in each group/category is not the same, In this case, # of projects launched by month is not the same, so showing only count may be misleading. 

From a limitations perspective, the dataset is an aggregate summary of each fundraising campaign. For example, it has the average donations, but not the median donation, and the range (lowest and highest amount). It may be helpful to also understand the demographics of the donors such as age and gender. This information may help Louise to further tailor her fundraising campaign.


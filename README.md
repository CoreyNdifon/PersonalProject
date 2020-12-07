## Motivation
Welcome to my personal dataset project. For my project I am focusing on the question: Who does the police kill the most. When this question is asked, people tend to go straight to the racial side of it. My mission for this project is to look at many types of demographics to try and find a trend. 

## Data Sources
The data I am using was collected from an ongoing database controlled by the Washington Post, who have an ongoing spreadsheet of police shootings throughout all of the United States starting from 2015 to present day. 

## Processing Steps
Due to the database of police shootings in the United States since 2015 was such a big dataset, I decided that I will only focus on Washington State for this project. The data in the spreadsheet given by the Washington Post was very organized and clean already, so luckily I only had to make a few additions to the set in order to start work. A struggle that I had with this datset is that a lot of it is string or boolean based. This meant I had to make some choices in how I was going to interpret them in python. For the boolean data types I just converted the cells to integers using `INT(cell)` to change them into 1s and 0s. For the string based data I decided to group some of the data together before changing them into integers. For example, I changed the FLEE table to 1s and 0s to interpret people in the database whether they fled or not. From there I just created some scatter plots and line graphs (histograms) of different components to try and find some trends. 

## Visualization
Once I processed the data and isolated shooting incidents to only Washington State, I created a simple but clear histogram that divided the police shootings by race. To do this, I made a secondary column next to the `RACE` column in the spreadsheet and created corresponding numbers to each of the races in the dataframe (I put other and unknown races together for a cleaner set). From this visualization, we can see that there are about twice as many white men shot and killed by police than other races.

![](Visualization.png)

After completing my main task of finding the highest number of people who were shot by police in Washington from 2015 - present, I became curious as to how I can use the database's various other variables to look at the data from another perspective. The first plot here is an overall look into how many of the people shot and killed fled and did not flee. 

![](https://github.com/CoreyNdifon/PersonalProject/blob/master/General%20Flee%20Analysis.PNG)

The next plots are a series of flee plots, but separated by race to give some insight on the situations that occured for each race. 

![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Flee%20White.PNG) ![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Flee%20Black.PNG)
![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Flee%20Asian.PNG) ![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Flee%20Hispanic.PNG)
![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Flee%20NA.PNG) ![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Flee%20Other.PNG)

Here is a plot that shows the race of each person shot by police by age:
![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Age%20by%20Race.PNG)

The final one that was interesting to me was that there were fewer people with mental illness shot and killed by police than there was without mental illness. 

![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Mental%20Ill..PNG)

## Analysis
For my analysis I wanted to do a boxplot for the `AGE` column, but ran into issues as pandas refused to form it, therefore I revisited the Age by Race plot and looked for outliers on that graph. 

![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Age%20by%20Race.PNG)

Since I couldn't use pandas to find some statistical numbers, I went to excel to calculate some statistics to analyze. 

![](https://github.com/CoreyNdifon/PersonalProject/blob/master/Statistics.PNG)

A shocking find was that once a boy turns 4 in Washington, your chances of being shot by police increases a considerable amount. Once you turn 68 in Washington, you chances decrease again. For 64 years in your life, you are at a hightened risk of being shot and killed by police. That in itself should call for some sort of reform. 

## About The Raw Data
The spreadsheet has many variables that are ambiguous to those who aren't particularly familiar with the data or subject itself. This section is to help the reader understand the spreadsheet better.

`ID`: Shows the chronological order of the police shootings. Data with an ID of 1 means that was the first shooting in the dataset, 2 meaning the second shooting, and so forth.

`NAME`: The name of the person who was killed in the police shooting.

`DATE`: Date of the shooting in the format D/MM/YYYY.

`MANNER OF DEATH`: This column will show:
- `shot`
- `shot and tasered`

`AGE`: The age of the person killed in the police shooting.

`GENDER`: The gender of the person killed in the police shooting:
- `M` for Male 
- `F` for Female
- `None` for other identified gender

`RACE`: The race of the person killed.  
- `W`: White (non-Hispanic)
- `B`: Black (non-Hispanic)
- `N`: Native-American
- `A`: Asian
- `H`: Hispanic
- `O`: Other
- `None`: Unknown

`CITY`: The city of origin where the police shooting occured.

`STATE`: The state of origin where the police shooting occured. In this project, the state will always be Washington.

`MENTAL ILL.`: Indicates if there was a case of mental illness in the person killed by police.

`THREAT LEVEL`: Indicates what level of threat the officer(s) felt at the time of the shooting. By law, an officer is allowed to use lethal force if they feel that there is a direct and immediate threat to life. The levels in the spreadsheet include:
- `attack`: The most direct and immediate threat level, which allows an officer of the law enact lethal force on the person causing that direct and immediate threat towards them. 
- `other` and `undetermined`: The remaining threat levels in the remaining cases. 

`FLEE`: Category that indicates whether the person tried to flee before being killed. 
- `Not Fleeing`: indicates that the person did not flee
- `Foot`: Indicates the person fled by foot
- `Car`: Indicates the person fled by car

`BODY CAM`: Indicates if the police officer(s) involved in the shooting had a body camera/had their body camera on. This will result in each cell having either `TRUE` or `FALSE`.

`LONG` and `LAT` show the latitude and longitude of the shooting.

`EXACT GEOCODING`: If the latitude and longitude is accurate to 100 meters of the actual location of the shooting, the cell will show `TRUE`. If not, the cell will show `FALSE`. 

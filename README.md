## Motivation
Welcome to my personal dataset project. For my project I am focusing on the question:
Who is most affected by police shootings. My motivation behind this project is the 
constant discussions throughout my life of racial prejudice in the relationship between
the African-American population and the various police forces througout the country.

Being a black person myself, I feel the need to shine a light on truth of the situation using data
analytics. Being a serious issue, I pledge to let the numbers tell the story. I understand that
numbers do not lie, but people can make the numbers tell any story they want to. This being known,
I feel it is my duty to take on this project from a ethical perspective and attitude, and let the truth speak in the purest way possible. 
## Data Sources
The data I am using was collected from an ongoing database controlled by the Washington Post, who have an ongoing spreadsheet of police shootings throughout all of the United States starting from 2015 to present day. 
## Processing Steps
Due to the amount of police shootings throughout America being exponentially high, I have chosen 
to focus only on Washington State from 2015 - present. The process in cleaning this data was simple, mainly due to the Washington Post doing such a great job in keeping their dataset organized for all these years. Having the dataset already configured in a .csv, all I had to do was filter the state table in the spreadsheet to WA (for Washington) and copy and past the respective rows. Upon filtering the data, I noticed there were few rows that had a few missing columns. Because these rows were few, I felt comfortable deleting those entire rows in order to get more complete data. Since race is a major issue in my motivation for this project, I make sure the rows I am deleted had good diversity in race to ensure no bias would occur. Exceptions to this case are cells that have missing location coordinates, as my research points are not concerned with the exact location the shootings took place. Another case are the names, as my research is not concerned with the individual names either. 
## About The Data
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

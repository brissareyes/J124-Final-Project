# J124 Final Project: California Foodbanks 
## By Brissa Reyes 
### Data Analysis Process

The first step to analyzing data is cleaning it! I used the program, [OpenRefine](https://openrefine.org/), to clean the data set named "Foodbanks in California" by [The California Association of Foodbanks](https://www.cafoodbanks.org/our-members/).

**_The following questions are based on this data-set (a csv.file in Google Sheets):_**

__Step-by-Step Answer"__

Question 1: _Which San Francisco Bay area counties are there foodbanks located in?_

1. To organize the data based on location we will isolate the area codes using the phone numbers. First, navigate to INSERT and choose PIVOT TABLE. Use the recommended settings that includes all the fields of data. 
2. Within your PIVOT TABLE settings, place the "County" data with the __Row__ field and the "Phone" data within the __Values__ field. The setting for the "Phone" can be set to _Summarize by_ COUNTA and _Show as_ Default. 
3. Next, we will use the _Filter_ function to organize the data based on region. Navigate to the _Filter by values_ option. In the text box input the values or, in this case, the area codes that are to be isolated. The area codes for San Francisco Bay Area are: 415, 510, 650, and 408. These should be typed in the format that your data is in (in this case using parenthesis, e.g (510)).
4. The pivot table will look as follows:
![Screenshot (48)](https://user-images.githubusercontent.com/109770923/183323155-77c209e7-0305-4c5b-af67-afad43b5d96b.png)
__Answer: The food banks are located in Alameda, Marin, San Francsico, San Mateo, and Santa Clara counties.__

Question 2: _Based on this data set, which zip codes have the highest number of foodbanks?_

For this question, we will need to organize the data and create new columns. 
1. Organizing our data would be a lot easier if we had the zip codes isolated. Since the zip codes are at the end of each address, one way to complete this function navigate to the DATA tab and use the "Split text to columns" feature. Within the _Seperator_ field, use the comma option. 
_Note: If your data is clean this should split them evenly, however, if there are discrepancies some fields will not split correctly._
2. The data should like as follows:
![Screenshot (49)](https://user-images.githubusercontent.com/109770923/183333415-de6982d1-f855-478e-978f-9f3715115ecf.png)
3. However, you may notice that the state and zip code fields are attached. This is becuase there were no commas seperating them in the cells. To fix this, perform the  "Split text to columns" feature once again isolating "CA" and the individal zip codes. Since the whole data set lists only California foodbanks we can disregard the column that lists the state. 
4. Now, in order to see which zip code has the highest amount of foodbanks we'll have to create another PIVOT TABLE.
5. This time, seperate the "Name" and "Zip Code" data into the _Rows_ section and "County" into _Values_ with the settings configured to COUNTA and DEFAULT.
6. The, you will filter the DATA, using the "Sort Range" feature and then using the "Advanced range sorting option". Sort the Zip Code Column from Z-->A. 
7. The data should look as follows: 
![Screenshot (51)](https://user-images.githubusercontent.com/109770923/183334808-e4c77a71-d03b-411d-b921-13864a69d6a8.png)
__Answer: The zip code with the highest number of food banks is 95973.__

Question 3: __We know which zip codes have the highest amount of foodbanks, but which city in California has the most?__
1. Similar before, create a PIVOT TABLE.
2. However, instead your __Rows__ field will include "City" and __Values__ will include "Name", with the settings set to COUNTA and DEFAULT. 
3. Change the settings in the __Rows__, "City", field so that your _Order_ DESCENDING and it's _Sorted By_ COUNTA of "Name". 
4. The data should look as follows:
![Screenshot (52)](https://user-images.githubusercontent.com/109770923/183337673-f811d0d8-75f0-4097-878e-84161fabe8aa.png)
__Answer: The city with the largest number of foodbanks is Chico, California.__

Question 4: __































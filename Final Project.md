# J124 Final Project: Mapping Foodbanks in California
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
2. The data should look as follows:
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

Question 4: _Which foodbanks are in each individual county?_
1. Utilizing the PIVOT TABLE function one again, create a table so we can easily see the foodbanks within each county. 
2. In the __Rows__ field add the "County" and "name" data. 
3. Keep the settings as their default options. 
4. The pivot table will organize the data as follows:
![Screenshot (53)](https://user-images.githubusercontent.com/109770923/183344013-8704afb4-db23-41d1-bd2c-0836f5b9f986.png)
__Answer: The Pivot table shows all the counties and the foodbanks within their locations!__

Question 5: _Which regions in California with the highest poverty rates have foodbanks?_

Some research one which counties have the highest poverty rates must be known before approaching this question. From a [Google Search](https://www.ppic.org/publication/poverty-in-california/#:~:text=Yolo%20(20.9%25)%20and%20Los,local%20areas%20and%20legislative%20districts.), the areas of Yolo and Los Angeles County were idenitified.

1. For this question, you can easily find the answer by sorting the data.
2. In the main, "California-Foodbanks" tab sort the data using the Filter function at the top area of Google Sheets.
3. Use the _Filter by values_ function to find Yolo and Los Angeles County. 
![Screenshot (54)](https://user-images.githubusercontent.com/109770923/183345176-700ac9db-be74-4d76-bd2c-f6f7031ac29b.png)
__Answer: The major foodbanks that are in the county's with the highest poverty rate are the Yolo Food Bank, Westside Food Bank, and Los Angeles Regional Food Bank.__

### Story Summary and Sourcing
Based on the data provided by The California Association of Foodbanks, it is interesting that urban areas that presumably have larger populations do not have a significantly higher number of foodbanks in their local areas. For example, Los Angeles County has around 10.04 million people compared to Yolo County, which has less than half a million residents. Although this data set was created in 2021, due to the ongoing effects of the pandemic, the number of food banks in California may have fluctuated in the recent year. A possible story arising from this data would be investigating the documentation of food banks opening and closing within the last year of the ongoing COVID-19 pandemic. To enhance this story, the data can also shed light on the specific area codes and regions that the food banks are serving. 

Some possible people to interview for this type of story can be those running the various food banks, including volunteers and coordinators, and those who receive food from these programs. In addition, to focus this story on the East Bay Area, it would be interesting to examine what food resources have opened up recently around the Berkeley Area. The [Basic Needs Center](https://basicneeds.berkeley.edu/pantry) on campus runs a pop-up food pantry available to students throughout the week. The website lists multiple volunteers which can be potential sources, with their contact information listed as foodpantry@berkeley.edu. Another potential source may be the [Alameda County Community Foodbank](https://www.accfb.org/) which has multiple distribution centers throughout the region. Regi Young, the Executive Director of the program, may have some more insight into the organization and effects of the pandemic on the numerous locations around the Bay Area. The organization???s main phone number is 1-510-635-FOOD (3663).

The [Data Dashboard](https://www.sfdph.org/dph/files/mtgsgrps/foodsectaskfrc/docs/datadashboard-combined-529.pdf) by the San Francisco Board of Supervisors, created by Paula Jones (SF Department of Public Health), would be a helpful source for a story documenting food security in the Bay Area. The creator???s contact information is paula.jones@sfdph.org. This resource contains numerous data visualizations and resources for organizations that provide food and information regarding food insecurity.Another source that might be beneficial for analyzing the broader picture of California and food insecurity can be the [2020 American Community Survey](https://data.census.gov/cedsci/table?q=poverty%20in%20California&tid=ACSST5Y2020.S1701) on poverty status in California. This source can provide the bigger picture of how poverty levels may overlap with food insecurity if particular areas.  

### Data Visualization
![yu8Yo-california-s-major-food-banks-and-where-their-headquarters-are-located-by-region (3)](https://user-images.githubusercontent.com/109770923/183468551-081c4af5-84d4-4498-b51a-ba9a52561147.png)



# J124 Final Project: California Foodbanks 
## By Brissa Reyes 
### Data Analysis Process

The first step to analyzing data is cleaning it! I used the program, [OpenRefine](https://openrefine.org/), to clean the data set named "Foodbanks in California" by [The California Association of Foodbanks](https://www.cafoodbanks.org/our-members/).

**_The following questions are based on this data-set (a csv.file in Google Sheets):_**

__Step-by-Step Answer"__

Question 1: _Where are all the foodbanks located in the San Francisco Bay Area?_

1. To organize the data based on location we will isolate the area codes using the phone numbers. First, navigate to INSERT and choose PIVOT TABLE. Use the recommended settings that includes all the fields of data. 
2. Within your PIVOT TABLE settings, place the "County" data with the __Row__ field and the "Phone" data within the __Values__ field. The setting for the "Phone" can be set to _Summarize by_ COUNTA and _Show as_ Default. 
3. Next, we will use the _Filter_ function to organize the data based on region. Navigate to the _Filter by values_ option. In the text box input the values or, in this case, the area codes that are to be isolated. The area codes for San Francisco Bay Area are: 415, 510, 650, and 408. These should be typed in the format that your data is in (in this case using parenthesis, e.g (510)).
4. The pivot table will look as follows:
![Screenshot (48)](https://user-images.githubusercontent.com/109770923/183323155-77c209e7-0305-4c5b-af67-afad43b5d96b.png)

Question 2: _Based on this data set, which region of California has the most number of foodbanks (Northern, Central, and Southern California)?_

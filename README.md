# surfs_up
Module 9 - SQLite

## Project Overview

The client wants more information about temperature trends before opening the surf shop. Using the hawaii.sqlite database the goal is to provide statistical results and recommendations about the new investment. To simplify the analysis two months, june and december, were designated to represent opposite seasons, this way, we can provide evidence that the surf and ice cream shop business is sustainable year-round. 

This document will provide results based on temperature data collected from multiple stations from 2010 to 2017. Temperature is not the only variable when it comes to determine whether the business is going to be successful or not, but for sure it's one of the main ones. We will start with temperature since ice cream and surf have a strong relationship with hot weathers, but the decision-making process can also benefit from other variables, such as population age, life style, precipitations, etc. 

**Analysis file: [SurfsUp_Challenge.ipynb](https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/SurfsUp_Challenge.ipynb)**

Deliverable 1
- [x] 1. A working query is written to retrieve the June temperatures from the date column of the Measurement table
- [x] 2. The temperatures are added to a list
- [x] 3. The list of temperatures is converted to a Pandas DataFrame
- [x] 4. Summary statistics are generated for the DataFrame


Deliverable 2
- [x] 1. A working query is written to retrieve the December temperatures from the date column of the Measurement table 
- [x] 2. The temperatures are added to a list
- [x] 3. The list of temperatures is converted to a Pandas DataFrame
- [x] 4. Summary statistics are generated for the DataFrame


Deliverable 3
- [x] 1. Overview of the analysis: Explain the purpose of this analysis
- [x] 2. Results: Provide a bulleted list with three major points from the two analysis deliverables. Use images as support where needed
- [x] 3. Summary: Provide a high-level summary of the results and two additional queries that you would perform to gather more weather data for June and December


## Resources 

- Database - SQLite file: [hawaii.sqlite](https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/hawaii.sqlite)
- Software: Python 3.7.6, Visual Studio Code 1.58.1, Jupyter Notebook 6.3.0, SQLite 3.35.4



## Results

Using the hawaii.sqlite database and filtering June and December in two different tables, we can calculate average, deviation and other statistical outcomes.

- The first thing we can observe is that the calculated mean temperature for June and December are quite similar, with a difference of only 3,9°F. The surf and ice cream shop will not be affected by severe seasonal changes, which is a good evidence that the business will be sustainable year-round.


---
<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/june_describe.png">
</kbd>  &nbsp;
<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/december_describe.png">
</kbd>  &nbsp;

----


- The values for max and min have a difference of 21°F in June and 27°F in December. Both months show maximum temperature above 80°F, and minimum below 65°F, it's a huge difference that can represent variation among stations rather than time of the year.



Another statistical analysis was made for June and December using the mean per day instead of the individual observations. This time, the count is actually the amount of days used in the research and the difference among stations is not relevant to the deviance. 

---
<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/june_describe.png">
</kbd>  &nbsp;
<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/december_describe.png">
</kbd>  &nbsp;
->
<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/june_avg_describe.png">
</kbd>  &nbsp;
<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/december_avg_describe.png">
</kbd>  &nbsp;

----

- The mean values and percentages are similar to the previous analysis, however, when we look at the max, min and deviation we can see the impact of using the groupby function and calculating the mean temperature per day before calculating the overall results. The standard deviations are significantly lower showing that the difference among stations might be more important to our decision-making process than the seasonal analysis.  


## Summary 

The temperature analysis for June and December is a good evidence that the business can be sustainable year-round. With only 3,9°F difference among mean temperatures and an overall above 70°F for both months we can say that the weather is appropriate for the segment and the shop is not going to suffer with seasonality.

The temperature observations are also affected by the location of each station, so it would be interesting to narrow down a few options for the location of the investment and analyse stations individually.  


The client already has one location in mind for the project and to finalize this temperature analysis we are going to focus on station USC00519281. 

---
<kbd> 
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/station_june.png">
</kbd>  &nbsp;

<kbd>
  <img src="https://github.com/GabrielaTuma/surfs_up/blob/31deeb35d5697deecaa908aab2a22b429f876272/Images%20for%20Analysis%20/station_december.png">
</kbd>  &nbsp;

----

Station USC00519281 is a bit below average, if we only consider the temperature variable, there are better options for the shop's location. In order to make a more conscious decision, more locations and more variables should be considered. 

We are assuming that warmer places tend to bring more business, but what if it rains a lot? What if nobody in that area is really interested in buying the products? The temperature analysis might be done, but there's a lot more that can be explored, analysing population's age and life style would be a great next step to consolidate the business idea with more insights.    




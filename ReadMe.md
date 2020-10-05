## Manhattan Real Estate Analysis Project

    Flatiron Module 2 Project Avidan Berman

### Project Overview
Real Estate Professionals generally use a buildings income, expenses and cap rate to predict a buildings value.
My goal is to create a model that can best predict a multifamily buildings value using publicly available information.
The questions I am looking to answer are:

1) Does a communities average household income effect sales prices?

2) Does the distance of the building to the closest subway effect sales price?

3) What can we expect the value of a prewar building(built before 1940) to be if it was sold in 2019?

4) Are the amount of residential units in a building independent of the zipcodes population?

5) How did the Housing Stability and Tenant Protection Act passed in July 2019 effect the amount of sales in 2019?

### The Approach
- Downloaded sales data and subway locations from nyc.gov, downloaded zip code information from the US Census
- Cleaned and analyzed data using the Pandas and Numpy Libraries
- Made API Calls from Nominatim
- Visualized the data using the MatPlotlib and Seaborn Libraries
- Created projection models using the Scipy and Sklearn Libraries

### Conclusions
1) Used a Scatterplot and a Two Tail T-test for findings. Scatterplot shows a strong positive correlation between a communities average household income and sales price. This is supported by a T-test which shows that the average size of apartments stays the same as household income rises.

![Scatter%20Income:price.png](attachment:Scatter%20Income:price.png)


2) The Scatterplot shows that there is a weak relationship between distance from subway and sales price. After diving deeper into the correlation we do see that it is slightly negative.

![subway%20scatter.png](attachment:subway%20scatter.png)

3) Using a Confidence Interval method, we find with 95% certainty that the average sale of a prewar building sold in 2019 would be within the range of (4025273.9476241507, 4025650.2607091824)

4) Using the Chi Squared method we reject the null hypothesis that the residential units in a building sold is independent of the buildings zipcode population

5) Yes, we saw an immediate decrease in sales. There was a bump at the end of the year as buyers and sellers want to close sales in time to apply it to their taxes for that year but the jump wasn't particularly large and tailed off in December of 2019.

 

![Line%20Chart.png](attachment:Line%20Chart.png)

### The Model
- Tested using a Train Test Split model and a Lasso model
- Tested multiple datasets with a different combination of features.
- The lasso model that didn't include the distance from the subway or age of the building performed the best.
- Model results:
Training Error: 905,736.133
Testing Error: 1,249,514.13


### Recommendations and Future of the Project
- The combination of Housing Stability and Tenant Protection Act and COVID-19 will likely make 2020 a slow year in terms of sales.

- We can project that area's with higher average household income will also have higher rents as the tennents can afford to pay more to live in the location they desire.

- Ammenities such as having a subway close by doesn't seem to have an effect on building sales, we can assume that also means that it doesn't have much of an effect on rent.

- In the future, this model will be helped a great deal by being able to better project rent for builings and automatically populate with data on the building by giving just an address.

# Group project to analyze - Does the size of a household impact ability to obtain higher education

# Team Members
Nick Adzema, Alice Arnold, Jasmine Bates, Maxbooz Homidas

## Files of interest in this reposiory
Team Dingo-2-2.pptx - powerpoint reviewed in class<br />
JupyterNotebooks\Edu_vs_Famv2.ipynb  - cleaned Jupyter notebook with calculations and charts used in powerpoint<br />
JupyterNotebooks\Merged.csv - final csv data file used in our final calcuations and charts<br />
Chart images are the .png files located in JupyterNotebooks folder<br />

## Null/Alternative Hypothesis
Ho : The household size has no impact on the ability to obtain higher education<br />
HA: The household size does have impact on the ability to obtain higher education<br />

## Data Sources:
We looked a Kaggle and Statista website data.  Kaggle didn't have what we were looking for and Statista required payment<br />
In the end we found both household and education data in 2019 household census data<br />
Specifically we used the census American Community Survey (ACS) 2019 data tables<br />

## Census Data Cleanup:
Data came in the form of multiple CSVs with a Geographic Area name (County,State) and some counties with blank values<br />
First step we took was merging all data into one csv and dropping the blanks (Merged.csv)<br />
Then in our Jupyter notebook code we had to remove one row with string data<br />
We also split the Geographic Area name into two columns, County and State<br />
Finally we converted datatypes to int/float and renamed columns for ease of reading<br />

## Census Data Described:
There were 50 states plus DC and Puerto Rico.  We dropped Puerto Rico as it was blank<br />
The data had over 150 variables, each variable with a column for Estimate, Percent, Percent Margin of Error, Estimate Margin of error<br />
We focused on 2 variables - Percent of population 25 years and older with a bachelor’s degree and Average Family size<br />
Note Average Family per census definitions includes the family householder (person who owns or rents the home) and all other people in the living quarters who are related to the householder by birth, marriage, or adoption.<br />
While the data is at county level (3971 counties), we took the mean across all counties to get one state value<br />

## When grouping by state, the following descriptive statistics were observed in the two variables of interest:
Percent educational attainment mean =16.439686520228584<br />
Percent educational attainment median =16.243137254901956<br />
Percent educational attainment standard deviation =3.546377864546357<br />
Avg Family Size Mean =3.097651993300869<br />
Avg Family Size Median =3.048257575757576<br />
Avg Family Size standard deviation =0.17238587465693725<br />

The lower quartile of Percentage of Education is: 13.869074675324672<br />
The upper quartile of Percentage of Education is: 18.140404040404036<br />
The interquartile range of Percentage of Education is: 4.271329365079364<br />
Values below 7.462080627705626 could be outliers.<br />
Values above 24.54739808802308 could be outliers.<br />
DC is an outlier at 25.25%<br />

The lower quartile of Avg Family size is: 2.985346902654867<br />
The upper quartile of  Avg Family size is: 3.215403138528138<br />
The interquartile range of  Avg Family size is: 0.23005623587327095<br />
The the median of Avg Family size: 3.048257575757576<br />
Values below 2.6402625488449605 could be outliers.<br />
Values above 3.5604874923380443 could be outliers.<br />
Utah is right at the outlier limit at 3.56%<br />

## Analysis of the correlation between Percent educational attainment and Average Family size:
We did scatter plot with Education/Avg family size<br />
We added a linear regression model and calculated the pearson r vaule<br />
The calcuated R Value was -.09<br />
Since thie R value is so close to 0, it showed us the correlation was not significant enough to accept the alternative hypothesis<br />
Also futher analysis with chi square and pvalue were not necessary as we already knew to reject the alternative hypotehsis.<br />

## Conclusion:
R-value of -0.09 is too insignificant and so close to 0; we accept the null hypothesis<br />

## Some additional analysis we'd look at next if we continued our project:
We could do more analysis at county level<br />
We'd look at additional potential factors like income and geographic regions<br />
We could also build a heat map to visualize the high and low areas more easily<br />
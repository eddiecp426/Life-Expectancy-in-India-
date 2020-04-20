# Life-Expectancy-in-India

## Project Purpose and Description

In this project, I looked at the the various features that influence Life Expectancy in seven states in India.  I analyzed the features to determine if people that tend to come from a certain demographic live a shorter or longer life. I then tested models that would predict average life expectancy.

## Tools (all using Python and its various libraries)
   - Pandas
   - Numpy
   - Seaborn
   - Matplotlib
   - Scikit Learn
   
## Data:
The data used was in the form of a csv from [Kaggle](https://www.kaggle.com/rajanand/mortality).

Over 480,000 individual records pertaining to the death of people in different states in India between the years 2002 and 2012

<ins> Features </ins>

household number, state, district, rural, sex, usual residence, age, marital status, highest qualification status, occupation status, disability status, illness type, chew, smoke, alcohol, owner status, is water filtered, is toilet shared,  does household have electricity, lighting source, cooking fuel, kitchen availability, has refrigerator, is covered by health scheme

## Target

### Age

<p align="center">
 <img src="images/outcome.png" width="500">
</p>

## EDA

<p align="left">
<img src="images/districtno.png" width="550"/>
</p>
  
<p align="center">
<img src="images/occupation.png" width="550"/>
</p>

<p align="right">
<img src="images/maritalstatus.png" width="550"/>
</p>
  
<p align="center">
<img src="images/elevel.png" width="550"/>
</p>
  
<p align="left">
<img src="images/elevel.png" width="550"/>
</p>
 
## Taking a Closer Look at the Data
<p align="center">
<img src="images/corr.png" width="1000">
</p>

## Modeling

### Is that data a good candidate for regression?

- There's little to no multicolinearity between the features
- The relationship between the features and the outcome in mostly linear
- The residuals are normalized
- The data is homoscedatic 

<p align="center">
<img src="images/nresiduals.png" width="500">
</p>


After cleaning the data, examining viewing correlations,  and determining that the dataset was viable for a Linear Regression, I ran a model and achieved an accuracy rate of 32%. 

<p align="center">
<img src="images/lr.png" width="500">
</p>

<p align="center">
<img src="images/olsresults.png" width="750">
</p>

<br/>

## Probability Plot
![](images/qqplot.png)

## Conclusion and Future work

In our final model, we achieved an adjusted r-squared value of 85% using a Ridge Regression.  Using the evaluation metric mean absolute error, we were able to pedict the price of a home within roughly $100,000. Although not excellent, the result was adequate.  In the future, we would like to explore using other models such as the Lasso Regression or a Neural Network. 


![](images/lrprediction.png)

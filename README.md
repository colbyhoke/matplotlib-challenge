# matplotlib-challenge
## About
This Jupyter Notebook takes in CSVs about mice and drug trials. CSVs are:
* /data/Mouse_metadata.csv.csv
* /data/Study_results.csv.csv

Analysis file:
* /pymaceuticals_ch.ipynb

<br>--------------------------------------------------------------------------------------------
<br>**OBSERVATIONS:**
1. The 4 key drug regimens I've been asked to go into more detail on are: Capomulin, Ramicane, Infubinol, and Ceftamin. However, based on the data seen in the summary tables, I think we could look at Propriva as another possibility as it seems to out perform Ceftamin and Infubinol in some aspects.
1. Ramicane seems to be very effective along with Capomulin nad has a, generally, smaller final tumor volume based on the data collected. It's overall distribution is also, on average, lower in tumor size.
1. The effectiveness over time for Capomulin suggests that it continues to reduce the tumor size for the length of time the mouse is on the regimen.
1. There's no data to support recurrent tumors post-regimen. More data is needed to see if tumor growth restarts after the end of the treatment.

<br>--------------------------------------------------------------------------------------------

## Reports in file:
### Number of entries / mice in the merged dataframe
Merged two dataframes from Mouse_metadata.csv.csv and Study_results.csv.csv
Confirm # of entries and # of datapoints

### Check for duplicate data entries
Based on Mouse ID and Timepoint

### Get all data for the mice with duplicates
All data, duplicated or not

### Create clean dataframe
Remove the mice with any duplicates
We can't tell which duplicated entries are valid, so remove the mouse entirely to not skew data

### Number of entries / mice in the clean dataframe
Confirm # of entries and # of datapoints

### Summary statistics tables
Mean, median, variance, standard deviation, and SEM of the tumor volume for each regimen
* First table uses multiple series and combines
* Second table uses a single groupby() function

### Bar plots
Using both Pandas's DataFrame.plot() that shows the number of total mice for each treatment regimen throughout the course of the study.
Using Matplotlib's pyplot that shows the number of total mice for each treatment regimen throughout the course of the study.

### Pie plots
Generate a pie plot showing the distribution of female versus male mice using pandas
Generate a pie plot showing the distribution of female versus male mice using pyplot

### Quartiles, outliers, and boxplots
Calculate the final tumor volume of each mouse across four of the most promising treatment regimens.
Calculate the IQR and quantitatively determine if there are any potential outliers. 
Built a function to handle repetitive nature of this work.
Generate a box plot of the final tumor volume of each mouse across four regimens of interest

### Line and scatter plots
Generate a line plot of time point versus tumor volume for a mouse treated with Capomulin
Generate a scatter plot of mouse weight versus average tumor volume for the Capomulin regimen

### Correlation and regression
Calculate the correlation coefficient and linear regression model for mouse weight and average tumor volume for the Capomulin regimen

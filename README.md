# Metadata Analysis-Module 5 Challenge
Goal: To utilize Matplotlib to analyze pharmaceutical lab test result data. 

 The data set consists of 249 mice who were identified with SCC tumors and were treated with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The study's purpose was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

I joined Pymaceuticals, Inc. and was given access to data from an animal study testing treatments for squamous cell carcinoma. The study involved 249 mice with SCC tumors who received a range of drug regimens. I was tasked with generating tables and figures for a technical report of the study results.

First, I prepared the data by merging the mouse_metadata and study_results DataFrames into a single DataFrame. Then, I checked for duplicate time points for mouse IDs, removed the data associated with any duplicates, and displayed the updated number of unique mice IDs.

Next, I generated a DataFrame of summary statistics for each drug regimen, including the mean, median, variance, standard deviation, and SEM of the tumor volume.

I created two identical bar charts showing the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study, using both Pandas DataFrame.plot() and Matplotlib's pyplot methods. I also generated two identical pie charts showing the distribution of female versus male mice in the study, using both Pandas DataFrame.plot() and Matplotlib's pyplot methods.

To calculate quartiles, find outliers, and create a box plot, I first created a grouped DataFrame that showed the last (greatest) time point for each mouse, and then merged it with the original cleaned DataFrame. Then, I created a list that held the treatment names and an empty list to hold the tumor volume data. I looped through each drug in the treatment list, located the rows in the merged DataFrame that corresponded to each treatment, and appended the resulting final tumor volumes for each drug to the empty list. I determined outliers by using the upper and lower bounds and printed the results. Finally, I generated a box plot using Matplotlib that showed the distribution of the final tumor volume for all mice in each treatment group, highlighting any potential outliers in the plot by changing their color and style.

I selected a single mouse treated with Capomulin and generated a line plot of tumor volume versus time point for that mouse. I also generated a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen. Finally, I calculated the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen and plotted the linear regression model on top of the scatter plot.

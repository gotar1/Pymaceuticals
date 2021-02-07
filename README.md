# Pymaceuticals Matplotlib - The Power of Plots

## Background

![Laboratory](Images/Laboratory.jpg)

Pymaceuticals Inc., a burgeoning pharmaceutical company based out of San Diego. Pymaceuticals specializes in 
anti-cancer pharmaceuticals. In its most recent efforts, it began screening for potential treatments for 
squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

In the company most recent animal study [result](/Pymaceutical/data/Study_results.csv), 249 mice identified with 
SCC tumor growth [data](/Pymaceutical/data/Mouse_metadata.csv) and were treated through a variety of drug regimens. Over the course of 45 days, tumor development
was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, 
Capomulin, versus the other treatment regimens. The executive team has asked for a top-level summary of the study results.

## Analysis

Our analysis was broken down as following:

* Before beginning the analysis, we checked the data for any mouse ID with duplicate time points.
* Duplicate mouse ID 'g989' was removed along with all data associated with id.

* Generate a summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

#### <a id="summary-statistics-table"></a>Summary Statistics Table
```
Drug          mean     median        var       std       sem
Ramicane   40.216745  40.673236  23.486704  4.846308  0.320955
Capomulin  40.675741  41.557809  24.947764  4.994774  0.329346
Infubinol  52.884795  51.820584  43.128684  6.567243  0.492236
Placebo    54.033581  52.288934  61.168083  7.821003  0.581331
Ceftamin   52.591172  51.776157  39.290177  6.268188  0.469821
Stelasyn   54.233149  52.431737  59.450562  7.710419  0.573111
Zoniferol  53.236507  51.818479  48.533355  6.966589  0.516398
Ketapril   55.235638  53.698743  68.553577  8.279709  0.603860
Propriva   52.320930  50.446266  43.852013  6.622085  0.544332
Naftisol   54.331565  52.509285  66.173479  8.134708  0.596466
```

* Generated a bar plot using Matplotlib to show the number of total mice for each treatment regimen 
throughout the course of the study.

#### <a id="bar-chart"></a>Bar Chart
![bar chart](../Images/bar.png)

* Generated a pie plot using Matplotlib that shows the distribution of female or male mice in the study.

#### <a id="pie-chart"></a>Pie Chart
![pie chart](../Images/pie.png)

* Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: 
Capomulin, Ramicane, Infubinol, and Ceftamin.
* Calculated the quartiles and IQR and quantitatively determined any potential outliers across all four treatment regimens.

* Using Matplotlib, generated a box and whisker plot of the final tumor volume for all four treatment regimens
and highlighted potential outliers in the plot.

#### <a id="box-whisker-chart"></a>Box and Whisker chart
![box chart](../Images/box.png)

* Selected the mouse that was treated with Capomulin and generated a line plot of time point versus tumor volume for that mouse.

#### <a id="line-chart"></a>Line Chart
![line chart](../Images/line.png)

* Generated a scatter plot of mouse weight versus average tumor volume for the Capomulin treatment regimen.

#### <a id="scatter-chart"></a>Scatter Chart
![scatter chart](../Images/scatter.png)

* Calculated the correlation coefficient and linear regression model between mouse weight and average tumor
volume for the Capomulin treatment.

#### <a id="regression-chart"></a>Regression Chart
The correlation coefficient is 0.95
R squared is: 0.903
y = 0.89x + 22.76
![regression chart](../Images/corr.png)

## Conclusion

* Overall, it is clear that Capomulin is a viable drug regimen to reduce tumor growth.
* Capomulin had the most number of mice complete the study, with the exception of Remicane, all other regimens observed a number of mice deaths across the duration of the study.
* There is a strong correlation between mouse weight and tumor volume, indicating that mouse weight may be contributing to the effectiveness of any drug regimen.
* There was one potential outlier within the Infubinol regimen. While most mice showed tumor volume increase, there was one mouse that had a reduction in tumor growth in the study.


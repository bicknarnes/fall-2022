
# wage

Recreate Figure 1.1 of ISLR2, which visualizes the Wage dataset.

* This in-class exercise gollow the progression in [here](notebooks/02-tidy-wage.ipynb)
* [colab notebook)](https://colab.research.google.com/drive/1AeHmRJ5AfIDIIB8I13qAd7TADeg0paeJ)

## Goals

* Access ISLR2 data in R format -- get it onto the local filesystem for processing with Python
* Introduce pandas for reading/processing tabular data (built with numpy & matplotlib)
* Debug a warning
* Deal with missing data
* Simple statistical plots
* Customing plots with matplotlib
* Introduce seaborn (statistical visualization library built with pandas and matplotlib)
* Prototype in Colab and migrate to version controlled github repo
* Reproducible anallysis and nicely documented according to the 6-month rule

## Exercises

1. Get the data out of R and into a CSV
  * [rdata repo](https://github.com/ds5110/rdata)
2. Download the data
3. Read the CSV with pandas
4. Inspect the data
5. Plot with pandas
6. Reproduce the scatterplots in Figure 1.1 of ISLR2
7. Customize the plot -- add a title
8. Reproduce the boxplots in Figure 1.1 of ISLR2
9. Debug the VisibleDeprecationWarning
  * STOPPED HERE (on day 1) (got the warning, but didn't debug it)
10. Deal with missing values
11. Customize the axis tick labels
12. Create a new column with `.apply()` -- transforming a dataframe
13. Revisit the scatterplot by year -- boxplots are more informative
14. Introducing seaborn
15. Customizing seaborn
  * [pandas.md](pandas.md)
  * [numpy.md](numpy.md)

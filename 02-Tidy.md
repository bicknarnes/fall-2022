
## 02-Tidy

* [colab notebook](https://colab.research.google.com/drive/1Esin7yuwnGj7r9oTg3WkYYtieqSOIuw0?usp=sharing)

## Goals

* Processing and managing tidy/tabular data -- Pandas & Numpy
* Visualization -- Matplotlib (foundational) & Seaborn (statistical)
* Reproducible analysis -- Git & Github vs Jupyter & Colab

## Reading -- for next week

* ISLR2
  * Section 2.2
* VanderPlas
  * [03.06-Concat-and-Append.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/03.06-Concat-And-Append.ipynb)
  * [03.07-Merge-and-Join.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/03.07-Merge-and-Join.ipynb)
* McKinney
  * [10 Data Aggregation & Group Operations](https://wesmckinney.com/book/data-aggregation.html)

## Continued from Day 1 (last week)

* projects
* student responsibilities
* github intro
* R or Python
* Command line...really?

## Resources -- overview

* McKinney, 3rd Edition
  * [Chapter 3: Built-in data structures, functions, and files](https://wesmckinney.com/book/python-builtin.html)
  * [Chapter 4: Numpy basics: arrays and vectorized computation](https://wesmckinney.com/book/numpy-basics.html)
  * [Chapter 5: Getting started with pandas](https://wesmckinney.com/book/pandas-basics.html)
    * Series (1-D)
    * DataFrames (2-D)
  * [Chapter 9: Plotting and visualization](https://wesmckinney.com/book/plotting-and-visualization.html)
    * matlotlib
    * seaborn
* [Data Science Handbook](https://github.com/jakevdp/PythonDataScienceHandbook) (2016) by Jake VanderPlas
  * Chapter 2 -- Introduction to Numpy
  * Chapter 3 -- Introduction to Pandas
  * Chapter 4 -- Introduction to Matplotlib
* API reference docs
  * [numpy](https://numpy.org/doc/stable/reference/index.html)
  * [pandas](https://pandas.pydata.org/docs/reference/index.html#api)
  * [matplotlib](https://matplotlib.org/stable/api/pyplot_summary.html)
    * [matplotlib.pyplot](https://matplotlib.org/stable/api/pyplot_summary.html)
  * [seaborn](https://seaborn.pydata.org/api.html)
* How to search the reference docs
  * stackoverflow can be a great path to the documentation -- if used wisely!
  * google your error message (colab offers a search of stackoverflow for you)
  * it helps if you know [How to ask a question](https://stackoverflow.com/help/how-to-ask) -- stackoverflow.com

### Seaborn

* [Data structures accepted by Seaborn](https://seaborn.pydata.org/tutorial/data_structure.html)
  * describes "tidy" data -- long-form and wide-form
* the good: many things are easy with seaborn -- caveat: you need tidy data
* the bad: it's too easy to use as a black box, and stackoverflow and the web are full of bad ideas
  * solving data-science problems with google (kaggle, blogs, etc.) is like getting your news from social media
* the limitations: 
  * [heterogeneous data](https://www.tensorflow.org/tutorials/load_data/pandas_dataframe#a_dataframe_as_a_dictionary)
    * dataframes aren't sufficient for many modern algorithms (deep learning) that involve nested arrays
    * for example: it's super easy to import pandas dataframes into tensorflow, but not the other way around
  * tensorflow array dimensions: [batch size, # of samples, # of predictors]

## Conventions

Standard practice
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
Bad idea
```
from numpy import *
```

### VanderPlas

Sections that may be useful for the wage-data analysis

* [3.02 - Indexing](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/03.02-Data-Indexing-and-Selection.ipynb)
* [3.04 - Missing Values](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/03.04-Missing-Values.ipynb)
* [3.08 - Aggregation and Grouping](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/03.08-Aggregation-and-Grouping.ipynb)
* [4.00 - Introduction to Matplotlib](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/04.00-Introduction-To-Matplotlib.ipynb)

## In-class exercise

Tidy Wage dataset

* [wage.md](wage.md)
* Reproduce the three graphs in Figure 1.1 of ISLR2
* [pandas](pandas.md)
* [numpy](numpy.md)

## In-class exercise

git and github

* [git.md](git.md)

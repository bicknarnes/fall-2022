
# 01 -- Intro

## Goals

* Introductions
* Course overview
* Tools -- Git, Github, Colab and libraries

## Reading (for next week)

* Intro to statistical learning
  * Ch 1: [ISLR2](https://www.statlearning.com/) -- Background and notation
    * Bring any questions if you have on this chapter to class.
  * Ch 2: [ISLR2](https://www.statlearning.com/) -- Intro/overview
    * We'll review Section 2.1 in class, so bring any questions you have on this section.
    * We'll implement some of the material in Python.
    * Skim Section 2.2 -- the material is important and we'll get to it at some point.
    * We won't cover Sections 2.3 and 2.4, which depend on R.
* [Seaborn data structures](https://seaborn.pydata.org/tutorial/data_structure.html) -- pydata.org
  * This section in the Seaborn documentation describes "tidy" data -- this reading is an optional look ahead.
  * We'll start working with seaborn and matplotlib next week to visualize tidy data.
* [How to ask a good question](https://stackoverflow.com/help/how-to-ask) -- stackoverflow.com
  * It's important to know how to ask a good technical question.
  * Stackoverflow can be a great resource for answering good questions and debugging, provided it's used well.
  * Be careful about how you use google.
* For awareness...
  * [Ch 12: R4DS](https://r4ds.had.co.nz/tidy-data.html) -- Tidy data (the R perspective)
  * [Introduction to licenses](https://observablehq.com/@observablehq/licenses) -- observablehq.com
    * Attribution and licenses are important when using published work.
    * [Northeastern's academic integrity policy](https://osccr.sites.northeastern.edu/academic-integrity-policy/)
    * Copy and paste could have legal implications that extend beyond academic integrity (unlikely for us right now).

## Introductions

Brief introductions.

## Syllabus

Review the syllabus.

## Projects

* [stinky2](https://ds5110.github.io/stinky2/)
* [conservation](https://github.com/ds5110/project-conservation)

## Github intro

* [Github Quickstart](https://docs.github.com/en/get-started/quickstart)
* Make sure you can clone a repo, make local changes, and push them back to github.
* Be ready to ask question next time if you have difficulty with this.

## Q: R or Python?

* R or Python or...?
  * [Berkeley](https://bootcamp.berkeley.edu/blog/most-in-demand-programming-languages/)
  * [Northeastern](https://www.northeastern.edu/graduate/blog/most-popular-programming-languages/)
  * [Tiobe index](https://www.tiobe.com/tiobe-index/)
* R perspective
  * Data science overview -- [Hadley Wickham's perspective](https://r4ds.had.co.nz/explore-intro.html)
  * [ISLR2 online course](https://www.statlearning.com/online-course)
  * [Lecture 1](https://youtu.be/5N9V07EIfIg) -- youtube
* Python perspective
  * [NumPy.org](https://numpy.org/)
    * The feature gallery on the home page is worth reviewing
    * The core of NumPy is well-optimized C code
    * [Black Hole case study](https://numpy.org/case-studies/blackhole-image/)
    * Note [the data-processing pipeline](https://numpy.org/case-studies/blackhole-image/#the-challenges)
  * [Python for data analysis](https://wesmckinney.com/) (2022) by Wes McKinney
    * McKinney's book focusses on "structured data" -- tidy/tabular
    * [1. Preliminaries](https://wesmckinney.com/book/preliminaries.html)
    * [Why Python?](Reviews the core packages)

## Student responsibilities

* python -- the latest release installed locally
* editor -- vscode, or others (e.g., vim), but not atom as it was deprecated over the summer:-(
* REPL -- make sure you can run REPL (read-eval-print-loop) from the command line
* [Installation](https://wesmckinney.com/book/preliminaries.html#installation_and_setup)
  * McKinney's book has modern recommendations (miniconda and conda-forge)
  * Section 1.3: Essential Python Libraries
  * Section 1.4: Installation and setup

## In-class exercise -- colab intro

* [Data Science Handbook](https://github.com/jakevdp/PythonDataScienceHandbook) by Jake VanderPlas
  * The book is available as jupyter notebooks that open automatically in Colab
  * [Colab](https://colab.research.google.com/)
  * [Colab & Tensorflow](https://youtu.be/inN8seMm7UI)
    * Video featuring Jake VanderPlas
* Colab -- https://colab.research.google.com/
  * Colab is Jupyter as a service, with GUI improvements & GPU access (and an underlying business model)
  * Authenticate with your husky.neu.edu email
  * Colab and jupyter are for prototyping and in-class exercises, but NOT for code submission.
  * You can share Colab notebooks, but editing is not synchronous.  You need to "save" explicitly.
* Accessing the iris dataset from Colab
  * Look here: https://github.com/mwaskom/seaborn-data/blob/master/iris.csv
  * Use the "raw" link
  * `!curl -O "https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv"`

## Command line...really?

* The following excerpts come from [this Nature article](../resources/nature_observable.pdf)
  * "A 2019 study found that just 24% of 863,878 publicly available Jupyter notebooks on GitHub could be successfully re-executed, and only 4% produced the same results."
  * "Notebooks are messy. You write stuff, keep old crusty code behind, and it's hard to kind of figure out which cells to execute in the right order because you're trying different things.?
* For these and other reasons...
  * Colab for prototyping & class interactions
  * GitHub for assignments & projects

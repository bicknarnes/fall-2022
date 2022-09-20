
# 03-relational

### Goals

* Reproducibility & github submission format
* Intro to RDBMS in Python (SQLite3 & Pandas)
* Working with relational tables

### Reading (for next week)

* ISLR2 -- Chapter 3: Linear regression
  * Sections 3.1-3.4 only.
* [Chapter 3 slides](https://hastie.su.domains/ISLR2/Slides/Ch3_Linear_Regression.pdf)
  * Use the slides as a study guide.
* [Chapter 3 lectures](https://www.dataschool.io/15-hours-of-expert-machine-learning-videos/)
  * Lectures are optional for those who prefer this approach.

### Reading (questions)

* [quiz](quiz.md)

### Reproducibility

Review github classroom and submission workflow

* [git-intro](https://github.com/ds5110/git-intro)
* [git.md](https://github.com/ds5110/git-intro/blob/main/git.md)

### SQL and pandas

* [Merging](https://pandas.pydata.org/docs/user_guide/merging.html) -- pandas.pydata.org
  * There is extensive documentation on merging, joining, concatenating and comparing tables (Series & DataFrames)
* [Concatenating objects](https://pandas.pydata.org/docs/user_guide/merging.html#concatenating-objects)
  * There are a range of flags, including "verify_integrity", which is False by default.
  * Check checking for duplicates when merging "can be very expensive relative to the actual data concatenation."
* [Set logic on other axes](https://pandas.pydata.org/docs/user_guide/merging.html#set-logic-on-the-other-axes)
  * "When gluing together multiple DataFrames, you have a choice of how to handle the other axes (other than the one being concatenated)." 
  * This can be done in the following two ways:
    * Take the union of them all, join='outer'. This is the default option as it results in zero information loss.
    * Take the intersection, join='inner'.
  * The documentation has many examples demonstrating how things work.
* The following table comes from "a brief primer on merge methods and relational algebra" in the [pandas documentation](https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html#brief-primer-on-merge-methods-relational-algebra)

| Merge method | SQL Join Name | Description |
| ---          | ---           | ---         |
| left | LEFT OUTER JOIN | Use keys from left frame only |
| right | RIGHT OUTER JOIN | Use keys from right frame only |
| outer | FULL OUTER JOIN | Use union of keys from both frames |
| inner | INNER JOIN | Use intersection of keys from both frames |
| cross | CROSS JOIN | Create the cartesian product of rows of both frames |

### Intro to SQLite in Python

[03-SQLite-starter.ipynb](notebooks/03-SQLite-starter.ipynb)

### Exercises

[sqlite3](sqlite3.md)

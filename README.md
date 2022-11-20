# ML
ML Set0
## Problem 1

*Topic: basic data analysis, software tools* 
### About the topic
  
The course will contain
  examples in Python and R. The textbook examples are in R. While you are not required to know
  any specific programming language beforehand,
  you should in this course and your future career have the
  sufficient background to be able to learn to do basic independently
  data analysis operations in any of the commonly used programming
  languages.
  
 
Before the course, I recommend that you install the [RStudio Desktop](https://rstudio.com/products/rstudio/) and the [Anaconda Individual Edition](https://www.anaconda.com/distribution/). I recommend that you start by
  writing your answers to this exercise set using, e.g., RStudio Desktop and R Markdown. R Markdown supports, e.g., LaTeX math notation, and several output formats, including pdf, and languages including [R](https://www.r-project.org/) and Python (and [SciPy](https://www.scipy.org/)). I have complied this file using R Markdown! You can familiarize yourself with R Markdown by going through a brief tutorial course at <https://rmarkdown.rstudio.com/lesson-1.html>, see the [book by Xie et al.](https://bookdown.org/yihui/rmarkdown/) for further information.
  
Reading material: [OP](https://python-s20.mooc.fi/), [An introduction to R](https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf).

**Prerequisite courses:**
TKT10002 Introduction to Programming or FYS1013 Scientific computing. Recommended: programming experience or TKT10003 Advanced course in programming or FYS2085 Scientific computing II.

## Task a

```{python}
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
fpath = "/Users/summer/Desktop/UHstudy/ML/x.csv"
data = pd.read_csv(fpath)
df = pd.DataFrame(data)
df.loc["variance"] = df.apply(lambda x:np.var(x),axis=0)
vd = df.iloc[-1].tolist()
index1 = vd.index(sorted(vd)[-1])
index2 = vd.index(sorted(vd)[-2])
data_set1 = df[df.columns[index1]]
data_set2 = df[df.columns[index2]]
plt.scatter(data_set1,data_set2)
plt.show()
```

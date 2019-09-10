# Representational similarity analysis
# 表征相似性分析

### Tutorial for Methods in Neuroscience at Dartmouth (MIND) 2018
### 快速方法入门教程 翻译自 Methods in Neuroscience at Dartmouth (MIND) 2018 夏令营

表征相似性分析（RSA）是一种基于二阶同构（second-order isomprhisms）的 fMRI 数据分析方法。这种方法并不是直接分析某个测量数据和另一个测量数据之间的关系，而是计算某个测量数据与其他数据之间的相似性，并进一步比较这些相似性数据。RSA 方法由 [Kriegeskorte, Mur, and Bandettini (2008, Frontiers in System Neuroscience)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2605405/) 在 2008 年开创，并从此成为了分析神经成像数据的流行方法。本方法之所以能够变得非常流行，是因为RSA方法使用二阶同构进行分析，从而使得该方法能够将不同的脑成像和行为数据联系起来。

在 fMRI 的分析过程中使用 RSA 方法，常常是需要在神经活动模式的相似性与任务、评分或者模型之间计算相关或者回归。在这个教程当中，我们会学习如何使用 RSA 进行验证性或探索性分析。

### Installation

First, if you have not already done so, please install [R](https://cran.r-project.org/) and [RStudio](https://www.rstudio.com/products/rstudio/download/#download).

Clone this repository to your local machine, and open "Representational_similarity_analysis.Rmd" with RStudio. From the "Run" dropdown menu in the upper left pane, select "Run All". When the script completes, save the .Rmd file, and then select "Preview" to view the R Notebook. To make changes, edit the code in the .Rmd file, re-run the corresponding code-chunk(s), and then save changes - the preview will update automatically.

Alternatively, a static version of the R Notebook can be viewed directly through your web browser by downloading the file ending in ".nb.html" and then opening it with the browser of your choice. Viewing this version does not require R/RStudio, but changes cannot be made to the code.




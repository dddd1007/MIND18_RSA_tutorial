# Representational similarity analysis
# 表征相似性分析

### Tutorial for Methods in Neuroscience at Dartmouth (MIND) 2018
### 快速方法入门教程 翻译自 Methods in Neuroscience at Dartmouth (MIND) 2018 夏令营

*暑期学校：http://mindsummerschool.org*

### 简介

表征相似性分析（RSA）是一种基于二阶同构（second-order isomprhisms）的 fMRI 数据分析方法。这种方法并不是直接分析某个测量数据和另一个测量数据之间的关系，而是计算某个测量数据与其他数据之间的相似性，并进一步比较这些相似性数据。RSA 方法由 [Kriegeskorte, Mur, and Bandettini (2008, Frontiers in System Neuroscience)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2605405/) 在 2008 年开创，并从此成为了分析神经成像数据的流行方法。本方法之所以能够变得非常流行，是因为RSA方法使用二阶同构进行分析，从而使得该方法能够将不同的脑成像和行为数据联系起来。

在 fMRI 的分析过程中使用 RSA 方法，常常是需要在神经活动模式的相似性与任务、评分或者模型之间计算相关或者回归。在这个教程当中，我们会学习如何使用 RSA 进行验证性或探索性分析。

### 安装

**step1**
本教程全部使用 R 实现全部分析过程。请提前安装 [R](https://cran.r-project.org/) 和[RStudio](https://www.rstudio.com/products/rstudio/download/#download)。


**step2**
将本仓库克隆到你到本地设备。或直接在该页面点击 “Clone or download” 绿色按钮，然后选择 “Download ZIP” 到本地。解压后使用 RStudio 打开"Representational_similarity_analysis_Chinese_edition.Rmd" 文件。选择编辑器右上角的 Run” 菜单中的 “Run ALL” 按钮。

你同样可以选择文件夹中的 “表征相似性分析示例.html” 文件打开，这是我已经编译好的版本。

### 补充知识

二阶同构




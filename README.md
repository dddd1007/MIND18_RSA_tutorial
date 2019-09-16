# Representational similarity analysis
# 表征相似性分析

### Tutorial for Methods in Neuroscience at Dartmouth (MIND) 2018
### 快速方法入门教程 翻译自 Methods in Neuroscience at Dartmouth (MIND) 2018 夏令营

*暑期学校：http://mindsummerschool.org*

### 简介

表征相似性分析（RSA）是一种基于二阶同构（second-order isomprhisms）的 fMRI 数据分析方法。这种方法并不是直接分析某个测量数据和另一个测量数据之间的关系，而是计算某个测量数据与其他数据之间的相似性，并进一步比较这些相似性数据。RSA 方法由 [Kriegeskorte, Mur, and Bandettini (2008, Frontiers in System Neuroscience)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2605405/) 在 2008 年开创，并从此成为了分析神经成像数据的流行方法。本方法之所以能够变得非常流行，是因为RSA方法使用二阶同构进行分析，这种令人惊叹的分析技术可以将不同类型的脑成像、行为数据等研究数据联系起来。

![](https://camo.githubusercontent.com/145331f874ae96bf99ce3cd124e702f5dee9ac34/687474703a2f2f7777772e6d72632d6362752e63616d2e61632e756b2f2f706572736f6e616c2f6e696b6f6c6175732e6b7269656765736b6f7274652f666967355f6b7269656765736b6f7274655f5253415f464e532e676966)

在 fMRI 的分析过程中使用 RSA 方法，常常是需要在神经活动模式的相似性与任务、评分或者模型之间计算相关或者回归。在这个教程当中，我们会学习如何使用 RSA 进行验证性或探索性分析。

### 安装

**step1**

本教程全部使用 R 实现全部分析过程。请提前安装 [R](https://cran.r-project.org/) 和[RStudio](https://www.rstudio.com/products/rstudio/download/#download)。

**step2**

将本仓库克隆到你到本地设备。或直接在该页面点击 “Clone or download” 绿色按钮，然后选择 “Download ZIP” 到本地。解压后使用 RStudio 打开 "Representational_similarity_analysis_Chinese_edition.Rmd"  文件。选择编辑器右上角的 Run” 菜单中的 “Run ALL” 按钮。

你同样可以选择文件夹中的 “表征相似性分析示例.html” 文件打开，这是我已经编译好的版本。

### 补充知识

二阶同构(second-order isomprhisms)

*注：由于二阶同构是 RSA 分析的一个较为核心的概念，因此认为需要对该概念进行解释，以便对该方法有较为深入的了解。但是目前查到的资料大多偏于数学，因此为了适用于心理学专业的学生阅读，在此我对概念进行了简化，并补充了少量解释。这有可能导致错误，如有疏漏，欢迎提交 PR ！*

**同构**

同构是一个抽象代数当中的概念。本概念是指两个数学对象之间存在一个保持结构的双射，而双射则是指一个在两个集合之间存在一个映射关系，且该关系既能满足两个集合的元素一一对应（单射），同时又能保证每一个元素都存在该映射关系（满射）。

具体来讲，在做 RSA 分析时，我们可能会将两个 ROI 或两个 Voxel 之间的 BOLD 信号求解相关（或不一致性），则此时即存在映射函数 $BOLD_{ROI_{2}} = \beta \cdot BOLD_{ROI_{1}} + \xi$ 。此时我们可知这两个 BOLD 信号间存在一个同构关系。

RSA 分析的基本逻辑是将
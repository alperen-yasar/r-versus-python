---
title: "A Comparison of Data Visualisation"
output: 
  html_document: 
    code_folding: hide
    keep_md: yes
    preserve_yaml: false
---

# A comparison of data visualisation on Python and R

In this notebook, I'll show different plot options in both Python and R to show you the basic differences in both coding and plotting. 







```r
library(ggplot2)

scatter <- ggplot(data=iris, aes(x = Sepal.Length, y = Sepal.Width)) 
scatter + geom_point(aes(color=Species, shape=Species), size=3) +
  xlab("Sepal Length") +  ylab("Sepal Width") +
  ggtitle("A gglot2 Scatterplot")
```

![](visualisation_comparison_files/figure-html/unnamed-chunk-3-1.png)<!-- -->



```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

iris_pd = r.iris

ax = sns.scatterplot(x='Sepal.Length', y='Sepal.Width', data=iris_pd, hue="Species", style="Species")
ax.set_title("A Seaborn Scatterplot")
```

<img src="visualisation_comparison_files/figure-html/unnamed-chunk-4-1.png" width="672" />



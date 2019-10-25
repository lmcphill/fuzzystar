
```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)

ny<-read.table("/Users/lindseymcphillips/Desktop/cs73.dat",header=T); dim(ny)  #  916  11
ny2<-na.omit(ny); dim(ny2) # 914  11
attach(ny2)
lpop <- log(ny2$pop)
lexpen <- log(ny2$expen)


```

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

```{r}

plot(lpop, lexpen, xlab = "Log-Population", ylab = "Log-Expenditures")
lines(lowess(lpop, lexpen), col="blue")

```

```{r cars}
summary(cars)
```

## Including Plots

You can also embed plots, for example:

```{r pressure, echo=FALSE}
plot(pressure)
```

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

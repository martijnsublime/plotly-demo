---
title       : Getting started with Plotly
description : This chapter illustrates how Plotly will work within DataCamp. It will introduce you to plotly and how you can use R and plotly together to create stunning data visualizations. 

--- type:NormalExercise lang:r xp:100 skills:1 key:cec50a4fcb
## Let's get started

In this exercise, you'll be introduced to plotly and how you can use plotly to creating stunning data visualizations in R!

By default, plotly for R runs locally in your web browser or in the R Studio viewer. You can publish your charts to the web with plotly's web service. For more information go to [plot.ly/r/getting-started](https://plot.ly/r/getting-started)


Let's get started by loading the `plotly` library. 

*** =instructions
- Load the `plotly` library
- Use the `head()` function on `mtcars` to view the first few lines in the data.frame
- Replace the blank spaces in the `plot_ly()` function to plot the weight, `wt`, of each car on the x-axis by the miles per gallon, `mpg`, on the y-axis. 


*** =hint
- Use the `library()` function
- Simply enter `head(mtcars)`
- Set `x=` in the `ploy_ly()` function to `mtcars$wt`


*** =pre_exercise_code
```{r}
# You can also prepare your dataset in a specific way in the pre exercise code


# Clean up the environment

```

*** =sample_code
```{r}
# load the `plotly` library


# Use the `head()` function on `mtcars` 


# Use the `ploy_ly()` function to assign the correct value to `p`
plot_ly(x = ___, y = ___, mode = "markers")


```

*** =solution
```{r}
# load the `plotly` library
library(plotly)

# Use the `head()` function on `mtcars` 
head(mtcars)

# Use the `ploy_ly()` function to assign the correct value to `p`
plot_ly(x = mtcars$wt, y = mtcars$mpg,  mode = "markers")


```

*** =sct
```{r}
# SCT written with testwhat: https://github.com/datacamp/testwhat/wiki

test_function("head", args = "x",
              not_called_msg = "You didn't call `head()`!",
              incorrect_msg = "You didn't call `head()` with the correct object, `mtcars`.")


test_function("plot_ly", args = "x")
test_function("plot_ly", args = "y")
test_function("plot_ly", args = "mode")

test_error()

success_msg("Good work! You can plot and save in the cloud with 'plotly_POST()`.")
```

--- type:NormalExercise lang: xp: skills: key:e5bce93213
## Three basic plots

In the next couple of exercises, you will learn how to use Plotly to create three basic plot types -  a line plot, a scatter plot, and a bar chart. You've likely encountered these plots before and used them in your own research. Plotly let's you turn these basic plots into interactive masterpieces!

To keep things simple, we've gone ahead and created two unique objects, `data1` and `data2`. These are available in the console. 

Let's start with the first graph, a line plot!


*** =instructions

- Replace the blanks in the `plot_ly()` function to create a line plot where `data1` is on the x-axis and `data2` is on the y-axis. 


*** =hint



*** =pre_exercise_code
```{r}
library(plotly)

# load data
data1 <- c(1,2,3,4,5,6,7,8,9,10)
data2 <- c(5,6,7,8,9,10,11,12,13,14)

```


*** =sample_code
```{r}
# Create a line plot with the `plot_ly()` function
graph1 <- plot_ly(x= ___ ,y= ___ ,type="scatter", mode="lines") 

# Print graph objects
graph1



```

*** =solution
```{r}
# Create a line plot with the `plot_ly()` function
graph1 <- plot_ly(x=data1,y=data2,type="scatter",mode="lines") 

# Print graph objects
graph1


```

*** =sct
```{r}

test_function("plot_ly", args = "x")
test_function("plot_ly", args = "y")
test_function("plot_ly", args = "type")
test_function("plot_ly", args = "mode")

test_object("graph1")

test_error()

success_msg("Good work! Pay attention to the `type = ` and `mode = ` arguments and how they impact the output!")

```
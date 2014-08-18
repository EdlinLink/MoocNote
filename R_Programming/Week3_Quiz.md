## Question 1

Take a look at the 'iris' dataset that comes with R. The data can be loaded with the code:

	library(datasets)
	data(iris)

A description of the dataset can be found by running

	?iris

There will be an object called 'iris' in your workspace. In this dataset, what is the mean of 'Sepal.Length' for the species virginica? (Please only enter the numeric result and nothing else.)

> 筛选出`iris$Species=="virginica"`的行；提取`vir$Sepal.Length`列；最后用mean()函数计算均值。


## Question 2

Continuing with the 'iris' dataset from the previous Question, what R code returns a vector of the means of the variables 'Sepal.Length', 'Sepal.Width', 'Petal.Length', and 'Petal.Width'?

+ apply(iris, 1, mean)
+ colMeans(iris)
+ apply(iris[, 1:4], 2, mean)
+ apply(iris, 2, mean)

> `apply`函数的第二个参数1表示row，2表示col；`colMeans`和`mean`函数需要所有列都是可求均值的才可以。


## Question 3

Load the 'mtcars' dataset in R with the following code

	library(datasets)
	data(mtcars)

There will be an object names 'mtcars' in your workspace. You can find some information about the dataset by running

	?mtcars

How can one calculate the average miles per gallon (mpg) by number of cylinders in the car (cyl)?

+ mean(mtcars$mpg, mtcars$cyl)
+ tapply(mtcars$cyl, mtcars$mpg, mean)
+ lapply(mtcars, mean)
+ tapply(mtcars$mpg, mtcars$cyl, mean)

> `mean`函数的函数原型是`mean(x, trim = 0, na.rm = FALSE, ...)`；`lapply`函数是对list中的每一个元素执行输入的函数；`tapply`函数的函数原型是`tapply(X, INDEX, FUN = NULL, ..., simplify = TRUE)`，通过对index进行分类，然后对不同类别执行输入的函数。


## Question 4

Continuing with the 'mtcars' dataset from the previous Question, what is the absolute difference between the average horsepower of 4-cylinder cars and the average horsepower of 8-cylinder cars?

> 根据Question 3原理计算。


## Question 5

If you run

	debug(ls)

what happens when you next call the 'ls' function?

+ Execution of 'ls' will suspend at the beginning of the function and you will be in the browser.
+ The 'ls' function will return an error.
+ The 'ls' function will execute as usual.
+ You will be prompted to specify at which line of the function you would like to suspend execution and enter the browser.

> 参考PPT Debugging - debug. 自行实践。 

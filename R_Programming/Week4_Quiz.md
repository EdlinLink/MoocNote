## Question 1

What is produced at the end of this snippet of R code?

	set.seed(1)
	rpois(5, 2)

+ A vector with the numbers 1, 4, 1, 1, 5
+ A vector with the numbers 3.3, 2.5, 0.5, 1.1, 1.7
+ It is impossible to tell because the result is random
+ A vector with the numbers 1, 1, 2, 4, 1

> `set.seed`用于设定random的随机种子，`rpois`是按柏松分布生成随机数。

## Question 2

What R function can be used to generate standard Normal random variables?

+ dnorm
+ qnorm
+ rnorm
+ pnorm

> 参考PPT Simulation - Generating Random Numbers.

## Question 3

When simulating data, why is using the set.seed() function important?

+ It ensures that the random numbers generated are within specified boundaries.
+ It can be used to generate non-uniform random numbers.
+ It ensures that the sequence of random numbers is truly random.
+ It ensures that the sequence of random numbers starts in a specific place and is therefore reproducible.

> 参考PPT Simulation - Generating Random Numbers.

## Question 4

Which function can be used to evaluate the inverse cumulative distribution function for the Poisson distribution?

+ dpois
+ qpois
+ ppois
+ rpois

> `dpois, ppois, qpois, rpois`分别代表`Density, distribution function, quantile function and random generation for the Poisson distribution with parameter ‘lambda’.`

## Question 5

What does the following code do?

	set.seed(10)
	x <- rbinom(10, 10, 0.5)
	e <- rnorm(10, 0, 20)
	y <- 0.5 + 2 * x + e

+ Generate data from a Normal linear model
+ Generate uniformly distributed random data
+ Generate random exponentially distributed data
+ Generate data from a Poisson generalized linear model

> `rbinom`表示random generation for the binomial distribution。

## Question 6

What R function can be used to generate Binomial random variables?

+ pbinom
+ rbinom
+ dbinom
+ qbinom

> 使用`?pbinom`查看各个函数。

## Question 7

What aspect of the R runtime does the profiler keep track of when an R expression is evaluated?

+ the global environment
+ the working directory
+ the package search list
+ the function call stack

> 参考PPT Profiler - The R Profiler. 

## Question 8

Consider the following R code

	library(datasets)
	Rprof()
	fit <- lm(y ~ x1 + x2)
	Rprof(NULL)

(Assume that y, x1, and x2 are present in the workspace.) Without running the code, what percentage of the run time is spent in the 'lm' function, based on the 'by.total' method of normalization shown in 'summaryRprof()'?

+ 23%
+ It is not possible to tell
+ 50%
+ 100%

> 其实不懂。

## Question 9

When using 'system.time()', what is the user time?

+ It is the "wall-clock" time it takes to evaluate an expression
+ It is the time spent by the CPU evaluating an expression
+ It is a measure of network latency
+ It is the time spent by the CPU waiting for other tasks to finish

> 参考PPT Progiler - Using system.time(). 

## Question 10

If a computer has more than one available processor and R is able to take advantage of that, then which of the following is true when using 'system.time()'?

+ user time is always smaller than elapsed time
+ elapsed time may be smaller than user time
+ user time is 0
+ elapsed time is 0

> 参考PPT Progiler - Using system.time(). 



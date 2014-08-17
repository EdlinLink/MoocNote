## Question 1

Suppose I define the following function in R
	cube <- function(x, n) {
		x^3
	}

What is the result of running

	cube(3)
	
in R after defining this function?

+ An error is returned because 'n' is not specified in the call to 'cube'
+ The users is prompted to specify the value of 'n'.
+ The number 27 is returned
+ A warning is given with no value returned.

> 参考PPT Functions - Lazy Evaluation. 

## Question 2

The following code will produce a warning in R.
	x <- 1:10
	if(x > 5) {
		x <- 0
	}

Why?

+ The expression uses curly braces.
+ There are no elements in 'x' that are greater than 5
+ You cannot set 'x' to be 0 because 'x' is a vector and 0 is a scalar.
+ The syntax of this R expression is incorrect.
+ 'x' is a vector of length 10 and 'if' can only test a single logical statement.

> 自行实践。

## Question 3

Consider the following function

	f <- function(x) {
		g <- function(y) {
			y + z
		}
		z <- 4
		x + g(x)
	}

If I then run in R

	z <- 10
	f(3)
	
What value is returned?

+ 10
+ 7
+ 16
+ 4

> 参考PPT Scoping - Lexical Scoping. Lexical Scoping(词法域)是一种用来定义环境及外部变量的方法，如果嵌套过程中的参数如果外部过程已经定义过了，对于该嵌套过程，可以省略参数，但是过程内部仍然可以使用外部过程定义过的参数。程序首先定义了z=10，进入f()函数中，x等于3；在f函数中将z的值变更为4，f函数的返回值是3+g(3)，其中g(3)的定义是返回y+z，输入g的参数y=3、z=4，g(3)返回7；最终f(3)返回计算值。

## Question 4

Consider the following expression:

	x <- 5
	y <- if(x < 3) {
		NA
	} else {
		10
	}

What is the value of 'y' after evaluating this expression?

+ 5
+ 10
+ NA
+ 3

> 自行实践。

## Question 5

Consider the following R function

h <- function(x, y = NULL, d = 3L) {
	z <- cbind(x, d)
	if(!is.null(y))
		z <- z + y
	else
		z <- z + f
	g <- x + y / z
	if(d == 3L)
		return(g)
	g <- g + 10
	g
}

Which symbol in the above function is a free variable?

+ f
+ z
+ d
+ L
+ g

> 参考PPT Scoping - Lexical Scoping. "Free variables are not formal arguments and are not local variables."

## Question 6

What is an environment in R?

+ a list whose elements are all functions
+ an R package that only contains data
+ a collection of symbol/value pairs
+ a special type of function

> 参考PPT Scoping - A Diversion on Binding Values to Symbol。

## Question 7

The R language uses what type of scoping rule for resolving free variables?

+ dynamic scoping
+ compilation scoping
+ lexical scoping
+ global scoping

> 参考PPT Scoping - Lexical vs. Dynamic Scoping. 

## Question 8

How are free variables in R functions resolved?

+ The values of free variables are searched for in the environment in which the function was called
+ The values of free variables are searched for in the working directory
+ The values of free variables are searched for in the global environment
+ The values of free variables are searched for in the environment in which the function was defined

> 参考PPT Scoping - Lexical Scoping

## Question 9

What is one of the consequences of the scoping rules used in R?

+ All objects must be stored in memory
+ R objects cannot be larger than 100 MB
+ All objects can be stored on the disk
+ Functions cannot be nested

> 参考PPT Scoping - Consequences of Lexical Scoping.


## Question 10

In R, what is the parent frame?

+ It is always the global environment
+ It is the environment in which a function was defined
+ It is the environment in which a function was called
+ It is the package search list

> 参考PPT Scoping - Lexical vs. Dynamic Scoping. 建议阅读[参考资料2]。

## 参考资料
1. [词法域. 百度百科](http://baike.baidu.com/view/3066567.htm?fr=aladdin)
2. [关于R语言的scoping. C6H5NO2. 豆瓣](http://www.douban.com/note/269216547/)


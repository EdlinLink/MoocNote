## Question 1

The R language is a dialect of which of the following programming languages?

+ C  
+ S  
+ Lisp  
+ Fortran  

> 参考PPT OverviewHistoryR - What is R?.

## Question 2

The definition of free software consists of four freedoms (freedoms 0 through 3). Which of the following is NOT one of the freedoms that are part of the definition?

+ The freedom to improve the program, and release your improvements to the public, so that the whole community benefits.
+ The freedom to restrict access to the source code for the software.
+ The freedom to redistribute copies so you can help your neighbor.
+ The freedom to run the program, for any purpose.

> 参考PPT OverviewHistoryR - Free Software

## Question 3

In R the following are all atomic data types EXCEPT

+ array
+ logical
+ complex
+ numeric

> 参考PPT DataTypes - Objects

## Question 4

If I execute the expression x <- 4 in R, what is the class of the object 'x' as determined by the 'class()' function?

+ vector
+ numeric
+ integer
+ list

> 参考PPT DataTypes - Numbers. 在R中数字赋值一般会认为是numberic类型，如果要赋值为integer类型需要在数字后面加上字母L。

## Question 5

What is the class of the object defined by the expression x <- c(4, "a", TRUE)?

+ mixed
+ character
+ numeric
+ integer

> 参考PPT DataTypes - Creating Vectors. c()函数是用于生成vector对象的。vector中只能保存一种数据类型。如果vector中保存了不同类型的对象，则coercion(强制类型转换)就会发生，以保证只存在一种类型的对象。

## Question 6

If I have two vectors x <- c(1,3, 5) and y <- c(3, 2, 10), what is produced by the expression cbind(x, y)?

+ a vector of length 2
+ a vector of length 3
+ a numeric matrix with 3 rows and 2 columns
+ a 2 by 3 matrix

> 参考PPT DataTypes - cbind-ing and rbind-ing.  bind-ing可以将vector组合成matrix。

## Question 7

A key property of vectors in R is that

+ elements of a vector can only be character or numeric
+ elements of a vector all must be of the same class
+ the length of a vector must be less than 32,768
+ a vector cannot have have attributes like dimensions

> 参考PPT DataTypes - Objects. 

## Question 8

Suppose I have a list defined as x <- list(2, "a", "b", TRUE). What does x[[2]] give me?

+ a character vector of length 1.
+ a list containing the number 2 and the letter "a".
+ a character vector with the elements "a" and "b".
+ a list containing a character vector with the elements "a" and "b".

> 参考PPT DataTypes - Lists. List是一种特别的vector，它可以存放不同类型的元素。

## Question 9

Suppose I have a vector x <- 1:4 and y <- 2:3. What is produced by the expression x + y?

+ a warning
+ an integer vector with the values 3, 5, 3, 4.
+ a numeric vector with the values 1, 2, 5, 7.
+ an integer vector with the values 3, 5, 5, 7.

> 自行实践.

## Question 10

Suppose I have a vector x <- c(17, 14, 4, 5, 13, 12, 10) and I want to set all elements of this vector that are greater than 10 to be equal to 4. What R code achieves this?

+ x[x > 10] <- 4
+ x[x > 4] <- 10
+ x[x >= 10] <- 4
+ x[x > 10] == 4

> 自行实践.

## Question 11

In the dataset provided for this Quiz, what are the column names of the dataset?

+ Ozone, Solar.R, Wind
+ 1, 2, 3, 4, 5, 6
+ Month, Day, Temp, Wind
+ Ozone, Solar.R, Wind, Temp, Month, Day

> 首先需要读取文件data = read.table('hw1_data.csv', header=TRUE, sep=",")。读取的数据类型为data.frame。查看data.frame的列和行使用方法是如下:
> data[i,] 选取第i行; 
> data[i:j,] 选取第i到j行; 
> data[c(i,j,k),] 选取第i,j,k行; 
> data[data$type=='l'] 假设第一列名为type，选取type列为l的所有行; 
> 列同理，data[i,j] 选取第i行第j列。

## Question 12

Extract the first 2 rows of the data frame and print them to the console. What does the output look like?

		Ozone	Solar.R	Wind	Temp	Month	Day
	1	7		NA		6.9		74		5		11
	2   35		274		10.3	82		7		17
 
		Ozone	Solar.R	Wind	Temp	Month	Day
	1   9		24		10.9	71		9		14
	2   18		131		8.0		76		9		29

		Ozone	Solar.R Wind	Temp	Month	Day
	1   18		224		13.8	67		9		17
	2   NA		258		9.7		81		7		22

		Ozone	Solar.R Wind	Temp	Month	Day
	1	41		190		7.4		67		5		1
	2   36		118		8.0		72		5		2

> head(data)命令能够查看前10行。 

## Question 13
		
How many observations (i.e. rows) are in this data frame?
		
+ 45
+ 129
+ 153
+ 160

> tail(data)命令能够查看后10行，并知道行号。

## Question 14

Extract the last 2 rows of the data frame and print them to the console. What does the output look like?

		Ozone	Solar.R	Wind	Temp	Month	Day
	152	31		244		10.9	78		8		19
	153	29		127		9.7		82		6		7
			 
		Ozone	Solar.R Wind	Temp	Month	Day
	152	11      44		9.7		62		5		20
	153	108     223		8.0		85		7		25
				 
		Ozone	Solar.R Wind	Temp	Month	Day
	152	18		131		8.0		76		9		29
	153	20		223		11.5	68		9		30
					 
		Ozone	Solar.R Wind	Temp	Month	Day
	152 34		307		12.0	66		5		17
	153 13		27		10.3	76		9		18

> tail(data)命令能够查看最后10行。

## Question 15

What is the value of Ozone in the 47th row?

+ 63
+ 21
+ 18
+ 34

>  使用命令data[47,]

## Question 16

How many missing values are in the Ozone column of this data frame?

+ 9
+ 43
+ 37
+ 78

> 多种方法，例如data[is.na(data$Ozone), ]获得了对应的行，dim()或者nrow()知道行数。

## Question 17

What is the mean of the Ozone column in this dataset? Exclude missing values (coded as NA) from this calculation.

+ 42.1
+ 18.0
+ 31.5
+ 53.2

> data[is.na(data)=F]表示索引出x中不是缺失值的元素，colMeans()函数能够计算列均值。

## Question 18

Extract the subset of rows of the data frame where Ozone values are above 31 and Temp values are above 90. What is the mean of Solar.R in this subset?

+ 334.0
+ 212.8
+ 205.0
+ 185.9

> 先将Question 17的data赋值到一个新变量中成为newdata，筛选Ozone>31和Temp>90，最后使用colMeans()计算。

## Question 19

What is the mean of "Temp" when "Month" is equal to 6?

+ 79.1
+ 90.2
+ 75.3
+ 85.6

> 筛选Month==6，利用colMeans()计算。

## Question 20

What was the maximum ozone value in the month of May (i.e. Month = 5)?

+ 18
+ 100
+ 97
+ 115

> 筛选，然后利用max()函数计算。


## 参考资料

1. [对data.frame和matrix的一些操作技巧总结. maver. 炼数成金](http://f.dataguru.cn/thread-16331-1-1.html)
2. [R语言快速入门~ 真的很快~. 大爷你啥样. 百度贴吧统计狂魔吧](http://tieba.baidu.com/p/1840660429)
3. [R语言怎样求行均值? sociology. cos论坛统计之都统计学论坛](http://cos.name/cn/topic/12365)


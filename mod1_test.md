---
title       : Intro to R - Module 1
subtitle    : Basic Operations and Data Types
author      : Nick Carchedi
job         : Johns Hopkins Bloomberg School of Public Health
logo        : bloomberg_shield.png
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
url:
  lib: /libraries
  assets: /assets
widgets     : [mathjax]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

In this module, we will explore some basic building blocks of the R programming language.

---

In it's simplest form, R can be used as an interactive calculator. Type `5 + 7` and press Enter.


```r
5 + 7
```

```
## [1] 12
```


--- 

R simply prints the result of 13 by default. However, R is a programming language and often the reason we use a programming language as opposed to a calculator is to automate some process or avoid unneccessary repetition.

---

In this case, we may want to use our result from above in a second calculation. Instead of retyping `5 + 7` every time we need it, we can just create a new variable that stores the result.

---

The way you assign a value to a variable in R is by using the assignment operator, which is just a "less than" symbol followed by a dash. It looks like this: <-

---

Think of the assignment operator as an arrow. You are assigning the value on the right side of the arrow to the variable name on the left side of the arrow.

---

To assign the result of `5 + 7` to a new variable called `x`, you type `x <- 5 + 7`. This can be read as "x gets 5 plus 7." Give it a try now.


```r
x <- 5 + 7
```


---

You'll notice that R did not print the result of 13 this time. When you use the assignment operator, R assumes that you don't want to see the result immediately, but rather that you intend to use the result for something else later on.

---

To view the contents of the variable `x`, just type `x` and press Enter. Try it now.


```r
x
```

```
## [1] 12
```

---

Now, store the result of `x - 3` in a new variable called `y`.


```r
y <- x - 3
```


---

What is the value of `y`? Type `y` to find out.


```r
y
```

```
## [1] 9
```


---

In the examples above, we know the numbers 3, 5, and 7 to be integers, but R sees them differently.

---

If you want to use integers in R, you must specify the `L` suffix. Otherwise, R will treat numeric values as real (decimal) numbers. Let's explore this and other differences by looking the most fundamental data types in R.

---

First, it's useful to distinguish data structures from data types. You can think of data structures as containers that hold data. Data types describe fundamental properties of that data.

---

The most basic data structure in R is a vector. Vectors are just collections of objects. Even single numbers are considered vectors of length 1.

---

There are two different flavors of vectors in R: atomic vectors and lists. The data contained in an atomic vector must all be of the same type, whereas the data contained in a list can be of many different types.

---

Let's take a closer look at atomic vectors, since they are so fundamental to everything else in R.

---

The easiest way to create an atomic vector in R is with the `c()` function, which stands for concatenate or combine.

---

To create a vector containing the numbers 2, 3, and 4, you type `c(2, 3, 4)`. Try it now and store the result in a variable called `z`.


```r
z <- c(2, 3, 4)
```


---

Since numVect is an atomic vector, all of its elements must be the same data type. In this case, we might expect that data type to be "integer". However, as we mentioned in the last example, R doesn't think this way.

---

The 4 most common types of atomic vectors in R are "character", "double" (often called "numeric"), "integer", and "logical" (TRUE/FALSE).

---

If you want to know the type of data stored in an atomic vector, use the `typeof()` function. Try `typeof(numVect)` to see how R views our numbers 2, 4, 6, and 8.

---

So R considers 2, 4, 6, and 8 to be of type "double", which essentially means decimal or real numbers. This is R's default data type for numeric data. If you explicitly want an integer in R, you have to specify the `L` suffix.

---

For example, let's create a new vector called intVect that contains the integers 3 and 7. To do this, type `intVect <- c(3L, 7L)`.

---

Now, check that intVect is of type integer using the `typeof()` function.

---

Create one of each of 4 most common types of atomic vector


```r
numVect <- c(4, 2.12, 88, 0.3)
intVect <- c(3L, 7L)
charVect <- c("Nick", "Carchedi")
logVect <- c(TRUE, FALSE, TRUE)
```

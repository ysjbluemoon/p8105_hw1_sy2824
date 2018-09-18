hw1
================

This is the first homework of data science.

Problem 1
=========

A random sample of size 10 from a uniform\[0, 5\] distribution

``` r
x = rnorm(10)
```

A logical vector indicating whether elements of the sample are greater than 2

``` r
def_larger_than_two = ifelse(x > 2 , TRUE, FALSE)
```

A (length-10) character vector

``` r
char_leng_ten = c("a" , "b" , "c" , "e" , "f", "g", "h", "i", "j", "k")
length(char_leng_ten)
```

    ## [1] 10

A (length-10) factor vector

``` r
fac_leng_ten = factor(c("a" , "b" , "c" , "e" , "f", "g", "h", "i", "j", "k"))
length(fac_leng_ten)
```

    ## [1] 10

Section 2
=========

Create a dataframe of four vectors:

``` r
set.seed(1)
x = rnorm(1000)

y = rnorm(1000)

log_flag = ifelse(x + y > 0, TRUE, FALSE)

num_flag = as.numeric(log_flag)

fac_flag = as.factor(log_flag)

data_frame_q2 = data.frame(x,y,log_flag,num_flag,fac_flag)
str(data_frame_q2)
```

    ## 'data.frame':    1000 obs. of  5 variables:
    ##  $ x       : num  -0.626 0.184 -0.836 1.595 0.33 ...
    ##  $ y       : num  1.135 1.1119 -0.8708 0.2107 0.0694 ...
    ##  $ log_flag: logi  TRUE TRUE FALSE TRUE TRUE FALSE ...
    ##  $ num_flag: num  1 1 0 1 1 0 1 0 0 1 ...
    ##  $ fac_flag: Factor w/ 2 levels "FALSE","TRUE": 2 2 1 2 2 1 2 1 1 2 ...

This is a brief introduction of this dataset:

The size of the dataset is 5 colums and 1000 rows.

The mean of x is -0.0116481 and median is -0.0353242.

The proportion of cases for which the logical vector is 0.2

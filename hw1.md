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
def_larger_than_two = ifelse (x > 2 , TRUE, FALSE)
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

``` r
x = rnorm(1000)

y = rnorm(1000)

log_flag = ifelse(x + y > 0, TRUE, FALSE)

num_flag = as.numeric(log_flag)

fac_flag = as.factor(log_flag)

data_frame_q2 = data.frame(x,y,num_flag,fac_flag)
str(data_frame_q2)
```

    ## 'data.frame':    1000 obs. of  4 variables:
    ##  $ x       : num  0.584 -0.155 0.638 -0.749 -0.802 ...
    ##  $ y       : num  0.0847 1.7337 -1.5126 0.1823 0.9332 ...
    ##  $ num_flag: num  1 1 0 0 1 0 1 1 1 0 ...
    ##  $ fac_flag: Factor w/ 2 levels "FALSE","TRUE": 2 2 1 1 2 1 2 2 2 1 ...

The size of the dataset is

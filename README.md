Assignment 4
================
Tuwilika
27 July 2016

Hello Octocat
-------------

I love OCtocat. SHe's the coolest cat in town. ![](https://dl.dropboxusercontent.com/u/11805474/painblogr/biostats/images/octocat.png)

``` r
data(anscombe)
dim("anscombe")
```

    ## NULL

``` r
names(anscombe)
```

    ## [1] "x1" "x2" "x3" "x4" "y1" "y2" "y3" "y4"

``` r
head(anscombe, n=6)
```

    ##   x1 x2 x3 x4   y1   y2    y3   y4
    ## 1 10 10 10  8 8.04 9.14  7.46 6.58
    ## 2  8  8  8  8 6.95 8.14  6.77 5.76
    ## 3 13 13 13  8 7.58 8.74 12.74 7.71
    ## 4  9  9  9  8 8.81 8.77  7.11 8.84
    ## 5 11 11 11  8 8.33 9.26  7.81 8.47
    ## 6 14 14 14  8 9.96 8.10  8.84 7.04

``` r
tail(anscombe, n=6)
```

    ##    x1 x2 x3 x4    y1   y2   y3    y4
    ## 6  14 14 14  8  9.96 8.10 8.84  7.04
    ## 7   6  6  6  8  7.24 6.13 6.08  5.25
    ## 8   4  4  4 19  4.26 3.10 5.39 12.50
    ## 9  12 12 12  8 10.84 9.13 8.15  5.56
    ## 10  7  7  7  8  4.82 7.26 6.42  7.91
    ## 11  5  5  5  8  5.68 4.74 5.73  6.89

``` r
summary(anscombe)
```

    ##        x1             x2             x3             x4    
    ##  Min.   : 4.0   Min.   : 4.0   Min.   : 4.0   Min.   : 8  
    ##  1st Qu.: 6.5   1st Qu.: 6.5   1st Qu.: 6.5   1st Qu.: 8  
    ##  Median : 9.0   Median : 9.0   Median : 9.0   Median : 8  
    ##  Mean   : 9.0   Mean   : 9.0   Mean   : 9.0   Mean   : 9  
    ##  3rd Qu.:11.5   3rd Qu.:11.5   3rd Qu.:11.5   3rd Qu.: 8  
    ##  Max.   :14.0   Max.   :14.0   Max.   :14.0   Max.   :19  
    ##        y1               y2              y3              y4        
    ##  Min.   : 4.260   Min.   :3.100   Min.   : 5.39   Min.   : 5.250  
    ##  1st Qu.: 6.315   1st Qu.:6.695   1st Qu.: 6.25   1st Qu.: 6.170  
    ##  Median : 7.580   Median :8.140   Median : 7.11   Median : 7.040  
    ##  Mean   : 7.501   Mean   :7.501   Mean   : 7.50   Mean   : 7.501  
    ##  3rd Qu.: 8.570   3rd Qu.:8.950   3rd Qu.: 7.98   3rd Qu.: 8.190  
    ##  Max.   :10.840   Max.   :9.260   Max.   :12.74   Max.   :12.500

GitHub Documents
----------------

This is an R Markdown format used for publishing markdown documents to GitHub. When you click the **Knit** button all R code chunks are run and a markdown file (.md) suitable for publishing to GitHub is generated.

Including Code
--------------

You can include R code in the document as follows:

``` r
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
library(readr)
library(tidyr)
data("anscombe")
plot(x=anscombe$x1, y=anscombe$y1)
abline(lm(y1 ~ x1, data = anscombe))
```

<img src="./figures/xy_PLOT-1.svg" style="display: block; margin: auto;" />

Including Plots
---------------

You can also embed plots, for example:

``` r
path <- file.path('~', 'Assignment 4', 'analgesic.csv')
df <- data.frame('analgesic.csv')
df <- read.csv('analgesic.csv')
```

``` r
dim(df)
```

    ## [1] 40  5

``` r
names(df)
```

    ## [1] "ID"            "Group"         "Measurement_1" "Measurement_2"
    ## [5] "Measurement_3"

``` r
head(df, n=6)
```

    ##   ID     Group Measurement_1 Measurement_2 Measurement_3
    ## 1  1 Analgesic            26            26            21
    ## 2  2 Analgesic            29            26            23
    ## 3  3 Analgesic            24            28            22
    ## 4  4 Analgesic            25            22            24
    ## 5  5 Analgesic            24            28            23
    ## 6  6 Analgesic            22            23            26

``` r
tail(df, n=6)
```

    ##    ID   Group Measurement_1 Measurement_2 Measurement_3
    ## 35 35 Placebo            17            21            15
    ## 36 36 Placebo            19            17            15
    ## 37 37 Placebo            14            19            13
    ## 38 38 Placebo            17            19            13
    ## 39 39 Placebo            11            20            18
    ## 40 40 Placebo            15            18            12

``` r
summary(df)
```

    ##        ID              Group    Measurement_1   Measurement_2 
    ##  Min.   : 1.00   Analgesic:20   Min.   :10.00   Min.   : 8.0  
    ##  1st Qu.:10.75   Placebo  :20   1st Qu.:17.00   1st Qu.:17.0  
    ##  Median :20.50                  Median :20.00   Median :20.0  
    ##  Mean   :20.50                  Mean   :20.12   Mean   :20.7  
    ##  3rd Qu.:30.25                  3rd Qu.:24.00   3rd Qu.:25.0  
    ##  Max.   :40.00                  Max.   :30.00   Max.   :32.0  
    ##  Measurement_3  
    ##  Min.   :12.00  
    ##  1st Qu.:16.00  
    ##  Median :20.50  
    ##  Mean   :20.52  
    ##  3rd Qu.:24.25  
    ##  Max.   :30.00

``` r
df_1 <- gather(df, key = Measures, value = Value, Measurement_1, Measurement_2, Measurement_3, -ID)
df_2 <- group_by(df_1, ID, Group)
summarise(df_2, mean = mean(Value))
```

    ## Source: local data frame [40 x 3]
    ## Groups: ID [?]
    ## 
    ##       ID     Group     mean
    ##    <int>    <fctr>    <dbl>
    ## 1      1 Analgesic 24.33333
    ## 2      2 Analgesic 26.00000
    ## 3      3 Analgesic 24.66667
    ## 4      4 Analgesic 23.66667
    ## 5      5 Analgesic 25.00000
    ## 6      6 Analgesic 23.66667
    ## 7      7 Analgesic 26.66667
    ## 8      8 Analgesic 23.33333
    ## 9      9 Analgesic 22.66667
    ## 10    10 Analgesic 24.00000
    ## # ... with 30 more rows

Chicken weights
===============

Null Hypothesis
---------------

-   the chick weights are not dependent on the feed

ALternative Hypothesis
----------------------

-   the chick weights are dependent on the feed

``` r
# Read chick-weights.csv
x <- read.csv("chick-weights.csv")

# Tidy chick-weights data using boxplot
boxplot(x$weight ~ x$feed)
```

![](README_files/figure-markdown_github/unnamed-chunk-2-1.png)

``` r
# State null and alternative hypotheses
"H0 : the chick weights are dependent on the feed" 
```

    ## [1] "H0 : the chick weights are dependent on the feed"

``` r
"H1 : the chick weights are not dependent on the feed"
```

    ## [1] "H1 : the chick weights are not dependent on the feed"

``` r
# State and run statistical test
chickanova <- aov(weight~feed, data = x)
summary(chickanova)
```

    ##             Df Sum Sq Mean Sq F value   Pr(>F)    
    ## feed         5 231129   46226   15.37 5.94e-10 ***
    ## Residuals   65 195556    3009                     
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

``` r
# Comparing means of three or more groups

# State degree of freedom and p-value
Df = 5
'p-value <0.05'
```

    ## [1] "p-value <0.05"

``` r
"Reject null hypothesis and accept alternative hypothesis"
```

    ## [1] "Reject null hypothesis and accept alternative hypothesis"

The Hot Zone
============

Null hypothesis
---------------

-   water contamination does not cause gastroenteritis

Alternative hypothesis
----------------------

-   water contamination does cause gastroenteritis

``` r
# Read gastroenteritis data
x <- read.csv("gastroenteritis.csv")

# Tidy gastroenteritis data using scatter plot
y <- xtabs(~Consumption + Outcome, data=x)
y
```

    ##                     Outcome
    ## Consumption          ill not ill
    ##   < 1 glasses/day     39     121
    ##   > 4 glasses/day    265     146
    ##   1 to 4 glasses/day 265     258

``` r
#Plot barplot
barplot(y, beside = TRUE, ylab = 'water consumption', xlab = 'clinical outcome', main = 'Gastroenteritis', col = c('pink', 'turquoise', 'grey'))
legend ('top', c('< 1 glasses/day', '> 4 glasses/day', '1 to 4 glasses/day'), fill = c('pink', 'turquoise', 'grey'))
```

![](README_files/figure-markdown_github/unnamed-chunk-3-1.png)

``` r
# Statistical test
z <- chisq.test(y, correct = TRUE)
z
```

    ## 
    ##  Pearson's Chi-squared test
    ## 
    ## data:  y
    ## X-squared = 74.925, df = 2, p-value < 2.2e-16

Test assumptions
----------------

-   determining whether there is an association between 2 variables
-   analysing 2 catagorical variables

Outcome Interpretation
----------------------

-   df = 2
-   p-value &lt;0.05, therefore, reject the null hypothesis and accept the alternative hypothesis

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot. \# Nausea \#\# Null hypothesis \* Receiving emetogenic chemotherapy does not cause nausea

Alternative hypothesis
----------------------

-   Receiving emetogenic chemotherapy does cause nausea

``` r
# Read Nausea data
x <- read.csv("nausea.csv")

#Plotting data
plot(x$Nausea_before ~ x$Patient, type = "l", ylim = c(0,6), xlab = 'Patient', ylab = 'Nausea_intensity', main = 'Nausea intensity decreases with treatment', col= 'purple')
lines(x$Nausea_after)
legend ('top', c('Nausea_before', 'Nausea_after'), fill = c('purple', 'black'))
```

![](README_files/figure-markdown_github/unnamed-chunk-4-1.png)

``` r
# Statistical test
wilcox.test(x$Nausea_before, x$Nausea_after, paired = TRUE)
```

    ## Warning in wilcox.test.default(x$Nausea_before, x$Nausea_after, paired =
    ## TRUE): cannot compute exact p-value with ties

    ## 
    ##  Wilcoxon signed rank test with continuity correction
    ## 
    ## data:  x$Nausea_before and x$Nausea_after
    ## V = 26, p-value = 0.2906
    ## alternative hypothesis: true location shift is not equal to 0

Test assumptions
----------------

-   Data is paired, and non-parametric
-   Two pairs of measurements taken on same experimental group

Outcome interpretation
----------------------

-   Df = 7
-   p-value &lt;0.05, therefore reject null hypothesis and accept alternative hypothesis

Housing Prices
==============

``` r
# Import dataset
goo <- read.csv("housing-prices.csv")
goo
```

    ##    interest_rate median_house_price_USD
    ## 1             10                 183800
    ## 2             10                 183200
    ## 3             10                 174900
    ## 4              9                 173500
    ## 5              8                 172900
    ## 6              7                 173200
    ## 7              8                 173200
    ## 8              8                 169700
    ## 9              8                 174500
    ## 10             8                 177900
    ## 11             7                 188100
    ## 12             7                 203200
    ## 13             8                 230200
    ## 14             7                 258200
    ## 15             7                 309800
    ## 16             6                 329800
    ## 17            NA                     NA

``` r
interest = goo$interest_rate
house_price = goo$median_house_price_USD
head(cbind(interest, house_price))
```

    ##      interest house_price
    ## [1,]       10      183800
    ## [2,]       10      183200
    ## [3,]       10      174900
    ## [4,]        9      173500
    ## [5,]        8      172900
    ## [6,]        7      173200

``` r
plot(interest, house_price, xlab = "interest_rate", ylab = "median_house_price_USD", pch = 19, col = 'grey', main = 'Interest Rate decreases Housing Price')
abline(lm(goo$median_house_price_USD ~ goo$interest_rate,data = goo), col= 'pink', lwd = 2)
```

![](README_files/figure-markdown_github/unnamed-chunk-5-1.png)

``` r
# Linear regression
 goo1 <- lm(goo$median_house_price_USD ~ goo$interest_rate, data = goo)
 summary(goo1)
```

    ## 
    ## Call:
    ## lm(formula = goo$median_house_price_USD ~ goo$interest_rate, 
    ##     data = goo)
    ## 
    ## Residuals:
    ##    Min     1Q Median     3Q    Max 
    ## -55865 -31631 -16406  27212  80735 
    ## 
    ## Coefficients:
    ##                   Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)         399229      74427   5.364 9.99e-05 ***
    ## goo$interest_rate   -24309       9205  -2.641   0.0194 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 43180 on 14 degrees of freedom
    ##   (1 observation deleted due to missingness)
    ## Multiple R-squared:  0.3325, Adjusted R-squared:  0.2848 
    ## F-statistic: 6.974 on 1 and 14 DF,  p-value: 0.01937

``` r
 # Diagnostic plot 1
 plot(x = goo1$fitted.values, y = goo1$residuals, main = 'Homoskedasticity', pch = 19, col = 'grey')
 abline(h = 0, col = 'pink', lwd = 3)
```

![](README_files/figure-markdown_github/unnamed-chunk-5-2.png)

``` r
 # Diagbnostic plot 2: gaussian residual distribution
 qqnorm(goo1$residuals)
 qqline(goo1$residuals)
```

![](README_files/figure-markdown_github/unnamed-chunk-5-3.png)

``` r
 # Binary outcome variabe
 glm( goo$median_house_price_USD ~ goo$interest_rate, data = goo)
```

    ## 
    ## Call:  glm(formula = goo$median_house_price_USD ~ goo$interest_rate, 
    ##     data = goo)
    ## 
    ## Coefficients:
    ##       (Intercept)  goo$interest_rate  
    ##            399229             -24309  
    ## 
    ## Degrees of Freedom: 15 Total (i.e. Null);  14 Residual
    ##   (1 observation deleted due to missingness)
    ## Null Deviance:       3.91e+10 
    ## Residual Deviance: 2.61e+10  AIC: 390.8

Null hypothesis: the housing price is not dependent on the interest rate
------------------------------------------------------------------------

Alternative hypothesis: the housing price is dependent on the interest rate
---------------------------------------------------------------------------

Analysis Assumption:
--------------------

-   Ran scatter plot to see trend
-   Diagnostics for linear regression; QQ-plot to determine whether the residuals are normally distributed and the guassian residual distribution to determine the variance for all the fitted values.
-   GLM was used as the diagnostics were not bormally distributed and did not fit along the line of best fit.

Test interpretation
-------------------

-   F-statistic : 6.974 on 1
-   p-value = 0.01937, therefore reject H0 and accept the alternative hypothesis.
-   DF: 14

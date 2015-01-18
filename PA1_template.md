# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
activity <-read.csv('activity.csv')
aggSteps <- aggregate(steps ~ date, data = activity, sum, na.rm =TRUE)
summary(aggSteps)    
```

```
##          date        steps      
##  2012-10-02: 1   Min.   :   41  
##  2012-10-03: 1   1st Qu.: 8841  
##  2012-10-04: 1   Median :10765  
##  2012-10-05: 1   Mean   :10766  
##  2012-10-06: 1   3rd Qu.:13294  
##  2012-10-07: 1   Max.   :21194  
##  (Other)   :47
```

## What is mean total number of steps taken per day?
###1. Histogram of total number of steps taken

```r
hist(aggSteps$steps)
```

![](PA1_template_files/figure-html/unnamed-chunk-2-1.png) 

##2. Mean and Median total number of steps take per day

```r
mean(aggSteps$steps, na.rm=TRUE)
```

```
## [1] 10766.19
```

```r
median(x = aggSteps$steps, na.rm = TRUE)
```

```
## [1] 10765
```
- The mean total is `10766.19` steps per day
- The median total is `10765` steps

## What is the average daily activity pattern?



## Inputing missing values



## Are there differences in activity patterns between weekdays and weekends?

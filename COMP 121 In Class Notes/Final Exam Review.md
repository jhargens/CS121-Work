## Final Exam Review

### Loop Example 

```r
sumloop <- function(x) {
    sum1 <- 0
    for (k in 1:length(x)) {
        sum2 <- k
        sum1 <- sum2 + sum1
    }
    return(sum1)
}
```

Test Statement: 

```r
sumloop(1:5)
```

```
## [1] 15
```


## Recursion 

### Exercises:


```r
addNSeq <- function(v) {
    sum <- 0  #accumulator
    for (k in 1:length(v)) {
        sum <- sum + v[k]
    }
    return(sum)
}
```

Simplification
  present -> base case
  v[1]+addNSeq(v[-1])
  

```r
addRecursively <- function(v) {
    if (length(v) == 0) 
        return(0)
    return(v[1] + addRecursively(v[-1]))
}
```


Test Cases:

```r
addNSeq(1:10)
```

```
## [1] 55
```


```r
addRecursively(1:10)
```

```
## [1] 55
```


### Natural Settings for Recursion



```r
integrateRecursive <- function(f, a = 0, b = 1) {
    bigBins <- simpleRiemann(f, a = a, b = b, n = 5)
    smallBins <- simpleRiemann(f, a = a, b = b, n = 10)
    if (abs(bigBins - smallBins) < 1e-05) 
        return(smallBins) else {
        mid <- (a + b)/2
        total <- integrateRecursive(f, a = a, b = mid) + integrateRecursive(f, 
            a = mid, b = b)
        return(total)
    }
}
```


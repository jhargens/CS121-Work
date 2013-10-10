# Base Conversion 

## Task 1


```r
toBase <- function(Z, b) {
    Z <- Z
    sofar <- c()
    repeat {
        r <- Z%%b
        sofar <- c(r, sofar)
        Z <- (Z - r)/b
        if (Z == 0) 
            break
    }
    return(as.character(sofar))
}
```

Test Statements: 

```r
toBase(Z = 10, b = 2)
```

```
## [1] "1" "0" "1" "0"
```


```r
toBase(Z = 100, b = 3)
```

```
## [1] "1" "0" "2" "0" "1"
```


```r
toBase(Z = 1000, b = 16)
```

```
## [1] "3"  "14" "8"
```


## Task 2
### Without Loop:

```r
baseToNumeric <- function(Nvec, b) {
    howMany <- length(Nvec)
    herdsize <- b^((howMany - 1):0)
    return(sum(as.numeric(Nvec) * herdsize))
}
```

Test Statement:

```r
baseToNumeric(c("7", "6", "5", "4"), 8)
```

```
## [1] 4012
```


### With Loop:

```r
convertAsALoop <- function(Nvec, b) {
    Nvec <- as.numeric(Nvec)
    sheepCount <- 0
    boxSize <- 1
    for (k in length(Nvec):1) {
        sheepCount <- sheepCount + boxSize * Nvec[k]
        boxSize <- boxSize * b
    }
    return(sheepCount)
}
```

Test Statement: 

```r
convertAsALoop(c("7", "6", "5", "4"), 8)
```

```
## [1] 4012
```


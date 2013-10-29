## Derivatives as Finite Differences

### Evaluate Derivative 

```r
evalD <- function(f, x) {
    h <- 1e-08  #'small h'
    return((f(x + h) - f(x - h))/(2 * h))
}
```


### In Class & First Order Derivative 

```r
myD <- function(f, h = 1e-07) {
    fprime <- function(x) {
        (f(x + h) - f(x))/h
    }
    return(fprime)
}
```


### Second & Higher Order Derivative

```r
myD2 <- function(f, h = 1e-09) {
    fprime <- myD(f, h = h)
    eprime <- myD(fprime, h = h)
    return(eprime)
}
```


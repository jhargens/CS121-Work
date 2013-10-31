## String Transformer Functions 

### Reverser 


```r
reverse <- function(x) {
    L <- strsplit(x, "")[[1]]
    R <- rev(L[[1]])
    paste(R, collapse = "")
}
```


Test Statement: 

```r
reverse("hello")
```

```
## [1] "h"
```


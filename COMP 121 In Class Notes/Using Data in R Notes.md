## Using Data in R Notes

```r
require(mosaic)
```

```
## Loading required package: mosaic
```

```
## Warning: package 'mosaic' was built under R version 3.0.2
```

```
## Loading required package: grid
## Loading required package: lattice
```

```
## Warning: package 'lattice' was built under R version 3.0.2
```

```
## 
## Attaching package: 'mosaic'
## 
## The following objects are masked from 'package:stats':
## 
##     binom.test, cor, cov, D, fivenum, IQR, median, prop.test, sd,
##     t.test, var
## 
## The following object is masked from 'package:base':
## 
##     max, mean, min, print, prod, range, sample, sum
```

```r
require(DCF)
```

```
## Loading required package: DCF
## Loading required package: ggplot2
```

```
## Warning: package 'ggplot2' was built under R version 3.0.2
```

```
## Loading required package: reshape2
```

```
## Warning: package 'reshape2' was built under R version 3.0.2
```

```
## Loading required package: plyr
```

```
## Warning: package 'plyr' was built under R version 3.0.2
```

```
## 
## Attaching package: 'plyr'
## 
## The following object is masked from 'package:mosaic':
## 
##     count
## 
## 
## Attaching package: 'DCF'
## 
## The following object is masked from 'package:mosaic':
## 
##     fetchGapminder, getVarFormula, mScatter, ntiles
```

```r
data(package = "DCF")
```

#### Operations for use in data frames 
1. names()
2. nrow()
3. ncol()
4. with()
5. $ (#will specify a certain element of data in the data frame)

### Task (how to return diabetes (diab) in patients, red if yes, blue if no)

```r
diacolors <- with(small, ifelse(diab == 0, alpha("blue", 0.2), alpha("red", 
    0.4)))
```

```
## Error: object 'small' not found
```


xyplot( wgt~hgt, data=small,group=sex, main="", auto.key=list(space="right"))

### Dataframe Operators:
1. mutate
2. subset
3. ddply
4. join 

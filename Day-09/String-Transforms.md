## String Transformer Functions 

### Reverser 


```r
reverse <- function(x) {
    L <- strsplit(x, NULL)
    R <- rev(L[[1]])
    return(paste(R, collapse = ""))
}
```


Test Statement: 

```r
reverse("hello")
```

```
## [1] "olleh"
```


### Scrambler 

```r
scramble <- function(x) {
    L <- strsplit(x, NULL)
    R <- sample(L[[1]])
    return(paste(R, collapse = ""))
}
```

Test Statement:

```r
scramble("Robert")
```

```
## [1] "rRtebo"
```

### Vowel Bleeper

```r
vowelbleeper <- function(x) {
    gsub("[AEIOUaeiou]", "*", x)
}
```

Test Statement:

```r
vowelbleeper("James Hargens")
```

```
## [1] "J*m*s H*rg*ns"
```

### L33t

```r
L33t <- function(x) {
    First <- gsub("[Ee]", "3", x)
    Second <- gsub("[Aa]", "4", First)
    Third <- gsub("[Oo]", "0", Second)
    Fourth <- gsub("[Ll]", "1", Third)
    gsub("[Ss]", "5", Fourth)
}
```

Test Statement:

```r
L33t("Soccer is the best sport in the world")
```

```
## [1] "50cc3r i5 th3 b35t 5p0rt in th3 w0r1d"
```

## Sets of Words

```r
# Reverser
Reverse <- function(x) {
    reverse <- function(x) {
        L <- strsplit(x, NULL)
        R <- rev(L[[1]])
        return(paste(R, collapse = ""))
    }
    sapply(x, reverse)
}
```

Test Statement:

```r
Reverse(c("hello", "world"))
```

```
##   hello   world 
## "olleh" "dlrow"
```


```r
# Scrambler
Scramble <- function(x) {
    scramble <- function(x) {
        L <- strsplit(x, NULL)
        R <- sample(L[[1]])
        return(paste(R, collapse = ""))
    }
    sapply(x, scramble)
}
```

Test Statment:

```r
Scramble(c("hello", "world"))
```

```
##   hello   world 
## "lhloe" "wrdlo"
```


```r
# Vowel Bleeper
Vowelbleeper <- function(x) {
    vowelbleeper <- function(x) {
        gsub("[AEIOUaeiou]", "*", x)
    }
    sapply(x, vowelbleeper)
}
```

Test Statment:

```r
Vowelbleeper(c("hello", "world"))
```

```
##   hello   world 
## "h*ll*" "w*rld"
```


```r
# L33t
l33t <- function(x) {
    L33t <- function(x) {
        First <- gsub("[Ee]", "3", x)
        Second <- gsub("[Aa]", "4", First)
        Third <- gsub("[Oo]", "0", Second)
        Fourth <- gsub("[Ll]", "1", Third)
        gsub("[Ss]", "5", Fourth)
    }
    sapply(x, L33t)
}
```

Test Statement:

```r
l33t(c("hello", "world"))
```

```
##   hello   world 
## "h3110" "w0r1d"
```







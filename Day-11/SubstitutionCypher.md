## Substitution Cypher 

### Step One (The Key)

```r
mykey <- function(word) {
    key <- unlist(strsplit(tolower(word), NULL))
    result <- character(0)
    for (k in 1:length(key)) {
        num <- which(key[k] == letters)
        result <- c(result, num)
    }
    result <- paste(result, collapse = "")
    return(as.numeric(result))
}
```

Test Statement:

```r
mykey("hello")
```

```
## [1] 85121215
```


### The Cypher

```r
encrypt <- function(keyword, message) {
    cSet <- c(letters, LETTERS, ".", ",", "?", " ", "!", "()")
    set.seed(mykey(keyword))
    code <- sample(cSet)
    open <- paste(cSet, collapse = "")
    close <- paste(code, collapse = "")
    telegram <- chartr(open, close, message)
    return(telegram)
}
```

Test Statment: 

```r
encrypt("world", "This means hello!")
```

```
## [1] "rSz!At?Pl!AS?..BV"
```


### Decryption 

```r
decrypt <- function(keyword, message) {
    cSet <- c(letters, LETTERS, ".", ",", "?", " ", "!", "()")
    set.seed(mykey(keyword))
    code <- sample(cSet)
    open <- paste(cSet, collapse = "")
    close <- paste(code, collapse = "")
    telegram <- chartr(close, open, message)
    return(telegram)
}
```

Test Statment:

```r
decrypt("world", "rSz!At?Pl!AS?..BV")
```

```
## [1] "This means hello!"
```


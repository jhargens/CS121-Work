## Crosswords, Scabble, and Regular Expressions


```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))
```

### SUmmarazing the List

```r
Length1 <- function(x) {
    analyze <- grepl("^.$", x)
    return(length(x[analyze]))
}
Length1(words)
```

```
## [1] 0
```


```r
Length2 <- function(x) {
    analyze <- grepl("^..$", x)
    return(length(x[analyze]))
}
Length2(words)
```

```
## [1] 85
```



```r
words[grep("^.b...$", words)]
```

```
##  [1] "abaca" "abaci" "aback" "abaft" "abaka" "abamp" "abase" "abash"
##  [9] "abate" "abbes" "abbey" "abbot" "abeam" "abele" "abets" "abhor"
## [17] "abide" "abied" "abies" "abler" "ables" "abmho" "abode" "abohm"
## [25] "aboil" "aboma" "aboon" "abort" "about" "above" "abris" "abuse"
## [33] "abuts" "abuzz" "abyed" "abyes" "abysm" "abyss" "ebbed" "ebbet"
## [41] "ebons" "ebony" "mbira" "obeah" "obeli" "obese" "obeys" "obias"
## [49] "obits" "oboes" "obole" "oboli" "obols"
```


```r
makepattern <- function(length, ...) {
    letters <- list(...)
    str <- c("^", rep(".", length), "$")
    for (k in 1:length(letters)) str[letters[[k]] + 1] <- names(letters[k])
    paste(str, collapse = "")
}
```


### Final Product:

```r
Scrabblehelper <- function(length, ...) {
    words[grep(makepattern(length, ...), words)]
}
```


```r
Scrabblehelper(length = 7, y = 3, f = 6)
```

```
## [1] "hayloft" "layoffs" "payoffs"
```


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


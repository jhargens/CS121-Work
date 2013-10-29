## Numbers and Strings 

### Help for Crossworld Puzzles

```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))

findscrable <- function(letters) {
    for (k in 1:length(letters)) {
        words <- words[grep(letters[k], words)]
        if (length(words) < 10) 
            break
    }
    return(words)
}
```



```r
summary(cars)
```

```
## Warning: closing unused connection 5
## (http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt)
```

```
##      speed           dist    
##  Min.   : 4.0   Min.   :  2  
##  1st Qu.:12.0   1st Qu.: 26  
##  Median :15.0   Median : 36  
##  Mean   :15.4   Mean   : 43  
##  3rd Qu.:19.0   3rd Qu.: 56  
##  Max.   :25.0   Max.   :120
```


You can also embed plots, for example:


```r
plot(cars)
```

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3.png) 



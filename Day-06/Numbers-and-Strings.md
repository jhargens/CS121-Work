## Numbers and Strings 

### Basic Statistics 

### Numbers and Languages 

```r
EnglishNumbers <- c("zero", "one", "two", "three", "four", "five", "six", "seven", 
    "eight", "nine")
digitToWord <- function(n, language) {
    return(language[n + 1])
}
digitToWord(4, EnglishNumbers)
```

```
## [1] "four"
```

### Help for Crossword Puzzles 

```r
lettersMatch <- function(words, pattern) {
    words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))
    analyze <- grepl(pattern, words)
    return(words[analyze])
}
# 8 letter words starting with 'h' ending in 'ed'
lettersMatch(words, "^h.....ed")
```

```
##  [1] "hachured"  "halloaed"  "hallooed"  "hallowed"  "haltered" 
##  [6] "hammered"  "hampered"  "hangared"  "hankered"  "hanseled" 
## [11] "happened"  "harassed"  "harbored"  "hardened"  "harkened" 
## [16] "harrowed"  "hastened"  "haunched"  "havocked"  "hawkweed" 
## [21] "hawkweeds" "hazarded"  "hectored"  "heehawed"  "helmeted" 
## [26] "hempseed"  "hempseeds" "hempweed"  "hempweeds" "heralded" 
## [31] "heroized"  "hiccuped"  "highbred"  "hijacked"  "hilloaed" 
## [36] "hindered"  "hirseled"  "hocussed"  "hoidened"  "hollered" 
## [41] "holloaed"  "hollooed"  "hollowed"  "homebred"  "homebreds"
## [46] "honoured"  "hoodooed"  "hoorahed"  "hoorayed"  "hosteled" 
## [51] "houseled"  "hovelled"  "hoydened"  "hulloaed"  "humified" 
## [56] "humoured"  "hungered"  "hunkered"  "hurrahed"  "hurrayed" 
## [61] "huzzahed"  "hydrated"  "hyphened"
```


### Have Your Pie Two Ways

```r
piSeries <- function(n) {
    state <- 0
    for (k in 1:(length(n))) {
        result <- ((-1)^(k + 1))/(2 * k - 1)
        state <- state + result
    }
    return(state * 4)
}
piSeries(1:10000)
```

```
## [1] 3.141
```


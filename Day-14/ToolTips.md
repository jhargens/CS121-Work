## Constructing "ToolTips" in HTML

### Technique 
<style>
.hiword {background:pink;}
</style>

This <span class='hiword' title='This one!'>set of words</span> has a tooltip. 

### From R to HTML

```r
formatWord <- function(word, translation, classInput) {
    if (is.na(translation) == TRUE) 
        return(as.character(word)) else {
        paste("<span class=", "'", classInput, "'", " ", "title=", "'", translation, 
            "'", ">", word, "</span>", sep = "")
    }
}
```

Test Statement:

```r
formatWord("Hello", "hi there!", class = "hiword")
```

```
## [1] "<span class='hiword' title='hi there!'>Hello</span>"
```


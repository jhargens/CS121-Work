## Constructing "ToolTips" in HTML

### Technique 
<style>
.hiword {background:pink;}
</style>

This <span class='hiword' title='This one!'>set of words</span> has a tooltip. 

### From R to HTML

```r
formatWord <- function(word, translation, class) {
    if (is.na(translation) == TRUE) 
        return(as.character(word)) else {
        paste("<span class='", class, "',title='", translation, "'>", word, 
            "</span>")
    }
}
```

Test Statement:

```r
cat(formatWord("Hello", "hi there!", class = "hiword"))
```

<span class=' hiword ',title=' hi there! '> Hello </span>



```r
cat(formatWord("Hello", "hi there!", class = "hiword"), "to, all, of, you, in", 
    formatWord("Television Land", "TV Viewers", "hiword"))
```

<span class=' hiword ',title=' hi there! '> Hello </span> to, all, of, you, in <span class=' hiword ',title=' TV Viewers '> Television Land </span>




## Blank "Canvasas" Circles and Squares
========================================================
Establishes the Canvas for the Graphics 

```r
canvas <- function(mn = 0, mx = 100) {
    plot(1:2, ylim = c(mn, mx), xlim = c(mn, mx), asp = 1, xaxt = "n", yaxt = "n", 
        type = "n", bty = "n", xlab = "", ylab = "")
}
circle <- function(x, y, r, ry = r, ...) {
    angs <- seq(0, 2 * pi, length = 200)
    xpts <- x + r * cos(angs)
    ypts <- y + ry * sin(angs)
    polygon(xpts, ypts, ...)
}
```



```r
canvas()
circle(50, 50, 20, col = "blue", border = NULL)
circle(35, 70, r = 20, ry = 30, col = "pink", border = NULL)
polygon(c(20, 40, 40, 20), c(40, 40, 60, 60), col = "green", border = "blue", 
    lwd = 5)
polygon(c(38, 48, 48, 38), c(33, 33, 23, 23), col = "red", border = "black")
polygon(c(67, 60, 75, 90, 83), c(45, 60, 72, 60, 45), col = "yellow", border = NULL)
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2.png) 

```r

```


## install packages if not installed

```r
if (!require("pacman")) install.packages("pacman")
pacman::p_load(package1, pagckage2, …)
```

## draw density line-plot with date x-axis

```r
plot(Count ~ Date, data = source, xaxt = 'n', type = 'l')
axis(1, source$Date, format(source$Date, "%d %b"), cex.axis = 0.7)
```

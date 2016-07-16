## install packages if not installed

```r
if (!require("pacman")) install.packages("pacman")
pacman::p_load(package1, pagckage2, …)
```

## redefine `+` operator for strings

```r
"+" = function(x, y) {
    if(is.character(x) || is.character(y)) {
        paste(x, y, sep = '')
    } else {
        .Primitive("+")(x, y)
    }
}
```

## store key-value pairs

The simplest choice is to use the `environment` object, it is a hash map in essence.

```r
map <- new.env(hash = T, parent = emptyenv())

map[[key]] <- val
map$key    <- val

print( map$key )
```

If you don't care about fast operations you can try lists (the same syntax).

## draw density line-plot with date x-axis

```r
plot(Count ~ Date, data = source, xaxt = 'n', type = 'l')
axis(1, source$Date, format(source$Date, "%d %b"), cex.axis = 0.7)
```

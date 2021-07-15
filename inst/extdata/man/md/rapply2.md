rapply2
=======

Usage
-----

    rapply2(X , FUN)

| Argument | Description                  |
| -------: | :--------------------------- |
|        X | a `matrix`                   |
|      FUN | a `function` of one argument |

Value
-----

An object of `nrow(X)` elements, where each element is the
result of applying `FUN` to the corresponding row of `X`.

The return type is expected to be consistent with a call to
`vapply` with `FUN.VALUE = FUN(X[1,])`

Examples
--------

    m <- matrix(1:9, 3)
    m
           [,1] [,2] [,3]
    # [1,]    1    4    7
    # [2,]    2    5    8
    # [3,]    3    6    9
    rapply2(m, sum)
    # [1] 12 15 18

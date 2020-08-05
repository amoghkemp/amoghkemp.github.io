# Python Programs 
* TOC {:toc}
for all the grid problems one must import grid.py
```
from grid import*
```

## Diagonal 
paint the diagonal squares black 
```python
n=8
create_grid(n,n)
for i in range(n):
    paint_black(i,i)
show()
```

## output 
<img src="/images/diagonal.PNG" alt="diagonal" width="200"/>

## Paint Row
write a function that takes as input a number *r* and paints the *r*th row
```python
n=8
create_grid(n,n)
def paint_row(r):
    for i in range(n):
        paint_black(r-1,i)
paint_row(3)
```

## output
<img src="/images/paint_row.png" alt="paint_row" width="200"/>

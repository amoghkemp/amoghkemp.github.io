# Python Programs 
* TOC {:toc}
for all the grid problems one must import grid.py
```python
from grid import *
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

## Prime_number
type a number and check if its a prime number 
```python
def prime_number(n):
    prime=True
    if n==1 or n==0:
        return(False)
    for i in range(n):
        if i>=2:
            if n%i==0:
                prime=False
    return(prime)
prime_number(17)
```

## output
```python
True
```

## greatest common divisor
takes two numbers and checks and returns the greatest common divisor
```python
def gcd(a,b):
    count=0
    largest=1
    for i in range(1,a+1):
        if a%i==0 and b%i==0:
            count+=1
            if i>largest:
                largest=i
    print(largest)
gcd(18,42)
```

## output
```python
6
```

## lowest common multiple 
takes two numbers and checks and return the lowest common multiple of the two numbers
```python
def lcm(a,b):
    for i in range(1,a*b+1):
        if i%a==0 and i%b==0:
            return(i)
lcm(54,24)
```

## output
```python
216
```

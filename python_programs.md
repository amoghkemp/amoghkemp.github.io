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

## hexagon spiral 
makes a spiral
```python
# import turtle library
import turtle             
colors = [ "red","purple","blue","green","orange","yellow"]
my_pen = turtle.Pen()
turtle.bgcolor("black")
for x in range(80):
    my_pen.pencolor(colors[x % 6])
    my_pen.width(x/100 + 1)
    my_pen.forward(x)
    my_pen.left(59)
turtle.exitonclick()
```
## output
![](/images/hexagon_spiral.png)

## bullseye 
makes concentric rings 
```python
from turtle import *

s=getscreen()

speed(0)

t=Turtle()
```
```python
def draw_circle(x,y,r,color):
    t.penup()
    t.goto(x,y-r)
    t.pendown()
    t.color("black",color)
    t.begin_fill()
    t.circle(r)
    t.end_fill()
```
```python
def draw_ring(x,y,r,t):
    draw_circle(x,y,r,"black")
    draw_circle(x,y,r-t,"white")
```
```python
def draw_concentric_ring(x,y,r,n):
    t=r/n
    for i in range(n):
        if r>0:
            draw_ring(x,y,r,t)
            r=r-(t*2)
```
```python
draw_concentric_ring(0,0,100,10)
done()
```
## output 
![](/images/bullseye.png)

## square spiral
replace the function `draw_circle` with `draw_rectangle` to get this 
```python
def draw_rectangle(x,y,r,color):
    t.penup()
    t.goto(0-(r),0+(r))
    t.pendown()
    t.color("black",color)
    t.begin_fill()
    t.fd(r*2)
    t.rt(90)
    t.fd(r*2)
    t.rt(90)
    t.fd(r*2)
    t.rt(90)
    t.fd(r*2)
    t.rt(90)
    t.end_fill()
```
## output 
![](/images/square_ring.png)

## pascal 
adds adjacent numbers in a list 
```python 
def pascal(l):
    r=[]
    r.append(1)
    for i in range(len(l)):
        if i<len(l)-1:
            n=l[i]+l[i+1]
            r=r+[n]
    r.append(1)
    return(r)
```
```python
pascal([1,3,3,1])
```
## output 
```python
[1, 4, 6, 4, 1]
```

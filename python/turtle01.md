# [turtle 기본문법]
## Draw a line
```
import turtle
turtle.bgcolor("orange")    # 배경색

# 환경설정
t = turtle.Turtle()
t.width(5)                  # 선굵기
t.speed("fast")             # 속도
t.shape("circle")           # arrow, turtle, circle, square, triangle, classic 

# 선그리기
t.fd(100)     # forward 단축
t.rt(90)      # right 단축
t.fd(100)     
t.lt(90)      # left 단축
t.fd(100)     

# 펜이동하기
t.penup()                   # 펜들기(그리지멈춤)
t.goto(-100, 100)           # 좌표이동
t.pendown()                 # 펜내리기(그리기시작)

# 원그리기/색채우기
t.fillcolor("green")
t.begin_fill()
t.circle(100)
t.end_fill()

t.done()
```

## Drawing a square.
```
import turtle

silly = turtle.Turtle()

silly.fd(50)
silly.rt(90)   

silly.fd(50)
silly.rt(90)

silly.fd(50)
silly.rt(90)

silly.fd(50)
silly.rt(90)

turtle.done()
```

## Drawing a triangle.
```
import turtle
turtle.bgcolor("orange")
t = turtle.Turtle()
t.width(5)
t.shape("circle")

t.fd(100)
t.rt(120)
t.fd(100)
t.rt(120)
t.fd(100)
t.rt(120)
t.done()
```

## Drawing a circle
```
import turtle

t = turtle.Turtle()

t.circle(100)

t.penup()
t.goto(120, 0)
t.pendown()

t.circle(100)


t.done()
```

## Drawing a square (using loops)
```
import turtle 

smart = turtle.Turtle()

# Loop 4 times. Everything I want to repeat is 
# *indented* by four spaces.
for i in range(4):
    smart.fd(50)
    smart.rt(90)
    
# This isn't indented, so we aren't repeating it.
turtle.done()
```
# [turtle 응용]
## Drawing tree
```
import turtle 

t = turtle.Turtle()

t.penup()
t.goto(0, 200)
t.pendown()

t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)

t.penup()
t.goto(0, 150)
t.pendown()

t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)

t.penup()
t.goto(0, 100)
t.pendown()

t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)
t.lt(120)
t.fd(100)

t.done()
```

## Drawing a star
```
import turtle 

star = turtle.Turtle()

for i in range(50):
    star.fd(50)
    star.rt(144)
    
turtle.done()
```

## Spiraling star
```
import turtle 

spiral = turtle.Turtle()

for i in range(20):
    spiral.fd(i * 10)
    spiral.rt(144)
    
turtle.done()
```

## Changing line color
```
import turtle 

painter = turtle.Turtle()

painter.pencolor("blue")

for i in range(50):
    painter.fd(50)
    painter.lt(123) # Let's go counterclockwise this time 
    
painter.pencolor("red")
for i in range(50):
    painter.fd(100)
    painter.lt(123)
    
turtle.done()
```


## Variables
```
import turtle 

polygon = turtle.Turtle()

num_sides = 6
side_length = 70
angle = 360.0 / num_sides 

for i in range(num_sides):
    polygon.fd(side_length)
    polygon.rt(angle)
    
turtle.done()
```

## Nested loops
```
import turtle 

seurat = turtle.Turtle()

dot_distance = 25
width = 5
height = 7

seurat.penup()

for y in range(height):
    for i in range(width):
        seurat.dot()
        seurat.fd(dot_distance)
    seurat.backward(dot_distance * width)
    seurat.rt(90)
    seurat.fd(dot_distance)
    seurat.lt(90)
    
turtle.done()
```

## Jumping around and changing speed
```
import turtle 

ninja = turtle.Turtle()

ninja.speed(10)

for i in range(180):
    ninja.fd(100)
    ninja.rt(30)
    ninja.fd(20)
    ninja.lt(60)
    ninja.fd(50)
    ninja.rt(30)
    
    ninja.penup()
    ninja.setposition(0, 0)
    ninja.pendown()
    
    ninja.rt(2)
    
turtle.done()
```

[ref](https://opentutorials.org/module/2980/17289)

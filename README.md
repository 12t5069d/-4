4.3 練習課題

1.
 from swampy.TurtleWorld import*
 world = TurtleWorld()
 bob = Turtle()
 def square(t):
     for i in range(4):
         fd(t, 100)
         lt(t)

 square(bob)


2.
def square(t, lenght):
    for i in range(4):
        fd(t, lenght)
        lt(t)

square(bob, 200)



3.
def polygon(t, lenght, n):
    angle = 360 / n
    for i in range(n):
        fd(t, lenght)
        lt(t, angle)

polygon(bob, 7, 70)

4.
 def circle(t, r):
     circumferance = 2 * math.pi * r
     n = 50
     lenght = circumferance / n
     polygon(t, lenght, n)

 import math
 circle(bob, 50)

5.
 def polyline(t, n, lenght, angle):
     for i in range(n):
       fd(t, lenght)
       lt(t, angle)

 def polygon(t, n, lenght):
     angle = 360.0 / n
     polyline(t, n, lenght, angle)

 def arc(t, r, angle):
     arc_lenght = 2 * math.pi * r * angle / 360
     n = int(arc_lenght / 3) + 1
     step_lenght = arc_lenght / n
     step_angle = float(angle) / n
     polyline(t, n, step_lenght, step_angle)

 def circle(t, r):
     arc(t, r, 360)

 circle(bob, 70)


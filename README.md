import math

# PARENT CLASS
class Circle:
    def __init__(self, radius):
        self.radius = radius
# AREA OF THE CIRCLE
    def area(self):
        area = math.pi * (self.radius ** 2)
        print('The area of circle is:', round(area, 2))

# CIRCUMFERENCE OF THE CIRCLE:
    def circumference(self):
        circumference = 2 * math.pi * self.radius
        print('The circumference of this circle is :', round(circumference, 2))

# CHILD CLASS
class Cone(Circle):
    def __init__(self, radius, height):
        super().__init__(radius)
        self.radius = radius
        self.height = height

# AREA OF THE CONE :
    def conearea(self):
        area = math.pi * self.radius * (self.radius + math.sqrt(self.height ** 2 + self.radius ** 2))
        print('The area of the cone is :', round(area, 2))

# VOLUME OF THE CONe
    def volume(self):
        volume = 1/3 * (self.height * math.pi * (self.radius ** 2))
        print('The volume of the cone is:', round(volume, 2))



radius1 = int(input("Input the radius:"))
print("AREA AND CIRCUMFERENCE OF CIRCLE")
P1 = Circle(radius1)
P1.area()
P2 = Circle(radius1)
P2.circumference()
print('----------------------------------------------')
radius2 = int(input("Input the radius:"))
height = int(input('Input the height:'))
print("AREA AND VOLUME OF CONE")
C1 = Cone(radius2, height)
C1.conearea()
C2 = Cone(radius2, height)
C2.volume()


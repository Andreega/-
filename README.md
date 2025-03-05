python
class Report:
    def generate_report(self, data):
        return f"Report: {data}"

    def save_report(self, report):
        with open('report.txt', 'w') as file:
            file.write(report)


python
class ReportGenerator:
    def generate_report(self, data):
        return f"Report: {data}"

class ReportSaver:
    def save_report(self, report):
        with open('report.txt', 'w') as file:
            file.write(report)


#2

python
class AreaCalculator:
    def calculate_area(self, shape):
        if isinstance(shape, Circle):
            return 3.14 * shape.radius ** 2
        elif isinstance(shape, Rectangle):
            return shape.width * shape.height



python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
def area(self):
        return self.width * self.height

class AreaCalculator:
    def calculate_area(self, shape: Shape):
        return shape.area()


#3

python
class Bird:
    def fly(self):
        print("Flying")

class Ostrich(Bird):
    def fly(self):
        raise Exception("Ostrich can't fly!")



python
class Bird:
    def move(self):
        pass

class Sparrow(Bird):
    def move(self):
        print("Flying")

class Ostrich(Bird):
    def move(self):
        print("Running")



#4

python
class Machine:
    def print(self, document):
        pass

    def scan(self, document):
        pass

    def fax(self, document):
        pass




python
class Printer:
    def print(self, document):
        pass

class Scanner:
    def scan(self, document):
        pass

class FaxMachine:
    def fax(self, document):
        pass


#5

python
class LightBulb:
    def turn_on(self):
        print("Light is ON")

    def turn_off(self):
        print("Light is OFF")

class Switch:
    def __init__(self, bulb):
        self.bulb = bulb
        
    def operate(self):
        self.bulb.turn_on()





python
class Switchable:
    def turn_on(self):
        pass

    def turn_off(self):
        pass

class LightBulb(Switchable):
    def turn_on(self):
        print("Light is ON")

    def turn_off(self):
        print("Light is OFF")

class Switch:
    def __init__(self, device: Switchable):
        self.device = device

    def operate(self):
        self.device.turn_on()

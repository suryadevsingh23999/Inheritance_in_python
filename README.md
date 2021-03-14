# Inheritance_in_python
# In this repository you will get basic programs of different types of inheritance in python 
# Inheritance : with inheritance one class can derive the properties of another class
# Types of Inheritance : inheritance is of four types - Single inheritance, Multiple inheritance, Multi level Inheritance and hybrid inheritance 
# Here is example of basic inheritance :
class Vehicle:
    def __init__(self,mileage,cost):
        self.mileage=mileage
        self.cost=cost
    def show_vehicle_details(self):
        print("Mileage of vehicle is",self.mileage)
        print("Cost of vehicle is",self.cost)
        print("I am a Vehicle")
v1=Vehicle(300,500)
v1.show_vehicle_details()

# This is a Super class or parent class now we have to create a child class
class Car(Vehicle):
    def show_car_details(self):
        print("I am a Car")
c1=Car(250,800)
c1.show_car_details()

# Multiple inheritance in Python : In multiple inheritance, the child inherits from more than 1 parent class 
# For this we have to create two parents class and one child class which inherits both the parents class
# Now we have to create a first parent class -
class Parent1():
    def assign_string_one(self,str1):
        self.str1=str1
    def show_string_one(self):
        return self.str1
# then we have to create a second parent class -
class Parent2():
    def assign_string_two(self,str2):
        self.str2=str2
    def show_string_two(self):
        return self.str2
# and finally we have to create a child class
class Child(Parent1,Parent2):
    def assign_string_three(self,str3):
        self.str3=str3
    def show_string_three(self):
        return self.str3
my_child=Child()
my_child.assign_string_one("I am string of parent 1")
my_child.assign_string_two("I am string of parent 2")
my_child.assign_string_three("I am string of parent 3")
my_child.show_string_one()
my_child.show_string_two()
my_child.show_string_three()
# So, this is the concept of multiple inheritance

# Multi-level-inheritance in Python : In multi level inheritance we have parent,child,grand-child relationship
# Now we have create a Parent class -
class Parent():
    def get_name(self,name):
        self.name=name
    def show_name(self):
        return self.name
# then we have to create a child class -
class Child(Parent):
    def get_age(self,age):
        self.age=age
    def show_age(self):
        return self.age
# and finally we have to create a Grandchild class -
class GrandChild(Child):
    def get_gender(self,gender):
        self.gender=gender
    def show_gender(self):
        return self.gender
gc=GrandChild()
gc.get_name("RISHABH")
gc.get_age(22)
gc.get_gender("Male")
gc.show_name()
gc.show_age()
gc.show_gender() 
# So, this is the concept of multi-level-inheritance 




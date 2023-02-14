# Report on OOPS concepts

 As the software industry started progressing, the OOPs utilization became more popular among the modern programming languages. The implementation of OOPs plays an important role to increase the scope of modern programming languages such as representing real life objects, writing shorter and simple code, eliminate redundant code making the code reusable.

OOPs stands for Object Oriented Programming System, in which a program is written by creating classes that contains data and functions which are known as Methods. An instance of such a class is termed as an Object. This concept of a class that combines data and methods together and could represent any real-world object. 

In a class, the data is usually fed as variable either directly or through constructor and along with it, the operations or functions are given that could utilize, inspect or modify the data which are called Methods. A class is like a blueprint for creating an object. The classes in programming can be understood by an example of a Car, where the class stores data like Car model number, Engine power, Height, Colour, and methods represent the operations related to it such as turning engine ON/OFF, changing the speed, changing gears, steering the wheel, etc.

The features of an object created are defined by what data and methods were given while defining the class. This Object Oriented Programming system allows programmer to combine all information of an object and operations related to it, in a single unit. Therefore, programmers can make their code systematic, modular and reusable as compared to traditional Structure Programming Language.

## Why OOPs languages are used over Functional languages 

In a Structure or a Functional programming language, the code is written in a way that data structure are defined to stores a data, and functions are written in order to access or change this data. When we consider this approach to develop software, it may solve the problem or fulfil the requirement for that particular scenario when it was created, but in this age of big data where billions of files and information are processed or used, this written code will began to create a problem after a certain size limit, and then managing this codebase and sections that are interrelated to  each other becomes very difficult. Changing one section of code can even lead to failure in functioning of other parts or entire application. 

This problem is solved by Object-Oriented Programming languages where all the operations are specifically used to operate on the data encapsulated in a single unit called object. So, any changes to data are done by their related methods, and dependencies of functions on each other are reduced. So, we can easily manage our code and make any required changes. 

## Elements of Object-Oriented Programming System: -

### 1. Class 
A class can be expressed as a user defined data type just like structures in C programming languages. In structures, we can store different data in a single unit whereas in a class we can store data along with the functions related to it. This element is the base of Object-Oriented Programming and is used to create objects.

### 2. Objects
When we initiate the data inside a class or in other words create an instance of class, an object is created. It is the actual running element used in the code whose structure is defined by the class through which it was created. These objects are real world representation of a specific Object. Traditionally, in functional programming languages, a solution to a problem is created by segmenting the code into functions, whereas in Object-Oriented Programming we divide problem into objects.

### 3. Constructor 
A Constructor is a very important element used while creating a class. This functions assigns the data to the object variables inside it, that was given while creating the object. Once the variables are initialized, they can be accessed by any methods of an object.

### 4. Destructors 
Destructors are used to terminate the object when it is not referenced any more or program ends, in order to free memory. This element is not mandatory but is considered as a good practice as it acts as a garbage collector, saving memory for future use.

## OOPs Concepts:-

### 1. Inheritance 
Inheritance is one of four core functionality of OOPs, where a pre existing class known as parent class is inherited inside another class called child class. This allows the child class to reuse the functions and data inside the parent class, thus reducing the generation of redundant code. A child class can either used all or few functions and data of its parent class, and also override and change the inherited function.

Below is the example of Inheritance in Python
```
# parent class
class Vehicle:
  def __init__(self, brand, colour):
    self.Brand = brand
    self.Colour = colour

  def printname(self):
    print(f"Vehicle brand is '{self.Brand}' and it's colour is {self.Colour}.")

# child class
class Car(Vehicle):
  def Print(self):
    print("This is a Car.")
     
car = Car("HONDA", "White")
 
# calling parent class function
car.printname()
 
# Calling child class function
car.Print()
```

### 2. Encapsulation

Encapsulation property is used to ensure the security of the code, by keeping our object’s original data and methods secure from outside interference and getting altered. This is a way to prevent the direct access to the essential parts of our code from getting misused or damaged, and hide them while running the code.

Example of Encapsulation in Python
```
# Creating a base class
class parent:
	def __init__(self):

		# Protected data
		self._a = 2

# Creating a derived class
class child(parent):
	def __init__(self):

		# Calling constructor of
		# Base class
		parent.__init__(self)
		print("Calling protected member of base class: ",
			self._a)

		# Modify the protected variable:
		self._a = 3
		print("Calling modified protected member outside class: ", self._a)


obj1 = child()

obj2 = parent()

# Calling protected member
print("Accessing protected member of obj1: ", obj1._a)

# Accessing the protected variable outside
print("Accessing protected member of obj2: ", obj2._a)

```

### 3. Polymorphism 

Polymorphism is the ability of code to be used in more than one form. This is one of the crucial concepts of OOPs, so that we can utilize the given functions or property in other useful way. The terms like overriding and overloading are examples of this concept. Overriding occurs when multiple methods have same name and parameters, and Overloading happens when methods of same names have different parameters.

Example of Polymorphism in python 
```
# Using 'for' to print all numbers in the range
for i in range(1, 11):
    print(i, end=" ")

print()

# Using 'for' to print all elements of the list
l = ["A", "B", "C"]
for i in l:
    print(i, end=" ")
```
### 4. Abstraction
The process of abstraction in OOPs is used to hide any complicated data from user or any functions, and it displays only relevant and required data. This is done in order to increase simplicity of code, increase efficiency, and provided smooth workflow.

Example for Abstraction using python and it's 'abc' Library
```
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def brand(self):
        pass
        
class Car(Vehicle):

    def engine_start(self):
        print("The engine is running.")
 

c = Car()
print(c.engine_start())
```



<br/><br/>  

# References :-

### 1. [What is a Code Base.](https://www.techtarget.com/whatis/definition/codebase-code-base)
### 2. [ What is Refactoring ? (as a software developer)](https://www.youtube.com/watch?v=DQJGRV9np40)
### 3. [Code Refactoring](https://www.youtube.com/watch?v=vhYK3pDUijk)  
### 4. [What Are OOP Concepts in Java?](https://stackify.com/oops-concepts-in-java/)

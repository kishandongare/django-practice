# Oops Concept

Object Oriented Programming as the name suggests uses object in programming.
Object means real world entity such as pen, copy, laptop, car.
It simplifies the software development.

In c language our program was structured around function and logic (or procedural programming).
But in c++ our program is object orianted approach.

# ```Oops Provides some concept(Feature):```

1.Object

2.Class

3.Polymorphism

4.Encapsulation

5.Abstraction

6.Inheritance

# ```Object```

>> Object is a real world entity such as pen,laptop, mobile.

>> Object is an instance of a class.

>> Object is created many times as per requrement.

>> Object allocated memory when it is created.

>> Example: class->Human and Object -> Man, Woman

# ```Class```

>>Class is a blueprint or templates from which objects are created.

>>Class is a group of similar objects.

>>Class doesn't allocated memory when it is created.

# ```__init__```

>>The init method or function is similar to constructor in c++ and java.

>>When we create objects of class it is automatic called.

# ```self```

>> By using the self keyworld we can access the attributes and function of the class in program.

>> It is a first parameter of any function.

```python

class person:
  def __init__(self,name):
        self.name = name
  def say_hi():
        print("Hello, My Name is",self.name)
p = person('kishan')
p.say_hi()

```

# ```Polymorphism```

>> The term "Polymorphism" is the combination of "poly" and "morphs" which means many forms.

>> Example: The + operator is used to perform two specific operations

![image](https://user-images.githubusercontent.com/66677660/208247018-519d4931-3609-47e8-9069-bc7fba9451cf.png)

 1.When it is used with numbers, it performs additions

```python
a=5
b=6
print(a+b)
```

2.When we use the  + operator with string it performs string concatenation

```python
firstname = "kishan"
lastname = "dongare"
print(firstname+lastname)
```
# Function Overloading

Function overloading is defined as the process of having two or more functions with the same name,
but different in parameters (argument) is known as function overloading in c++.

```c++

#include<iostream.h>
using namespace std;
int sum(int num1, int num2)
{  
   return num1+num2;
}
double sum(double num1, double num2)
{  
   return num1+num2;
}
int sum(int num1, int num2, int num3)
{  
   return num1+num2+num3;
}
int main()
{
cout<<"sum1 = "<<sum(5,6)<<endl;
cout<<"sum2 = "<<sum(5.5,6.8)<<endl;
cout<<"sum3 = "<<sum(5,6,7)<<endl;
return 0;
}
```

python does not support method overloading by default.

```python
def product(a,b):
   p = a*b
   print(p)
def product(a,b,c):
   p = a*b*c
   print(p)
product(3,4,5) # this line will call second product function
```
Note:When we pass 2 argument It will through error( Type error)

# Operator Overloading

Operator overloading is a compile-time polymorphism. Polymorphism allows 
the same operator name or symbol to be used for multiple operations.

```python

# Python program to show use of
# + operator for different purposes.
 
print(1 + 2)
 
# concatenate two strings
print("Geeks"+"For")
 
# Product two numbers
print(3 * 4)
 
# Repeat the String
print("Geeks"*4)

```
# functon overriding

If derived class defines same function as defined in its base class, it is known as function overriding.

```python
class parent:    #base class
    def __init__(self):
        self.value = "Inside Parent"
    def show(self):  
        print(self.value)
class child(parent): #derived class
    def __init__(self):
        self.value = "Inside Child"
    def show(self):     
        print(self.value)
ob = child()
ob1 = parent()
ob.show()
ob1.show()      

```
# Encapsulation

>> Wrapping up of data and function into a single unit is known as encapsulaton.

>> encapsulation is a process of wrapping similar code in one place.

>>We can implement encapsulation by using access specifiers.(Private, Public, Protected)


# Abstraction

>>Data abstraction refers to providing only essential information 
to the outside world and hiding their background details.

>>It give the programmer to control on what data or function 
are to be made visible to the user and what are kept secret.

```c++

#include<iostream.h>
#include<math.h>
int main()
{
int n = 4;
int power = 3;
int result = pow(n,power);
cout<<"cube of n is :"<<result;
return 0;
}

```
# Inheritance

>>Inheritance provides code reusability to program.

>>We do not have to write same code again and again, 
we can just inherit the propertice we need in child class.

Single Inheritance: 

```python

# Python program to demonstrate
# single inheritance

# Base class
class Parent:
	def func1(self):
		print("This function is in parent class.")

# Derived class


class Child(Parent):
	def func2(self):
		print("This function is in child class.")


# Driver's code
object = Child()
object.func1()
object.func2()

```

Multilevel

```python
# Base class

class Vehicle:
    def Vehicle_info(self):
        print('Inside Vehicle class')

# Child class
class Car(Vehicle):
    def car_info(self):
        print('Inside Car class')

# Child class
class SportsCar(Car):
    def sports_car_info(self):
        print('Inside SportsCar class')

# Create object of SportsCar
s_car = SportsCar()

s_car.Vehicle_info()
s_car.car_info()
s_car.sports_car_info()

```
Multiple Inheritance

```python
class SuperClass1:
    num1 = 3

class SuperClass2:
    num2 = 5

class SubClass( SuperClass1, SuperClass2):
    def addition(self):
        return self.num1 + self.num2

obj = SubClass()
print(obj.addition())

```

Hierarchical Inheritance

```python

class Parent:
      def func1(self):
          print("this is function 1")
class Child(Parent):
      def func2(self):
          print("this is function 2")
class Child2(Parent):
      def func3(self):
          print("this is function 3")
 
ob = Child()
ob1 = Child2()
ob.func1()
ob.func2()
```
Hybrid Inheritance

```python
class Parent:
     def func1(self):
         print("this is function one")
 
class Child(Parent):
     def func2(self):
         print("this is function 2")
 
class Child1(Parent):
     def func3(self):
         print(" this is function 3"):
 
class Child3(Parent , Child1):
     def func4(self):
         print(" this is function 4")
 
ob = Child3()
ob.func1()
```


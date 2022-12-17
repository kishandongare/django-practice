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

>> Object is a real world entity such as pen, cae, mobile.
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
>> Example: The + operator in is used to perform two specific operations

![image](https://user-images.githubusercontent.com/66677660/208247018-519d4931-3609-47e8-9069-bc7fba9451cf.png)

1.When it is used with numbers, it performs additions
```python
a=5
b=6
print(a+b)
```

2. When we use the  + operator with string it performs string concatenation

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
def product(a,b, c):
   p = a*b*c
   print(p)
product(3,4,5) # this line will call second product function
```
Note:When we pass 2 argument It will through error( Type error)









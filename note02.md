# Object Oriented Programming notes: Part 2
## Encapsulation 
### What is encapsulation?
**Encapsulation** -> concealing data: limiting entry to specific methods & attributes in a class/object

**Why tho?**
-defend data from outsiders accessing it
-limiting specific methods to be callable 
**important**
+ Python does not really have this ability. However we can use a specific system for python. -> concealing attributes & methods via two underscores at the beginning

### Example 
```
class Student: 
  def __init__(self, nameF, nameL, num):
    self.firstName = nameF
    self.lastName = nameL 
    self.__studentNumber = num 
  def __getStudentNumber(self):
    return self.__studentNumber
#end of student 
s1 = Student("Mr.", "Park", 10)
print(s1.__getStudentNumber()) # Will cause an error 
print(s1.__studentNumber) # Will also cause an error 
```
### Why encapsulation is important 
``` 
class Student: 
  def __init__(self, nameF, nameL, num):
    self.firstName = nameF
    self.lastName = nameL
    self.__studentNumber = num 
# end of student 

s1 = Student("Mr.", "Park", 10) 
print(s1.firstName) # Returns/Outputs "Mr."

s1.firstName = "Ms."
print(s1.firstName) # Returns/Outputs "Ms."
```

### Common Practice 

```
class Student: 
  def __init__(self,nameF, nameL, num):
    self.__firstName = nameF
    self.__lastName = nameL
    self.__studentNumber = num 
    
  def setFirstName(self, newName):
    self.__firstName = newName 
    
  def getFirstName(self):
    return self.__firstName 
``` 

## Overrides
### Overloading vs Overriding 

**Overloading** 
+ 2 methods in one class have are named identically, but their parameters are not the same 

**Overriding**
+ 2 methods named identically and have identical parameters

+ one method is in the parent class
+ the other is in the child class 
+ overrising enables the child class to supply certain implementation for a method that is present in the parent class
+ you are allowed to override built-in magic methods/base functions 

**IMPORTANT**: in python 3, overloading does not happen

## Polymorphism 
### What is polymorphism?
**Polymorphism**
+ a method that is allowed to be used across a variety of classes & objects that relies on the parameters 

Poly means many 
Morphism means forms 

**Ideas:**
+ Unlike classes (ones that are not inherited) are able to have methods that are named identically -> polymorphism 
+ inside a set of inherited class, they possess identical methods

### 2 different classes with the same method 
```
class Bear: 
  def sound(self): 
    print("Groarr")
class Dog: 
  def sound(self):
    print("Woof woof!")
def makeSound(animalType):
  animalType.sound()

bearObj = Bear()
dogObj = Dog()

makeSound(bearObj)
makeSound(dogObj)

'''
In conclusion:
We can give two different classes same methods; hence, **Polymorphism.**
'''
```
### Polymorphism & inheritance 
**overloading** 
+ in Python 3, it is forbidden. However, it is considered a type of polymorphism 

**Inherited classes altering inherited methods** (Overriding) -> Python 3 Polymorphism 

### Example of forbidden Overloading
```
class Person:
  def __init__(self,name,age):
    self.__name = name 
    self.__age = age
  def show(self): 
    return self.__name 
  def show(self, num):
    return "%s %d" % (self.__name, self.__age)
 ```
 ## Base overrides
 

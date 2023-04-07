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
### Python: Override & Polymorphism
we are able to have:
+ 2 unlike classes that possess identical attributes & methods 
+ A child of a parent possesses an overrided method, in which the child would use the method in a distinct way

Within Python, 2 basic ideas of overriding & polymorphism exist

We are able to override Python 3 built-in methods/operators. To add on, we can override the objects we created too.

Certain websites address them as "magic methods"

### Example
```
class Dog: 
  def __init__(self,name): 
    self.__name = name 
    
  def __str__(self):
    return "Woof, I'm %s." % self.__name
corgi = Dog("Tobasco")
print(corgi) -> "Woof, I'm Tobasco."
```

### Why override built-in methods & operators 
**Benefits:**
+ Able to begin to finish mathematical operations on the objects we made 
+ Able to begin to differentiate equality between objects we made 

**thus:** You are able to begin to influence how the object executes when it interacts with built-in methods & operators

## __repr__ base function 
### __repr__() base function 
>**repr(object)**
Return a string containing a printable representation of an object. For many types, this function makes an attempt to return a string that would yield an object with the same value when passed to eval(); otherwise, the representation is a string enclosed in angle brackets that contains the name of the type of the object together with additional information often including the name and address of the object. A class can control what this function returns for its instances by defining a __repr__() method. If sys.displayhook() is not accessible, this function will raise RuntimeError.

If you wanna make your custom objects be able to print, overriding __repr__ & __str__ is required.

__repr__ -> lets us show our project in print format 
__str__ -> lets us switch our object into a string

# Citations (MLA 8)
Park, Jasper. “U3L2 - Object Oriented Programming 2.” Google Slides, Mar. 2023, docs.google.com/presentation/d/1BSBVPl27YKaFtiNa_6EPyUd5gnM5o60fKHdrmtp2jGk/edit#slide=id.g55ff3e348b_0_90.

“Built-in Functions.” Python Documentation, docs.python.org/3/library/functions.html?highlight=repr#repr.

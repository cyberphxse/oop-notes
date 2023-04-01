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


# Object Oriented Programming notes: Part 3
## Inheritance 
>“When I see a bird that walks like a duck and swims like a duck and quacks like a duck, I call that bird a duck.” -James Whitcomb Riley

### What is inheritance?
**Inheritance** 
+ When an object or class is the offspring of a class; where their characteristics are based off a parent class
**Types:**
+ **Single inheritance:** a subclass that possesses the features of 1 superclass/parent class 
+ **Multiple inheritance:** a subclass that possesses the features of 2+ parent classes
+ **Multilevel inheritance:** a subclass that inherits features from another subclass A->B->C (A is the grandparent and C is the grandchild)

**Inheritance** has the ability to possess a ranking (branching similar to a family tree) &/or be a crossbreed between the inheritance types 

### What can we do with inheritance?
+ A child will possess every single atrribute & method from the parent 
+ The Child is able to amplify itself with updated or new attributes & methods
+ The child is able to override attributes & methods for their own favor/area of specialty 

### Notes 
if the child class inherits the parent class: 
+ The child is not required to have a new __init__() method. However, if it needs new attributes, it will need the method
+ The child is not required to reinstall the parent's methods. However, if you overrided them, then you have to reinstall them

### Python 3: Single inheritance 
``` 
class ParentClassName: 
  """ Define Parent Class"""
  .
  .
  .
class InheritanceClass(ParentClassName):
  """Define Inherited Class"""
  
  def __init__(self, param, param2):
    ParentClassName.__init__(self,param)
    self.param2 = param2
```

### example 
**Parent Class**
```
class Person: 
  def __init__(self,name):
    self.__name = name
    
  def getName(self): 
    return self.__name
```
**Inherited class**
```
class Student(Person): 
  def __init_(self,name,num):
    Person.__init__(self,name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" %(self.__sNum,self.getName()))
```
**Execution**
```
p = Person("Mr. Park")
s = Student("Random Child", "1234")
print(p.getName()) # Output: "Mr. Park" 
print(s.getStudentName(), "and", s.getName()) # Output: "1234: Random child and Random Child"
```
### What is super()?

super -> method that is built-in used for classes to reference their parent class
+ stops us from using ParentClass.method(self) 
+ Do not confuse yourself with the self within a self!




    

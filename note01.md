# Object Oriented Programming: First Chapter
## Video games portraying human life 
### Human species as a class 
Several atrributes humans possess
+ Race
+ Gender
+ Age 
+ Height 
+ Hair color 
+ Weight 
+ Preffered food 
+ IQ
### Actions that Humans possess
+ Eat/drink/sleep
+ Automatic → Monitor Breathing & Temperature
+ Speak
+ Interact with Other Objects/humans
### You -> an object under the Human class
+ every human alive is under the Human Class
+ All humans have built-in attributes and perhaps make offspring that will be part pf the same class
+ Some humans will be more advantaged than others. However, not worry because all humans will lose their privilege to roam the playable open world 
## Object 
### What is an Object?
In the realm of Computer Science: 
+ "Object can be a variable, a data structure, a function, or a method; therefore, a location in memory having a value that can be referenced by an identifier"
In the realm of Object Oriented Programming:
+ "Similar to an object as in CS, an object in OOP is an instance of a class where this object can be either a variable, a function, a data structure or a combination of such"
## The OOP Paradigm 
### Object Orient Programming (OOP)
+ Used in programming to create longlasting software systems that contain modules 
+ creates programs by making things called **Objects**
+ Concentrates on the representation of information over the IPO procedure (OOP vs procedure-based programming)
+ The objective is to make an object that we can establish as well as give purpose to resolve dilemmas
### Conceptual differentiation 
#### procedure-based 
A human specimen may need
+ calculations 
+ Logic based analysis 
+ ability to do recurring steps 
+ database
#### OOP
Making an object that represents a human 
+ What do name do they go by 
+ Where do they live 
+ What functions are built into this function
“OOP focuses on how to manipulate the data of the object rather than the logic required to manipulate them”
### Deeper evaluation into an object
**Object**: A mixture of data & function code. This can represent states & habits that a real world object may possess

**Remember that an object is an occurence**

**states**: What information can be measured about the object 

**habits**: What the object can do (what functions it can perform) 

Object's Data -> known in OOP as: attributes

Object's Code -> known in OOP as: methods 
### An example of an instance representing a dog
#### Dogs often possess the following **Attributes** 
+ Name 
+ Color
+ Breed
+ isHungry
+ isThirsty
#### Dogs often possess the following **Methods**
+ bark()
+ eat()
+ sleep()

If more attributes are added to the dog then we have an occurance, thus, an **object** is created
### Classes & Objects
**Class**: conceptual illustration of every object that can be created by this set class that can instantiate objects when needed 

**Attributes** are often found in a Class

**Attributes** are known as an object's available mechanisms

1. Fields: A class or object's variables
  -First type: the occurance of the class owns it 
  -Second type: the class owns it 
2. Methods: Functions that the object can use or call on demand
## OOP in Python 3 
### Important term: Class
**Class** -> a preset keyword available in python that can let us make our own classes

Example: 
```
  # The Most Basic Class
  
  class ClassName: # Notice that Class names are capitalized
     pass # An empty Block 
  # End of ClassName
  
  obj = ClassName()
  print(obj)
```
### Making a Class
1. Establish the Class name by using the keyword: **class**
2. Within the code block that defines your class, establish its attributes
3. Establish a variable along with an instantiation of the class to interact with it
  - Use brackets when calling the class name 
## Example with the person class
```
class Person: 
  pass # An Empty Block
# End of Person Class

student1 = Person() # Student1 is now a Person Object
print(student1)
```

### Making a method in a class
Classes have the ability to possess methods. To use them in Python 3, just like a new function, state them (no need to return)

Example:
```
  class Person:
    def greet(self):
       print('Hello, How are you?')
    #end of greet
  #end of class Person
  p = Person()
  p.greet() # outputs the greet message ...
  # the method is accessed with a period (.) 
  # Wait... what is the self????
```

### The __init__ methods & self parameter 
def __init__(self): -> known as the __init__ method (two underscores for each side)

+ Performs the second when the object of the class is instantiated 
+ Initializes the object's attributes 
+ **self** parameter -> indicates the method is already put in & available for access for the object itself 
+ To add on, **self** will view its own attributes as local

double underscores in python are important unseen characteristics which enables us to update python features & unseen information 

### example -> Person class
```
class Person: 
    def __init__(self,name):
        self.name = name 
    #end of initialization 
    
    def greet(self): # The self parameter is always required 
        print("Hello, my name is", self.name)
    #end of greet 
#end of class Person

p = person('Mr. Park')
p.greet()
```
## Example: List

### Python 3: List as an Object
L = [1,2,3,4]
+ L -> occurance of the list class; Thus, L is an object

#### Features 
L[i] -> indexing

L [i:j] -> slicing 
functions -> len(), min(), max()
operators -> + & * 
methods -> L.append(), L.count(), L.extend(), L.sort(), L.reverse()

**Important**
No need to know how these were coded, just need to know what abilities lists have 

## Citations (MLA 9):
Park, Jasper. “U3L1  - Object Oriented Programming 1.” Google Slides, Mar. 2023, docs.google.com/presentation/d/1wJ1SqLBaVSahdJUO41QRkyyLDmXpMWCROxV5TzdWsvU/edit#slide=id.p.




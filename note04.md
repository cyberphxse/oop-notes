# Object Oriented Programming note: part 4
## Iterable objects 
### Iterable objects
**Iterable Objects:** Objects that are able to be iterated through similar to a sequence 

**Examples**: Strings & lists (as well as sets & dictionaries)
+ remember that we are able to iterate through both strings & lists 
+ To grab single values w/o indexing, we can use for loops

**Important:**
+ The part of iterable object needs to be a sequence 
+ Just because something is iterable, it is not guaranteed that it can be indexed

### example- prints every card in the deck 
```
class Deck:
	… Code …
	def __iter__(self):
		return self

	def __next__(self):
		self.__index += 1
		if self.__index == len(self.__cards):
			self.__index = -1 # index reset
			raise StopIteration
		else:	
			return self.__cards[self.__index]

	… Code …	
```
### __iter__() & __next__()
**__init__()**
+ makes our object iterable, when called upon (ex. for loop), it will call the method. Often returns itself
**__next__()**
+ enables us to get the value after during iteration 
+ practice often used: 
 + put index attribute as -1 
 + put the index attribute by 1 until self.__index is as long as the sequence
 + when it reaches the final value, raise Stopiteration
### How about indexing?
Indexing is very complex, it needs many modules to be imported to let your own object to be indexable & sliceable 

# Citations (MLA 8) 
Park, Jasper. “U3L4 - Object Orientated Programming 4.” Google Slides, Mar. 2023, docs.google.com/presentation/d/1-Q1t0MzkhzI1iqMS6M0vO7iWNR5Ov6Gn-ClVVrjQT-Y/edit#slide=id.g2aa4fceed5_0_192.

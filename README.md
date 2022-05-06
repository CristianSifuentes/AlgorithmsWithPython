# AlgorithmsWithPython


   * [Object-oriented programming
](#object-oriented-programming)
      * [What you will learn about object-oriented programming and algorithms with Python
](#what-you-will-learn-about-object-oriented-programming-and-algorithms-with-python
)
      * [Object-oriented programming
](#object-oriented-programming)
      * [Abstract data types and classes, Instances
](#abstract-data-types-and-classes-instances)
       * [Decomposition
](#decomposition)  
       * [Decomposition
](#decomposition)  
       * [Abstraction
](#abstraction)     
       * [Functions: decorators base
](#functions-decorators-base)  
       * [Setters, getters and property decorador 
](#setters-getters-y-and-property-decorador) 
       * [Encapsulation, getters and setters
](#encapsulation-getters-and-setters) 
       * [Inheritance
](#inheritance)     
       * [Polymorphism
](#polymorphism)    

   * [Algorithmic complexitys
](#algorithmic-complexity)  
      * [Introduction to algorithmic complexity](#introduction-to-algorithmic-complexity) 
      * [Abstract operation count
](#abstract-operation-count) 
      * [Asymptotic notation
](#asymptotic-notation) 
      * [Algorithmic complexity classes
](#algorithmic-complexity-classes) 


   * [Search and sort algorithms
](#search-and-sort-algorithms
)   
       * [linear search
](#linear-search)   
       * [Binary search
](#binary-search)  
       * [Bubble sort
](#bubble-sort) 
       * [Insertion Sort
](#insertion-Sort) 
       * [Merge Sort
](#merge-sort) 

   * [Virtual environments
](#virtual-environments)   
       * [Virtual environments
](#virtual-environments) 

   * [Graphed
](#graphed
)   
       * [Why graph?
](#why-graph?) 
       * [Simple-chart
](#simple-chart) 


   * [Optimization algorithms
](#optimization-algorithms
)   
       * [Introduction to optimization
](#introduction-to-optimization) 
       * [The backpack problem
](#the-backpack-problem
) 
       * [Conclusions
](#Conclusions
) 




Object-oriented programming
============

What you will learn about object-oriented programming and algorithms with Python
-----------

* Understand how programming works
Object Oriented.
* Understand how to measure time efficiency and
spatial of our algorithms.
* Understand how and why to graph.
* Learn to solve search problems,
ordering and optimization.

Decomposition
-----------

* Break a problem into smaller problems.
* Classes allow you to create larger abstractions
in component form.
* Each class deals with a part of the problem
and the program becomes easier to maintain

Abstraction
-----------
* Focus on the relevant information.
* Separate core information from details
secondary.
* We can use variables and methods (private or
public)

Encapsulation, getters and setters
-----------

* It allows grouping data and its behavior.
* Control access to such data.
* Prevents unauthorized modifications.
Inheritance

```python
class CasillaDeVotacion:
 def __init__(self, identificador, pais)
 self._identificador = identificador
 self._pais = pais
 self._region = None
 @property
 def region(self):
 return self._region
 @region.setter
 def set_region(self, region):
 if region in self._pais:
 self._region = region
 raise ValueError(f'La region {region} no es valida en 
{self._pais}')
>>> casilla = CasillaDeVotacion(123, ['Ciudad de Mexico', ‘Morelos’])
>>> casilla.region
None
>>> casilla.region = 'Ciudad de Mexico'
>>> casilla.region
'Ciudad de México'
```
-----------

* Allows modeling a hierarchy of classes.
* Allows sharing common behavior in the
hierarchy.
* The parent is known as the superclass and the child
as a subclass.

Polymorphism
-----------
* The ability to take various forms.
* In Python, it allows us to change the
behavior of a superclass for
adapt it to the subclass.
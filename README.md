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
       * [Abstraction
](#abstraction)     
       * [Functions: decorators base
](#functions-decorators-base)  
       * [Setters, getters and property decorador 
](#setters-getters-and-property-decorador) 
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


Object-oriented programming
-----------

Abstract data types and classes, Instances
-----------

* In Python everything is an object and has a type.
  * Data representation and forms of interact with them.

* Ways to interact with an object:
  * Creation
  * Handling
  * Destruction

* Abstract data types
  * Advantages:
    * Decomposition
    * Abstraction
    * Encapsulation


```python
 definición de clase
class <nombre_de_la_clase>(<super_clase>):
 def __init__(self, <params>):
 <expresion>
 def <nombre_del_metodo>(self, <params>):
 <expresion>
```
```python
# Definición
class Persona:
 def __init__(self, nombre, edad):
 self.nombre = nombre
 self.edad = edad
 def saluda(self, otra_persona):
 return f'Hola {otra_persona.nombre, me 
llamo {self.nombre}.'
# Uso
>>> david = Persona('David', 35)
>>> erika = Persona('Erika', 32)
>>> david.saluda(erika)
'Hola Erika, me llamo David'

```

* While the class is a cast, the objects
created are known as instances.
* When an instance is created, it runs the
__init__ method
* All methods of a class receive
implicitly as first parameter self

* Instances
   * Class attributes allow us to:
   * Represent data
   * Procedures to interact with them (methods)
* Mechanisms to hide representation
internal.
   * Attributes are accessed with dot notation.
   * May have private attributes. by convention
start with _



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



Functions-decorators-base
-----------

Setters, getters and property decorador
-----------

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

Inheritance
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



Algorithmic complexitys
============

Introduction to algorithmic complexity
-----------

* Why do we compare the efficiency of a
algorithm?
* Temporal complexity vs spatial complexity
* We can define it as T(n)

Abstract operation count
-----------

* Time how long you run a
algorithm.
* Count steps with an abstract measure of
operation.
* Count the steps as we approach the
infinite.

Asymptotic notation
-----------

asymptotic growth

* Small variations do not matter.
* The focus is on what happens as the
problem size approaches infinity.
* Best case, average, worst case
* Big O
* Nothing else matters the largest term



```python
# Ley de la suma
def f(n):
 for i in range(n):
 print(i)
 for i in range(n):
 print(i)
# O(n) + O(n) = O(n + n) = O(2n) = O(n
```

```python
# Ley de la suma
def f(n):
 for i in range(n):
 print(i)
 for i in range(n * n):
 print(i)
# O(n) + O(n * n) = O(n + n²) = O(n²
```

```python

# Ley de la multiplicación
def f(n):
 for i in range(n):
 for j in range(n):
 print(i, j)
# O(n) * O(n) = O(n * n) = O(n²
```

```python
# Recursividad múltiple
def fibonacci(n):
 if n == 0 or n == 1:
 return 1
 return fibonacci(n - 1) + fibonacci(n - 2)
# O(2**n)
```

Algorithmic complexity classes
-----------


Complexity classes
algorithmic
-----------

* O(1) Constant
* Linear O(n)
* O(log n) Logarithmic
* O(n log n) log linear
* O(n**2) Polynomial
* O(2**n) Exponence




Search and sort algorithms
============

Linear search
-----------
* Search all elements in a way
sequential.
* What is the worst case?

Binary search
-----------
* Divide and conquer.
* The problem is divided into 2 at each iteration.
* What is the worst case?

Bubble sort
-----------
+ Bubble sort is an algorithm that
repeatedly iterates through a list you need
sort out Compare adjacent items and
swap if they are in the wrong order. East
procedure is repeated until no
require more exchanges, indicating that the
list is sorted

Insertion Sort
-----------


Merge Sort
-----------
  * Merge sort is a
divide and conquer algorithm
First split a list into parts
the same until sublists remain
1 or 0 items. Then the
recombines in an orderly fashion
# Design Patterns Ch-01 #
* Principle: Separate aspects of the application that vary from parts that remain constant
  * take the parts that vary and encapsulate them, so that later you can alter or extend the parts that vary without affecting those that don’t.
* Principle: Program to an interface, not an implementation
  * The point is to exploit polymorphism by programming to a supertype so that the actual runtime object isn’t locked into the code
  * the declared type of the variables should be a supertype, usually an abstract class or interface, so that the objects assigned to those variables can be of any concrete implementation of the supertype, which means the class declaring them doesn’t have to know about the actual object types!
  * think of object behaviours as a family of algorithms that the object can choose from at runtime, rather than a set of fixed behaviours
* Principle: Favour Composition over Inheritance
  * let’s you encapsulate a family of algorithms
  * this in-turn allows changing behaviour at runtime

### The Strategy Design Pattern ###
* Defines a family of algorithms, encapsulates each one, and makes them interchangeable.
* Lets the algorithm vary independently from the clients that use it

### Takeaways ###
* Good OO designs are reusable, extensible and maintainable.



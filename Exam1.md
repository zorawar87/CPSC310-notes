# Design Patterns Ch-01 #
  * Principle: Separate aspects of the application that vary from parts that remain constant
    * take the parts that vary and encapsulate them, so that later you can alter or extend the parts that vary without affecting those that don’t.
  * Principle: Program to an interface, not an implementation
    * The point is to exploit polymorphism by programming to a super-type so that the actual run-time object isn’t locked into the code
    * the declared type of the variables should be a super-type, usually an abstract class or interface, so that the objects assigned to those variables can be of any concrete implementation of the super-type, which means the class declaring them doesn’t have to know about the actual object types!
    * think of object behaviours as a family of algorithms that the object can choose from at run-time, rather than a set of fixed behaviours
  * Principle: Favour Composition over Inheritance
    * let’s you encapsulate a family of algorithms
    * this in-turn allows changing behaviour at run-time

### The Strategy Design Pattern ###
  * Defines a family of algorithms, encapsulates each one, and makes them interchangeable.
  * Lets the algorithm vary independently from the clients that use it

### Takeaways ###
  * Good OO designs are reusable, extensible and maintainable.

----

# Clean Code Ch-01: Clean Code #
  * Wading
    * we wade through bad code
    * as in: struggle through 
  * Leblanc's law: Later equals never
  * Spending time keeping your code clean is not just cost effective; it’s a matter of professional survival

### The primal conundrum ###
  * *All developers know that previous messes slow them down, yet all developers feel the pressure to make messes in order to meet deadlines*
  * *True professionals know that the second part of the conundrum is wrong*
    * *You will not make the deadline by making the mess*
  * Keep the code as clean as possible at all times

### On Writing Clean Code ###
  * a programmer who writes clean code is an artist who can take a blank screen through a series of transformations until it is an elegantly coded system.

### Definitions of Clean Code ###

#### Bjarne Stroustrup ####
  * > code should be elegant and efficient
    * elegant = pleasing to read
  * > logic should be straightforward to make it hard for bugs to hide,

  * > the dependencies minimal to ease maintenance,

  * > error handling complete according to an articulated strategy, and
    * clean code exhibits close attention to detail
  * > performance close to optimal so as not to tempt people to make the code messy with unprincipled optimizations
    * Bad code tempts the mess to grow
  * > **Clean code does one thing well.**
    * Bad code has muddled intent and ambiguity of purpose
    * Clean code is focused


#### Grady Booch ####
  * > Clean code is simple and direct.

  * > reads like well-written prose

  * > never obscures the designer’s intent

  * > is full of crisp abstractions and straightforward lines of control
    * "crisp abstractions" oxymoron:
      * crisp =  briskly decisive and matter-of-fact; nearly a synonym for concrete
    * code should be matter-of-fact

#### Dave Thomas ####
  * > can be read, and enhanced by a developer other than its original author
    * clean code makes it easy for other people to enhance it
  * > has unit and acceptance tests

  * > has meaningful names

  * > has minimal dependencies

  * > should be literate since not all necessary information can be expressed clearly in code alone
    * soft reference to Knuth’s literate programming
      * > combines a programming language with a documentation language
    * code should be composed in such a form as to make it readable by humans

#### Michael Feathers ####
  * > looks like it was written by someone who cares

  * > nothing obvious that you can do to make it better

#### Ron Jeffries ####
  * > Runs all the tests;

  * > Contains no duplication;

  * > Expresses all the design ideas that are in the system;

  * > Minimizes the number of entities such as classes, methods

#### Ward Cunningham ####
  * > routine you read turns out to be pretty much what you expected
    * Programs that are that clean are so profoundly well written that you don’t even notice it. 
    * the designer makes it look ridiculously simple like all exceptional designs.
  * > beautiful code when the code also makes it look like the language was made for the problem

### WE ARE AUTHORS ###
  * The `@author` field of Javadoc tells us who we are
  * > ***The next time you write a line of code, remember you are an author, writing for readers who will judge your effort***
  * Ratio of time spent reading v. writing is at least 10:1
  * Prioritise writing well to make reading easier, than writing quicker and just getting it done
  * This logic is absolute and there's no getting around it

### The Boy scout Rule ###
  > Leave the campground cleaner than you found it.5
  * It doesn't have to be a big cleanup, it can be something as small as replacing a given variable with a clearer variable name
  * *Continuous improvement is an intrinsic part of professionalism*

# Clean Code Ch-02: Meaningful Names #
  1. *Use intention revealing names*
    * choosing a good name takes time, but it's worth it
    * makes reading easier. Remeber the 10:1 ratio

  2. *Avoid Disinformation*
    * don't leave false clues that obscure the meaning of code
    1. don't use well-recognised abbreviations as variable names (e.g. `hp` for hypotenuse; `hp` refers to a platform)
    2. don't encode types in name (e.g. `accountList` is bad, even if it is a list, especially if it is not; `accountGroup` or `bunchOfAccounts` is better)
    3. don't use similar variable names (that vary by very little)

  3. *Make Meaningful Distinctions*
    * don't write code that just *works* or *compiles*
    * > not sufficient to add number series or noise words, even though the compiler is satisfied. If names must be different, then they should also mean something
    * Number-series naming (`a1`, `a2`, ... `aN`) is disinformative and pointless: they do not provide any clue to the author's intention
    * don't use "Noise words" e.g. class `Product`, `ProductInfo` and `ProductData` mean essentially the same: `Info` and `Data` are noise words

  4. *Use Pronounceable Names*
  5. *Use Searchable Names*
    * longer names trump shorter names, and any searchable name trumps a constant in code.
    * single-letter names can ONLY be used as local variables inside short methods
    * if a variable/constant is used multiple times, make its name searchable
  6. Avoid Encoding 
    * Don't use the hungarian notation -- which encodes the type in the var name; this worked with primitive compilers. no need for java
    * Don't prefix variable names. KISS
  7. Interfaces and Implementations
    * If you must name a concrete class by its implementation interface, use the `Template` for the interface and `TemplateImp` for the concrete class
  8. Avoid Mental Mapping
    * you shouldn't have to mentally translate what a var name means. the name should be self explanatory
    * clarity is king. Write code that you don't have to explain to people
  9. Class Names
    * should be noun / noun phrases e.g. `Customer`, `WikiPage`, `Account` et c.
    * A class name should **not** be a verb
  10. Method Names
    * should be verb/ verb phrases e.g. `postPayment`, `deletePage`, or `save`
    * Accessors, mutators and predicates should be prefixed with `get`, `set`, and `is` according to the java standard
    * When constructors are overloaded, use static factory methods with names that describe the argument
      > `Complex fulcrumPoint = Complex.FromRealNumber(23.0);`

  instead of 
      > `Complex fulcrumPoint = new Complex(23.0);`
  11. Don't be cute
    * If you use clever names, only people who understand the reference will find it memorable; to the rest it's wtf
    * avoid colloquialism / slang / culture-dependent jokes
  12. Pick one word per concept
    * Don't use "fetch", "get", "retrieve" to refer to the same concept
  13. Don't pun
    * Don't use the same word in different contexts just because it's funny or to overdo consistency
    * If you have a lot of methods prefixed with `add`, then you should use `insert` if
    * Rule of thumb: if the methods are semantically equivalent (similar structure for return values/params), all's good
    * 




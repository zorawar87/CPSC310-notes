<details>
<summary>Lecture 02</summary>

# Lecture 02 #
## Software Development ##
  * Process of creating and maintaining software
  * typical phases
    * understand the problem & gather requirements
    * design the solution
    * implement it
    * test
    * deploy
    * maintain

## Software Development Methodologies ##
  * Dictates how the development phases is executed in practice
  1. Waterfall 
  2. Agile

### Waterfall (a.k.a traditional) Methodology ###
  * focuses on a linear, top to bottom development
  * sequential, non-iterative process in which progress is seen as flowing steadily downwards through phases
    1. Problem Statement
    2. Analysis
    3. Design
    4. Implementation 
    5. Testing
    6. Deployment
    
#### Limitations of Waterfall ####
  * Does not accommodate Change in design. 
  * If all features are not accounted for during the design phase, then it's game over

### Agile Methodology ###
  * based on iterative and incremental development
  * Dev cycle is the same that of Waterfall, except that it is iterative -- i.e. the process repeats
  * follows the agile manifesto
  * Is collaborative and client focused
    * client is involved throughout the development because they are the ultimate source of information
    * client guides the project
  * Improvements with each iteration
  * Focus on Minimum Viable Products (MVPs) over short periods of time
  * Backlog to keep track of features and requirements
  * promote sustainable development

#### Agile Manifesto Principles ####
  * Regular Delivery of Software
    * "Working software over comprehensive documentation" (#2)
    * Deliver working software frequently and regularly
    * Working software is the primary measure of success
    * satisfy the customer through early and continuous delivery of MVPs
  * Team Communication
    * "Individuals and and interactions over processes and tools" (#1)
    * "Customer collaboration over contract negotiation" (#3)
    * business people and developers must work together daily throughout the project
    * convey information to and within the team face to face. it's the most effective way
    * regularly reflect on how to become more effective and tweak behaviour accordingly.
    * build projects around motivated individuals. give them the env and trust to get the job done
  * Design Excellence
    * "Responding to change over following a plan" (#4)
    * continuous attention to the technical excellence and good design enhances agility
    * Simplicity is essential
      * Simplicity = art of maximising the amount of work not done
    * be open to changing requirements, even late in development

### Show down ###
Waterfall                                | Agile
-----------------------------------------|--------------------------------------
\+ Easy learning curve                   | + Adaptability and flexibility
\+ Clear Deadlines                       | + Immediate user feedback
\+ Well-defined milestones               | + Test driven development
\+ Requires stability                    | + Teamwork
\+ Predictable, and Easy to manage time  | - Unpredictable time-line
\- Very low flexibility                  | - High commitment 
\- Requirements must be known at start   | - Skill dependent teams  
\- Tendency to neglect testing           | - Tendency to neglect documentation


## Scrum (implements the Agile Framework)  ##
  * lightweight, people-centric framework for organising and managing work

### Scrum Roles ###
  * Product Owner
    * knows the product; communicates what the client wants
  * Scrum Master
    * project manager
  * Development Team
    * people who get the work done
### Scrum Activities ###
### Artifacts  ###
  * Product Backlog
  * Scrum Backlog
  * Potentially Shippable Product
</details>

-------

<details>
<summary>Lecture 03</summary>

# Lecture 03 #
## Software Design ##
  * *process* in which a **blueprint** is developed from which we can construct a software artifact
  * *process* of **defining** the architecture, components, interfaces and other **characteristics of a system**, and its result
  * i.e. understand the problem, design a solution, implement the solution

## Software Design Goals ##
  * Reliability
    * each component of the app should be responsible for a specific property an behaviour
    * supports validation and testing
      * does it do what it should?
      * is it done correctly and robustly?
        * Correct = produces correct answer
        * Robust = is correct regardless of the input; deals with a variety of inputs and unexpected errors
  * Re-usability
    * components are modular and independent
    * takes advantage of existing code libraries
    * supports timely production of large-scale software
  * Extensibility
    * components can be changed and added
    * supports maintenance and evolution of software
  * Flexibility
    * modifications can be made without affecting many components

### Object Oriented Programming ###
  * supports all the aforementioned goals
  * all about classes and objects
    * classes: blueprint for objects defined what an object can store and do
    * objects: instance of a class

#### Object-Oriented Principles (mnemonic: A PIE) ####
  * Abstraction 
    * extracting relevant features and removing what is unnecessary
    * allows modeling and representing objects in the simplest manner
    * GOAL: simplify the description of an object to its essentials
  * Encapsulation
    * binding certain features together in order to hide and protect them
  * Inheritance
    * allows a new class to be defined based upon an existing class
    * creates a parent/super-child/sub class relationship
    * *is a* relationship between parent and child
  * Polymorphism
    * lit. "many forms"
    * allows performing the behaviour corresponding with the type of what we're working with
    * brings flexibility; we can do the right thing at the right time

## From Problem to Solution ##
  1. Gather your requirements
    * What should the software do?
  2. Describe the solution
    * How do users use this solution?
  3. Identify the most important objects
    * What classes do we need?
  4. Identify the interactions between objects
    * What responsibilities and behaviours do we need?
  5. Create a class diagram
    * Visual rep of classes

### Gathering Requirements ###
  * *Functional Requirements*: What does it do?
    * Features and capabilities
    * must-haves over nice-to-haves
    * E.G: 
      * Customer must be able to see their balance
      * Customer must be able to pay their bill online
      * Customer must be able to open a new account online
  * *Non-functional Requirements*: Other
    * Help, documentation, performance, support
    * E.G:
      * Customer must be able to load page in under 5 seconds
      * Customer data must be encrypted to comply with ... 
      * Server must have a 99% up-time 

#### FURPS / FURPS+ ####
represents a model for classifying software quality attributes
  * **F**unctional: features, capabilities, security
  * **U**sability: human factors, help, documentation
  * **R**eliability: frequency of failure, recover-ability
  * **P**erformance: speed, resource consumption, throughput, scalability
  * **S**upportability: adaptability, maintainability, internationalisation, repair speed
  * **+** more requirements
</details>

-----

<details>
<summary>Lecture 04</summary>

# Lecture 04 #
## From Requirements to solution ##
Once we know what the functional requirements are, we need to describe the system from the user's PoV.

Agile approach advocates for user-centric design and process

### Use Cases ###
  * defines the interactions between actors and the system to accomplish a goal
  * can get very long, complex and tedious to create; in such a case it is not agile

### User Stories ###
  * informal description of one or more features of a software system
  * written in plain English
  * expresses a relatively small feature
  * intentionally kept short and simple
  * Note: Epic is  very large user story/user activity that needs to be broken down into user *stories*
  * *Cards, Conversation, Confirmation* (The Three C's of User Stories)
    * Cards: written on physical cards 
    * Conversation: discussed at different times and places throughout the project; often verbal
    * Confirmation: specific requirements to confirm that a feature expressed in a user story is properly completed
  * Follows the format: *As a* **(role)**, *I want* **(something)** *so that* **(benefit)**
    * *As a* student, *I want* to log into Moodle *so that* I can view lecture notes
    * *As a* shopper, *I want* to add items to a wish list *so that* I can purchase them later on.
    
#### Story mapping ####
  * Arranging user stories into a useful model to understand and outline the functionality of the system
  * *user story map* gives an overview of the system and is a useful tool for planning:
    * visually represent the product backlog
    * Identify the MVP
    * identify the potential product releases

#### Acceptance Criteria ####
  * defines the boundaries for user stories (features) and specify the requirements that must be met for a user story to be considered completed and working as expected
  * should be developed alongside user stories to reduce surprises late on and give a better idea of when a project can be considered complete
  * follows the format: *Given* **(precondition)** *When* **(do some action)** *Then* **(expect some result)**
    * *Given* that a wish list is empty *When* a shopper adds a new item *Then* the list should contain 1 item.

</details>

-----

<details>
<summary>Lecture 05</summary>
 
# Lecture 05 #

## From User Stories to Conceptual Model ## 
From the user story, identify:
  * different components i.e. classes 
    * nouns i.e. objects in the user story will correspond to a class
  * different behaviours i.e. class responsibilities
    * action verbs; assign responsibilities to identified classes (nouns)
    * these will become class methods
    * *pay close attention to what class takes what responsibility.
This needs thought*
      * often certain objects will initiate the behaviour, but they shouldn't be _doing_ the job
    * ***DESIGN PRINCIPLE***: An object should always be responsible for itself
      * "Tell don't ask"
        * tell objects to do things, don't query their internal state and make a decision yourself
    * It's easy to overload an object with a lot of responsibilities and create a *God object*
      * an all encompassing "system" object that takes on all behaviours
  * different interactions i.e. class collaborators
    * identify how objects interact
    * Class responsibility collaboration (CRC) Cards
      * top section: Class Name
      * Bottom left: Responsibilities
      * Bottom right: Collaborations
</details>

-----

<details>
<summary>Lecture 06</summary>
 
# Lecture 06 #

## Object Relationship ## 
  * Inheritance : *is-a* relationship
  * Composition : *has-a* relationship
  
## Inheritance ##
  * a subclass inherits everything from the super-class except for the
constructors
  * explicitly invoke `super()` to call the super's constructor
  * sub-classes may:
    * override existing behaviour
    * extend by providing new methods and fields

## Polymorphism ##
  * Ability of a reference variable to take different forms
  * can be assigned an instance of its class or any subclass
  * Up-casting (using a more general class) is automatic
  * Down-casting (using a more specific class) is manual
  ```java
    Person person1 = student1;  //automatically upcasted to person
    Student student2 = (Student) person1;  //manual downcasting to student
  ```

### Dynamic Dispatch ###
  * checks object's fields/behaviours against that of the variable type
</details>

-----

<details>
<summary>Lecture 07</summary>
 
# Lecture 07 #

## Interfaces ##
  * collection of method signatures with no data or bodies
  * form a contract between the class and the outside world
  * NAMING:
    * adjectives ending with *-able* or *-ible* if they provide a capability
    * nouns otherwise

## Abstract Classes ##
  * may or may not include abstract methods
    * method declared without an implementation
  * cannot be instantiated but can be sub-classed
  * generic enough to allow for specific implementation in sub-classes

Interfaces | Abstract Classes
-----------|-----------------
Extend only one class a time | Extend any number of interfaces at a time
Extend a concrete or or abstract class | only extend another interface
Have both abstract and concrete methods | only have abstract methods
use any access modifiers | only use public (not protected | private)
have use static, final, or static final variables | only use [public static final cont variable

Implementation inheritance (sub-classing) | Interface inheritance (sub-typing)
-----------------------------------------|--------------------------------------
subclass inherits behaviors and its implementation from the base class | subclass inherits the description of behaviour from the base class and provides the implementation itself
defines an object's implementation in terms of another object's implementation   | described when an object can be used in place of another
</details>

-----

<details>
<summary>Lecture 08</summary>
 
# Lecture 08 #

## Fragile Class Problem ##
the super classes are considered "fragile" because seemingly safe
modifications to a base class, when inherited by the derived clases,
may cause the derived class to malfunction.
  * You cannot easily determine whether a base class change is safe
simply by examining it in isolation

## Inheritance Issues ##
Inheritance tends to create a **high/tight coupling**
i.e.  subclasses are highly dependent on the base classes
  * white-box reuse, when the internals are exposed, breaks encapsulation

"Inheritance exposes a subclass to details of its parent's implementation so,
'inheritance breaks encapsulation'" (GoF)

## Composition and Aggregation ##
[Association  [Aggregation  [Composition  ]]]

### Association ###
  * No ownership. no lifetime dependency

### Aggregation ###
  * One parent instance. no lifetime dependency
  * *has-a* relationship
  * implies that objects can survive separately
    * `Student` and `Course`
    * `Student` can have a `Course` within it, or `Course` can have `Student`s within it.
    * just because the course is over, doesn't mean that the student stops existing
    * doesn't mean that when a course is created, then a student must be created too -- the student could've existed before
    * there is a directional association, but we imply no lifetime dependency

### Composition ###
  * one parent instance. lifetime of child depends on parent

Using an instance variable that references to other objects
  * *part-of* relationship
  * an object is *composed* of other object
  * implies that objects cannot survive separately
    * `Cat` and `Tail`
    * `Tail` must be created when `Cat` is, and when `Cat` dies, then `Tail` does too
    * they are tightly coupled

## Design Principles ##
  1. High cohesion, low coupling
  2. Encapsulate what varies
  3. Favour composition over inheritance
  4. Program to interfaces, not implementation

### Inheritance v. Composition ###
#### Benefits of Inheritance ####
  1. Polymorphism and dynamic binding (dispatch) make code easier to change
  2. new implementations or similar things are easy
  3. naturally expresses `ChildObject` *is a special kind of* `ParentObject`

#### Benefits of Composition ####
  1. Black-box reuse
  2. emulate multiple inheritance
  3. reuse only necessary behaviours
  4. control the visibility of the compoosed object

## UML ##
</details>

-----

<details>
<summary>Lecture 09</summary>
 
# Lecture 09 #

SimUDuck Application. Refer to `hf-design-patterns.md:Ch-01`.

</details>

-----

<details>
<summary>Lecture 10</summary>
 
# Lecture 10 #

Rick's Guitar Inventory homework discussion.

</details>

-----

<details>
<summary>Lecture 11</summary>
 
# Lecture 11 #

## Clean Code ##
Refer to `clean-code.md:Ch-01`

## Code Smell ##
surface indication that usually corresponds to a deeper problem in the system
  * not necessarily bugs; corresponding code may work fine 
  * symptoms of poor design and implementation choices

## Refactoring ##
  * change to the internal structure of software to make it easier to unstand and cheaper to modify without changing observable behaviour
### When to Refactor ###
REMEMBER THE BOYSCOUT RULE
  * on adding/changing functionality
  * after fixing bugs
  * when code smells

### How to Refactor ###
  * make sure all tests that passed before, passed after
  * improve the code
  * repeat until code smell is gon

## SOLID ##
  * **S**RP - Single Responsibility Principle
    * A class should have only one reason to change
    * do one thing, and do it well; no God objects
    * reinforces: *an object should be responsible for itself*
    * Violations of SRP:
      * "Change once, break everywhere"
      * can't unit test easily
  * **O**CP - Open/Closed Principle
    * classes should be open for extension but closed for modification
    * add new features through inheritance; think of plugins and extensions
    * should not have to change existing classes, except for bug fixes
  * **L**SP - Liskov Substitution Principle
    * a superclass may be replaced by its subclasses
    * ensures that every subclass follows the contract defined by its superclass
    * subclass must provide support for all behaviour supported by the super class
  * **I**SP - Interface Segregation Principle
    * many specific interfaces are better than one general purpose interface
    * prevents "God" interfaces
    * makes it easier to extend or specialize parts of the system
  * **D**IP - Dependency Inversion Principle
    * high-level modules should not depend on low-level modules. Both should depend on abstractions.
    * abstractions should not depend on details. the converse should be true

## Design Principles ##
  * DRY: Don't repeat yourself
  * YAGNI: You aren't gonna need it
    * avoid features that might come in use some day, but not now
  * KISS
</details>

-----

<details>
<summary>Lecture 12</summary>
 
# Lecture 12 #

## Code Smells ##
  1. The Bloaters
    Bloater smells represents something that has grown so large that it cannot be effectively handled
    * Long method
    * Large class
    * Data clumps
    * Long parameter list
    * Primitive obsession
  2. The Tool Abusers
    the solution does not fully exploit the possibilities of object-oriented design
    * Switch statements 
      * using switch based on type, rather than polymorphosising
    * Refused Bequest (legacy)
      * not following the superclass's constraints
      * Violation of LSP
  3. The Change Preventers
    * divergent change
      * changing one section causes multiple (divergent) changed results
      * Violation of SRP
    * shotgun surgery
      * class is not responsible for itself; changing one part breaks another
    * parallel inheritance hierarchies
  4. The Dispensibles
    * Lazy Class
      * doesn't do much work. just is there.
    * Speculative Generality
    * Data Class
      * that mimics a data structure; does not have any context specific behaviours, only basic data-structure related methods
    * Duplicated Code
    * Dead Code
  5. The Couplers
    * feature envy
      * one class repeatedly accesses methods of another class. should probably get a hold of itself
      * class wishes it has the access/behaviours of the other class
    * inappropriate intimacy
      * classes know more about each other than they should
    * message chains
    * middle man
      * an empty middleman between two classes, doesn't do anything else
    * indecent exposure
      * things that should be private/protected are public
      * creates high coupling

## Meaningful Names ##
Refer to `clean-code.md`
</details>

-----

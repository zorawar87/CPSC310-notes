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
  * written in plain english
  * expresses a realtively small feature
  * intentionally kept short and simple
  * Note: Epic is  very large user story/user activity that needs to be broken down into user *stories*
  * *Cards, Conversation, Confirmation* (The Three C's of User Stories)
    * Cards: written on physical cards 
    * Conversation: discussed at different times and places throughout the project; often verbal
    * Confirmation: specific requirements to confirm that a feature expressed in a user story is properly completed
  * Follows the format: *As a* **(role)**, *I want* **(something)** *so that* **(benefit)**
    * *As a* student, *I want* to log into Moodle *so that* I can view lecture notes
    * *As a* shopper, *I want* to add items to a wishlist *so that* I can purchase them later on.
    
#### Story mapping ####
  * Arranging user stories into a useful model to understand and outline the functionality of the system
  * *user story map* gives an overview of the system and is a useful tool for planning:
    * visually represnt the product backlog
    * Identify the MVP
    * identify the potential product releases

#### Acceptance Criteria ####
  * defines the boundaries for user stories (features) and specify the reqruirements that must be met for a user story to be considered completed and working as expected
  * should be developed alongside user stories to reduce surprises late on and give a better idea of when a project can be considered complete
  * follows the format: *Given* **(precondition)** *When* **(do some action)** *Then* **(expect some result)**
    * *Given* that a wishlist is empty *When* a shopper adds a new item *Then* the list should contain 1 item.

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
    * *pay close attention to what class takes what responsibility. This needs thought*
      * often certain objects will initiate the behaviour, but they shuooldn't be _doing_ the job
    * ***DESIGN PRINCIPLE***: An object should always be responsible for itself
      * "Tell don't ask"
        * tell objects to do things, don't query their internal state and make a decision yourself
    * It's easy to overload an object with a lot of responsibilites and create a *God object*
      * an all encompassing "system" obejct that takes on all behaviours
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
  * a subclass inherits everything from the superclass except fo the constructors
  * explicitly invke `super()` to call the super's constructor
  * subclasses may:
    * override existing behaviour
    * extend by providing new methods and fields

## Polymorphism ##
  * Ability of a reference variable to take different forms
  * can be assigned an instance of its class or any subclass
  * Upcasting (using a more general class) is automatic
  * Downcasting (using a more specific class) is manual
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
  * form a contract bw the class and the outside world
  * NAMING:
    * adjectives ending with *-able* or *-ible* if they provide a capability
    * nouns otherwise

## Abstract Classes ##
  * may or may not include abstract methods
    * method declared without an implementation
  * cannot be instantiated but can be subclassed
  * generic enough to allow for specific implementation in subclasses

Interfaces | Abstract Classes
-----------|-----------------
Extend only one class a time | Extend any number of interfaces at a time
Extend a concrete or or abstract class | only extend another interface
Have both abstract and concrete methods | only have abstract methods
use any access modifiers | only use public (not protected | private)
have use static, final, or static final variables | only use [public static final cont variable

Implementation inheritance (subclassing) | Interface inheritance (subtyping)
-----------------------------------------|--------------------------------------
subclass inherits behaviors and its implementation from the base class | subclass inherits the description of behaviour from the base class and provides the implementation itself
defines an object's implementation in terms of another object's implementation   | described when an object can be used in place of another
</details>

-----

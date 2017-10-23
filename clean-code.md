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
      ```java
        Complex fulcrumPoint = Complex.FromRealNumber(23.0);
      ```

      instead of
      
      ```java
        Complex fulcrumPoint = new Complex(23.0);
      ```

  11. Don't be cute
    * If you use clever names, only people who understand the reference will find it memorable; to the rest it's wtf
    * avoid colloquialism / slang / culture-dependent jokes
  12. Pick one word per concept
    * Don't use "fetch", "get", "retrieve" to refer to the same concept
  13. Don't pun
    * Don't use the same word in different contexts just because it's funny or to overdo consistency
    * If you have a lot of methods prefixed with `add`, then you should use `insert` if
    * Rule of thumb: if the methods are semantically equivalent (similar structure for return values/params), all's good
  14. Use Solution Domain Names
    * Use technical terms because you can assume other people reading source code are programmers. You can use algorithm names,
      CS Terms et c.
  15. Use Problem Domain Names
    * If you can't find a name that comes from the solution set, use a term from the specific problem
  16. Prefix to provide context, if all else fails


### Takeaways ###
  * Don't be afraid to change the name, if it's bad. Your team will thank you.
  * People don't remember each and every variable and stuff. If change it within reason, your team will be as surprised as they would wth a good code improvement
  * Don’t be afraid to make a name long.  A long descriptive name is better than a long descriptive comment.
  * Don’t be afraid to spend time choosing a name

# Clean Code Ch-03: Functions #

### Basics ###
  * Functions should be small. Like really small. Upto 20 lines is good.
  * One level of abstraction per function
  * Stepdown rule: functions should be followed by those at the next level of abstraction so the program reads top-down
  * ***Do one thing only, and do it well***

### Stuff within fns ###
  * Code blocks (conditionals, loops) should be one line long --- probably a function call; at most two nested indents
  * this implies that functions should not be large enough to hold nested structures.
  * If you must use a **switch**, then make sure you aren't switching types. Polymorphise for that. Use switch for N values.

### Fn Args ###
  * Ideal # of function args is zero. More than 3 means you need to rethink
  * Monadic Function (One param)
    * Used to  ask a question about that argument and return something e.g. `boolean fileExists("MyFile")`
    * Used to transform the arg object and return it e.g. `InputStream fileOpen("MyFile")`
    * As an event that the program uses to alter its state and return nothing e.g. `void passwordAttemptFailedNtimes(int attempts)`
    * AVOID other forms
    * Flag Arguments
      * if you pass a boolean to a function, you're function does too much. Don't.
  * Dyadic and Triadic Functions are significantly harder to understand so use them carefully
  * Polyadic Functions
    * More than two or three args means that you can wrap it in a class of its own
  * Arg list
    * Arg lists (`Obj... name`) are treated as a single param
    * So `printf(String, Obj... name)` is dyadic

### General Rules  ###
  * Command Query Separation: Either do someting, or answer something. not both.
  * Prefer Exceptions to Error codes. Error codes require nested structures. This also violates CQS.
  * Extract the contents of a try catch blocks into their own function. Throwing an exception is one thing; error processing is its own.
  * Error handling is one thing. A function that handles errors should not do anything else.

### Structured Programming ###
  * Rules by Edsger Dijkstra
  > Every function, and every block within a function, should have one entry and one exit. 
  
  * Implication: There should be only one `return` statement in a fn, no `break` or `continue` statements in a loop, and no `goto` statements

  
# Clean Code Ch-04: Comments #
  * If you fail to express it in code, you use a comment.
  * Don't use comments to makeup for bad code. Rewrite bad code.
  * Explain yourself in code
    ```java
      // Check to see if the employee is eligible for full benefits
      if ((employee.flags & HOURLY_FLAG) && (employee.age > 65)) 
    ```
  
    instead of
    
    ```java
      if (employee.isEligibleForFullBenefits())
    ```

### Good Comments ###
  * Legal Comments
    * Talk about Copyright, License, Release Terms et c.
    * go at the top of the source code
  * Informative Comments
    * basic information about the structure --- but it should be done with the structure name 
    * Explaining some specificity e.g. 
      ```java
        // format matched kk:mm:ss EEE, MMM dd, yyyy
        Pattern timeMatcher = Pattern.compile("\\d*:\\d*:\\d* \\w*, \\w* \\d*, \\d*");
      ```
  * Explanation of Intent
    * explains the intent behind a decision -- "why was this implemented this way?"
  * Clarification 
    * translate the meaning of some obscure argument or return value into something that’s readable
  * Warning of Consequences
    * Warns of some unexpected or undesirable consequence 
  * TODO Comments
  * Amplification --- to make something that might seem inconsequential more pronounced
  * JavaDoc

### Bad Comments ###
  * Mumbling Comments: If you're writing a comment, write a good one;
  * Redundant Comments: Useless JavaDoc, hard to read comments
  * Misleading Comments
  * Mandated Comments: Not every function requires a javadoc 
  * Journaled Commments: Writing a changelog within the file. 
  * Noise Comments: "Default Constructor", "The day of the month" for `int dayOfMonth`
  * Closing Brace Comments
  * Commented out code
  * HTML Comments

# Clean Code Ch-05: Formatting #
  * Just fucking format within reason

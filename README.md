## Human Design notes

### Hypothesis

Code is a product that has to be designed for usability, but we don't see it as a product for [probably lots of reasons].  Use human psychological studies to drive the design decisions we should make, like UX and information designers do.  Focus on the human.

### Complex Systems Are Everywhere

Time and time again, systems are built that are complex, difficult to scale, difficult to change languages in, don't handle failure well, don't change from web to background well, etc.

The tools and languages we use have limited complexity.  It's not until developers implement a system does it get complicated.

There are drastically more systems where the engineers will say "it's in dire need of refactoring/rewrite" vs. "we have an otherwise clean and maintainable system".  Dissatisfaction is the norm.

"every software problem is really a people problem" seems to make sense?

### Is Human Error To Blame For Bad Software?

Humans write the software, and design the systems.  It's common to hear the phrase "it is a people problem" https://blog.codinghorror.com/no-matter-what-they-tell-you-its-a-people-problem/

In "The Field Guide to Understanding Human Error", "human error" is a cop-out that doesn't really explain why error occured.  Though this is an essay in how humans commit error in systems, as opposed to creating the systems themselves.

"...errors are symptoms of trouble deeper inside a system.  Errors are the other side of people trying to persue success in an uncertain, resource constrained world." loc 267

"Or you can see human error as a symptom of trouble in a system that is not basically safe."

"Error is a starting point, not a conclusion."

"Human error is not random.  It is systematically connected to features of people's tool, tasks and operating environment." 460

errors committed by humans is variable, and a measure of system complexity.  The more errors humans make, the more complex the system.

In building systems from scratch, the complexity of the resulting system is a direct relationship with how well the the tools, processes and environment used facilitated that end result.

Viewing our systems now, we will take the viewpoint that the people building them are otherwise reliable and competent.

### What are the error-producing conditions we face?

Focus on the human -- their ability to understand, and make change.  A good example is to just have forwarding from conduit to beehive.  Then you minimize the amount of files you need to explicitly change, and there is just one source of truth for the API.

For example, light-service is structured for understanding of behavior.  But what about understanding performance?  Or safety/security of testing?

### Hindsight Bias

Hindsight bias is interesting.  We often look at code and say "What were they thinking?!"  Obviously, looking at the code after it has been developed, it is much easier to pick apart the design than if you had a blank slate and designed it from scratch.  What influenced the person to write the code that way initially?  A new language/framework?  Not realizing what changes will have to take place later in time?  What pressures did they face in getting it done, and with what technologies?

Thinking about this as a way to structure constraints per level of employee:
Dreyfus model of skill acquisition: https://en.wikipedia.org/wiki/Dreyfus_model_of_skill_acquisition

### Depth of No Greater than 3

http://www.eurekalert.org/pub_releases/2005-03/aps-hmc030805.php

study shows that humans can only keep track of about 3 things reliably.  By the 4th, performance degrades considerably.

This also means that you can have a large breadth to the design, so long as each step has a depth limit of 3.

This doesn't mean you should aim for 3.  Aim to have as little depth as possible, and favor breadth over depth.  Breadth means explicitness, depth is hidden knowledge that has to be searched for.

### Conway's Law

https://en.wikipedia.org/wiki/Conway%27s_law

"organizations which design systems ... are constrained to produce designs which are copies of the communication structures of these organizations"

From https://www.thoughtworks.com/insights/blog/demystifying-conways-law

> In "Exploring the Duality between Product and Organizational Architectures", a study by The Harvard Business School carried out an analysis of different codebases to see if they could prove Conway’s original hypothesis as applied to software systems. In it, they took multiple examples of software created to solve the same purpose (for example word processing, financial management and database software), and compared the code bases created by loosely-coupled open source teams, and those created by tightly-coupled teams. Their study found that the often co-located, focused product teams created software that tended more towards tightly-coupled, monolithic codebases. Whereas the open source projects resulted in more modular, decomposed code bases.

He later discusses how microservices give organizations the ability to mirror their architectures to their team structures.

From http://www.addsimplicity.com/adding_simplicity_an_engi/2010/11/conways-law.html

He argues to structure your teams first, then build the infrastructure.  So before you start building, decide on a good communication and team structure that is cohesive to developing the architecture.

### The design is the user interface

https://medium.com/@mbostock/what-makes-software-good-943557f8a488#.xvjyqkdr2

While developers are writing code to sell as a product.  The code itself is a product for other developers, though they often don't have a choice in whether to purchase the product.

### Keep Things Small

In "Rules" by Sandi Metz (https://www.youtube.com/watch?v=npOGOmkxuio) she demonstrates how smaller objects are easier to understand for new developers, and give them more confidence when making changes. 

But there is a middle ground.  How small until the cost of abstraction impeeds understanding?

Fowler has the "This big" rule (from: https://www.youtube.com/watch?v=sAsRtZEGMMQ)

Both of these ideas have to do with the size of an object and doesn't address the composition of these objects for a use case.

### The Architecture Elevator Pitch

Can you completely explain your architecture in 30 seconds or less?

### Do usability testing

It is really interesting to see someone that hasn't seen code before talk through it, and voice their assumptions or understandings of what it does, and what questions they have.

UX designers do the same for their designs to get empirical feedback on how easy it is to use.  Do the same to gain insight into your designs.

### One Goal

Have one goal, and that goal can never be broken.  When I was doing work on orchestrators, the one goal that had to always be true is that behavior could never hide.  From a high-level, the code had to be WYSIWYG.  The depths is where danger lies.

### What not to do

Defining what you can't do, but everything else is fair game is much more empowering than saying only what you can do.

1. Do not have more than 50 lines of code in a single file
2. Do not have more than 3 nodes of call depth in a use case (breadth is fine)
3. Do not have anything that increases cyclomatic complexity below the first level of the tree (loops, conditionals, error handling, concurrency) -- need to prove this out
4. Do not keep code that when read by someone else, results in more than 3 questions
5. Do not commit to an architecture in which you can't explain in 30 seconds or less.

### Testing What not to do

1. Do not have more lines in your test file than your src file
2. Do not mock

### An Overview of Architectures

Layered Architecture

Hexagonal Architecture

Microservices and SoA

Lambda/Kappa Architecture; Kleppmans ideas; streaming or batch processing architectures

### Constraints

Automated constraints will yield a significantly better codebase, and demonstrate rules for a high level architecture that responds to change of any kind: capacity, language, failure, or type of processing (from request-response to async to batch processing)

TODO research:

- hickey's talk about simplicity
- books on architecture
- becks four rules: http://martinfowler.com/bliki/BeckDesignRules.html
- blogs/papers from below and http://www.scielo.cl/pdf/arq/n49/art11.pdf
- built in constraints to languages, like haskell, golang's compiler, and eiffel: https://www.eiffel.org/doc/eiffel/ET%3A%20General%20Properties

http://www.ibm.com/developerworks/rational/library/collaborative-design-management/

- check for tree structure/dependency chains.  Could simply count the number of files you have to open to understand how a feature works.
- rules
- contracts constraints
- articulate how you look at/analyze code and see if some sort of standardizations could occur/rulification

really interesting to see the kpis and dependency spreadsheet from attila.  The dependency spreadsheet, and maybe some other visual way to see the architecture, and break it down into layers, or what segment talks with which other one, and the dependency flow.  The spread sheet is simple, fast and obvious vs. some tool

so: 
- decide on KPIs for your project immediately, like a business
- have consistency in architecture
- what conventions should be used to ensure better naming?

### Things that should be constraints

https://github.com/bbatsov/rubocop/blob/master/config/default.yml

- style (like string and hash styles in rubocop)
- class and method size
- ABC metrics/Complexity Metrics
- performance 

These are all in the following categories:

- simpler code
- more performant code

What areas of software are we missing that add to complexity?

### Idiom vs Constraint

Idiom/convention is not explicitly forced.  Constraints cannot be avoided.

### Don't drink the kool-aid

Is it possible that constraints will result in impractical working conditions?

Are there such a thing as bad constraints?  Who decides on the constraints?

### Humans are failure prone

Prove that humans are the most failure-prone part of the development cycle.  Studies that show humans make mistakes when tired, hungry, angry, happy, pretty much any emotional state.  That humans are prideful (working with others), or commonly fail to see things from another's perspective (when writing their code for others to consume) or handle complex systems poorly (software is complex), and that humans are easily swayed from opinion to opinion, and every person is different depending on nature and nurture.

Then, if humans are the most failure prone component, by having tools that reduce human error, we have better products.

If failure is caused by complexity, then constraints aim to keep a system as simple as possible for as long as possible.  (And this could also mean to keep your constraints simple, too)

http://web.mit.edu/2.75/resources/random/How%20Complex%20Systems%20Fail.pdf

https://www.mnot.net/blog/2007/05/10/eames -- design is the sum of constraints

Example of constraints in languages: static typing vs dynamic typing; erlang forces you to define the function and airity of any public function (interfaces); Ruby!...well, ruby let’s you do anything so I don’t have much to say there).  Erlang’s decision to not have else since catchalls are harder to read (loc 1226 in learn you some)

The closer you can get to only one way to execute business logic, the better off the codebase will be.

Style guides: dive into style guides, which is one aspect of a constraint: https://github.com/bbatsov/ruby-style-guide

Another benefit: constraints teach.  Like learning more about ruby from rubocop.

Two questions I’d still like to answer:

How strict should the constraints be?   What should I constrain?  Examples of a properly constrained codebase?

Probably you want to add a constraint to the system from the very beginning of a convention being set.  The longer you wait, the more permutations of convention you will have.  Does this imply that you will have constraint driven development?  A different constraint driven convention per directory/module?

How do I know if my constraints are well-chosen?

Give examples of constraints you like to enforce.

Don’t drink the kool-aid:
It may be right to ignore constraints for spiking code.  Like in beehive and listing of the actions, ignoring rubocop is the right call.  Does that mean that our design should change to make applying automated constraints easier?
The constraint could be for some files that have a looser convention, a PR must be issued, anything that has a strong constraint over it can just be merged.

Another finding: constraints are a lot of work to write!  Probably could write a simple CoR app in ruby to deal with adding your own constraint framework easily, with built in gems?

basic constraints in...
- git (non-language specific constraints)
- design basics (module size) (language specific constraints)
- dialyzer (built-in tools)
- testing (non-language specific?)


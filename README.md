## Human Design notes

### Hypothesis

Code is a product.  Not just for the end set of features someone non-technical will use, but also for other developers.  The code itself is a product other developers use.

When viewed in this manner, how would our designs change if we applied the same strategies and disciplines that UX, interaction and product designers do when they design a product?

Story of going through a codebase and getting angry, even files we've been through before, or ramp-up taking a month.

Instead of design patterns, or previously experienced frameworks or tools, designs should be chosen because of psychological and behavorial research.

##### Following SOLID or DRY or Design Patterns without thought of human understanding is bad

Solve the root need -- human understanding and discoverability.

### Fundamental Principles of Interaction

Affordances, Signifiers, Mappings, Constraints, Feedback and Conceptual Models

##### Affordances 

are the possible interactions between the product and the environment.

##### Signifiers 

show what action is possible and how it can be done.

##### Feedback 

communicates the results of an action.  It must be immediate and pertinent.

##### Mapping 

is the relationship between two sets of things and describes the full set of operations that can occur. Devices are easy to use when the set of possible actions is visible, and when the controls exploit natural, spatial mappings.

##### Constraints 

limit the possible actions to simplify what needs to be held in memory and understood.

##### Conceptual models 

are simplified understandings of how the system works, and are either from previous use of something similar, or built from the	the perceived structure -- the signifiers, affordances, mappings and constraints.  An understanding of the relationship between the controls and the outcomes.

### Emotion

The subconsious/conscious mind and emotion

##### Emotion assigns value

Cognition provides understanding, emotion provides value (1195).

A large part of what we consider to be good software is based off of emotional, mostly subconscious value judgements.

#### How is emotion derived?

In three stages: visceral, behavorial and reflective

##### Emotion (thus value) are derived mostly subconsiously

Immediate perception triggers visceral responses -- so the physical characteristics drive immediate perception, and the precursor to emotion.  Nothing about usability, but all about attraction or repulsion.

Behavorial states are learned, and every action has an expectation, and the outcome impacts their emotions.  Bad emotions == less value.

The behavioral level is the home of interaction -- which means that based on previous experiences we have expectations with our interactions -- conceptual models.

Pattern matching: subconsious thought matches previously experienced patterns to the new situation.  It'll make predictions, trends, and is fast.

##### Our consious mind is heavily influenced by emotion

The reflective -- slow thinking -- evaluates the circumstances and assigns responsibility -- either praise or shame -- and makes predictions.  This state is the most protracted and the memories here last far longer.

##### Valuable software manages the emotions of the developer

"Understanding arises at a combination of the behavorial and reflective levels.  Enjoyment requires all three."

visceral -- immediate enjoyment; beauty (simplicity and order/heirarchy)  Can do this by focusing on uniformity of color and shape.

behavioral -- meets expectations -- expectations set from previous experiences and current signifiers and constraints and mappings

pay attention to initial reactions, then as they read it, what expections are experienced.

### Memory

Not much has to be remembered -- behavior can be guided by "knowledge in the world" -- which are constraints.  Arrange things so complete knowledge is unnecessary.

We only need sufficient knowledge to get the task at hand done.  The whole system need not be known.  This is done by using signifiers, constraints and natural (spatial) mappings.

"declarative knowledge" is the knowledge of facts and rules.  This is easy to teach and write.

##### STM (short term or working memory) can hold 3-5 items at a time

Think of them like pointers.  Normally it is 5-7, but for complex things 3-5 is the limit.  More like 3 for software.

##### LTM is unreliable and composed of fragments

We reconstruct long term memory in fragments, and compose them with a bias of our present condition, so it is unreliable.  It is also much slower than STM access.

##### Favor subconsious decision making by using conceptual models

Short term memory is small, yet most often used.  Conscious thinking takes time and effort, subconsious focuses on patterns and is much faster and easier -- more enjoyable.

If there is an initial investment of learning, then after it should allow unconsious control of the product.  There should be no re-learning, and minimize the need for consious reasoning.

You should just "know" exactly where things happen and how.

Use approximate or conceptual models to simplify the memory task.  If the story is consistent across the whole product, then the learning should be a one-time cost.

##### Limit the amount of information held in our short-term memory by using prospective, external memory

Prospective memory means the task of remembering to do some activity at a future time.  Memory for the future denotes planning abilities and the ability to imagine future scenarios.

Do not rely on your own memory for most things -- use notes, calendars, or recording services.

A reminder has a signal, and a message.  The signal tells that something is to be remembered, the message, the info itself.

Google, the "cybermind" makes our memory much stronger because all we have to know is how to access the information.

Knowing how to quickly access any information you need is incredibly valuable since our memories can't hold it all reliably.

The goal is to quickly and easily know what behavior is in the system, and where to find it.

##### Use constraints and mappings to limit options to choose

Make strong use of constraints to simplify what must be kept in memory, and choosing options.  Constraints should mix in with the conceptual model to limit the amount of actions to take when accomplishing a goal.

Semantic constraints rely upon the meaning of the situation to control the set of possible actions (like in production, you can only do 1 or 2 actions (or none))

Logical constraints -- like a puzzle or lego set -- you see a piece can fit in one place, so you put it there.  You don't understand the whole, but the constraints drive limited action.  This seems like a physical constraint as well.

There are also cultural constraints.

More include forcing functions: which are constraints where failure at one stage prevents the next stage from happening.

Interlocks forces operations to happen in a specific sequence. Like the microwave turning off before the door is allowed open.

Lock-ins keeps an operation active, preventing someone from prematurely stopping it. (nice in the ES drop case) like a "are you sure" before quitting.

Lockouts keeps someone out.  They are used for safety reasons.

##### The evaluate-action cycle: feedback is essential

Assume the system will sometimes not be clear or easy enough, or the human takes the wrong move.  Feedback must be utilized to quickly and easily tell the user the result and other information to make the evaluate-action cycle simple and enjoyable.  Error must be easy to recover from and correct.

We need fast turn around from a question -- this is true of memory loss as well.

##### Affordances, signifiers, mappings and constraints simplify encounters with everyday objects

They specify what to do and where to do it.

Affordances are the actions that are possible, but these are easily discoverable only if they are perceivable: perceived affordances.  The signfier component allows people to determine the possible actions.  Convention allows one to go from the perception of an affordance to understanding the potential action.

Signifiers are part of certain conventions, so when reused, people will just know.

So constrain everything in a uniform way: all the colors used, the words used, the logic structures -- there should really only be one option, and that option should be obvious and consistent with the conceptual model of the system.

### Basic human execution and the human design process

HCD (humand centered design) ensures people's needs are met, that the resulting product is understandable and usable, accomplishes the desired task, and that the experience is positive and enjoyable.

##### The bridge of execution and evaluation

We determine a goal, then how to accomplish the goal, then take the action.  After the action is taken, we need feedback to evaluate whether what we did accomplished the goal.  Then we either move on to another goal, or we swing back to figure out why the action we took didn't accomplish the task.

Gaps in this process are places to improve the design.

##### Ideation

Generate mass quantities of ideas for how to solve the problem.

##### Prototyping

The wizard of oz protoyping method: just building a cheap immitation -- the narrative and not implementing it.

##### Testing

Have someone use the prototype.  5 people is considered a good batch.

Have them openly discuss their ideas, hypothesis and frustrations openly and naturally.

##### Iterate

Make changes based on prototype testing.

Instead of using human error as a metric to assign blame, use it as a metric for complexity.

Also, use question counting as a metric for complexity.

----------

Limit the number of colors?  The types of words used?

On using external memory tools:

In software, structure code to easily be grepped, or acked.  Our own google.  Consider structuring code/naming conventions specifically to aid in searches.

Consider structuring our code like a table of contents or index or documentation-like heirarchy -- things were are already used to using to find information.

On affordances:

All possible interactions between the product and the environment.  The environment is not only the developer.  It is also the OS, and other external services.  A system is a user to another system.

Not only does a software product afford the normal use cases, but also affordances of performance, fault tolerance and failure, and of security.


# Ideas

In a new project:

TLDR; Know the first question, prototype to solve it, test it on a human, then move to the next set of questions, repeating the process until fully developed.

List the affordances of the program.  This includes:

- The API

- The different tools/features devs can use in their own feature development

Other questions:

- How to add a new feature (this begs more questions about testing, performance, fault tolerance and security)

- What to do when a new feature doesn't follow the existing design

Then prototype to solve those problems using the tools explained earlier, and the following principles from our study of human psychology:

For emotion:

- That humans have visceral reactions to beauty, so focus on uniformity of shape and color

- Keep in mind the conceptual model decided, and the expectations it raises while being read.  Make sure the expectations are met.

For memory:

- We can only keep 3 things in STM at a time, do not branch a feature to more than 3 objects

- Aim to keep the description of the behavior in a single file, so a reader can follow it down as a form of external memory, and as a place holder.

- Have a strict set of constraints in an easy to explain conceptual model, so once it is learned, any other feature can be understood without re-learning.  If possible, enforce those constraints in the code programatically to make them impossible to break, and can educate those that do not know.  Doing this makes it possible to utilize the "fast" subconsious processing of the brain.

Then Prototype just the first question, and test it.  If it tests well, then move to the next question, and keep moving until the feature is fully prototyped.

### Keep the same conceptual models regardless of environment by having prodevelopment

Tests, debugging, deployment and infrastructure are all things that are solved in both development and production, but with completely different toolsets.

We invest heavily into development and testing that solves the same problems that production faces, but isn't reusable:

For feedback, can we use the effort we put into tests during production as well?  Tests are primarily for fast feedback the code works...we need to redo that effort in prod with monitoring as well.  We also put a lot of effort into the infrastructure after the tests -- why can't the same work be used for the tests and deployment?

In CI at scale: https://www.youtube.com/watch?v=zWR477ypEsc

They have to worry about scheduling, parallelization and auto-scaling, as well as fast environmental creation and cleanup.  The same mechanisms can be used for CI as for prod for immutable deployments and scheduled jobs.

Another reason to push all iterations or conditionals to the top level is it makes it obvious what states the program must be tested for.  The number of tests should match the cyclomatic complexity?

### Depth of No Greater than 3

http://www.eurekalert.org/pub_releases/2005-03/aps-hmc030805.php

study shows that humans can only keep track of about 3 things reliably.  By the 4th, performance degrades considerably.

This also means that you can have a large breadth to the design, so long as each step has a depth limit of 3.

This doesn't mean you should aim for 3.  Aim to have as little depth as possible, and favor breadth over depth.  Breadth means explicitness, depth is hidden knowledge that has to be searched for.

This is an example of external memory -- like a notepad or table of contents.  We can easily reference our current location.

With actions working together, we will likely need to reference previous action to remind ourselves what is happening.  We need to get there and back in the easiest way possible.  Don't decrease external memory storage.

### Keep Things Small

In "Rules" by Sandi Metz (https://www.youtube.com/watch?v=npOGOmkxuio) she demonstrates how smaller objects are easier to understand for new developers, and give them more confidence when making changes. 

But there is a middle ground.  How small until the cost of abstraction impeeds understanding?

Fowler has the "This big" rule (from: https://www.youtube.com/watch?v=sAsRtZEGMMQ)

Both of these ideas have to do with the size of an object and doesn't address the composition of these objects for a use case.

### The Architecture Elevator Pitch

Can you completely explain your architecture in 30 seconds or less?  This implies a strong conceptual model for our system.



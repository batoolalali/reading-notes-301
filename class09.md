## Concepts of Functional Programming in Javascript

#### What is functional programming?
Functional programming is a programming paradigm, a style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.

1. pure functions:
    - It returns the same result if given the same arguments (it is also referred as deterministic)
    - It does not cause any observable side effects
    - It returns the same result if given the same arguments

**Pure functions benefits:**
- The code’s definitely easier to test. We don’t need to mock anything.

2. Immutability
Unchanging over time or unable to be changed.
When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.

3. Functions as first-class entities

**Functions as first-class entities can:**
- refer to it from constants and variables
- pass it as a parameter to other functions
- return it as result from other functions

**Higher-order functions**
When we talk about higher-order functions, we mean a function that either:
- takes one or more functions as arguments, or
- returns a function as its result

4. Map
The idea of map is to transform a collection.


## Refactoring JavaScript for Performance and Readability

It's good to write very fast JavaScript. Some of the examples took it to the extreme and became very quick at the cost of being totally unmaintainable. There’s a middle ground between speed and comprehension and that’s where good code lives.
so we need time but also we need **Performance** and **Readability**
# The Principles of Programming World

Programming is an intricate and dynamic field that constantly evolves. As a Software Developer, it's crucial to adhere to certain 
principles that not only enhance the quality and efficiency of your code but also facilitate collaboration and maintainability.
This article is a compilation of some principles that every Software Developer should know. The list is incomplete, and sometimes trade-offs 
need to be made between conflicting principles. However, higher ranked principles usually beat lower ranked ones.

The list was inspired by <!-- markdown-link-check-disable-next-line -->
[The Principles of Good Programming](https://www.artima.com/weblogs/viewpost.jsp?thread=331531)
(down? [Google's cache](https://webcache.googleusercontent.com/search?q=cache:KU51T8hZ-0kJ:https://www.artima.com/weblogs/viewpost.jsp%3Fthread%3D331531+&cd=1&hl=en&ct=clnk&gl=nl&client=pub-3911176865765226)).
This article is a fork of [programming-principles repository by Lars Kappert](https://github.com/webpro/programming-principles), who has done most of the work collecting the material.

## Table of Contents
<!-- TOC -->
* [The Principles of Programming World](#the-principles-of-programming-world)
  * [Table of Contents](#table-of-contents)
  * [What are Programming Principles ?](#what-are-programming-principles-)
  * [Benefits of Programming Principles](#benefits-of-programming-principles)
  * [General Principles](#general-principles)
    * [Keep It Simple, Stupid ! (KISS)](#keep-it-simple-stupid--kiss)
    * [More Is More Complex (MIMC)](#more-is-more-complex-mimc)
    * [You Aren't Gonna Need It (YAGNI)](#you-arent-gonna-need-it-yagni)
    * [Don't Repeat Yourself (DRY)](#dont-repeat-yourself-dry)
    * [Rule of Explicitness (RoE)](#rule-of-explicitness-roe)
    * [Generalization Principle (GP)](#generalization-principle-gp)
    * [Boy Scout Rule (BSR)](#boy-scout-rule-bsr)
  * [Modularization Principles](#modularization-principles)
    * [Module Principle (MP)](#module-principle-mp)
    * [High Cohesion (HC)](#high-cohesion-hc)
  * [Module Communication Principles](#module-communication-principles)
    * [Law of Demeter (LoD)](#law-of-demeter-lod)
    * [Inversion of Control (IoC)](#inversion-of-control-ioc)
  * [Interface Design Principles](#interface-design-principles)
    * [Easy to Use and Hard to Misuse (EUHM)](#easy-to-use-and-hard-to-misuse-euhm)
    * [Principle of Least Surprise (PLS)](#principle-of-least-surprise-pls)
    * [Uniformity Principle (UP)](#uniformity-principle-up)
  * [Internal Module Design Principles](#internal-module-design-principles)
<!-- TOC -->

## What are Programming Principles ?

Programming Principles are fundamental guidelines or rules that help guide the process of writing efficient, maintainable, and reliable software.

## Benefits of Programming Principles

- **Readability and Collaboration**  
- **Flexibility, Maintainability and Scalability**  
- **Modularity and Reliability**

## General Principles

### Keep It Simple, Stupid ! (KISS)

The KISS principle is about striving for simplicity, KISS states that a solution 
is better when it uses less inheritance, less polymorphism, fewer classes, ect.
This does not mean that features like inheritance or polymorphism should not be used at all.
Rather they should only be used when they are necessary or there's some substantial advantage.

**_Strategy_**
- Avoid:
  - Complicated OOP concepts like inheritance, polymorphism or dynamic binding.
  - Low-level optimization of algorithms, especially when involving Assembler, Bit-operators and pointers.
  - Numerous classes and methods as well as large code blocks.
  - Avoid general solutions needing parameterization.
- Should:
  - Use simple brute-force solutions. Slower algorithms will work in the first place.
  - Use private methods instead of an additional class for slightly unrelated but rather small functional pieces.

**_Note:_** 
Many principles are contrary to KISS, Some of these needing consideration: **Generation Principle**, **Murphy's Law**, **Model Principle**.

**_References_**
- [_Keep It Simple Stupid (KISS)_, (principles-wiki.net)](http://principles-wiki.net/principles:keep_it_simple_stupid)
- [_KISS principle_, (wikipedia.org)](https://en.wikipedia.org/wiki/KISS_principle)
- [Shafayetul Islam, _Keep it Simple, Stupid – How to Use the KISS Principle in Design_](https://www.linkedin.com/pulse/keep-simple-stupid-how-use-kiss-principle-design-shafayetul-islam/)

### More Is More Complex (MIMC)
The MIMC Principle is a rule of thumb stating that the introduction of further modules usually has a higher complexity as a drawback.
The capabilities of the human mind are certainly limited. If there are many modules, looking for a particular module takes a long time,
the longer the searching takes, the more one will have forgotten what has been read previously. This results in the worst readability, understandability, and thus maintainability.

**_Strategy_**
- Avoid Many modules
  - Merge several modules into one.
  - Put the functionality into another module instead of introduce new module.
- Avoid Big modules
  - Divide large modules into several smaller ones.
  - Introduce new modules to group related functionality.

**_References_**
- [_More Is More Complex (MIMC)_, (principles-wiki.net)](http://principles-wiki.net/principles:more_is_more_complex)

### You Aren't Gonna Need It (YAGNI)
The YAGNI states a Programmer shouldn't add functionality until deemed necessary. This principle encourages
a minimalist approach to development, focusing on delivering the most critical features ini a timely manner.

**_Strategy:_** 
Always implement things when you actually need them, never when you just foresee that you need them.

**_References_**
- [_You aren't gonna need it_, (wikipedia.org)](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)
- [_YAGNI PRINCIPLE_, (developerexeprience.io)](https://developerexperience.io/articles/yagni-principle)

### Don't Repeat Yourself (DRY)
Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.
DRY principle states that if there is duplication, there shall be some "single source of truth". When one piece 
of information has several representations DRY demands one and only one representation being the definitive one.

**_Strategy_**
- Factor out a common base class.
- Add a new invokable module (a function, a method, a class, etc.) or use polymorphism instead of duplicating code.
- Use code generation when information has to be represented in multiple forms.
- Apply the [Rule of Three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)).

**_References_**
- [Andrew Hunt and David Thomas, _The Pragmatic Programmer_](https://pragprog.com/titles/tpp20/the-pragmatic-programmer-20th-anniversary-edition/)
- [_Don't Repeat Yourself (DRY)_, (principles-wiki.net)](http://principles-wiki.net/principles:don_t_repeat_yourself)

### Rule of Explicitness (RoE)
RoE states that explicit solutions are better than implicit ones. 
Indirection, side effects, configuration files, implicit conversions, etc. should be avoided.

**_Strategy_**
- _Avoid indirection_: (but keep [LC]() in mind)
  - Events, listeners, observers, etc. Use direct references instead.
  - Messaging middleware in favor of direct communication.
- _Avoid configurability_ (but keep [GP]() in mind):Configuration files for specifying behavior. Instead implement varying behavior explicitly.
- _Explicitly state which module to use_: Avoid importing all classes of a given package/namespace, import the needed classes explicitly.
- _Explicitly name parameters_: 
  - Avoid long parameter lists and use objects with explicit attribute assignments instead.
  - Use parameter types that explicitly state what the input is. Rather use specific types for parameters like customers, articles, URLs, colors, money, etc. 
    instead of using strings or integers for these values.

**_References_**
- [_Rule of Explicitness (RoE)_, (principles-wiki.net)](http://principles-wiki.net/principles:rule_of_explicitness)


### Generalization Principle (GP)

### Boy Scout Rule (BSR)
The Boy Scouts have a rule: "Always leave the campground cleaner than you found it". In development, 
we follow a similar rule in our code: "Always check a module in cleaner than when you checked it out".

**_Strategy_**
- Instituting frequent code reviews
- With each commit make sure it does not degrade the codebase quality.
- Any time someone sees some code that isn't as clear as it should be, they should take the opportunity to fix it right there and then.

**_References_**
- [Robert C.Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)

## Modularization Principles

### Module Principle (MP)

### High Cohesion (HC)

## Module Communication Principles

### Law of Demeter (LoD)

### Inversion of Control (IoC)

## Interface Design Principles

### Easy to Use and Hard to Misuse (EUHM)

### Principle of Least Surprise (PLS)

### Uniformity Principle (UP)

## Internal Module Design Principles

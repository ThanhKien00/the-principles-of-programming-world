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
    * [MIMC (More Is More Complex)](#mimc-more-is-more-complex)
    * [You Aren't Gonna Need It (YAGNI)](#you-arent-gonna-need-it-yagni)
    * [Don't Repeat Yourself (DRY)](#dont-repeat-yourself-dry)
    * [Rule of Explicitness (RoE)](#rule-of-explicitness-roe)
    * [Generalization Principle (GP)](#generalization-principle-gp)
    * [Boy Scout Rule](#boy-scout-rule-)
  * [Modularization Principles](#modularization-principles)
  * [Module Communication Principles](#module-communication-principles)
  * [Interface Design Principles](#interface-design-principles)
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

### MIMC (More Is More Complex)

### You Aren't Gonna Need It (YAGNI)
The YAGNI states a Programmer shouldn't add functionality until deemed necessary. This principle encourages
a minimalist approach to development, focusing on delivering the most critical features ini a timely manner.

**_Strategy:_** 
Always implement things when you actually need them, never when you just foresee that you need them.

**_References_**
- [_You aren't gonna need it_, (wikipedia.org)](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it)
- [_YAGNI PRINCIPLE_, (developerexeprience.io)](https://developerexperience.io/articles/yagni-principle)

### Don't Repeat Yourself (DRY)

### Rule of Explicitness (RoE)

### Generalization Principle (GP)

### Boy Scout Rule 
The Boy Scouts have a rule: "Always leave the campground cleaner than you found it". In development, 
we follow a similar rule in our code: "Always check a module in cleaner than when you checked it out".

**_Strategy_**
- Instituting frequent code reviews
- With each commit make sure it does not degrade the codebase quality.
- Any time someone sees some code that isn't as clear as it should be, they should take the opportunity to fix it right there and then.

**_References_**
- [Robert C.Martin, _Clean Code: A Handbook of Agile Software Craftsmanship_](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)

## Modularization Principles

## Module Communication Principles

## Interface Design Principles

## Internal Module Design Principles

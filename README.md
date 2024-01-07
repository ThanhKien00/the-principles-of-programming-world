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
  * [Common Principles](#common-principles)
    * [KISS (Keep It Simple, Stupid !)](#kiss-keep-it-simple-stupid-)
<!-- TOC -->

## What are Programming Principles ?

Programming Principles are fundamental guidelines or rules that help guide the process of writing efficient, maintainable, and reliable software.

## Benefits of Programming Principles

- **Readability and Collaboration**  
- **Flexibility, Maintainability and Scalability**  
- **Modularity and Reliability**

## Common Principles

### KISS (Keep It Simple, Stupid !)

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
  - use private methods instead of an additional class for slightly unrelated but rather small functional pieces.

**_Note:_** 
Many principles are contrary to KISS, Some of these needing consideration: **Generation Principle**, **Murphy's Law**, **Model Principle**.

**_References_**
- [_Keep It Simple Stupid (KISS)_, (principles-wiki.net)](http://principles-wiki.net/principles:keep_it_simple_stupid)
- [_KISS principle_, (wikipedia.org)](https://en.wikipedia.org/wiki/KISS_principle)
- [_Keep it Simple, Stupid – How to Use the KISS Principle in Design_, Shafayetul Islam](https://www.linkedin.com/pulse/keep-simple-stupid-how-use-kiss-principle-design-shafayetul-islam/)

### MIMC (More Is More Complex)

### YAGNI (You Aren't Gonna Need It)
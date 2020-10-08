# Day Ten Notes

# Topic: Debugging

## Table of Contents

- [Day 1](class-01.md)
- [Day 2](class-02.md)
- [Day 3](class-03.md)
- [Day 4](class-04.md)
- [Day 5](class-05.md)
- [Day 6](class-06.md)
- [Day 7](class-07.md)
- [Day 8](class-08.md)
- [Day 9](class-09.md)
- [Day 10](class-10.md)
- [Day 11](class-11.md)
- [Day 12](class-12.md)
- [Day 13](class-13.md)
- [Day 14](class-14.md), [Day 14 (Extended)](class-14b.md)
- [Day 15](class-15.md)
- [Day 16](class-16.md)
- [Day 17](class-17.md)
- [Day 18](class-18.md)
- [Day 19](class-19.md)
- [Day 20](class-20.md)

## Day Ten Reading:

Here are the chapters to read before class:

From the Duckett JS book:

JavaScript book, Ch. 10, “Error Handling & Debugging”

## Error Handling & Debugging


Order of Execution:

  To find the source of an error, it helps to know how scripts are processed. The order in which statements are executed can be complex; some tasks cannot complete unitl another statement or function has been executed.



Execution Contexts:

  The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new exectuion context. They correspond to variable scope.


The Stack:

  The JavaScript interpreter processes one line of code at a time. When a statenebt beeds data from another function, it stacks (or piles) the new function on top the current task.

![Debugging](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.lynda.com%2Fcourses%2F112414-636410898922723692_338x600_thumb.jpg&f=1&nofb=1)


Execution Context & Hoisting:

If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code.

Debugging is the process of finding errors. It involes a process of deduction.

The console helps narrow down the area in which the error is locatedm so you can try to find the exact error.

JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.

If you know that you may get an error, you can handle it gracefully using the try, catch, finally statements. Use them to give your users helpful feedback.

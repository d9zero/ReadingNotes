# Day Six Notes


# Topic: JS Object Literals; The DOM


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

# Day 6 Reading

Reading
Understanding the problem domain is the hardest part of programming
From the Duckett JS book

Chapter 3: “Object Literals” (pp.100-105)
Chapter 5: “Document Object Model” (pp.183-242)

# Document Object Model (DOM)

The Document Object Model specifies how browsers should create a model of an HTML page and how Javascript can access and update the contents of a web page while it is in the browser window. The DOM is neither a part of HTML, nor a part of Javascriptl it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas:

Making a model of the HTML page:
  - When the browser loads a web page, it creates a mdoel of the page in memory.
  - The DOM specifies the way in which the browser structure this model using a DOM tree.
  - The DOM is called an object model because the model is made of objects.
  - Each object represents a different part of the page loaded in the browser window.

Accessing and changing the HTML page:
  - The DOM also defines methods and properties to access and update each object in this model, which in turn updates what the user sees in the browser.
  - Also called an Application Programming Interface (API).
  - User interfaces let humans interact with programs.
  - APIs let programs and scripts talk to each other.
  - The DOM states what your script can ask the broswer about the current page, and how to tell the browser to update what is being shown to the user.


![DOM Example](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fd2h0cx97tjks2p.cloudfront.net%2Fblogs%2Fwp-content%2Fuploads%2Fsites%2F2%2F2019%2F08%2FJs-Dom-Tree.png&f=1&nofb=1)


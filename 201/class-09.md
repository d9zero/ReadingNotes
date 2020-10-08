# Day Nine Notes


# Topic: Forms and JS Events


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

## Day Nine Reading:

Here are the chapters to read/skim before class:

From the Duckett HTML book:

Chapter 7: “Forms” (p.144-175)
Chapter 14: “Lists, Tables & Forms” (pp.330-357)
From the Duckett JS book:

Chapter 6: “Events” (pp.243-292)


## API'S ##

Apies are used in browsers, scripts, and by websites that share functionality with other programs or sites.

APIs let you write code that will make a request, asking another program or script to do something.

APIs also specify the format in which the response will be given (so that the resonse can be understood).

To use an API on your website, you will need to include a script in the relevant web pages.

An API's documentation will usually feature tables of objectsm methods, and properties.

Providing you know how to create an object and call its methods, access its properties, and respond to its events, you should be able to learn any JavaScript API.

![DOM](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fdsmith77.files.wordpress.com%2F2008%2F07%2Fthe-document-object-model-dom.gif&f=1&nofb=1)


## Document Object Model

The represents the page using a DOM tree.

DOM trees have four types of noes: document nodes, element nodes, attribute nodes, and text notes.

You can select element nodes by their id or class attributes, by tag name, or using CSS selector syntax.

Whenever a DOM query can return more than one node, it will always return a NodeList.

From an Element node, you can access and update its content using properties such as text Content and innerHTML or using DOM manipulation techniques.

An element node can contain multiple text nodes and child elemnets that are siblings of each other.

In older browsers, implementation of the DOM is inconsistent (and is a popular reason for using jQuery).

Browsers offer tools for viewing the DOM tree.
# Day Four Notes


# Topic: HTML Links, JS Functions, and Intro to CSS Layout


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

## Day Four Reading: 

From the Duckett HTML book:

Chapter 4: Ch.4 “Links” (pp.74-93)
Chapter 15: “Layout” (pp.358-404)


![css](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.ytimg.com%2Fvi%2FwNX7lWzchow%2Fmaxresdefault.jpg&f=1&nofb=1)




# Positioning

Static:

body {

  width: 750px;

  font-family: Arial, Verdana, sans-serif;

  color: #665544;}

Absolute:
h1 {

    position: absolute;

    top: 0px;

    left: 500px;

    width: 250px;}

Fixed:
h1 { 

  position: fixed;}

z-index:

h1 {

  z-index 10;}

Float:

blockquote {

  float: right;}

# Layout

Fixed:

  Body {

    width: 960px;

    margin: 0 auto;}

  #content {

    overflow: auto;

    height: 100%;}

  .column1, .column2, .column3 {

    width: 300px;

    float: left;

    margin: 10px;}


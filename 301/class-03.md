# Class 03

## Navigation ##
 - [class 01](class-01.md)
 - [class 02](class-02.md)
 - [class 03](class-03.md) 
 - [class 04](class-04.md)
 - [class 05](class-05.md)
 - [class 06](class-06.md)
 - [class 07](class-07.md)
 - [class 08](class-08.md)
 - [class 09](class-09.md) 
 - [class 10](class-10.md)
 - [class 11](class-11.md)
 - [class 12](class-12.md)
 - [class 13](class-13.md)
 - [class 14a](class-14a.md)
 - [class 14b](class-14b.md)

## Readings: MUSTACHE and FLEXBOX
Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

![Mustache](https://miro.medium.com/max/1400/1*P9q0tkeaRY2l1JOXaVKAig.png)

## Reading ##
[Templating with Mustache](https://medium.com/@1sherlynn/javascript-templating-language-and-engine-mustache-js-with-node-and-express-f4c2530e73b2)
[A Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
[Flexbox Froggy](https://flexboxfroggy.com/)
  Complete all steps of this tutorial
Bookmark/Skim
Reference: [Mustache.js Official Documentation](https://github.com/janl/mustache.js)


### Mustache

Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.
It is often referred to as “logic-less” because there are no if statements, else clauses, or for loops. Instead, there are only tags. Some tags are replaced with a value, some nothing, and others a series of values.



### A Guide To Flexbox


flex-wrap
nowrap (default): all flex items will be on one line
wrap: flex items will wrap onto multiple lines, from top to bottom.
wrap-reverse: flex items will wrap onto multiple lines from bottom to top.

![flex-wrap](https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg)



flex-direction

This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as primarily laying out either in horizontal rows or vertical columns.

row (default): left to right in ltr; right to left in rtl
row-reverse: right to left in ltr; left to right in rtl
column: same as row but top to bottom
column-reverse: same as row-reverse but bottom to top

![flex-direction](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg)



justify-content


flex-start (default): items are packed toward the start of the flex-direction.
flex-end: items are packed toward the end of the flex-direction.
start: items are packed toward the start of the writing-mode direction.
end: items are packed toward the end of the writing-mode direction.
left: items are packed toward left edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
right: items are packed toward right edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
center: items are centered along the line
space-between: items are evenly distributed in the line; first item is on the start line, last item on the end line
space-around: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
space-evenly: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

![justify-content](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)






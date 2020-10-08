# Read: 01 - SMACSS and Responsive Web Design #

# Readings: RESPONSIVE WEB DESIGN and FLOATS #

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

![JS](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fgeekboots.sfo2.cdn.digitaloceanspaces.com%2Fpost%2Flet-vs-const-vs-var--1567744166855.jpg&f=1&nofb=1)

## Reading ##
- [Shay Howe’s intro to RWD](http://learn.shayhowe.com/advanced-html-css/responsive-web-design/)
- [All About Floats](https://css-tricks.com/all-about-floats/)
Bookmark/Skim
- [Don’t Overthink It Grids](https://css-tricks.com/dont-overthink-it-grids/)
- [CSS Floats Explained By Riding An Escalator](https://medium.freecodecamp.org/css-floats-explained-by-riding-an-escalator-57fa55232333) - If you took Code 201, review this article. If you did not take Code 201, this is Essential reading.

- [SMACSS Official Documentation](http://smacss.com/)



### Responsive Overview ###
Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop. Responsive web design is focused around providing an intuitive and gratifying experience for everyone. Desktop computer and cell phone users alike all benefit from responsive websites.

Responsive and adaptive web design are closely related, and often transposed as one in the same. Responsive generally means to react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change. With responsive design websites continually and fluidly change based on different factors, such as viewport width, while adaptive websites are built to a group of preset factors. A combination of the two is ideal, providing the perfect formula for functional websites. Which term is used specifically doesn’t make a huge difference.

Mobile, on the other hand, generally means to build a separate website commonly on a new domain solely for mobile users. While this does occasionally have its place, it normally isn’t a great idea. Mobile websites can be extremely light but they do come with the dependencies of a new code base and browser sniffing, all of which can become an obstacle for both developers and users.

## Float ##

![float](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/web-layout.png?resize=540%2C240&ssl=1)
![float left and right, clear](https://i1.wp.com/css-tricks.com/wp-content/csstricks-uploads/directionalclearing.png?resize=540%2C226&ssl=1)

Float’s sister property is clear. An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float. Again an illustration probably does more good than words do.


## Var, Let, Const
## Var ##
Scope of var
Scope essentially means where these variables are available for use. var declarations are globally scoped or function/locally scoped.

The scope is global when a var variable is declared outside a function. This means that any variable that is declared with var outside a function block is available for use in the whole window.

var is function scoped when it is declared within a function. This means that it is available and can be accessed only within that function.

## Let ##

let is now preferred for variable declaration. It's no surprise as it comes as an improvement to var declarations. It also solves the problem with var that we just covered. Let's consider why this is so.

let is block scoped
A block is a chunk of code bounded by {}. A block lives in curly braces. Anything within curly braces is a block.

So a variable declared in a block with let  is only available for use within that block.

## Const ##

Variables declared with the const maintain constant values. const declarations share some similarities with let declarations.

const declarations are block scoped
Like let declarations, const declarations can only be accessed within the block they were declared.

const cannot be updated or re-declared
This means that the value of a variable declared with const remains the same within its scope. It cannot be updated or re-declared. 




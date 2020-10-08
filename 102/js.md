## Table of Contents

- [Markdown Reading](markdown.md)
- [README](README.md)
- [Revision and the Cloud](revisions-and-the-cloud.md)
- [Structure web pages with HTML](structurehtml.md)
- [CSS](css.md)
- [Javascript](js.md)
- [Computer Architecture and Logic](comparch.md)
- [Programming in Javascript](programmingjs.md)
- [Operators and Loops](oploop.md)
- [TBD]


## Introduction to Javascript

Computers create models of the world using data. The models use objects to represent physical things. Objects can have : properties that tell us about the object; methods that perform tasks using the properties of that object; events which are triggered when a user interacts with the computer.

Programmers can write code to say "When this event occurs, run that code."

Web browsers use HTML markup to create a model of the web page. Each element creates its own node (which is a kind of object).

To make web pages interactive, you write code that uses the browsers's model of the web page. Web developers usuall talk about three languages that are used to create web pages which include HTML, CSS, and Javascript. Where possible, aim to keep the three languages in separate files with the HTML page linking to CSS and Javascript files. Each language forms a separate layer with a different purpose. Each layer, from left to right builds on the previous one.

As more and more web-enabled devices come onto the market, this concept is becoming more widely adopted. It's not just screen sizes that are varied - connection speeds and capabilites of each device can also differ. Also, some browsers are ran with Javascript turned off. So websites that are created should be designed with that manner in mind, so the webpage can provide services to the intended audience.

## Javascript In-depth

Javascript is written in plain text, just like a HTML and CSS. When Javascript is enabled into a webpage, the HTML file must have a .js _< script>_ element to tell the browser that there is a script. the _src_ attributes tells people where the .js file is stored.

<ul>
    <li>Statements: A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement; A statement is an individual instruction that the computer should follow. Statements should end with a semicolon, as it renders code more easy to follow and the Javascript interpreter indicates that processes should move to the next step. </li>
    <li>Comments: are descriptions of the present code and what it does, They help make your code easier to read and understand. This can help you and others who read your code.</li>
    <li>Multi-line Comments: Multi-line comments are often used for descriptions of how the script works, or to prevent a section of the script from running when testing it.</li>
    <li>Variables: variables temprarily stores data that is required perform scripts. Variables are also used to remember the values for _width_ and _height_. The information used to compare variables are temporary because once the client leaves the page, the browser will omit any information it holds.</li>
</ul>

 ![Data Types in Javascript](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.javatpoint.com%2Fimages%2Fjava-data-types.png&f=1&nofb=1)
 
<ul>
    <li> Number Data Type </li>
    <li> String Data Type </li>
    <li> Boolean Data Type </li>
</ul>


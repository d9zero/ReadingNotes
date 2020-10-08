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

# Operators and Loops

![brain](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fmedia3.s-nbcnews.com%2Fj%2Fnewscms%2F2017_15%2F1336291%2F151211-brain-intelligence-mn-1045_a3b47678f9fdb22dd063a70a8721c7c0.nbcnews-fp-1200-630.jpg&f=1&nofb=1)


## Operators

### Comparison Operators

    * Comparison operators usually return single values of true or false:
        * == is equal to
        * != is not equal to
        * === strict equal to
        * !== strict not equal to
        * greater than
        * __<__ less than
        * = greater than or equal to
        * <== less than or equal to

    ### Logical Operators

    * Logical operators allow you to compare the results of more than one comparison operator.
        
        * && "Logical And" This operator tests more than one condition.
        * || "Logical Or" This operator tests at least one condition.
        * ! "Logical Not" This operator takes a single Boolean value and inverts it.


![chart](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Foer.nios.ac.in%2Fwiki%2Fimages%2F3%2F3b%2FJavascript3.png&f=1&nofb=1)

## Loops

Example

    '''var sum = 0;
    var number = 1;
    while (number <= 50) {  // -- condition
      sum += number;        // -- body
      number++;             // -- updater
    }
    alert("Sum = " + sum);  // => Sum = 1275'''


Loops are used to repeatedly run a block of code - until a certain condition is met. When developers talk about iteration or iterating over, say, an array, it is the same as looping. JavaScript offers several options to repeatedly run a block of code, including while, do while, for and for-in. The condition is first evaluated. If true, the block of statements following the while statement is executed. This is repeated until the condition becomes false. This is known as a pre-test loop because the condition is evaluated before the block is executed. The number++ statement is called the updater. Removing it will result in an infinite loop. You must always include a statement in a loop that guarantees the termination of the loop or else you'll run into this problem. 

## While Loop

The block following do is executed first and then the condition is evaluated. If the while condition is true, the block is executed again and repeats until the condition becomes false. This is known as a post-test loop as the condition is evaluated after the block has executed.

'''var sum = 0;
    var number = 1;
    do {
       sum += number;         // -- body
       number++;              // -- updater
    } while (number <= 50);   // -- condition
    alert("Sum = " + sum);    // => Sum = 1275'''

The do-while loop is executed at least once whereas the while loop may not execute at all. The do-while is typically used in a situation where the body of a loop contains a statement that generates a value that you want to use in your conditional expression, like this

    '''do {
       // read a character from keyboard in the body 
  } while (if ch === '0');     // => terminate loop if '0' is entered.'''


## For Loop

The most frequently used loop in JavaScript is the for-loop. It consists of three parts, separated by semicolons. The first is the ***initializer*** (var i = 1) which initializes the loop and is executed only once at the start. The second is a test condition (i <= 50). When a conditional expression evaluates to true, the body of the loop is executed. When false, the loop terminates. The third part is an updater (i++) which is invoked after each iteration. The updater typically increments or decrements the loop counter.

    '''var sum = 0;
    for (var i = 1; i <= 50; i++) {
       sum = sum + i;
    }
    alert("Sum = " + sum);    // => Sum = 1275'''


## For-in Loop

A for-in loop iterates through the properties of an object and executes the loop's body once for each enumerable property of the object

## Break Statement

When JavaScript encounters a break statement in a loop it immediately exits the loop without executing any other statements in the loop. Control is immediately transferred to the statement following the loop body

## Continue Statement

When JavaScript encounters a continue statement in a loop it stops the execution of the current iteration and goes back to the beginning of the loop to begin the next iteration. The example below displays only even numbers.


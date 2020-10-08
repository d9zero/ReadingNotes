# Class 10 - The Call Stack and Debugging

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

 ## Reading
[The Call Stack defined on MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
[Understanding the JavaScript Call Stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
[JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)
 
 
 ## Call stack

 " A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function"

          - When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
          - Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
          - When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
          - If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.


## JavaScript Call Stack

The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.

![stack](https://cdn-media-1.freecodecamp.org/images/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv)


## How does the call stack handle function calls?

              function firstFunction(){
                console.log("Hello from firstFunction");
              }

              function secondFunction(){
                firstFunction();
                console.log("The end from secondFunction");
              }

              secondFunction();

## This is what happens when the code is run:

1. When secondFunction() gets executed, an empty stack frame is created. It is the main (anonymous) entry point of the program.
2. secondFunction() then calls firstFunction()which is pushed into the stack.
3. firstFunction() returns and prints “Hello from firstFunction” to the console.
4. firstFunction() is pop off the stack.
5. The execution order then move to secondFunction().
6. secondFunction() returns and print “The end from secondFunction” to the console.
7. secondFunction() is pop off the stack, clearing the memory.

## JavaScript error messages && debugging

### Types of error messages

Reference errors:

          This is as simple as when you try to use a variable that is not yet declared.


Syntax errors:

          This occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

Range errors: 

          An object with some kind of length, yielded an invalid length value.

Type errors:

          Types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

Debugging:

          To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).

# Tools to avoid runtime errors

        1. quokka to evaluate your code as you type
        2. eslint to make sure your style guide is consistency and it will grab you an error or two along the way and
        3. For those of you looking to make JS a more strong typed experience you can check out stuff like TypeScript (like I said in a previous article, when learning I rather avoid libraries that abstract the core language so I wouldn’t recommend this last one when starting).


# Class 06

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

## Readings: NODE.JS
Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

Reading
[An Introduction to Node.js on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js)


## What Is Node.js?

 Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

"It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute."

"features, such as a file system API, an HTTP library, and a number of operating system–related utility methods."

## How Do I Install Node.js?

You can check that Node is installed on your system by opening a terminal and typing node -v. If all has gone well, you should see something like v12.14.1 displayed. This is the current LTS version at the time of writing.

## Installing a Package Locally
We can also install packages locally to a project, as opposed to globally, on our system. Create a test folder and open a terminal in that directory. Next type this:

          npm init -y
          This will create and auto-populate a package.json file in the same folder. Next, use npm to install the lodash package and save it as a project dependency:

          npm install lodash --save
          Create a file named test.js and add the following:

          const _ = require('lodash');

          const arr = [0, 1, false, 2, '', 3];
          console.log(_.compact(arr));
          Finally, run the script using node test.js. You should see [ 1, 2, 3 ] output to the terminal.



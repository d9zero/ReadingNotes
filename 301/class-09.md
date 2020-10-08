# Class 09 - Read: 09 - Refactoring


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

 ## Refactoring JavaScript for Performance and Readability

          const URLstore = [];

          function makeShort(URL) {
            const rndName = Math.random().toString(36).substring(2);
            URLstore.push({[rndName]: URL});
            return rndName;
          }

          function getLong(shortURL) {
            for (let i = 0; i < URLstore.length; i++) {
              if (URLstore[i].hasOwnProperty(shortURL) !== false) {
                return URLstore[i][shortURL];
              }
            }
          }

Maps and Sets use under the surface. A hash function is used to map a given key to a location in the hash table. Below, this happens when we place our short URL into the store in makeShort and when we get it back out in getLong. Depending on how you're measuring run time, the result is that on average we only need to check one bucket

          function showProfile(user) {
            if (user.authenticated === true) {
              // ..
            }
          }

          // Refactor into ->

          function showProfile(user) {
            // People often inline such checks
            if (user.authenticated === false) { return; }
            // Stay at the function indentation level, plus less brackets
          }

## Concepts of Functional Programming in Javascript

"Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data "

          const charactersCounter = (text) => `Character count: ${text.length}`;

          function analyzeFile(filename) {
            let fileContent = open(filename);
            return charactersCounter(fileContent);
          }
# Day Three Notes


# Topic: HTML Lists, Control Flow with JS, and the CSS Box Model


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

## Day Three Reading:
From the Duckett HTML book:

Chapter 3: “Lists” (pp.62-73)
Chapter 13: “Boxes” (pp.300-329)
From the Duckett JS book:

Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)
Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182

# Box dimensions

  in CSS div {

            border: 2px solid black line;

            height: 300px;

            width: 400px;

            background-color: #ee3e80;]}
        
# Placement

  in CSS [selector] {
                  float: center;
                  padding: 5px;
                  margin: 0 px;}

![screenshot of demo](images/Screenshot_(490).png)
![screenshot of demo](images/Screenshot_(491).png)

# Loops

var mytool= 'hammer';

var mytoolshed= ['miter saw', 'band saw', 'drill press', 'table saw', 'planer', 'saw legs', 'impact drill'];

console.log('Challenge 1');

for(var i=0; i < mytoolshed.length; i++){

  console.log('the value of i is ' + i);

  console.log('the value of my array is ' + mytoolshed[i]);
}

console.log (mytoolshed);

console.log('Challenge 2');

var i = 0;

while(i< mytoolshed.length){

  if(mytoolshed[i] === 'band saw'){console.log(mytoolshed[i]);}

  i++;}

console.log('Challenge 3')

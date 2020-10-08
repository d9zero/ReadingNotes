# Day Seven Notes

# Topic: Object-Oriented Programming, HTML Tables


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

## Day Seven Reading:

Domain Modeling
From the Duckett HTML book:

Chapter 6: “Tables” (pp.126-145)
From the Duckett JS Book:

Chapter 3: “Functions, Methods, and Objects” (pp.106-144)

## Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

## Define a constructor and initialize properties

To define the same properties between many objects, you'll want to use a constructor function. Below is a table that summarizes a JavaScript representation:


        Property 	Data 	Type
        epicRating 	1 to 10 	Number
        hasAnimals 	true or false 	Boolean


      var EpicFailVideo = function(epicRating, hasAnimals) {
        this.epicRating = epicRating;
        this.hasAnimals = hasAnimals;
      }

      var parkourFail = new EpicFailVideo(7, false);
      var corgiFail = new EpicFailVideo(4, true);

      console.log(parkourFail);
      console.log(corgiFail);

## Generate random numbers

To model the random nature of user behavior, you'll need the help of a random number generator. Fortunately, the JavaScript standard library includes a Math.random() function for just this sort of occasion.

        var EpicFailVideo = function(epicRating, hasAnimals) {
          this.epicRating = epicRating;
          this.hasAnimals = hasAnimals;
        }

        EpicFailVideo.prototype.generateRandom = function(min, max) {
          return Math.floor(Math.random() * (max - min + 1)) + min;
        }

        var parkourFail = new EpicFailVideo(7, false);
        var corgiFail = new EpicFailVideo(4, true);

        console.log(parkourFail.generateRandom(1, 5));
        console.log(corgiFail.generateRandom(1, 5));
      

![hidethepain.meme](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fi2.kym-cdn.com%2Fphotos%2Fimages%2Ffacebook%2F000%2F854%2F491%2Fb7c.jpg&f=1&nofb=1)


## Calculate daily Likes

Popularity of a video is measured in Likes. And the formula for calculating Likes is the number of viewers times the percentage of viewers who'll Like a video. In other words, viewers times percentage.

To calculate the number of viewers per day, generate a random number between 10 and 30 and then multiply it by the epic rating of that video.

Example:

                var EpicFailVideo = function(epicRating, hasAnimals) {
                  this.epicRating = epicRating;
                  this.hasAnimals = hasAnimals;
                }

                EpicFailVideo.prototype.generateRandom = function(min, max) {
                  return Math.floor(Math.random() * (max - min + 1)) + min;
                }

                EpicFailVideo.prototype.dailyLikes = function() {
                  var viewers, percentage;

                  viewers = this.generateRandom(10, 30) * this.epicRating;

                  if (this.hasAnimals) {
                    percentage = 0.75;
                  } else {
                    percentage = 0.40;
                  }

                  return Math.round(viewers * percentage);
                }

                var parkourFail = new EpicFailVideo(7, false);
                var corgiFail = new EpicFailVideo(4, true);

                console.log(parkourFail.dailyLikes());
                console.log(corgiFail.dailyLikes());

## Snapshot

table element is used to add tables to a web
page.

A table is drawn out row by row. Each row is created
with the tr element.

Inside each row there are a number of cells
represented by the td element (or th if it is a
header).

You can make cells of a table span more than one row
or column using the rowspan and colspan attributes.

For long tables you can split the table into a thead,
tbody, and tfoot.
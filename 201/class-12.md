# Day Twelve Notes

# Topic: Chart.js, Canvas

![chart](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn-images-1.medium.com%2Fmax%2F1200%2F1*CPSTzfUTCCpUbllyiPvl_A.jpeg&f=1&nofb=1)

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


## Day Twelve Reading:

Assorted bits of documentation:
Read this article on the Chart.js API.
Chart.js docs: You’ll be needing these!
Read the following articles on the Canvas API.
•	Basic usage
•	Drawing shapes with canvas
•	Applying styles and colors
•	Drawing text


## Easily Create Stunning Animated Charts with Chart.Js

**Charts can be better for displaying data**

Setting up:

  

    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8" />
            <title>Chart.js demo</title>
            <script src='Chart.min.js'></script>
        </head>
        <body>
        </body>
    </html>

**Drawing a line chart:**

    

<:canvas id="buyers" width="600" height="400"><:/canvas>

      

<:script>
    var buyers = document.getElementById('buyers').getContext('2d');
    new Chart(buyers).Line(buyerData);
<:/script>





var buyerData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",
			strokeColor : "#ACC26D",
			pointColor : "#fff",
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	]
}

**Drawing a pie chart:**

<:canvas id="countries" width="600" height="400"><:/canvas>



      var countries= document.getElementById("countries").getContext("2d");
      new Chart(countries).Pie(pieData, pieOptions);

      var pieData = [
        {
          value: 20,
          color:"#878BB6"
        },
        {
          value : 40,
          color : "#4ACAB4"
        },
        {
          value : 10,
          color : "#FF8153"
        },
        {
          value : 30,
          color : "#FFEA88"
        }
      ];


      var pieOptions = {
        segmentShowStroke : false,
        animateScale : true
      }


**Drawing a bar chart:**

<:canvas id="income" width="600" height="400"><:/canvas>



var income = document.getElementById("income").getContext("2d");
new Chart(income).Bar(barData);



var barData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "#48A497",
			strokeColor : "#48A4D1",
			data : [456,479,324,569,702,600]
		},
		{
			fillColor : "rgba(73,188,170,0.4)",
			strokeColor : "rgba(72,174,209,0.4)",
			data : [364,504,605,400,345,320]
		}

	]
}

## Chart.js

**Creating a Chart**

<:canvas id="myChart" width="400" height="400"><:/canvas>
<:script>
var ctx = document.getElementById('myChart').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
});
<:/script>

## The canvas element

Indeed, the <:canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.

The id attribute isn't specific to the <:canvas> element but is one of the global HTML attributes which can be applied to any HTML element

    <:canvas id="stockGraph" width="150" height="150">
      current stock price: $3.15 + 0.15
    <:/canvas>

    <:canvas id="clock" width="150" height="150">
      <:img src="images/clock.png" width="150" height="150" alt=""/>
    <:/canvas>


## The rendering context

    var canvas = document.getElementById('tutorial');
    var ctx = canvas.getContext('2d');

## Checking for support

    var canvas = document.getElementById('tutorial');

    if (canvas.getContext) {
      var ctx = canvas.getContext('2d');
      // drawing code here
    } else {
      // canvas-unsupported code here
    }

## A template

remove ':' for use.

<:!DOCTYPE html>
<:html>
  <:head>
    <:meta charset="utf-8"/>
    <:title>Canvas tutorial<:/title>
    <:script type="text/javascript">
      function draw() {
        var canvas = document.getElementById('tutorial');
        if (canvas.getContext) {
          var ctx = canvas.getContext('2d');
        }
      }
    <:/script>
    <:style type="text/css">
      canvas { border: 1px solid black; }
    <:/style>
  <:/head>
  <:body onload="draw();">
    <:canvas id="tutorial" width="150" height="150"><:/canvas>
  <:/body>
<:/html>

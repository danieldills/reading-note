## Chart.js
(https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

- Setting Up
    - download Chart.js, and unzip folder into directory working in
    - create new HTML page
- Drawing a line chart
``` <canvas id="buyers" width="600" height="400"></canvas>```
- Write script that retrieves context from canvas

```
<script>
    var buyers = document.getElementByID('buyers').getContext('2d new Chart(buyers).Line(buyerData));
</script>
```
- You can draw charts
    - line chart
    - pie chart
    - bar chart

## Chart.js
example provided by:
(https://www.chartjs.org/docs/latest/)


```
<canvas id="myChart" width="400" height="400"></canvas>
<script>
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
</script>
```

### Basic Usage of Canvas
 - The Canvas API provides a means for drawing graphics in JavaScript and the HTML ```<canvas>``` element. It can be used for animation, game graphics, data visualization, photo manipulation, and real time video processing (MDN WebDocs Mozilla)

 ### Drawing shapes with canvas
 ```fillRect(x,y, width, height)``` Draws a filled rectangle
 ```strokeRect(x, y, width, height)``` Draws a rectangular outline
```clearRect(x, y, width, height)``` clears the specified rectangular area, making it fully transparent
(examples from MDN WebDocs Mozilla)

### Applying styles and colors
- ```fillstyle = color``` sets style used when filling shapes
- ```strokeStyle = color``` sets the style for shapes' outlines
(examples from MDN WebDocs Mozilla)

### Drawing Text
- ```fillText(text, x, y, [, maxWidth])```
fills given text at the given (x,y) position. Optionally with a maximum width to draw.
- ```strokeText(text, x, y [, maxWidth])```
strokes a given text at the given (x,y) position. Optionally with a maximum width to draw

[<== Back](README.md)
# Canvas 
to create animation we use canvas library, it is already exists and ready to use inside Chart.js.<br>
first the Chart.js needs to be imported in order to use it.<br>
import the script within html code as below:<br>
```html
<head>
  <script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>
</head>
```
to draw a line in canvas:<br>
```html
<canvas id="line" width="80%" height="200px"></canvas>
```

canvas used to draw animation, charts, and figures.<br>

to draw chart using canvas, first refer to canvas tag in html using its tag.<br>
then make an object of the constructor chart, by passing it the canvas element, that has been converted to 2d.<br>
then simply define the chart type to *pie* for example, and specify the data within the *data* property in the object as shown below:<br>

```html
<canvas id="myChart"></canvas>
<script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>
<script>
  var ctx = document.getElementById('myChart').getContext('2d');
  var chart = new Chart(ctx, {
  // The type of chart we want to create
  type: 'pie',

  // The data for our dataset
  data: {
      labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
      datasets: [{
          label: 'statistics for the last year',
          backgroundColor: ['rgb(0, 255, 255','rgb(0, 255, 0)','rgb(30, 150, 150)','rgb(100, 100, 100)','rgb(255, 255, 0)','rgb(255, 0, 0)','rgb(0, 0, 255)'],
          // borderColor: ['rgb(0, 50, 200)','rgb(0, 255, 0)','rgb(255, 0, 0)','rgb(255, 255, 0)','rgb(0, 0, 255)','rgb(100, 100, 100)'],
          data: [5, 10, 5, 2, 20, 30, 45]
      }]
  },

  // Configuration options go here
  options: {},
    
  
});
    chart.canvas.parentNode.style.height = '700px';
    chart.canvas.parentNode.style.width = '700px';
</script>
```
<br>

**The above code will display the below chart in the browser**


<canvas id="myChart"></canvas>
<script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>
<script>
  var ctx = document.getElementById('myChart').getContext('2d');
  var chart = new Chart(ctx, {
  // The type of chart we want to create
  type: 'pie',

  // The data for our dataset
  data: {
      labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
      datasets: [{
          label: 'statistics for the last year',
          backgroundColor: ['rgb(0, 255, 255','rgb(0, 255, 0)','rgb(30, 150, 150)','rgb(100, 100, 100)','rgb(255, 255, 0)','rgb(255, 0, 0)','rgb(0, 0, 255)'],
          // borderColor: ['rgb(0, 50, 200)','rgb(0, 255, 0)','rgb(255, 0, 0)','rgb(255, 255, 0)','rgb(0, 0, 255)','rgb(100, 100, 100)'],
          data: [5, 10, 5, 2, 20, 30, 45]
      }]
  },

  // Configuration options go here
  options: {},
    
  
});
    chart.canvas.parentNode.style.height = '400px';
    chart.canvas.parentNode.style.width = '700px';
</script>

to draw different charts type, simply change the type property in the chart object to be line if you
wanted to show the data as line, or to bar if you want to display your data values as bars.
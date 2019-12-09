---
title: "차대 사람 교통사고 유형"
date: 2019-12-10 03:28:00 -0400
categories: Datavisualization
---

<html>
   <head>
      <title>교통사고 유형</title>
      <script type = "text/javascript" src = "https://www.gstatic.com/charts/loader.js">
      </script>
      <script type = "text/javascript">
         google.charts.load('current', {packages: ['corechart']});
      </script>
   </head>

   <body>
      <div id = "container" style = "width: 550px; height: 400px; margin: 0 auto">
      </div>
      <script language = "JavaScript">
         function drawChart() {
            // Define the chart to be drawn.
            var data = google.visualization.arrayToDataTable([
               ['Year', '무단횡단', '보행노인','자전거','보행어린이','스쿨존어린이'],
               ['2012',  564,      508,       453,        198,        35],
               ['2013',  389,      552,       480,        158,        27],
               ['2014',  248,      586,       586,        130,        43],
               ['2015',  244,      606,       597,        117,        43],
               ['2016',  204,      586,       492,        91,        47],
               ['2017',  212,      552,       386,        79,        36],
               ['2018',  145,      529,       321,        79,        42],
            ]);

            var options = {title: '사고유형', isStacked:true};

            // Instantiate and draw the chart.
            var chart = new google.visualization.BarChart(document.getElementById('container'));
            chart.draw(data, options);
         }
         google.charts.setOnLoadCallback(drawChart);
      </script>
   </body>
</html>

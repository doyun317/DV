---
title: "차대 사람 인구대비 사고횟수"
date: 2019-12-10 03:27:30 -0400
categories: Datavisualization
---
<html>
  <head>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load("current", {packages:["corechart"]});
      google.charts.setOnLoadCallback(drawChart);
      function drawChart() {
        var data = google.visualization.arrayToDataTable([
          ['행정지역', '인구대비 사고 횟수'],
          ['대구광역시', 0.0004346955561146699],
          ['서울특별시',      0.0002938928271506573],
          ['제주특별자치도', 0.0002345636220208926],
          ['광주광역시', 0.00022481105247898736],
          ['부산광역시',  0.00022130893006317071],
          ['대전광역시', 0.00021961764971389076],
          ['전라도', 0.0001984004169111758],
          ['울산광역시', 0.00016671225204808606],
          ['경상도', 0.00016347587811556534],
          ['경기도',     0.00013921132751161197],
          ['충청도', 0.00014044656082409795],
          ['강원도', 0.00014278519395421527],
          ['인천광역시',    0.00012478108359351936]

        ]);

        var options = {
          title: '인구대비 사고 횟수',
          pieSliceText: 'label',
          pieHole: 0.3
        };

        var chart = new google.visualization.PieChart(document.getElementById('donutchart'));
        chart.draw(data, options);
      }
    </script>
  </head>
  <body>
    <div id="donutchart" style="width: 4096px; height: 2160px;"></div>
  </body>
</html>

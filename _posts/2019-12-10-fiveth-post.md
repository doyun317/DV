---
title: "차대 사람 주간 야간 기준 사고 발생 횟수"
date: 2019-12-10 03:29:30 -0400
categories: Datavisualization
---
<html>
  <head>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('current', {'packages':['bar']});
      google.charts.setOnLoadCallback(drawChart);

      function drawChart() {
        var data = google.visualization.arrayToDataTable([
          ['발생시각', '사고 횟수', '사상자수'],
          ['주간', 555, 602],
          ['야간', 881, 996],
        ]);

        var options = {
          chart: {
            title: '교통사고 발생 시각',
            subtitle: '주간,야간를 기준으로',
          }
        };

        var chart = new google.charts.Bar(document.getElementById('columnchart_material'));

        chart.draw(data, google.charts.Bar.convertOptions(options));
      }
    </script>
  </head>
  <body>
    <div id="columnchart_material" style="width: 800px; height: 500px;"></div>
  </body>
</html>

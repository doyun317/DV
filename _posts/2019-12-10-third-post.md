---
title: "차대 사람 요일별 사고횟수"
date: 2019-12-10 03:17:30 -0400
categories: Datavisualization
---
<html>
  <head>
  <title>요일별 사고 발생 횟수</title>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('current', {'packages':['corechart']});
      google.charts.setOnLoadCallback(drawVisualization);

      function drawVisualization() {
        // Some raw data (not necessarily accurate)
        var data = google.visualization.arrayToDataTable([
          ['Day of the week', '사고 횟수', '사상자수', '야간 사고횟수', '야간 사상자수'],
          ['월',  211,      181,         125,             152           ],
          ['화',  197,      207,         111,             121          ],
          ['수',  214,      250,         134,             166           ],
          ['목',  207,      225,         113,             120           ],
          ['금',  239,      260,         145,             155           ],
          ['토',  208,      238,         137,             156           ],
          ['일',  160,      191,         125,             152          ]
        ]);

        var options = {
          title : '요일별 사고횟수',
          hAxis: {title: '요일'},
          seriesType: 'bars',
          series: {3: {type: 'line'}, 2: {type: 'line'}}        };

        var chart = new google.visualization.ComboChart(document.getElementById('chart_div'));
        chart.draw(data, options);
      }
    </script>
  </head>
  <body>
    <div id="chart_div" style="width: 900px; height: 500px;"></div>
  </body>
</html>

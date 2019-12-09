---
title: "전국 인구수와 교통사고 횟수"
date: 2019-12-10 03:58:30 -0400
categories: Datavisualization
---
<html>
<title>전국 인구수와 교통사고 횟수</title>
  <head>
    <script type='text/javascript' src='https://www.gstatic.com/charts/loader.js'></script>
    <script type='text/javascript'>
     google.charts.load('current', {
       'packages': ['geochart'],
       // Note: you will need to get a mapsApiKey for your project.
       // See: https://developers.google.com/chart/interactive/docs/basic_load_libs#load-settings
       'mapsApiKey': 'AIzaSyBPZTjwvR5He2Vgexve0GPy2C7HUxMsiMA'
     });
     google.charts.setOnLoadCallback(drawMarkersMap);

      function drawMarkersMap() {
      var data = google.visualization.arrayToDataTable([
        ['Provinces',  '교통사고 횟수', 'Population' ],
        ['Chungbuk',339,1599854],
        ['Chungnam',230,2125732],
        ['Gangwon',220,1599854],
        ['Gyeonggi',1830,13145482],
        ['Gyeongbuk',493,2669731],
        ['Gyeongnam',494,3367857],
        ['Jeonbuk',402,1827871],
        ['Jeonnam',332,1871718],
        ['Seoul',2869,9762062],
        ['Daegu',1066,2452291],
        ['Busan',759,3429595],
        ['Incheon',369,2957179],
        ['Gwangju',328,1459003],
        ['Daejeon',326,1484398],
        ['Ulsan',192,1151685],
        ['Jeju',157,669328]

      ]);

      var options = {
        region: 'KR',
        colorAxis: {colors: ['#fee6ce','#fdae6b', '#f03b20']},
        backgroundColor: '#81d4fa',
        datalessRegionColor: '#ffffff',
        defaultColor: '#f5f5f5',
        resolution: 'provinces',

      };

      var chart = new google.visualization.GeoChart(document.getElementById('chart_div'));
      chart.draw(data, options);
    };
    </script>
  </head>
  <body>
    <div id="chart_div" style="width: 900px; height: 500px;"></div>
  </body>
</html>

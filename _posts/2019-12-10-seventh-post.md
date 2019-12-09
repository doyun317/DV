---
title: "인구 밀도별 교통사고 발생 횟수"
date: 2019-12-10 03:54:30 -0400
categories: Datavisualization
---
<html>
<title>인구 밀도별 교통사고 발생 횟수</title>
  <head>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('current', {
        'packages':['geochart'],
        // Note: you will need to get a mapsApiKey for your project.
        // See: https://developers.google.com/chart/interactive/docs/basic_load_libs#load-settings
        'mapsApiKey': 'AIzaSyBPZTjwvR5He2Vgexve0GPy2C7HUxMsiMA'
      });
      google.charts.setOnLoadCallback(drawRegionsMap);

      function drawRegionsMap() {
        var data = google.visualization.arrayToDataTable([
          ['Provinces',   '사고횟수/인구밀도'],
          ['Chungbuk',1.5767441860465117],
          ['Chungnam',0.8949416342412452],
          ['Gangwon',2.4444444444444446],
          ['Gyeonggi',1.4926590538336053],
          ['Gyeongbuk',3.49645390070922],
          ['Gyeongnam',1.5632911392405062],
          ['Jeonbuk',1.7709251101321586],
          ['Jeonnam',2.2739726027397262],
          ['Seoul',0.17532388169151797],
          ['Daegu',0.3819419562880688],
          ['Busan',0.16941964285714287],
          ['Incheon',0.13388969521044994],
          ['Gwangju',0.10936978992997666],
          ['Daejeon',0.11430575035063113],
          ['Ulsan',0.17454545454545456],
          ['Jeju',0.47865853658536583],


        ]);

        var options = {
          region: 'KR',
          colorAxis: {colors: ['#ffffcc', '#800026']},
          backgroundColor: '#81d4fa',
          datalessRegionColor: '#ffffff',
          defaultColor: '#f5f5f5',
          resolution: 'provinces',
          enableRegionInteractivity : true
        };

        var chart = new google.visualization.GeoChart(document.getElementById('geochart-colors'));
        chart.draw(data, options);
      };
    </script>
  </head>
  <body>
    <div id="geochart-colors" style="width: 700px; height: 433px;"></div>
  </body>
</html>

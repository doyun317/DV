---
title: "차대 사람 교통사고 발생자수 트리맵"
date: 2019-12-10 03:17:30 -0400
categories: Datavisualization
---
<html>
   <head>
      <title>교통사고 발생자수 트리맵</title>
      <script type = "text/javascript" src = "https://www.gstatic.com/charts/loader.js">
      </script>
      <script type = "text/javascript" src = "https://www.google.com/jsapi">
      </script>
      <script type = "text/javascript">
         google.charts.load('current', {packages: ['treemap']});
      </script>
   </head>

   <body>
      <div id = "container" style = "width: 550px; height: 400px; margin: 0 auto">
      </div>
      <script language = "JavaScript">
         function drawChart() {
            // Define the chart to be drawn.
            var data = new google.visualization.DataTable();
            var data = google.visualization.arrayToDataTable([
               ['Location', 'Parent', '교통사교 발생횟수', '교통사고 발생횟수 (color)'],
               ['교통사고 발생지역(횟수)',    null,                 0,                               0],
               ['서울특별시',   '교통사고 발생지역(횟수)',             0,                               0],
               ['경기도',    '교통사고 발생지역(횟수)',             0,                               0],
               ['강원도',      '교통사고 발생지역(횟수)',             0,                               0],
               ['충청도',    '교통사고 발생지역(횟수)',             0,                               0],
               ['전라도',    '교통사고 발생지역(횟수)',             0,                               0],
               ['경상도',    '교통사고 발생지역(횟수)',             0,                               0],
               ['대전광역시',    '교통사고 발생지역(횟수)',             0,                               0],
               ['인천광역시',    '교통사고 발생지역(횟수)',             0,                               0],
               ['광주광역시',    '교통사고 발생지역(횟수)',             0,                               0],
               ['울산광역시',    '교통사고 발생지역(횟수)',             0,                               0],
               ['부산광역시',    '교통사고 발생지역(횟수)',             0,                               0],
               ['제주특별자치도',    '교통사고 발생지역(횟수)',             0,                               0],

               ['서울',       '서울특별시',            2869,                              2869],

               ['경기',    '경기도',             1830,                              1830],

               ['강원',     '강원도',               220,                              220],

               ['충청',     '충청도',             569,                              569],

               ['전라',     '전라도',             734,                              734],

               ['경상',     '경상도',             987,                              987],

               ['인천',     '인천광역시',             369,                              369],

               ['대전',     '대전광역시',             326,                              326],

               ['광주',     '광주광역시',             328,                              328],

               ['울산',     '울산광역시',             192,                              192],

               ['부산',     '부산광역시',             759,                              759],

               ['제주',     '제주특별자치도',             157,                              157],


            ]);
            var options = {
               minColor: '#91bfdb',
               midColor: '#ffffbf',
               maxColor: '#fc8d59',
               headerHeight: 15,
               fontColor: 'black',
               showScale: true
            };

            // Instantiate and draw the chart.
            var chart = new google.visualization.TreeMap(document.getElementById('container'));
            chart.draw(data, options);
         }
         google.charts.setOnLoadCallback(drawChart);
      </script>
   </body>
</html>

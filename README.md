# 122
<html>
  <head>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('current', {'packages':['corechart']});
      google.charts.setOnLoadCallback(drawChart);

      function drawChart() {
        var data = google.visualization.arrayToDataTable([
          ['Mittausaika', 'Ilmankosteus'],
          ['12.13',  23,  23],
          ['12.14',  24,  23],
          ['12.15',  24,  23],
          ['12.16',  25,  23]
        ]);

        var options = {
          title: 'Lämpötila',
          curveType: 'function',
          legend: { position: 'bottom' }
        };

        
        var data = google.visualization.arrayToDataTable([
          ['Mittausaika', 'Ilmankosteus'],
          ['2014', 1000, 400, 200],
          ['2015', 1170, 460, 250],
          ['2016', 660, 1120, 300],
          ['2017', 1030, 540, 350]
        ]);

        var options = {
          chart: {
            title: 'Mittausaika',
            subtitle: 'Ilmankoseteus',
          }
        };

        var chart2 = new google.charts.Bar(document.getElementById('columnchart_material'));

        chart.draw(data, google.charts.Bar.convertOptions(options));
      }
    </script>
  </head>
  <body>
    <div id="columnchart_material" style="width: 800px; height: 500px;"></div>
  </body>
</html>

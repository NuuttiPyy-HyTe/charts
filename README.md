<html>
  <head>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('current', {'packages':['corechart']});
      google.charts.setOnLoadCallback(drawChart);

      function drawChart() {

        let url='https://api.thingspeak.com/channels/1527802/feeds.json?api_key=YJNIR6VZLRL9XWXJ&results=20';

        
        var data = google.visualization.arrayToDataTable([
          ['Mittausaika', 'Lämpötila'],
          ['12.13',  23],
          ['12.14',  24],
          ['12.15',  24],
          ['12.16',  25]
        ]);

        var options = {
          title: 'Lämpötila',
          curveType: 'function',
          legend: { position: 'bottom' }
        };

        
        var data2 = google.visualization.arrayToDataTable([
          ['Mittausaika', 'Ilmankosteus'],
          ['2014', 1000],
          ['2015', 1170],
          ['2016', 660],
          ['2017', 1030]
        ]);

        var options2 = {
          chart: {
            title: 'Mittausaika',
            subtitle: 'Ilmankosteus',
          }
        };

        var chart = new google.visualization.LineChart(document.getElementById('linechart_material'));

        chart.draw(data, options);

        var chart2 = new google.visualization.ColumnChart(document.getElementById('columnchart_material'));

        chart2.draw(data2, options2);
      }
    </script>
  </head>
  <body>
    <div id="linechart_material" style="width: 800px; height: 500px;"></div>
    <div id="columnchart_material" style="width: 800px; height: 500px;"></div>
  </body>
</html>

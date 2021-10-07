<html>

<head>
  <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
  <script type="text/javascript">
    google.charts.load('current', { 'packages': ['corechart'] });
    google.charts.setOnLoadCallback(drawChart);

    async function drawChart() {
      console.log('Päivittyi');

      let url = 'https://api.thingspeak.com/channels/1527802/feeds.json?api_key=YJNIR6VZLRL9XWXJ&results=20';

      const fetchResults = await fetch(url);
      const jsonResult = await fetchResults.json();
      const feedsResults = jsonResult.feeds;

      let editRows =  [['Mittausaika', 'Lämpötila']];

      for (const i in feedsResults) {
      editRows.push([feedsResults[i].created_at, parseInt(feedsResults[i].field1.split('.')[0])]);                                       //+= " " + feedsResults[i].field1.split('.')[0];
      }

      document.getElementById("resultTable").innerHTML = editRows;

      var data = google.visualization.arrayToDataTable(editRows);

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
      setTimeout(function(){ drawChart() }, 3000);
    }
  </script>
</head>
<body>
  <div id="resultTable"></div>
  <div id="linechart_material" style="width: 800px; height: 500px;"></div>
  <div id="columnchart_material" style="width: 800px; height: 500px;"></div>

</body>

</html>

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
      let editRows2 =  [['Mittausaika', 'Ilmankosteus']];
      let editRows3 =  [['Mittausaika', 'Höyrystymispiste']];
      let editRows4 =  [['Mittausaika', 'Tuntuukuin']];
      
      for (const i in feedsResults) {
        editRows.push([feedsResults[i].created_at, parseInt(feedsResults[i].field1.split('.')[0])]);      
        editRows2.push([feedsResults[i].created_at, parseInt(feedsResults[i].field2.split('.')[0])]); 
        editRows3.push([feedsResults[i].created_at, parseInt(feedsResults[i].field3.split('.')[0])]); 
        editRows4.push([feedsResults[i].created_at, parseInt(feedsResults[i].field4.split('.')[0])]);                       
      }

      //document.getElementById("resultTable").innerHTML = editRows;

     var data = google.visualization.arrayToDataTable(editRows);

      var options = {
        title: 'Lämpötila',
        curveType: 'function',
        legend: { position: 'bottom' } 
      };


      var data2 = google.visualization.arrayToDataTable(editRows2);

      var options2 = {
        chart: {
          title: 'Mittausaika',
          subtitle: 'Ilmankosteus',
        }
      };

      var data3 = google.visualization.arrayToDataTable(editRows3);

      var options3 = {
        title: 'kiehumispiste',
        curveType: 'function',
        legend: { position: 'bottom' } 
      };

      var data4 = google.visualization.arrayToDataTable(editRows4);

      var options4 = {
        title: 'tuntuukuin',
        curveType: 'function',
        legend: { position: 'bottom' } 
      };

      var chart = new google.visualization.LineChart(document.getElementById('linechart_material'));

      chart.draw(data, options);

      var chart2 = new google.visualization.ColumnChart(document.getElementById('columnchart_material'));

      chart2.draw(data2, options2);

      var chart3 = new google.visualization.BarChart(document.getElementById('BarChart_material'));

      chart3.draw(data3, options3);

      var chart4 = new google.visualization.AreaChart(document.getElementById('AreaChart_material'));

      chart4.draw(data4, options4);

      setTimeout(function(){ drawChart() }, 3000);
    }
  </script>
</head>
<body>
  <div id="resultTable"></div>
  <div id="linechart_material" style="width: 800px; height: 500px;"></div>
  <div id="columnchart_material" style="width: 800px; height: 500px;"></div>
<div id="BarChart_material" style="width: 800px; height: 500px;"></div>
<div id="AreaChart_material" style="width: 800px; height: 500px;"></div>
</body>

</html>

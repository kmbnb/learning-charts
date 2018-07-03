# learning-charts
where I sandbox making pretty data based visuals
      google.charts.load('current', {'packages':['corechart']});
      google.charts.setOnLoadCallback(drawVisualization);

      function drawVisualization() {
        // Some raw data (not necessarily accurate)
        var data = google.visualization.arrayToDataTable([
         ['Occupation', 'Male', 'Female'],
         ['Management', 20605, 13415],
         ['Business, Finance, and Administration',  14200, 38495],
         ['Applied and Natural Sciences',  16300, 4405],
         ['Health Occupations',  4870, 25865],
         ['Education, Law and Social, Community and Government Services', 15355, 30285],
         ['Art, Culture, Recreation, and Sport', 2925, 3685],
         ['Sales and Service Occupations', 36535,  54505],
         ['Trades, transport and equipment operators and related', 57015, 2910],
         ['Natural resources, agriculture and related production', 12280, 2205],
         ['Manufacturing and Utilities', 13130, 5495]
      ]);

    var options = {
      title : 'Numberof Men and Women Employed by Occupation in NB',
      vAxis: {title: 'Number of People'},
      hAxis: {title: 'Occupation'},
      seriesType: 'bars',
      series: {5: {type: 'line'}}
    };

    var chart = new google.visualization.ComboChart(document.getElementById('chart_div'));
    chart.draw(data, options);
  }

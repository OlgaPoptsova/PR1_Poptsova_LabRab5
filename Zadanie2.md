# PR1_Poptsova_YandexMaps
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>    
 <title>Примеры. Добавление шестигранника на карту Асунсьона.</title>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>  
    <!--         Подключаем API карт 2.x
         Параметры:
           - load=package.full - полная сборка;
        - lang=ru-RU - язык русский.     -->
      <script src="http://api-maps.yandex.ru/2.0/?load=package.full&lang=ru-RU"
             type="text/javascript"></script>
     <script type="text/javascript"> 

        ymaps.ready(init); 
 
        function init() { 
            var myMap = new ymaps.Map('map', { 
                center: [-25.33, -57.66], 
                zoom: 10           
 }),            
                 
 myPolygon = new ymaps.Polygon([[
                    // Координаты вершин шестиугольника.
			[-25.25,-57.61],
			[-25.30,-57.58],
			[-25.35,-57.61],
			[-25.35,-57.65],
			[-25.30,-57.68],
			[-25.25,-57.65]
                ]]);
  
            myMap.geoObjects.add(myPolygon)
                 .add(myPolygon); 
        }     </script> 
</head>  
<body> 
<h2>Добавление шестигранника на карту Асунсьона</h2>  
<div id="map" style="width:600px;height:400px"></div> </body>  
</html>  
 

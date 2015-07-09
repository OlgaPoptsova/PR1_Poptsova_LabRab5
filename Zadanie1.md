# PR1_Poptsova_YandexMaps
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head> 
    <title>Примеры. Добавление круга на карту Рио-де-Жанейро.</title>
     <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>  
    <!--    
     Подключаем API карт 2.x  
       Параметры:          
       - load=package.full - полная сборка;   
       - lang=ru-RU - язык русский.
     -->  
       <script src="http://api-maps.yandex.ru/2.0/?load=package.full&lang=ru-RU"
       type="text/javascript"></script> 
       <script type="text/javascript">  
       // Как только будет загружен API и готов DOM, выполняем инициализацию  

       ymaps.ready(init); 

       function init() {       
       var myMap = new ymaps.Map('map', {   
              center: [-22.912154, -43.175009],   
              zoom: 10             }),   
           // Создаем первый круг   
              myCircle = new ymaps.Circle([ 
            // Задаем координаты центра круга и радиус 
                    [-22.912154, -43.175009], 
                   15000                 ]),  
            // Альтернативный способ создания круга: 
            // создаем геообъект с типом геометрии "круг". 
                myGeoObject = new ymaps.GeoObject({ 
                    // Задаем модель геообъекта.    
                  // Модель = геометрия + свойства гообъекта. 
                    // Геометрия = тип геометрии + координаты геообъекта.   
                  geometry: {         
                // Тип геометрии - круг  
                       type: "Circle",   
                      // Координаты        
                 coordinates: [         
                    [-22.912154, -43.175009],  
                           15000
                        ]               
      }        
         });  
            myMap.geoObjects.add(myCircle)   
              .add(myGeoObject);         }     
  </script>
 </head>  
<body> 
<h2>Добавление круга на карту Рио-де-Жанейро</h2>  
<div id="map" style="width:600px;height:400px"></div> </body>  
</html> 

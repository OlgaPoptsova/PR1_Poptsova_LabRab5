# PR1_Poptsova_YandexMaps
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head> 
    <title>Примеры. Добавление треугольника на карту Юкон-Коюкек.</title>
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
              center: [65.509389, -151.390021],   
              zoom: 8             }),   

            myPolygon = new ymaps.Polygon([  
           // Задаем координаты треугольника 
                             [65.509389, -151.290021],
  
                     [65.409389, -151.490021],
    
                     [65.609389, -151.490021]
            ]),  
            // Альтернативный способ создания треугольника:    
         // создаем геообъект с типом геометрии . 
                myGeoObject = new ymaps.GeoObject({ 
                    // Задаем модель геообъекта.  
                    // Модель = геометрия + свойства гообъекта. 
                    // Геометрия = тип геометрии + координаты геообъекта. 
                    geometry: {   
                      // Тип геометрии
                         type: "Polygon",
                         // Координаты    
                     coordinates: [ 
                            [65.509389, -151.290021],
  
                     [65.409389, -151.490021],
    
                     [65.609389, -151.490021]
      ]     
                }       
          });  
            myMap.geoObjects.add(myPolygon)  
               .add(myGeoObject);    
     }      
  </script>
 </head>  
<body> 
<h2>Добавление треугольника на карту Юкон-Коюкек</h2>  
<div id="map" style="width:600px;height:400px"></div> </body>  

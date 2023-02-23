<h1 style="color:blue;"> Nuevas siete maravillas del mundo moderno </h1>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/New7Wonders.jpg/414px-New7Wonders.jpg"
     alt="Monumento a la ditacias" width="400" height="453" />

   <body>

    <h1>Calculadora de Distancia Nuevas siete maravillas del mundo moderno</h1>

    <p>Su ubicación actual: <span id="location"></span></p>

    <p>Distancia Nuevas siete maravillas del mundo moderno: <span id="distance"></span></p>



    <script>

      // Obtener la ubicación actual

      navigator.geolocation.getCurrentPosition(function (position) {

        var lat1 = position.coords.latitude;

        var lon1 = position.coords.longitude;



        // La ubicación de Quito es  ??

        var lat2 = -0.0102496 ;

        var lon2 = -78.4464668;



        // Función para calcular la distancia en kilómetros

        var R = 6371; // Radio de la Tierra (km)

        var dLat = (lat2 - lat1) * (Math.PI / 180);

        var dLon = (lon2 - lon1) * (Math.PI / 180);

        var a = Math.sin(dLat / 2) * Math.sin(dLat / 2) +

                Math.cos(lat1 * (Math.PI / 180)) * Math.cos(lat2 * (Math.PI / 180)) *

                Math.sin(dLon / 2) * Math.sin(dLon / 2);

        var c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1 - a));

        var d = R * c;



        // Mostrar la distancia en la página

        document.getElementById("location").innerHTML = lat1 + ", " + lon1;

        document.getElementById("distance").innerHTML = d + " km";

      });

    </script>

  </body>

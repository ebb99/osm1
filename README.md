<!DOCTYPE html>
<html>
<head>
  <title>Einfaches Beispiel für das Einbinden einer OSM-Karte mit leaflet</title>
  <meta charset="utf-8" />
  <link rel="stylesheet"
        href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css" />
  <script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js"></script>
</head>
<body>
  <div id="map" style="height:600px; width:100%"></div>
  <script>
    var lng = 13.453408, lat = 52.516701, zoom = 15;
    var map = L.map('map').setView([lat, lng], zoom);
    L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 19,
      attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
    }).addTo(map);
  </script>
</body>
</html>


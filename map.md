---
layout: default
title: Pub Dartboard Map
---

<h1>Pub Dartboard Reviews Map</h1>

<div id="map" style="height:600px;"></div>

<link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css"/>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

<script>

var map = L.map('map').setView([51.4545, -2.5879], 12);
var dartIcon = L.divIcon({
        html: "🎯",          // Dartboard emoji
        className: "dart-icon",
        iconSize: [30, 30],       // width, height of the div
        iconAnchor: [15, 30]       // point of the icon that corresponds to the lat/lon
    });

L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; OpenStreetMap contributors'
}).addTo(map);

{% for post in site.posts %}
{% if post.lat %}
L.marker([{{ post.lat }}, {{ post.lon }}], {icon: dartIcon})
.addTo(map)
.bindPopup("<b>{{ post.pub }}</b><br><a href='{{ post.url }}'>Read review</a>");

{% endif %}
{% endfor %}

</script>
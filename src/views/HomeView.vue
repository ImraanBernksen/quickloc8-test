<template>
  <NavBar />
  <h1>Map</h1>
  <div class="home">
    <div id="map">
  
    </div>
  </div>
  <Footer/>
</template>

<script>
import NavBar from '../components/NavBar.vue';
import Footer from '@/components/Footer.vue';
import L from 'leaflet';
import vehicleCoordinates from '../vehicleCoordinates.json';

export default {
  components: {
    NavBar,
    Footer
  },
  mounted() {
    var map = L.map('map').setView([-30.5595, 22.9375], 6);

    // var osm = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
    //   attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    // });

    // osm.addTo(map);

    var googleStreets = L.tileLayer('http://{s}.google.com/vt/lyrs=m&x={x}&y={y}&z={z}', {
      maxZoom: 20,
      subdomains: ['mt0', 'mt1', 'mt2', 'mt3']
    });

    googleStreets.addTo(map);

    var myIcon = L.icon({
    iconUrl: 'https://i.postimg.cc/P5qCgC95/ic-new-white-taxi.png',
    iconSize: [50, 50]});

    vehicleCoordinates.forEach(coord => {
      var singleMarker = L.marker([coord.latitude, coord.longitude], { icon: myIcon });
      var popup = singleMarker.bindPopup(coord.heading).openPopup();
      popup.addTo(map);
    });

  }
}
</script>
    
<style scoped>
.home {
  padding-top: 20px;
  padding-bottom: 20px;
}
#map {
  width: 98%;
  height: 100vh;
  margin: auto;
  border: 2px solid white;
  border-radius: 10px;
}
</style>

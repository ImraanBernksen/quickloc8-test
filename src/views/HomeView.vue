<template>
  <NavBar/>
  <h1>Welcome to QuickLoc8</h1>
  <div class="home">
    <!-- <mgl-map mapStyle="https://api.maptiler.com/maps/streets-v2/style.json?key=UJIHfP1Le2KEUnI1YoD1" :zoom=14
    :center="[8.7832, 34.5085]" style="width: 100%; height: 600px;">
    <mgl-marker :coordinates="[30.5595, 22.9375]" color="#42b883"/>
    <mgl-navigation-control position="top-left" />
  </mgl-map> -->
  </div>
</template>

<script>
import NavBar from '../components/NavBar.vue';
import { MglMap, MglNavigationControl, MglMarker } from 'vue-maplibre-gl';
export default {
  name: 'TaxiMap',
  components: {
    NavBar,
    MglMap,
    MglNavigationControl,
    MglMarker
  }
}
</script>
    
<style scoped>
body {
  margin-bottom: 40px;
}

</style>

<template>
  <div id="app">
    <l-map class="map" :zoom="zoom" :center="center">
      <l-tile-layer :url="url" :attribution="attribution"></l-tile-layer>
    </l-map>
  </div>
</template>

<script>
//import Vue from 'vue';
import { LMap, LTileLayer, } from 'vue2-leaflet';

export default {
  name: 'App',
  components: {
    LMap,
    LTileLayer,
  },
  data () {
    return {
      zoom: 9,
      center: [28.5383, -81.3792],
      url:'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      attribution:'&amp;copy <a href=&quot;http://osm.org/copyright&quot;>OpenStreetMap</a> contributors',
    }
  }
};
</script>

<style>
@import "./../node_modules/leaflet/dist/leaflet.css";
body {
 height: 100vh;
 width: 100vw;
}
#app{
height: 100%;
}
.map{
  height:100%;;
}
</style>

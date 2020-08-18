<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div id="map" width="300px"></div>;
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function () {
    return {
      message: "This is a Map",
    };
  },
  mounted: function () {
    mapboxgl.accessToken = process.env.VUE_APP_MAPBOX_KEY;
    var map = new mapboxgl.Map({
      container: "map", // container id
      style: "mapbox://styles/mapbox/streets-v11", // style URL
      center: [-74.5, 40], // starting position [lng, lat]
      zoom: 9, // starting zoom
    });
  },
  methods: {},
};
</script>

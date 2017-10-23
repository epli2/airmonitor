<template>
  <div class="google-map" id="map">map error</div>
</template>

<script>
/* global google */
export default {
  name: 'googlemap',
  data () {
    return {
      map: null,
      markerStart: null,
      markerSet: []
    }
  },
  mounted: function () {
    const element = document.getElementById('map')
    const startpoint = { lat: 35.289234, lng: 136.252167 }
    const options = {
      zoom: 11,
      center: startpoint
    }
    this.map = new google.maps.Map(element, options)
    this.markerStart = new google.maps.Marker({
      position: startpoint,
      map: this.map
    })
    this.markerSet.push(new google.maps.Marker({
      position: new google.maps.LatLng(35.3, 136.2),
      map: this.map
    }))
  }
}
</script>

<style scoped>
.google-map {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  background: gray;
}
</style>
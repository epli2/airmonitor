<template>
  <div class="pilot">
    <div class="row">
      <div class="col-md-4">
        <meter-pilot></meter-pilot>
      </div>
      <div class="col-md-8">
        <google-map></google-map>
      </div>
    </div>
  </div>
</template>

<script>
import MeterPilot from '@/components/MeterPilot'
import GoogleMap from '@/components/GoogleMap'

export default {
  name: 'pilot',
  components: {
    'meter-pilot': MeterPilot,
    'google-map': GoogleMap
  }
}
</script>

<style>
.pilot {
  height: 100%;
}
.row {
  height: 100%;
}
</style>

<template>
  <div class="meter">
    <div class="container vert-center">
      <div class="col align-content-center">
        <div class="alert alert-success" role="alert">
          <div class="text-center"> 気速 {{ speed }} m/s </div>
        </div>
      </div>
      <div class="col align-content-center">
        <div class="alert alert-danger" role="alert">
          <div class="text-center"> 回転数 {{ spin }} rpm </div>
        </div>
      </div>
      <div class="col align-content-center">
        <div class="alert alert-warning" role="alert">
          <div class="text-center"> 高度 {{ height }} m </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'meter-pilot',
  data () {
    return {
      speed: 'N/A',
      spin: 'N/A',
      height: 'N/A'
    }
  }
}
</script>

<style scoped>
.vert-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
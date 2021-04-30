<template>
  <div class="image_wheel">
    <img class="rot" src="../assets/images/wheel.png" alt="wheel">
  </div>
</template>


<script>

export default {
  name: "Wheel"
}
</script>

<style scoped>
img{
  width: 338px;
  height: 338px;
  animation-name: spin;
  animation-duration: 18000ms;
  animation-iteration-count: infinite;
  animation-timing-function: linear;

}

@keyframes spin {
  from { transform:rotate(0deg); }
  to { transform:rotate(360deg); }
}




</style>

<template>
  <wheel></wheel>
  <betting-field></betting-field>

</template>

<script>
import BettingField from "./components/BettingField";
import Wheel from "./components/Wheel";

export default {
  name: 'App',
  components: {
    BettingField,
    Wheel
  }
}
</script>

<style>
*{
  box-sizing: border-box;
}
body{
  margin: 0 auto;
  background: #131313;
  color: #FFFFFF;
}
button {
  padding: 0;
  border: none;
  font: inherit;
  color: inherit;
  background-color: transparent;
}
</style>

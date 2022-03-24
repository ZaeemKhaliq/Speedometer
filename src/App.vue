<template>
  <div class="root">
    <h1>SPEEDOMETER</h1>
    <br />
    <Speedometer />
  </div>
</template>

<script>
import Speedometer from "@/components/Speedometer.vue";

export default {
  name: "App",
  components: {
    Speedometer,
  },
};
</script>

<style lang="scss">
.root {
  font-family: Roboto, sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: black;
}
</style>

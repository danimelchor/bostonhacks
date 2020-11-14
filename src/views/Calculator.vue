<template>
  <div class="calculator">
    <h1>Calculator</h1>
    <Map />
  </div>
</template>

<style lang="scss" scoped></style>

<script>
import Map from "@/components/map.vue";

export default {
  name: "Calculator",
  components: {
    Map
  }
};
</script>

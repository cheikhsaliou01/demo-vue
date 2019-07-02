<template>
  <v-layout id="container">
    <LeftSide/>
    <RightSide/>
  </v-layout>
</template>

<script>
import LeftSide from "./leftSide/LeftSide";
import RightSide from "./rightSide/RightSide";

export default {
  name: "container",
  components: {
      LeftSide,
      RightSide
  }
};
</script>

<style>
#container {
  background: white;
}
</style>

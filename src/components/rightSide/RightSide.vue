<template>
  <v-flex sm3 id="right-side">
    <v-layout>
      <v-flex id="right-header" sm12></v-flex>
    </v-layout>
  </v-flex>
</template>

<script>
export default {
  name: "RightSide"
};
</script>

<style>
#right-header {
  height: 45px;
  -webkit-box-shadow: -1px 5px 5px -5px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: -1px 5px 5px -5px rgba(0, 0, 0, 0.75);
  box-shadow: -1px 5px 5px -5px rgba(0, 0, 0, 0.75);
}
#right-side {
  background: white;
  height: 700px;
  -webkit-box-shadow: -5px -2px 5px -6px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: -5px -2px 5px -6px rgba(0, 0, 0, 0.75);
  box-shadow: -5px -2px 5px -6px rgba(0, 0, 0, 0.75);
}
</style>

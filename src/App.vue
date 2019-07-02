<template>
  <v-app id="app">
    <v-container id="app-container" >
      <Container />
    </v-container>
  </v-app>
</template>

<script>
import Container from './components/Container'
export default {
  name: "app",
  components: {
    Container
  }
};
</script>

<style>
#app {
  background-image: url("./assets/background.jpg");
  min-height: 100vh;
}

#app > #app-container {
  background: #fff;
}
</style>

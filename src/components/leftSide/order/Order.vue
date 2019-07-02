<template>
  <v-layout class="order">
    <v-flex sm12>
      <v-layout id="cont1">
        <v-flex sm2 class="order-image">
          <img :src="getImageUrl(order.image)" alt height="50">
        </v-flex>
        <v-flex sm8>
          <v-flex class="font-weight-bold">{{ order.name}}</v-flex>
          <v-flex>
            <img src="../../../assets/device.png">
            {{ order.price }} py6.
          </v-flex>
          <v-flex>
            <img src="../../../assets/hours.png"> 6 нбр., 13:00 - 7 нбр., 14:00
          </v-flex>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  name: "Order",
  props: {
    order: Object
  },
  methods: {
    getImageUrl(url) {
      return require("../../../assets/" + url);
    }
  }
};
</script>

<style>
.order {
  margin-bottom: 10px;
}

.order-image {
    padding-left: 20px;
    padding-bottom: 3px;
}
#cont1{
  width: 460px;
  margin-left: -140px;
  margin-bottom: 15px;
}
</style>

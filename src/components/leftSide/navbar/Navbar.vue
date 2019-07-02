<template>
  <v-layout id="left-side">
    <v-flex sm8>
      <img src="../../../assets/order.png" alt class="order-logo">
     <p id="com1"> Заказы </p>
    </v-flex>
    <v-flex sm10>
      <v-tabs>
        <v-tab v-for="nav in navs" :key="nav.id + '-nav'">
          {{ nav.name }}
          <v-btn fab dark small color="primary">+{{nav.count}}</v-btn>
        </v-tab>
        <v-tabs-items>
          <NavbarItem v-for="item in items" :item="item" :key="item.id + '-item'"/>  
        </v-tabs-items>
      </v-tabs>
    </v-flex>
  </v-layout>
</template>

<script>
import NavbarItem from "./NavbarItem";

export default {
  name: "Navbar",
  components: {
    NavbarItem
  },
  data: () => {
    return {
      navs: [
        { id: 1, name: "Лента", count: 3 },
        { id: 2, name: "Созданные", count: 3 },

        { id: 3, name: "Мои отклики", count: 4 }
      ],
      items: [
        { id: 1, content: "dqshdqsjddqsjdqdlkdqds" },
        { id: 2, content: "dqshdqsjddqsjdqdlkdqds" },
        { id: 3, content: "dqshdqsjddqsjdqdlkdqds" },
      ]
    };
  }
};
</script>

<style>
.order-logo{
    margin-left: 60px;
    display:inline-block;
}
#com1{
    margin-left: 115px;
    margin-top: -30px;
}
#left-side{
    margin-right: 60px;
}
</style>

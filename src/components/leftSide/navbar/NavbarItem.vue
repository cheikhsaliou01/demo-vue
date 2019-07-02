<template>
  <fragment>
    <v-tab-item>
      <v-card flat>
        <v-card-text>
          <div id="under-navbar">
            <v-layout class="search" >
              <v-flex sm1>
                <img src="../../../assets/tools.png" height="22" id="tool-image">
              </v-flex>
              <v-flex
                class="under-navbar-button blue--text font-weight-bold"
                sm2
                align-content-center
              ><p id="nov"> Новые </p></v-flex>
              <v-flex class="under-navbar-button" sm4 align-content-center>Цена (по возрастанию)</v-flex>
              <v-flex class="under-navbar-button" sm4 align-content-center>Цена (по убыванию)</v-flex>
              <v-flex class="under-navbar-button" sm2 align-content-center>Срочные</v-flex>
            </v-layout>
          </div>
        <!--
          <v-layout class="search" > 
          <v-text-field append-icon="search" class="mx-3" flat label="поиск" solo-inverted  single-line>
            </v-text-field>
          </v-layout>
          -->
        <div class="wrap">
          <div class="search-input">
            <input type="text" placeholder="Поиск"/> 
            <div class="trapec">
              <div>
                  <div>
                    <img src="../../../assets/group.png" alt="" id="group1">
                  </div>
                </div>
            </div>
          </div>
          
        </div>
       </v-card-text>
        <Order v-for="order in orders" :order="order" :key="order.id +'-order'"/>
      </v-card>
    </v-tab-item
    >
  </fragment>
</template>
<script>
import Order from "../order/Order";

export default {
  name: "NavbarItem",
  props: {
    item: Object
  },
  components: {
    Order
  },
  data: () => {
    return {
      orders: [
        {
          id: 1,
          name: "Убрать квартиру в большом помещении",
          price: "1000",
          image: "order-1.png"
        },
        {
          id: 2,
          name: "Убрать квартиру в большом помещении",
          price: "1000",
          image: "order-2.png"
        },
        {
          id: 3,
          name: "Убрать квартиру в большом помещении",
          price: "1000",
          image: "order-3.png"
        },
        {
          id: 4,
          name: "Убрать квартиру в большом помещении",
          price: "1000",
          image: "order-4.png"
        },
        {
          id: 5,
          name: "Убрать квартиру в большом помещении",
          price: "1000",
          image: "order-1.png"
        }
      ]
    };
  }
};
</script>

<style>
#under-navbar {
  width: 483px;
  height: 35px;
  background: white;
  -webkit-box-shadow: 3px 1px 5px -2px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 3px 1px 5px -2px rgba(0, 0, 0, 0.75);
  box-shadow: 3px 1px 5px -2px rgba(0, 0, 0, 0.75);
  margin-right: 250px;
}

#tool-image {
  display: inline;
  margin-top: 1px;
  width: 39px;
}

.search {
  margin-top: 20px;
  width: 546px;
  margin-left: -130px;
}
.wrap {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
  position: relative;
  /* overflow: hidden; */
  z-index: 94;
  margin-left: -19%;
  margin-top: 10px;
}
.search-input {
  width: 748px;
  border: 1px solid #aeaeae;
  border-right: none;
  position: relative;
  height: 50px;
  display: flex;
  align-items: center;

}
.trapec {
  position: relative;
  height: 50px;
  width: 60px;
  z-index: 92;
  overflow: unset;
  position: absolute;
  right: -30px;
  top: 0;
  margin-left: 0px;
}
.trapec > div {
  transform: skew(45deg);
  border: 1px solid #aeaeae;
  height: 50px;
  width: 100%;
  /* box-shadow: 0px 2px 5px 0; */
  top: -2px;
  /* left: 0; */
  position: absolute;
  background-color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 98;
  overflow: unset;
}
.trapec > div > div {
  transform: skew(-45deg);

}
#trapez{
    transform: skew(deg);
}

.under-navbar-button{
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
}
#form1{
  margin-left: -150px;
  width:700px;
  height: 45px;
}
#group1{
 margin-top: 13px;
}
#nov{
  width: 57px;
  margin-left: 15px;
  height: 25px;
}
</style>
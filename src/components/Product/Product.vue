<template>
  <v-conteiner>
    <div class="d-flex mb-6 pb-6">
      <v-spacer></v-spacer>
      <div>
        <Product_Images />
      </div>
      <div id="center" class="mx-6">
        <h3 id="subTitle">Sneaker Company</h3>
        <h1 class="mx-auto">Fall Limited Edition Sneaker</h1>
        <p class="mx-auto">
          Try estimating the time it will take for you to build the project.
          Then see if the time taken matches up to your estimate. Project
          estimations are a skill that is often overlooked, but is important for
          professional developers
        </p>
        <div class="d-flex">
          <h2>{{ Price }}</h2>
          <v-card color="red pa-2 mx-3">
            <h4>50%</h4>
          </v-card>
        </div>
        <del class="d-flex mb-6 pb-6">{{ discount }}</del>
        <div class="d-flex">
          <v-btn @click="decreaseCounter">-</v-btn>
          <v-btn width="50" disabled text>{{ count }}</v-btn>
          <v-btn width="50" @click="incremetCounter">+</v-btn>

          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                color="orange"
                v-bind="attrs"
                v-on="on"
                elevation="7"
                width="250"
                height="37"
                class="mx-auto"
              >
                <v-icon> mdi-cart </v-icon> Add to Cart
              </v-btn>
            </template>
            <span>Add to cart</span>
          </v-tooltip>
        </div>
      </div>
    </div>
  </v-conteiner>
</template>

<script>
import Product_Images from "./Product_Images.vue";

export default {
  data: () => ({
    Price: "$125.00",
    count: 0,
    discount: "$250.00",
  }),
  methods: {
    incremetCounter: function() {
      this.count++;
    },
    decreaseCounter: function() {
      if (this.count > 0) {
        this.count = this.count - 1;
      }
    },
  },
  components: {
    Product_Images,
  },
};
</script>

<style>
#center {
  margin: auto;
  width: 50%;
  padding: 10px;
}
#product {
  color: navy;
  text-indent: 30px;
  display: flex;
  text-align: center;
  width: 35%;
  padding: 70px;
}
#subTitle {
  color: coral;
}
</style>

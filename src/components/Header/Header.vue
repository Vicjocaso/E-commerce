<template>
  <v-container>
    <v-app>
      <v-app-bar max-height="60" max-width="1200">
        <div>
          <a href="/">
            <v-img
              alt="Sneaker"
              class="shrink mr-2"
              contain
              src="./logo.svg"
              transition="scale-transition"
              width="100"
            />
          </a>
        </div>
        <div id="font" class="d-flex align-center mx-6">
          <div class="d-flex align-center mx-6">
            <button>Collections</button>
          </div>
          <div class="d-flex align-center mx-6">
            <button>Men</button>
          </div>
          <div class="d-flex align-center mx-6">
            <button>Women</button>
          </div>
          <div class="d-flex align-center mx-6">
            <button>About</button>
          </div>
          <div class="d-flex align-center mx-6">
            <button>Contact</button>
          </div>
        </div>
        <v-spacer></v-spacer>
        <div class="d-flex align-center">
          <div class="d-flex align-center mx-6">
            <v-icon>
              mdi-cart
            </v-icon>
          </div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn v-bind="attrs" v-on="on" rounded icon width="40">
                <v-img
                  alt="Account"
                  contain
                  src="./image-avatar.png"
                  transition="scale-transition"
                  width="30"
                />
              </v-btn>
            </template>
            <span>Account</span>
          </v-tooltip>
        </div>
      </v-app-bar>
      <Product />
    </v-app>
  </v-container>
</template>

<script>
import Product from "../Product/Product.vue";

export default {
  data: () => ({
    items: [],
  }),
  components: {
    Product,
  },
};
</script>

<style>
#font {
  font-family: "Courier New", Courier, monospace;
}
</style>

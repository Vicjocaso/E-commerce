<template>
  <conteiner>
    <div class="d-flex flex-row mb-6 pb-6">
      <v-spacer></v-spacer>
      <v-card max-width="344" class="mb-6" outlined>
        <v-img class="p-5" src="./image-product-1.jpg"></v-img>
      </v-card>
      <div class="mx-6">
        <h1>Fall Limited Edition Sneaker</h1>
        <p id="productp">
          Your challenge is to build out this e-commerce product page and get it
        </p>
        <v-spacer></v-spacer>
      </div>
    </div>
  </conteiner>
</template>

<script>
export default {
  data: () => ({
    loading: false,
    selection: 1,
  }),

  methods: {
    reserve() {
      this.loading = true;

      setTimeout(() => (this.loading = false), 2000);
    },
  },
};
</script>

<style>
#center {
  margin: auto;
  width: 50%;
  padding: 10px;
}
#productp {
  color: navy;
  text-indent: 30px;
}
</style>

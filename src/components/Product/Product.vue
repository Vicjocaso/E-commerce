<template>
  <v-card id="center" class="mx-auto my-12" max-width="374">
    <v-img height="250" src="./image-product-1.jpg"></v-img>
  </v-card>
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
</style>

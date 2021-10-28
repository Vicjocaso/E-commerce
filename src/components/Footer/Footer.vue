<template>
  <footer>
    <v-card-actions class="justify-center">
      <v-btn
        v-for="(social, i) in socials"
        :key="i"
        :color="social.color"
        class="white--text"
        fab
        icon
        small
      >
        <v-icon>{{ social.icon }}</v-icon>
      </v-btn>
    </v-card-actions>
  </footer>
</template>

<script>
export default {
  data: () => ({
    types: ["Places to Be", "Places to See"],
    cards: ["Good", "Best", "Finest"],
    socials: [
      {
        icon: "mdi-facebook",
        color: "indigo",
      },
      {
        icon: "mdi-linkedin",
        color: "cyan darken-1",
      },
      {
        icon: "mdi-instagram",
        color: "red lighten-3",
      },
    ],
  }),
};
</script>

<style></style>

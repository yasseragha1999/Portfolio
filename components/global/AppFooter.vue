<template>
  <v-footer class="footer mt-16 py-0" color="primary">
    <v-container>
      <v-row class="align-center justify-space-between">
        <v-col cols="12" md="4" class="text-center text-md-left mb-4 mb-md-0">
          <strong>© 2025 MyPortfolio</strong><br />
          Crafted with ❤️ using Nuxt & Vuetify
        </v-col>

        <v-col
          cols="12"
          md="4"
          class="mb-4 mb-md-0 d-flex justify-center justify-md-end"
          style="gap: 20px"
        >
          <v-btn icon @click="goToGitHub" target="_blank">
            <v-icon>mdi-github</v-icon>
          </v-btn>
          <v-btn icon @click="goToFLinkedIn" target="_blank">
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  methods: {
    goToGitHub() {
      window.open("https://github.com/yasseragha1999", "_blank");
    },
    goToFLinkedIn() {
      window.open(
        "https://www.linkedin.com/in/yasser-agha-4a3962278/",
        "_blank"
      );
    },
  },
};
</script>

<style scoped>
.footer {
  color: #ffffff;
  font-size: 0.9rem;
}
a {
  color: #90caf9;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>

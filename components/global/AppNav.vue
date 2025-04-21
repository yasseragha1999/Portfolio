<template>
  <v-app-bar app color="primary" dark flat>
    <v-container>
      <v-row class="justify-space-between align-center">
        <v-col cols="6" md="2">
          <v-toolbar
            style="background-color: transparent; cursor: pointer"
            color="primary"
            title="Y𝓪𝓼𝓼𝓮𝓻ツ"
            class="pa-0"
          ></v-toolbar>
        </v-col>

        <v-col cols="6" md="3">
          <div class="icon-nav justify-end d-flex" style="gap: 20px">
            <v-icon
              @click="goToFLinkedIn"
              style="font-size: 30px; cursor: pointer"
              >mdi-linkedin</v-icon
            >
            <v-icon @click="goToGitHub" style="font-size: 30px; cursor: pointer"
              >mdi-github</v-icon
            >
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-app-bar>
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
.nav-links {
  list-style: none;
  gap: 24px;
}

.nav-links li {
  font-weight: 600;
  font-size: 16px;
  color: white;
  cursor: pointer;
  transition: color 0.3s ease;
}

.nav-links li:hover {
  color: #ffcc00;
}

@media (max-width: 960px) {
  .nav-links {
    flex-direction: column;
    gap: 12px;
  }
}
</style>

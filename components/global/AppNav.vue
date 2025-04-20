<template>
  <div class="navbar">
    <v-app-bar>
      <v-container>
        <v-row class="justify-space-between align-center">
          <v-col cols="2">
            <div class="img-nav">
              <img
                style="cursor: pointer"
                src="/public/logo.png"
                class="w-25 mt-3"
                alt="yasser-porfolio"
                :to="{ name: 'index' }"
              />
            </div>
          </v-col>
          <v-col cols="4">
            <ul
              class="d-flex align-center justify-space-between"
              style="list-style: none"
            >
              <nuxt-link to=""><li>Fokir</li></nuxt-link>
              <nuxt-link to=""><li>DeFolio</li></nuxt-link>
              <nuxt-link to=""><li>Danils</li></nuxt-link>
              <nuxt-link to=""><li>Bakery</li></nuxt-link>
            </ul>
          </v-col>
          <v-col cols="3">
            <div class="icon-nav justify-end d-flex" style="gap: 20px">
              <v-icon
                @click="goToFLinkedIn"
                style="font-size: 30px; cursor: pointer"
                >mdi-linkedin</v-icon
              >
              <v-icon
                @click="goToGitHub"
                style="font-size: 30px; cursor: pointer"
                >mdi-github</v-icon
              >
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  methods: {
    goToGitHub() {
      window.location.href = "https://github.com/yasseragha1999";
    },

    goToFLinkedIn() {
      window.location.href =
        "https://www.linkedin.com/in/yasser-agha-4a3962278/";
    },
  },
};
</script>

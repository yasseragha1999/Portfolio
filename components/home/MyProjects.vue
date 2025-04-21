<template>
  <div class="all-project">
    <div class="title text-center">
      <v-card-title class="pl-0">𝓟𝓻𝓸𝓳𝓮𝓬𝓽</v-card-title>
    </div>
    <v-container class="mt-12">
      <v-row class="d-flex" :justify="isMobile ? 'start' : 'center'">
        <v-col
          cols="12"
          sm="6"
          md="3"
          v-for="(image, index) in projectImages"
          :key="index"
        >
          <v-card
            class="pa-4 project-card"
            elevation="4"
            style="border-radius: 30px; height: 260px"
          >
            <v-img
              :src="image"
              class="mb-4 rounded-lg w-100"
              height="250"
              style="border-radius: 50%"
              cover
            />
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMobile: false,
      projectImages: [
        "/Daniels.jpg",
        "/Bakery.jpg",
        "/DevFolio.jpg",
        "/Fokir.jpg",
      ],
    };
  },
  mounted() {
    this.checkMobile();
    window.addEventListener("resize", this.checkMobile);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.checkMobile);
  },
  methods: {
    checkMobile() {
      this.isMobile = window.innerWidth <= 600;
    },
  },
};
</script>

<style scoped>
.project-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.title {
  font-size: 3rem;
}

@media (max-width: 600px) {
  .title {
    font-size: 2rem;
  }

  .project-card {
    margin-bottom: 20px;
  }
}

@media (max-width: 960px) {
  .title {
    font-size: 2.5rem;
  }
}
</style>

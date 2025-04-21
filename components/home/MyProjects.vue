<template>
  <div class="all-project">
    <div class="title text-center">
      <v-card-title class="pl-0" style="font-size: 45px; font-weight: 900"
        >𝓟𝓻𝓸𝓳𝓮𝓬𝓽</v-card-title
      >
    </div>
    <v-container class="mt-12">
      <v-row class="d-flex" :justify="isMobile ? 'start' : 'start'">
        <v-col
          cols="12"
          sm="6"
          md="4"
          v-for="(project, index) in projectImages"
          :key="index"
        >
          <v-card
            class="pa-16 project-card"
            elevation="24"
            style="
              border-radius: 20px;
              height: auto;
              cursor: pointer;
              transition: transform 0.3s ease, box-shadow 0.3s ease;
            "
            @click="openProject(project.route)"
            @mouseover="hover = index"
            @mouseleave="hover = null"
            :style="
              hover === index
                ? 'transform: translateY(-5px); box-shadow: 0 12px 24px rgba(0,0,0,0.1)'
                : ''
            "
          >
            <v-img
              :src="project.image"
              class="w-100"
              height="250"
              cover
              style="border-radius: 0 75px"
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
      hover: null,
      projectImages: [
        { image: "/Daniels.jpg", route: "https://daniels-iota.vercel.app" },
        { image: "/Bakery.jpg", route: "https://bakery-pearl-six.vercel.app" },
        {
          image: "/DevFolio.jpg",
          route: "https://devfolio-steel-one.vercel.app",
        },
        { image: "/Fokir.jpg", route: "https://fokir-lake.vercel.app" },
        { image: "/furqan.jpg", route: "https://furqan-kappa.vercel.app" },
        { image: "/ella.jpg", route: "https://ella-ecommerce.vercel.app" },
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
    openProject(url) {
      window.open(url, "_blank");
    },
  },
};
</script>

<style scoped>
.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
}
</style>

<template>
  <div class="desc mt-5">
    <v-container>
      <v-row class="d-flex justify-space-between  align-center mt-16">
        <v-col cols="5" class="d-flex justify-end pr-8">
          <v-card class="elevation-10" width="450" height="450" tile shaped>
            <v-img src="/public/main.jpg" height="100%" cover></v-img>
          </v-card>
        </v-col>
        <v-col cols="6" class="pl-8">
          <v-card elevation="0">
            <v-card-title class="px-0" style="font-size: 25px; font-weight: 900"
              >Front-End Developer</v-card-title
            >
            <v-card-text class="px-0" style="font-size: 18px; font-weight: 600"
              >KeyWords:</v-card-text
            >
            <ul
              style="list-style: decimal; gap: 50px"
              class="d-flex align-center pl-8"
            >
              <li>Html</li>
              <li>Css</li>
              <li>JS</li>
            </ul>
            <v-card-text class="px-0" style="font-size: 18px; font-weight: 600"
              >FrameWork:</v-card-text
            >
            <ul
              style="list-style: decimal; gap: 50px"
              class="d-flex align-center pl-8"
            >
              <li>React.JS</li>
              <li>Next.JS</li>
              <li>Vue.JS</li>
              <li>Nuxt.JS</li>
            </ul>
            <v-card-text class="px-0" style="font-size: 18px; font-weight: 600"
              >UI Component Library:</v-card-text
            >
            <ul
              style="list-style: decimal; gap: 50px"
              class="d-flex align-center pl-8"
            >
              <li>Material UI (MUI)</li>
              <li>Vuetify</li>
              <li>Bootstrap</li>
              <li>Tailwind UI</li>
            </ul>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style scoped>
.v-card {
  border-radius: 20px;
  overflow: hidden;
  transition: transform 0.3s ease;
}
.v-card:hover {
  transform: scale(1.05);
}
</style>

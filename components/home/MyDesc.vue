<template>
  <div class="desc mt-5">
    <div class="image-cover">
      <v-container>
        <v-row
          class="d-flex justify-space-between align-center mt-16"
          align="center"
        >
          <!-- Image Card -->
          <v-col
            cols="12"
            md="5"
            class="d-flex justify-center justify-md-end pr-md-8 mb-6 mb-md-0"
          >
            <v-card
              class="elevation-10 d-flex align-center justify-center overflow-hidden"
              width="100%"
              max-width="450"
              height="450"
              style="border-radius: 30px 75px 30px 75px"
            >
              <v-img
                src="/public/main.jpg"
                cover
                height="100%"
                width="100%"
                class="transition-slow"
              ></v-img>
            </v-card>
          </v-col>

          <!-- Text Card -->
          <v-col cols="12" md="6" class="pl-md-8 text-white">
            <v-card
              elevation="0"
              color="#212121"
              class="pa-8 pa-md-16"
              style="width: 100%; max-width: 600px"
            >
              <v-card-title
                class="px-0 pb-4 pb-md-6"
                style="font-size: 22px; font-weight: 900"
              >
                ~-- Front-End Developer --~
              </v-card-title>

              <v-card-text
                class="px-0"
                style="font-size: 17px; font-weight: 600"
              >
                KeyWords:
              </v-card-text>
              <ul class="keyword-list pl-6 pl-md-8">
                <li>Html</li>
                <li>Css</li>
                <li>JS</li>
              </ul>

              <v-card-text
                class="px-0"
                style="font-size: 17px; font-weight: 600"
              >
                FrameWork:
              </v-card-text>
              <ul class="keyword-list pl-6 pl-md-8">
                <li>React.JS</li>
                <li>Next.JS</li>
                <li>Vue.JS</li>
                <li>Nuxt.JS</li>
              </ul>

              <v-card-text
                class="px-0"
                style="font-size: 17px; font-weight: 600"
              >
                UI Component Library:
              </v-card-text>
              <ul class="keyword-list pl-6 pl-md-8">
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
  </div>
</template>

<style scoped>
.desc {
  position: relative;
}

.image-cover {
  position: relative;
  height: 100%;
  min-height: 80vh;
  overflow: hidden;
}

/* Background layer */
.image-cover::before {
  content: "";
  background-image: url(/public/image-cover.png);
  background-size: cover;
  background-position: center top;
  opacity: 0.9;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

/* Ensure content appears above background */
.v-container {
  position: relative;
  z-index: 2;
}

/* Hover effect for image card */
.v-card {
  border-radius: 20px;
  overflow: hidden;
  transition: transform 0.3s ease-in-out;
  z-index: 5;
  opacity: 1 !important;
}

.v-card:hover {
  transform: scale(1.05);
}

/* Responsive spacing for keyword lists */
.keyword-list {
  display: flex;
  flex-wrap: wrap;
  gap: 12px 24px;
  margin-bottom: 16px;
}

/* List reset */
.keyword-list li {
  list-style: decimal;
  font-size: 16px;
}

/* Responsive tweaks for text */
@media (max-width: 600px) {
  .v-card-title {
    font-size: 20px !important;
  }

  .keyword-list li {
    font-size: 15px;
  }
}
</style>

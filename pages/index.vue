<template>
  <div class="home-page">
    <MyDesc />
    <MyProjects />
    <AppFooter />
  </div>
</template>

<script setup>
import MyDesc from "~/components/home/MyDesc.vue";
import MyProjects from "~/components/home/MyProjects.vue";
useSeoMeta({
  title: "Yasser-Agha",
});
</script>

<template>
  <div class="home-page">
    <MyDesc />
    <MyProjects />
    <MySkills />
    <AppFooter />
  </div>
</template>

<script setup>
import MyDesc from "~/components/home/MyDesc.vue";
import MyProjects from "~/components/home/MyProjects.vue";
import MySkills from "../components/home/MySkills.vue";
useSeoMeta({
  title: "Yasser-Agha",
});
</script>

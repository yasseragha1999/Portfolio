<template>
  <div class="layout">
    <v-layout class="ma-0 pa-0" style="min-height: 100vh">
      <AppNav />
      <v-main class="ma-0 pa-0" style="padding-top: 0">
        <slot></slot>
      </v-main>
      <!-- <AppFooter /> -->
    </v-layout>
  </div>
</template>

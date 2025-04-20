<template>
  <div class="layout">
    <v-layout>
      <AppNav />
      <v-main style="padding-top: 49px">
        <slot></slot>
      </v-main>
      <AppFooter />
    </v-layout>
  </div>
</template>

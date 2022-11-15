<script setup>
import { RouterView } from 'vue-router';
import Navbar from './components/layouts/NavbarView.vue';
</script>

<template>
  <Navbar/>

  <RouterView />
</template>

<style>
@import "@/assets/css/styles.css";
</style>

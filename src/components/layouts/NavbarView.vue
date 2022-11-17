<script setup>
import { RouterLink } from "vue-router";
import Logo from "./LogoView.vue";
import Navigation from "./NavigationView.vue";
import UserInfo from "./UserInfoView.vue";
import AuthButton from "./AuthButton.vue"
</script>

<template>
  <nav
    class="mx-auto max-w-7xl bg-white border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-800"
  >
    <div
      class="container flex flex-wrap items-center justify-between mx-auto my-2"
    >
      <logo/>
      <AuthButton/>
      <!-- <UserInfo/> -->
      <Navigation/>
    </div>
  </nav>
</template>

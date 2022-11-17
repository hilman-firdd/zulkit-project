<script setup>
import { ref } from 'vue';
import Items from './../ItemsCard.vue';

const items = ref([
  {
    id: 1,
    title: "Mobile UI Kit", 
    subtitle: "Mobile UI Kit", 
    image: "items-1.jpg"
  },
  {
    id: 2,
    title: "Online Doctor Consultation", 
    subtitle: "Website UI Kit", 
    image: "items-2.jpg"
  },
  {
    id: 3,
    title: "Banking Crypto", 
    subtitle: "Mobile UI Kit", 
    image: "items-3.jpg"
  }
]);

</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
      <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
      <div class="flex flex-wrap -mx-1 lg:-mx-4">
        <Items 
        v-for="item in items"
        :id="item.id"
        :key="item.id"
        :title="item.title"
        :subtitle="item.subtitle"
        :image="item.image"
        />
      </div>
    </div>
</template>
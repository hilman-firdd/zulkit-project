<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';
import CategoriesCard from './../CategoriesCard.vue';

const categories = ref([]);
async function getCatagoriesData(){
  const res = await axios.get('https://zullkit-backend.buildwithangga.id/api/categories?show_product=1');
  categories.value = res.data.data.data
}


onMounted(() => {
  getCatagoriesData();
});

</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12" id="categories">
      <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
      <div class="flex flex-wrap -mx-1 lg:-mx-4">
        <CategoriesCard
          v-for="item in categories"
          :id="item.id"
          :key="item.id"
          :title="item.name"
          :count="item.products_count"
          :image="item.thumbnails"
        />
      </div>
    </div>
</template>
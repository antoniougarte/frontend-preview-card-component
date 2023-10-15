<template>
  <div id="app">
    <div v-for="(category, index) in categories" :key="index">
      <CardComponent
      :title="category.title"
      :icon="category.icon"
      :text="category.text"
      :bgColor="category.bgColor"
      />
    </div>
    <img :src="iconLuxury" alt="">
  </div>
</template>

<script>
import CardComponent from '@/components/CardComponent/CardComponent.vue'
import { categories } from "@/core/category.js";

export default {
  name: 'App',
  components: {
    CardComponent,
  },
  data(){
    return{
      categories: categories,
    }
  }
}
</script>

<style>
#app {
  
  margin: 3rem;
}
@media (min-width: 992px) { 
  #app {
    margin: auto;
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: 950px;
}
}
</style>

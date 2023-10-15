<template>
  <div :style="{ backgroundColor: bgColor }" class="container">
    <div>
      <img :src='icon' alt="test">
    </div>
    <div>
      <h2 class="text-white title">{{ title }}</h2>
    </div>
    <div>
      <p class="text-white text">{{ text }}</p>
    </div>
    <div>
      <button
      :style="{ '--button-bg-color': bgColor }"
      class="button">Learn More
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    icon: String,
    text: String,
    bgColor: String,
  },
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Big+Shoulders+Display&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700&family=Lexend+Deca&display=swap');
.text-white{
  color: white;
}
.button{
background-color: transparent;
text-decoration: none;
padding: .5rem 1.5rem;
border-radius: 20px;
border: 2px solid white;
cursor: pointer;
color: white;
}
.button:hover {
  background-color: white; 
  color: var(--button-bg-color);
}
.container{
  max-width: 1200px;
  display: flex;
  flex-direction: column;
  padding: 4rem;
  height: 100%;
}
.title{
  margin: 1.5rem 0 1.5rem ;
  padding: 0;
  font-family: 'Big Shoulders Display', sans-serif;
  font-size: 44px;
}
.text{
  margin: 0 0 1.5rem 0;
  padding: 0;
  font-family: 'Lexend Deca', sans-serif;
  line-height: 30px;
}
@media (min-width: 992px) { 
  .container{
  
    height: 380px;
}
}
</style>

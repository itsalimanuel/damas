<template>
      <Header/>
      <div class="main">
        <NuxtPage/>
      </div>
      <Footer/>

</template>
<script setup>
// layouts/custom.vue
const layout = 'default'
</script>
<style lang="scss">
@import './public/base';

.main{
  padding: 0 50px;
  padding-top: var(--pageTop);
  @media (max-width: 480px) {
    padding: 0 20px;
    padding-top: 40px;
  }
}
</style>

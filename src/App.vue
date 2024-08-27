<script setup>
import PageFooter from './components/PageFooter.vue';
import PageCards from './components/PageCards.vue';
import PageHeader from './components/PageHeader.vue';
</script>

<template>

  <main>
      <div class="wrapper">
      <PageHeader />
      <PageCards />
      </div>
      <PageFooter />
  </main> 

</template>

<style scoped>
main{
  background-color: #E8EFF4;
  min-width: 1080px;
  height: 1920px;
  font-family: "Inter", sans-serif;
  min-height: 100vh;
  position: relative;
  overflow: hidden;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
  .wrapper {
  margin-left: 60px;
  margin-right: 60px;
  flex: 1;
}
</style>


<script setup>
import { ref } from 'vue';
const showtext = ref(false); 
</script>

<template>
  <main>
    <Transition name="fade">

      <h1 v-if="showtext">HelloWorld</h1> 
    </Transition>

 <button @click="showtext = !showtext"> Toggle </button>
  </main>
</template>
<style scoped>

.fade-enter-from{
  /* background-color: yellow; */
  opacity: 0;
}

.fade-enter-to{
  /* background-color: blue; */
  opacity: 1;
}
.fade-enter-active{
  transition: all 5s ease;

}
</style>

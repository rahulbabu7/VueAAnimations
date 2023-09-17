<script setup>
import { ref } from "vue";
const showtext = ref(true);
</script>

<template>
  <main>
    <section>
      <Transition name="fade">
        <h1 v-if="showtext">HelloWorld</h1>
        <h1 v-else>BIE</h1>
      </Transition>
    </section>
    <button @click="showtext = !showtext">Toggle</button>
  </main>
</template>
<style scoped>
.fade-enter-from {
  /* background-color: yellow; */
  opacity: 0;
}

/* default property is opacity 1
.fade-enter-to{
  /* background-color: blue; 
  opacity: 1;
} */
.fade-enter-active {
  transition: all 5s ease;
}
/* default property is opacity 1
.fade-leave-from{
  opacity: 1;

} */
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active {
  transition: all 5s ease;
}
section{
  position: relative;
}
h1{
  position:absolute;
}
button{
  margin-top: 50px;
}
</style>

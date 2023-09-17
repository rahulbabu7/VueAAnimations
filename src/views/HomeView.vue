<script setup>
import { ref } from "vue";
// const showtext = ref(true);
const textInput = ref("");
const names = ref(['sunny','amal'])
</script>

<template>
  <main>
    <!-- <section>
      <Transition name="fade">
        <h1 v-if="showtext">HelloWorld</h1>
        <h1 v-else>BIE</h1>
      </Transition>
    </section>
    <button @click="showtext = !showtext">Toggle</button> -->
    <section>
      <input type="text" placeholder="Enter the name" v-model="textInput">
      <ul v-for="name in names">
      
        <li>
         {{ name }}
         
        </li>
        
      </ul>
    </section>
  </main>
</template>
<style scoped>
/* .fade-enter-from {
  /* background-color: yellow; 
  opacity: 0;
}

/* default property is opacity 1
.fade-enter-to{
  /* background-color: blue; 
  opacity: 1;
} 
.fade-enter-active {
  transition: all 5s ease;
}
/* default property is opacity 1
.fade-leave-from{
  opacity: 1;

} 
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
} */

section{
  max-width: 300px;
  margin: 0 auto;
}
input{
  width: 100%;
  border-radius: 5px;
  border: 1px solid rebeccapurple;
  padding: 10px;
  margin-bottom: 20px;
  box-shadow: 1px 1px 10px rgba(0,0,0,0.12);
}
ul{
  display: inline;
  list-style: none;
  margin: 0px;
  padding: 0px;
}
li{
  list-style: none;
  border-radius: 5px;
  width: 300px;
  padding: 5px 10px;
  margin-top: 10px;
  box-shadow: 1px 1px 10px rgba(0,0,0,0.12);
  text-align: center;
  cursor: pointer;

}
</style>

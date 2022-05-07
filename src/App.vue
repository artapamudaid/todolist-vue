<script>
import Todolist from './components/Todolist.vue'
export default {
  components: {
    Todolist
  }
}
</script>

<template>
<main>
  <Todolist/>
</main>
</template>

<style>
body {
  font-family: sans-serif;
  background-color: rgb(38, 35, 54);
  color: #fff;
  box-sizing: border-box;
}

main {
  width:  100%;
  height:  100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>

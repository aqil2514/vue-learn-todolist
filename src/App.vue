<script setup lang="ts">
import NavigationBar from './components/NavigationBar.vue'
import InputForm from './components/InputForm.vue'
import ToDoList from './components/ToDoList.vue'
</script>

<template>
  <NavigationBar />
  <div class="container-tdl">
    <InputForm />
    <ToDoList />
  </div>
</template>

<style scoped>
.container-tdl {
  border: 2px solid black;
  width: 50%;
  max-height: 400px;
  margin: 2rem auto;
  overflow-y: scroll;
}
</style>

<script setup lang="ts">
import { ref } from 'vue'

const listes = ref(JSON.parse(localStorage.getItem('list') as string) || [])
const divClass = ref('list-container')
</script>

<template>
  <div v-if="listes.length === 0" :class="divClass">To Do List masih kosong</div>
  <div v-else :class="divClass">
    <ul>
      <li v-for="(list, i) in listes" :key="i">
        {{ list }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.list-container {
  padding: 1rem 3rem;
  font-size: 1.2rem;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}

.list-container ul li {
  list-style: none;
  margin: 0.5rem 0;
}

.list-container ul li::before {
  content: '>>';
  font-size: 0.7rem;
  font-weight: 900;
  margin: 0 0.2rem;
}
</style>

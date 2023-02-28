<script setup lang="ts">

withDefaults(defineProps<{
  name: string,
  showForm: boolean,
  toggleForm: () => void
}>(), {
  name: 'John',
  showForm: false
})

// OR
// defineProps({
//   name: {
//     type: String,
//     default: 'John'
//   }
// })

</script>

<template>
  <header>
    <h1>
      Hello, {{ name }}
    </h1>
    <button class="button" @click.stop="toggleForm">{{ showForm ? 'Close' : 'Add Task' }}</button>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
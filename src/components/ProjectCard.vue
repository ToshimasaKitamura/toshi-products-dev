<template>
  <div class="project-card">
    <h3>{{ project.title }}</h3>
    <p>{{ project.description }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps<{ project: { id: number; title: string; description: string } }>();
</script>

<style scoped>
.project-card {
  background: #222;
  padding: 1%;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
  color: #fff;
  width: 80%;
}
</style>
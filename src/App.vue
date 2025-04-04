<template>
  <div id="app">
    <Header />
    <main>
      <section class="intro">
        <h1>ごあいさつ。</h1>
        <p>こんにちは。ここでは、自作のプロダクトを紹介していきます。</p>
        <a href = "https://github.com/ToshimasaKitamura">掲載しているプロダクトは全て、Githubからダウンロードできます。</a>
      </section>
      <section class="projects">
        <h2>♦Products</h2>
        <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
      </section>
    </main>
    <Footer />
  </div>  
</template>

<script setup lang="ts">
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import ProjectCard from './components/ProjectCard.vue';
import { ref } from 'vue';

const projects = ref([
  { id: 1, title: 'Project 1', description: 'なんちゃら' },
  { id: 2, title: 'Project 2', description: 'かんちゃら' }
]);
</script>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  min-height: 10vh;
}

main {
  flex: 1; /* これでmainが残りのスペースを埋める */
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 20px;
}

.intro {
  margin-bottom: 40px;
  padding-left: 4%;
}

.projects {
  /* display: flex; */
  padding-left: 4%;
  flex-wrap: wrap;
  justify-content: center;
  gap: 100px;
}
</style>

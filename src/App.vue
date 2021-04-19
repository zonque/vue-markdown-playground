<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Project
        v-for="project in projects"
        v-bind:key="project.id"
        v-bind:html="project.html"
    />
  </div>
</template>

<script>
import Project from './components/Project.vue'

export default {
  name: 'App',
  components: {
    Project
  },
  data: function() {
    return {
      projects: [
        { id: "1", html: require("./assets/test.md") },
        { id: "2", html: require("./assets/lisa.md") },
      ],
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

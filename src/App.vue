<template>
  <div id="app">
    <VSpace>
      <VButtonVue variant="primary">Primary</VButtonVue>
      <VButtonVue variant="secondary">Secondary</VButtonVue>
      <VButtonVue variant="danger">Danger</VButtonVue>
    </VSpace>
  </div>
</template>

<script>
import VButtonVue from "./components/VButton.vue"
import VSpace from "./components/VSpace.vue"
export default {
  name: 'App',
  components: {
    VButtonVue,
    VSpace,
  }
}
</script>

<style>

* {
  box-sizing: border-box;
}

html, body {
  margin: 0;
}

#app {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #fff;
}
</style>

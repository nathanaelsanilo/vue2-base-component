<template>
  <div id="app">
    <section id="buttons">
      <fieldset>
        <legend>Buttons</legend>
        <VSpace>
          <VButtonVue variant="primary">Primary</VButtonVue>
          <VButtonVue variant="secondary">Secondary</VButtonVue>
          <VButtonVue variant="danger">Danger</VButtonVue>
        </VSpace>
      </fieldset>
    </section>
    <hr />
    <section id="tabs">
      <VTabs>
        <VTab title="Tab 1" >Content Tab 1</VTab>
        <VTab title="Tab 2" >Content Tab 2</VTab>
        <VTab title="Tab 3" >Content Tab 3</VTab>
      </VTabs>
    </section>
  </div>
</template>

<script>
import VButtonVue from "./components/VButton.vue"
import VSpace from "./components/VSpace.vue"
import VTabs from "./components/VTabs.vue"
import VTab from "./components/VTab.vue";
export default {
  name: 'App',
  components: {
    VButtonVue,
    VSpace,
    VTabs,
    VTab,
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
  flex-direction: column;
  align-items: center;
  height: 100vh;
  background-color: #fff;
}
</style>

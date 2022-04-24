<template>
  <div>
    <ul>
      <li v-for="(tab, idx) in tabs" :key="idx" @click="selectTab(idx)">{{ tab.title || "-" }}</li>
    </ul>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "VTabs",
  data() {
    return {
      tabs: [],
      activeTab: 0,
      activeTitle: "",
    }
  },
  provide() {
    return {
      selectedTitle: () => this.activeTitle
    }
  },
  created() {
    this.tabs = this.$children
  },
  mounted() {
    this.selectTab(0);
  },
  methods: {
    selectTab(i) {
      this.activeTab = i

      this.tabs.forEach((tab, indx) => {
        tab.isActive = (indx === i)
      })
    },
    provideTab(title) {
      this.activeTitle = title;
    }
  }
}
</script>

<style>

</style>
<template>
  <div v-show="isActive">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "VTab",
  inject: {
    selectedTitle: {
      from: "selectedTitle",
      default: () => ""
    }
  },
  props: {
    title: {
      type: String,
      default: 'Tab',
    }
  },
  data() {
    return {
      isActive: true,
    }
  },
  computed: {
    showTab() {
      console.log("computed", this.selectedTitle())
      return this.selectedTitle() === this.title;
    }
  },
}
</script>

<style>

</style>
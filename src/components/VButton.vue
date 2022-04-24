<template>
  <button v-bind="attrs">
    <slot>Button</slot>
  </button>
</template>
<script>
export default {
  name: "VButton",
  // functional: true,
  props: {
    variant: {
      type: String,
      default: undefined,
    },
    size: {
      type: String,
      default: "default",
    },
  },
  computed: {
    attrs() {
      return {
        ...this.$attrs,
        class: this.classes,
        variant: this.variant,
        size: this.size,
        type: "button",
      }
    },
    classes() {
      return {
        btn: true,
        'btn--primary': this.variant === "primary",
        'btn--secondary': this.variant === "secondary",
        'btn--danger': this.variant === "danger",
      }
    }
  },
  created() {
    console.log(this.$attrs)
  }
}
</script>
<style scoped>
.btn {
  outline: none;
  border-radius: 12px;
  background-color: #fff;
  color: #4d4d4d;
  padding: 12px;
  border: 1px solid;
  box-shadow: none;
  cursor: pointer;
}

.btn--primary:active {
  background-color: #155549;
}

.btn--primary {
  background-color: #30a793;
  color: #fff;
}

.btn--secondary {
  background-color: #464E2E;
  color: #fff;
}

.btn--danger {
  background-color: #FD5D5D;
  color: #fff;
}

</style>

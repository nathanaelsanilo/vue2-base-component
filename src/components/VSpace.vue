<template>
  <div class="spacer">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "VSpace",
}
</script>

<style scoped>
.spacer {
  display: flex;
  align-items: center;
}

.spacer  :nth-child(n + 1) {
  margin-left: 15px;
}

</style>
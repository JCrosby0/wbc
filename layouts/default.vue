<template>
  <div class="layout-container">
    <TheNav class="nav" />
    <slot></slot>
    <TheFooter class="footer" />
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.layout-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

slot {
  overflow: scroll;
}

nav {
  z-index: 2;
  position: sticky;
  top: 0;
}

.footer {
  height: 80vh;
  background-color: black;
  color: white;
  text-align: center;
  position: relative;
}
</style>
<template>
  <div class="parent">
    <div
      class="vert-tile"
      :style="{
        '--url': `url('../assets/${props.filename}')`,
        '--translate': `${-15 * props.idx - 10}%`
      }"
    ></div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  'filename': {
    type: String,
    required: false
  },
  'idx': {
    type: Number,
    required: true,
    default: () => 0
  }
})
</script>

<style scoped>
.parent {
  display: flex;
  justify-content: center;
}

.vert-tile {
  background-image: var(--url);
  border: 1px green solid;
  background-size: cover;
  background-position: center;
  width: 200px;
  height: 450px;
  box-sizing: border-box;
  will-change: top;
  z-index: 1;
  transition: 1s;
  filter: unset;
}

.vert-tile:hover {
  scale: 150%;
  translate: var(--translate);
  transition: 0.5s;
  width: 600px;
  z-index: 2;
}
</style>
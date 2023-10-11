<template>
  <div class="division-card">
    <div
      class="photo"
      :style="{ '--bg-url': `url('../assets/${props.filename}')` }"
    ></div>
    <div class="division">
      <slot name="division"></slot>
    </div>
    <div class="ages">
      <slot name="ages"></slot>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(['filename'])

</script>

<style scoped>
.division-card {
  outline: 4px var(--green) solid;
  border: 4px var(--gold) solid;
  width: 12rem;
  height: 18rem;
  margin: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  transition: 1s;
  z-index: 1;
}

.division-card:hover {
  scale: 1.25;
  rotate: 5deg;
  transition: 1s;
  z-index: 2;
}

.division {
  font-size: large;
}

.ages {
  font-size: small;
}

.photo {
  background-image: var(--bg-url);
  border: 1px var(--green) solid;
  height: 100%;
  background-size: cover;
  background-position: center;
}

.division,
.ages {
  background: var(--gold);
  width: 100%;
  text-align: center;
}
</style>
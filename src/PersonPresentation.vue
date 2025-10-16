<script setup lang="ts">
const props = defineProps({
  name: {
    type: Object,
    required: true,
  },
  role: {
    type: Object,
    required: true,
  },
  img: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="container">
    <img :src="props.img" alt="profile picture" />
    <div>
      <h3>{{ props.name }}</h3>
      <p>{{ props.role }}</p>
    </div>
  </div>
</template>

<style scoped>
.container {
    display: flex;
    align-items: center;
    gap: .5em;
}

img {
    width: 2em;
    border-radius: 100%;
    border: 1px solid rgb(235, 235, 235);
}

h3 {
    font-size: 13px;
    font-weight: 500;
}

p {
    opacity: 0.8;
    font-size: 13px;
}
</style>

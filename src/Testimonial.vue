<!-- eslint-disable vue/multi-word-component-names -->
<script setup lang="ts">
import PersonPresentation from "./PersonPresentation.vue";

const props = defineProps({
  person: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div>
    <PersonPresentation :name="props.person.name" :role="props.person.role" :img="props.person.img" />
    <h3>{{ props.person.title }}</h3>
    <p>{{ props.person.text }}</p>
  </div>
</template>

<style scoped>
h3 {
    margin: 1em 0;
    font-size: 16px;
    font-weight: 600;
    
}
p {
    font-size: 13px;
    line-height: 130%;
}
</style>

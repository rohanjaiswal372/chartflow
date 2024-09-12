<template>
  <q-tab :label="props.title">
    <router-link :to="props.link"></router-link>
  </q-tab>
</template>

<script setup>
defineOptions({
  name: "NavbarComponent",
});

const props = defineProps({
  title: {
    type: String,
    required: true,
  },

  link: {
    type: String,
    default: "#",
  },
});
</script>

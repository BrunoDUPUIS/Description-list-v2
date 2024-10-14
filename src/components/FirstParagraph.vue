<script setup>
const props = defineProps({ age: Number, job: String, gender: String })
</script>

<template>
  <p>
    {{ gender === 'female' ? 'She' : 'He' }} is a {{ age }}-year-old {{ job }}
  </p>
</template>

<style scoped></style>

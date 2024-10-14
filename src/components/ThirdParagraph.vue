<script setup>
const props = defineProps({
  pet: Object,
  gender: String,
})
console.log(props.pet)
console.log(props.pet.age)
</script>

<template>
  <p>
    At home, {{ gender === 'female' ? 'her' : 'his' }} lively companion is{{
      pet.name
    }}
    a {{ pet.age }}-years-old
    {{ pet.species }}
  </p>
</template>

<style scoped></style>

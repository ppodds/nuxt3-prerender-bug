<template>
  <div>
    {{ a }}
  </div>
</template>
<script setup lang="ts">
const { data: test } = await useFetch("/api/test");
console.log("1");
console.log(test.value);
const a = computed(() => {
  console.log("2");
  console.log(test.value);
  return test.value.sort();
});
</script>

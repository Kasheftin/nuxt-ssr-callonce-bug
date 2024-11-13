<template>
  <div>
    ddd: {{ ddd }}
  </div>
</template>

<script setup lang="ts">

const ddd = useState('ddd')

callOnce(async () => {
  const data = await $fetch('https://new.lozinskis.com/items/pages')
  ddd.value = data
  console.log('callOnce', data)
})
</script>

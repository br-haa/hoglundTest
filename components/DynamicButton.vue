<template>
<button @click="$emit('buttonClick')">
<slot></slot>
</button>
</template>

<script>
export default {
  name: 'dynamicButton'
}
</script>

<style scoped>

</style>

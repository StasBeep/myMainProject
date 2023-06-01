<template>
  <div>
    <h2 :class="[$style.content]">Основная часть</h2>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld'
}
</script>

<style module lang="scss" scoped>
.content {
    color: red;
}
</style>

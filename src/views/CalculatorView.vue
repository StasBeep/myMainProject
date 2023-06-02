<template>
  <div class="wrapper wrapper-forcontent">
    <div class="content-without-footer">
      <header>
        <MenuRouting />
      </header>
      <main>
        <SimpleCalculator />
      </main>
    </div>
    <footer>Версия: 0.0.0</footer>
  </div>
</template>

<script>

import MenuRouting from '../components/MenuRouting.vue'
import SimpleCalculator from '../components/SimpleCalculator.vue'

export default {
  name: 'CalculatorView',

  components: {
    MenuRouting,
    SimpleCalculator
  }
}
</script>

<style src="../scss/style.scss" lang="scss" scoped />

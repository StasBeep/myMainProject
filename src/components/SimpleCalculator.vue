<template>
  <div class="simplecalc">
    <input class="simplecalc-number" type="number" v-model.number="varible1">
    <div class="simplecalc-list">
      <button class="simplecalc-list-button" v-for="(item, idx) in operations" :key="idx" @click="calculation(item)">
        {{ item }}
      </button>
      </div>
    <input class="simplecalc-number" type="number" v-model.number="varible2">
    <div class="simplecalc-result">
      = {{ result }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'SimpleCalculator',

  data: () => ({
    operations: ['+', '-', 'x', '/'],
    result: 0,
    varible1: 0,
    varible2: 0
  }),

  methods: {
    calculation (operation) {
      switch (operation) {
        case '+':
          this.result = this.varible1 + this.varible2
          break
        case '-':
          this.result = this.varible1 - this.varible2
          break
        case 'x':
          this.result = this.varible1 * this.varible2
          break
        case '/':
          if (this.varible2 === 0) {
            alert('На 0 делить нельзя!')
            break
          }
          this.result = this.varible1 / this.varible2
          break
        default:
          alert('Ошибка!')
      }
    }
  }
}
</script>

<style src="../scss/style.scss" lang="scss" scoped/>

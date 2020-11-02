
<template>
  <div>
    <h2>{{currentValue}}</h2>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  methods: {
    increment(){
      this.$store.commit('INCREMENT_COUNTER')
    },
    decrement(){
      this.$store.commit('DECREMENT_COUNTER')
    },
  },
  computed: {
    currentValue() {
      return this.$store.state.currentValue
    }
  }
}
</script>

<style>

</style>
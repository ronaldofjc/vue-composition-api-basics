<template>
  <div class="home">
    <div class="btn">
      <button @click="decreaseCounter" class="btn">-</button>
      <span class="counter">{{ counter }}</span>
      <button @click="increaseCounter" class="btn">+</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0
    }
  },
  methods: {
    increaseCounter() {
      this.counter++
    },
    decreaseCounter() {
      this.counter--
    }
  }
}
</script>

<style>
.home {
  padding: 20px;
  text-align: center;
}
.btn, .counter {
  font-size: 40px;
  margin: 10px;
}
</style>
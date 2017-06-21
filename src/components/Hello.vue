<template>
  <div class="container">
    <div class="row text-center">
      <h3>Clicked: {{ $store.state.count }} times, counter is {{ evenOrOdd }}</h3>

      <button class="btn btn-success" @click="increment">Increment</button>
      <button class="btn btn-danger" @click="decrement">Decrement</button>

      <button class="btn" @click="incrementIfOdd">IfOdd</button>
      <button class="btn" @click="incrementAsync">Async</button>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'

export default {
  name: 'hello',
  computed: mapGetters([
    'evenOrOdd'
    ]),
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
    ])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

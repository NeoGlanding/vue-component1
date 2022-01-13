<template>
  <h1>Hello to Vue</h1>
  <Card is-man="1" name="Ihsan" school-class="12 TKJ 1" phone-number="08568881510" />
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  methods: {
    getData(data) {
      console.log(data)
    }
  }
}
</script>

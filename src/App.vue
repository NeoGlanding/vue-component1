<template>
  <h1>Hello to Vue</h1>
  <Card is-man="1" name="Ihsan" school-class="12 TKJ 1" phone-number="08568881510" />
  <Card2 :active="true" name="Jonas" />
  <Card2 @find-name="getData" v-for="(friend, index) in friends" :key="index" :name="friend.name" :active="friend.active" />
</template>

<script>
import Card from './components/Card.vue'
import Card2 from './components/Card2.vue'

export default {
  name: 'App',
  components: {
    Card,
    Card2
  },
  data() {
    return {
      friends: [
        {
          name: 'Joe Kal',
          active: true
        },
        {
          name: 'Dafy Tuasamu',
          active: false
        }
      ]
    }
  },
  methods: {
    getData(data) {
      console.log(data)
    }
  }
}
</script>

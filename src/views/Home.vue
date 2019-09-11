<template>
  <div class="home">
    <h1>{{val}}</h1>
    <Card title="First" @sendEvent="receiveEvent">{{title}}</Card>
    <Card title="Second" @sendEvent="receiveEvent"></Card>
  </div>
</template>

<script>
// @ is an alias to /src
import Card from '../components/Card.vue'

export default {
  name: 'home',
  components: {
    Card
  },
  props: ['title'],
  data: function()
  {
    return {
      val:"",
    }
  },
  components: {
    Card
  },
  methods:{
    receiveEvent: function(title){
      this.val = title
    }
  }
}
</script>

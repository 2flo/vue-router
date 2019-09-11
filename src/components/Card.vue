<template>
    <div class="card" style="width: 18rem;">
      <div class="card-body">
        <h2 class="card-title">{{title}}</h2>
          <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
          <button @click="sendEvent">OK</button>
      </div>
    </div>
</template>
<script>
export default {
    name: 'Card',
    props: ['title'],
    methods:{
    sendEvent: function(){
      this.$emit('card-title',this.title)
    }
}
}

</script>
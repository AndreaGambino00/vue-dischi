<template>
  <section class="container">
    <div class="row">

    </div>
  </section>
    
    
    
  

</template>

<script>
import axios from 'axios';
export default {
  name: 'Cards',
  data () {
    return {
      APIurl: 'https://flynn.boolean.careers/exercises/api/array/music',
      CardsList: []
    }
  },
  created() {
    this.getCards();
  },
  methods: {
    getCards() {
      axios
        .get(this.APIurl)
        .then(res => {
          this.Cards.Cards = res.data;
        }) 
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>

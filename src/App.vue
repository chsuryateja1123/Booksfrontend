/* eslint-disable */
<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header heading="Tourism Guider" />


    <Bookbox :tourist_places="tourist_places"  />




  </div>
</template>

<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Header from './components/Header.vue'
import Bookbox from './components/Bookbox.vue'


// data url: http://localhost:5555/books , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component
    Header,
    Bookbox
  },

  data(){
    return {
      tourist_places: []
    }
  },
  methods: {
    // promises

      async fetchTourist_places(){

       const res= await fetch('https://suryatejafinalproject.herokuapp.com/api')
       //     const res= await fetch('http://localhost:5959/api')
      const data= await res.json()
       console.log(data)
      return data
      }

  },

  async created(){
    this.tourist_places = await this.fetchTourist_places()
  }
}
</script>





<style>


@import url('https://fonts.googleapis.com/css2?family=Roboto+Slab&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Roboto Slab', serif;
}

.container {
  max-width: 700px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 7px;
}

div{
  margin-bottom: 0.5em;
}



</style>
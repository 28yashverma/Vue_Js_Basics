<template>
  <h2>Computed Full name : {{ fullName }}</h2>
  <h2>Volume tracker (0-20)</h2>
  <h3>Current volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
  <div>
    <input type="text" v-model="movie">
  </div>
  <div>
    <input type="text" v-model="movieInfo.titile">
  </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
      volume: 0,
      movie:'Batman',
      movieInfo: {
        titile: ''
      }
    };
  },
  methods: {
    
  },
  computed: {
    fullName(){
      return `${this.firstName} ${this.lastName}`
    }
  },
  watch: {
    volume(newValue, oldValue) {
      if(newValue > oldValue && newValue === 16) {
        alert("listening for a high volume for a long time may damage your hearing")
      }
    },
    movie:{
      handler(newValue) {
        console.log(`calling api name with movie name = ${newValue}`)
      },
      immediate:true
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Title of the movie is = ${newValue}`)
      },
      deep:true
    }
  },
  components: {
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>

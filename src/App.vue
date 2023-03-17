<template>
  <h2>Computed Full name : {{ fullName }}</h2>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne"
    };
  },
  methods: {
    
  },
  computed: {
    fullName(){
      return `${this.firstName} ${this.lastName}`
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

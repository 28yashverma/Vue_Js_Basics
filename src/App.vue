<template>
  <MyGreet name="Yeshendra" heroName="Batman"/>
  <MyGreet :name="name" :hero-Name="channel"/>
</template>

<script>

import MyGreet from './components/Greet.vue';

export default {
  name: 'App',
  components: {
    MyGreet,
  },
  data() {
    return {
      name: 'Yeshendra',
      channel: 'My code'
    }
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

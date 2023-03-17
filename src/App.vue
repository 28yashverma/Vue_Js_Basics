<template>
  <!-- <MyGreet name="Yeshendra" heroName="Batman"/>
  <MyGreet :name="name" :hero-Name="channel"/> -->
  <ArticleComponent title="Article title"/>
  <ArticleComponent/>
  
  <div>
    <h2 v-bind="$attrs">{{ title }}</h2>
  </div>
</template>

<script>

//import MyGreet from './components/Greet.vue';
import ArticleComponent from './components/Article.vue';

export default {
  name: 'App',
  components: {
    //MyGreet,
    ArticleComponent
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

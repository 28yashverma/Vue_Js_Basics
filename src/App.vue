<template>
  <!-- <MyGreet name="Yeshendra" heroName="Batman"/>
  <MyGreet :name="name" :hero-Name="channel"/> -->
  <ArticleComponent title="Article title"/>
  <ArticleComponent/>
  
  <div>
    <h2 v-bind="$attrs">{{ title }}</h2>
  </div>
  <div>
    <h2>
      <ComponentA/>
    </h2>
  </div>
</template>

<script>

//import MyGreet from './components/Greet.vue';
import ArticleComponent from './components/Article.vue';
import ComponentA from './components/ComponentA.vue';

export default {
  name: 'App',
  components: {
    //MyGreet,
    ArticleComponent,
    ComponentA
},
  data() {
    return {
      name: 'Yeshendra',
      channel: 'My code'
    }
  },
  provide:{
    username: 'Yeshendra provided from App component'
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

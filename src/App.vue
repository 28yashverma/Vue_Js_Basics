<template>
  <h2>Form Handling</h2>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
      {{ formValues.name }}
    </pre>
  </div>
  <form @submit.prevent="submitform">
    <div>
      <label for="name">Name: </label>
      <input type="text" id="name" v-model.trim="formValues.name">
    </div>
    <div>
      <label for="age">Age</label>
      <input type="number" id="age" v-model.number.lazy="formValues.age">
    </div>
    <div>
      <button >Submit</button>
    </div>
  </form>
  
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      formValues: {
        name: '',
        age: null
      }
    };
  },
  methods: {
    submitform() {
      
      console.log('Form values', this.formValues)
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

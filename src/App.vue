<template>
  <h2>Form Handling</h2>
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
      {{ formValues.name }}
    </pre>
  </div>
  <form @submit="submitform">
    <div>
      <label for="name">Name: </label>
      <input type="text" id="name" v-model="formValues.name">
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
        name: ''
      }
    };
  },
  methods: {
    submitform(event) {
      event.preventDefault()
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

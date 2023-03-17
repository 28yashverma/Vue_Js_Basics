<template>
  <div>{{greet}} {{name}}</div>
  <div v-html="channel"> </div>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Button</button>
  <h2 class="underline">Underline text</h2>
  <h2 v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 v-bind:class="isSoldOut ? 'issoldOut' : 'new'">SoldOut? Movie</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldOut,
    isSoldOut: isSoldOut
  }">Object conditional movie</h2>

  <h2 v-bind:style="{
    color: highlightColor,
    'font-size': headerSize + 'px'
  }">Inline style</h2>
  <h2 v-bind:style="headerStyleObject">Style Object</h2>

  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">the number is negative</h2>
  <h2 v-else-if="num > 0">the number is positive</h2>
  <h2 v-else>Not a number</h2>

  <div v-if="display">
    <h2>Yeshendra</h2>
    <h2>My code</h2>
    <h2>Vue</h2>
  </div>

  <h2 v-show="display">Using v-show</h2>

  <h2 v-for="(n, index) in names" :key="n">{{index}} {{ n }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h2>

  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'Bruce'">{{ name }}</h2>
  </template>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      greet: "Hello",
      name: "Yeshendra",
      channel: "<b>My channel</b>",
      headingId: 'heading',
      isDisabled: false, 
      status: 'danger',
      isPromoted: true,
      isSoldOut:false,
      highlightColor: 'orange',
      headerSize: 25,
      headerStyleObject: {
        color: 'orange',
        fontSize: 50 + 'px'
      },
      num: 5, 
      display: true, 
      names: ['Bruce', 'Clarke', 'Diana'], 
      fullNames: [
        {first: 'Bruce', last: 'Wayne'},
        {first: 'Clarke', last: 'Kent'}
      ]
    };
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

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.issoldOut {
  color: red;
}
</style>

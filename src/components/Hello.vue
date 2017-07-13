<template>
<div class="hello">
  <h1>{{ msg }}</h1>
  <h2>{{greeting}}</h2>
  <div>
    <ul>
      <li v-for="user in users">
        {{user.first}} {{user.last}}
      </li>
    </ul>
  </div>
  <div >
    <input type="text" v-model="cheese">
    <span v-text="cheese"></span>
  </div>
  <div>
    <button type="button" v-on:click="counter++">Dont click me fool</button>
    <span>{{counter}}</span>

  </div>
</div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      greeting: 'this is a test',
      msg: 'Welcome to Your Vue.js App',
      users: [
        {first: 'James', last: 'schul'},
        {first: 'cody', last: 'face'},
        {first: 'peaches', last: 'aldo'},
      ],
      cheese: '',
      counter: 0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
  color: red;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: red;
}
</style>

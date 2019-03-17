<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <pre v-on:click="clear">{{ message }}</pre>
    <hr>
    <div><input type="text" v-on:keydown="type"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String,
  },
  data: function () {
    return {
      message: '',
    }
  },
  methods: {
    type: function(event) {
      this.message += event.key + ' ';
      if (event.key == 'Escape') {
        this.message = '';
      }
      event.target.value = '';
    },
    clear: function () {
      this.message = '';
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h3 {
  margin: 40px 0 0;
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
  color: #42b983;
}

pre {
  font-size: 14pt;
  line-height: 1.25;
}

div.out {
  padding: 5px 0;
  background-color: #eee;
  width: 300px;
  height: 200px;
}

div.mid {
  padding: 5px 0;
  background-color: #ddd;
  width: 200px;
  height: 175px;
}

div.in {
  padding: 5px 0;
  background-color: #ccc;
  width: 100px;
  height: 150px;
}

</style>
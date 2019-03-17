<template>
  <div class="hello">
    <h1>{{title}}</h1>
    <p>{{message}}</p>
    <hr>
    <p>val: {{val}}</p>
    <div>*2 <input type="number" v-model="a"></div>
    <div>^2 <input type="number" v-model="b"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String
  },
  data: function () {
    return {
      message: 'バリデーションチェック',
      val: 0,
    }
  },
  computed: {
    a: {
      get: function () {
        return this.val * 2;
      },
      set: function (value) {
        this.val = Math.floor(value / 2);
      }
    },
    b: {
      get: function () {
        return this.val * this.val;
      },
      set: function () {
        this.val = Math.floor(Math.sqrt(value))
      }
    },
  },
  created: function () {
    this.val = 10;
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
</style>

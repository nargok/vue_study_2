<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <p>{{message}}</p>
    <hr>
    <ul>
      <li><slot name="a"></slot></li>
      <li><slot name="b"></slot></li>
      <li><slot name="c"></slot></li>
    </ul>
    <hr>
    <slot />
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
      message: 'This is a message',
    };
  },
}
</script>

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

.inner {
  color: red;
  font-size: 14pt;
}
.etc {
  color: green;
  background-color: #eee;
  font-size: 12pt;
  padding: 5px;
}
</style>

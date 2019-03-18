<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <p>{{message}}</p>
    <hr>
    <button v-on:click="doAction">
      {{btn}}
    </button>
    <transition name="transit">
      <p v-if="flg" class="trans">Transition!</p>
    </transition>
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
      message: 'Transition Sample!',
      flg: true,
      btn: 'Show/Hide',
    };
  },
  methods: {
    doAction: function () {
      this.flg = !this.flg;
    },
  },
}
</script>

<style>
.trans {
  background-color: #ddf;
  padding: 10px;
  font-size: 20pt;
}
</style>

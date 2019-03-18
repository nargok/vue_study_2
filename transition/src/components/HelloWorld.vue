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

v-enter-active {
  transition: opacity 0.5s;
}

.transit-enter-active, .transit-leave-active {
  transition: opacity .5s;
}

.transit-enter-active {
  transition: all .3s ease;
}
.transit-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.transit-enter, .transit-leave-to
  /* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}


</style>

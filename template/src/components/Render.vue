<script>
  export default {
    name: "Render",
    render: function (h) {
      return h('div', {}, [
        h('h1', 'Render'),
        h('p', 'this is render sample.'),
      ]);
    }
  }
</script>

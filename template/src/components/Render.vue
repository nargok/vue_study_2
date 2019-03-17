<script>
  export default {
    name: "Render",
    data: function() {
      return {
        title: 'JSX',
        message: 'これは, dataに用意したメッセージです'
      }
    },
    render: function (h) {
      return (
        <div>
            <h1>{this.title}</h1>
            <p>{this.message}</p>
        </div>
      )
    }
  }
</script>

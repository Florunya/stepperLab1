<script>
new Vue({
  el: "#app2",
  data: {
    images: [
      'https://images.unsplash.com/photo-1512319302256-dc970e613e2c?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=3150&q=80',
      'https://picsum.photos/600/200',
      'https://picsum.photos/600/200'
    ],
    selectedImage: null
  },
  methods: {
    randomItem (items) {
      return items[Math.floor(Math.random()*items.length)];
    }
  },
  created() {
    this.selectedImage = this.randomItem(this.images)
  }
})
</script>
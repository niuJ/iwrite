<template>
  <div class="iw-home">
        <Carousel></Carousel>
  </div>
</template>

<script>
import Carousel from '../components/comm/carousel'

export default {
  name: 'iw-home',
  components: {
    Carousel
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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

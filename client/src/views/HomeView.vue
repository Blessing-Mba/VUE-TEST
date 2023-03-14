<template >
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Table from '@/components/Table.vue'

export default {
  name: 'HomeView',
  components: {
    Table
  },
  created() {
  document.body.style.backgroundColor = "#FFF"
}
}
</script>

<template>
  <div class="hello">
   <ul>

     <li></li>

   </ul>
  </div>
</template>

<script>
  import Axios from 'axios'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  created() {

    Axios.get(`/api/manage/category/get_category.do`).then(res=>{


      console.log(res)


    })

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

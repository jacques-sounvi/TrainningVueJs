<template>
 <div>
   <div class="demo" :style="{backgroundColor: color}"></div>
   <div class="demo"></div>
   <div class="demo"></div>
   <hr>

   <input type="text" v-model="color">

 </div>
  


</template>

<script>
export default {
  data() {
    return{
      color: 'green'
    };
    
  }
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
.demo{
  width: 100px;
  height: 100px;
  background-color: gray;
  display: inline-block;
  margin: 10px;
}
</style>

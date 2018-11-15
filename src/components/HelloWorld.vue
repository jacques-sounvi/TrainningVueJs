<template>
 <div>
   <ul>
     <li v-for="(ingredient,i) in ingredients">{{ingredient}} {{i}}</li>
   </ul>
 </div>
  


</template>

<script>
export default {
  data() {
    return{

      ingredients: ['meat','fruit','cookies'],
      persons:[
        {name: 'max',age: 27, color:'red'},
        {name: 'jack',age: 28, color:'blue'},
      ]
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

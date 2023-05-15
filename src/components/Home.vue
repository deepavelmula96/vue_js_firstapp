<template>
<h1>Home Component</h1>
interpollation
<p>without curly braces 10+10</p>
<p>with curly braces {{ 10+10 }}</p>
<p>length {{ "deepa".length }}</p>
<!-- <p>direact email :{{ direactEmail }}</p> -->
<p>mobile : {{ mobile }}</p>
<p>mobile :{{ mobile=889898 }}</p>
<p>mobile : {{ mobile }}</p>
<p>data email : {{ email }}</p>
<p>methods : {{ getName("deepa_method") }}</p>

<p>data:  {{ getName("deepa_data") }}</p>
<!-- first preferrence methods inside the data -->
<!--6.  methods properties access -->
<p>methods properties access :{{ getData().name +" "+getData().email }}</p>
<!--7. click onChange, onClick,  -->
<button v-on:click="wishing('hi deepa Good morning')">Click to wish</button>
<br>
 count {{ count }} 
<button v-on:click="incCount()">count inc</button>
<!-- 8. input  -->
<h2>Two way data binding</h2>
<input type="text" v-model="data">
<h3>{{ data }}</h3>

</template>

<script>
export default {
    name:"Home",
    // direactEmail:"deepa@gmail.com",
    data(){
      return{
        email:"deepa@gmail.com",
        mobile:9900,
        getName(x){
          return x
        },
        count:0,
        data:100
      }
    },
    methods:{
      getName(name){
        return name;
      },
      getData(){
        return {
          name:'deepa',
          email:"deepa@gmail.com"
        }
      },
      wishing(x){
        alert(x)
      },
      incCount(){
        this.count=this.count+1
      }
    }
}
</script>

<style scoped>
h1{
  color: red;
  background: blue;
  text-align: center;
  margin: 5px 300px;
}
</style>

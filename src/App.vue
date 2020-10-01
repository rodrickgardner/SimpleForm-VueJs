<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <!--<router-view/>-->
    <add-form></add-form>




  </div>
</template>

<script>
import addForm from './components/addForm.vue';

export default {
  components:{
    'add-form':addForm
  },
  

  data(){
    return{


    }
  },
  methods:{


  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body{
  margin:0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
#add-form*{
  box-sizing:border-box;
}
#add-form{
  margin:20px auto;
  max-width:500px;
}
label{
  display:block;
  margin:20px 0 10px;
}
input[type="text"],textbox{
  display:block;
  width:100%;
  align:center;
  padding:8px;
}
#preview{
  padding:10px 20px;
  border:1px dotted #ccc;
  margin:30px 0;
}
h3{
  margin-top:10px;
}
</style>

<template>
  <div id="app">
    <!--<input type="text" v-model="title" /> -->
    <!--<input type="text" :value="title" @input="title=$event.target.value" />-->
    <editor v-model="content"></editor>
    <file></file>

  </div>
</template>

<script>
import Editor from "./components/Editor";
import File from "./components/file.vue";
export default {

  name: 'App',
  components: {
    Editor,
    File,
  },
  data(){
    return{
      title:"",
      content:""
    }
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
</style>

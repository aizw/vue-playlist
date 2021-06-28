<template>
 <footer v-on:click="changeFooter">
   <h1>{{title}}{{title1}}</h1>
 </footer>
</template>

<script>
  export default {
    name: 'app-footer',
    props:{
      title:{
        type:String,
        required:true,
      }
    },
    data () {
      return {
        title1:"footer Right"
      }
    },
    methods: {
      changeFooter:function () {
        this.title1="改变footer的值"
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
footer{
  background: red;
  padding:6px;
  text-align:center;
  font-size: 12px;
}
</style>

<template>
  <div id="home">
    <app-header v-on:titleChanged="updateTitle($event)" v-bind:title="title"></app-header>
    <user v-bind:users="users"></user>
    <user v-bind:users="users"></user>
    <app-footer v-bind:title="title"></app-footer>
    <app-logo></app-logo>
  </div>
</template>

<script>
  // 局部注册组件
  import Header from './Header'
  import User from './User'
  import Footer from './Footer'
  import Logo from './Logo'

  export default {
    name: 'home',
    data() {
      return {
        users:
          [
            // {name: 'Email', position: "web前段", show: false},
            // {name: 'Email', position: "web前段", show: false},
            // {name: 'Email', position: "web前段", show: false},
            // {name: 'Email', position: "web前段", show: false},
            // {name: 'Email', position: "web前段", show: false},
            // {name: 'Email', position: "web前段", show: false}
            ],
        title: "传递的是一个值，（number，string，boolean）",
      }
    },
    methods:{
      updateTitle(tit){
        this.title=tit;
      }
    },
    components: {
      "user": User,
      "app-header": Header,
      "app-footer": Footer,
      "app-logo": Logo
    },
    created(){
      this.$http.get("http://jsonplaceholder.typicode.com/users").then((data) => {
        // alert(JSON.stringify(data))
        this.users=data.body;
      })
    }

  }
</script>

<!--解决样式-->
<style>
  * {
    padding: 0;
    margin: 0;
  }

  h1 {
    color: green;
  }
</style>

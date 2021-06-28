<template>
  <div class="users">
    <ul>
      <li v-for="user in users">
        <h2>{{user.name}}</h2>
        <h3>{{user.email}}</h3>
      </li>
    </ul>
    <button v-on:click="deleteUser">删除</button>
  </div>
</template>

<!--
传值：string number boolean
引用：array object
-->
<script>
  export default {
    name: "user",
    // props:["users"],
  props:{
      users: {
        type:String,
          required:true
      }

  },
    data() {
      return {}
    },
    methods:{
      deleteUser:function(){
        this.users.pop()
      }
    }
  }
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1 {
    color: red;
  }

  .users {
    width: 100%;
    max-width: 1200px;
    margin: 40px auto;
    padding: 0 20px;
    box-sizing: border-box;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
  }

  ul li {
    flex-grow: 1;
    flex-basis: 200px;
    text-align: center;
    padding: 20px;
    border: 1px solid #000;
    margin: 10px;
    height: 80px;
  }
</style>

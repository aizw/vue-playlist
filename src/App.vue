<template>
  <div id="app">
    <ul>
      <li>
        <router-link to="/">home</router-link>
      </li>
      <li>
        <router-link to="/helloworld">hello</router-link>
      </li>
    </ul>
    <router-view></router-view>
  </div>
</template>

<script>

  export default {
    name: 'app',
    data() {
      return {

      }
    },
    methods:{


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

<template>
 <div class="app">
   <Navbar />
   <router-view></router-view>
 </div>
</template>
<script>
import Navbar from './components/Navbar.vue'
export default {
  components:{
    Navbar,
  }
}
</script>

<style lang="scss">
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 100%;
  box-sizing: border-box;
  max-width:  1230px;
  min-height: 100vh;
  margin: 0 auto;
  padding: 0 20px;
  box-shadow: 0 0 35px #eee ;
}
a{
  text-decoration: none;
}
ul li{
  list-style: none;
}
button{
  border: none;
  outline: none;
  background: transparent;
  cursor: pointer;
}
</style>

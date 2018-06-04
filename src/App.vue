<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <router-view/>
    <!--<Header :message="parentMag"></Header>-->
    <!--<Section></Section>-->
    <!--<Footer></Footer>-->
    <!--<Home></Home>-->
  </div>
</template>

<script>
import Home from './components/Home.vue'
export default {
  name: 'App',
  data () {
    return {
      flag: 1,
      parentMag: 'a message form parent'
    }
  }
//  components: {Home}
//  components: {Header, Section, Footer}
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  /*margin-top: 60px;*/
}
body,div,p,ul,ol,li,h1,h2,h3,h4,form,input,select,textarea,dl,dt,dd,header,footer,section{
  margin: 0;
  padding: 0;
  font-family: Arial;
}
img{  border: none;  }
li{  list-style: none;  }
a{  text-decoration: none;  }
a:hover{  text-decoration: underline; }

body{
  background: #ececec;
}
html{
  font-size: 10px;
}

</style>

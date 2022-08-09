<template>
  <div>
    <NavBar/>
    <InfoHtml/>
    <FooTer/>
  </div>
</template>

<script>
import NavBar from './components/NavBar'
import FooTer from './components/FooTer'
import InfoHtml from './components/InfoHtml'

export default {
  name: 'App',
  components: {
    NavBar,
    InfoHtml,
    FooTer,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

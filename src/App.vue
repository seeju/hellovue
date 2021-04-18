<template>
  <div>
    <Header />
    <NavBar />
    <SideBar />
    <Article />
  </div>
</template>

<script>
import Header from './components/Header'
import NavBar from './components/NavBar'
import SideBar from './components/SideBar'
import Article from './components/Article'

export default {
  name: 'App',
  components: {
    Header,
    NavBar,
    SideBar,
    Article
  }
}
</script>

<style scoped>

</style>
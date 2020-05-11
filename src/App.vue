<template>
  <div class="is-light-mode" id="app">
    <Header></Header>
    <TopCardList></TopCardList>
    <Overview></Overview>
  </div>
</template>

<script>
  import './assets/css/globals.css'
  import TopCardList from "@/components/TopCardList"
  import Overview from "@/components/Overview"
  import Header from "@/components/Header"

  export default {
    name: 'App',
    components: {
      Header,
      Overview,
      TopCardList,
    },
    created() {
      const mq = window.matchMedia('(prefers-color-scheme: dark)')
      console.log(mq)

    }
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
</style>

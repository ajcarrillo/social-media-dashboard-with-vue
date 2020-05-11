<template>
  <div :class="isDarkMode" id="app">
    <Header>
      <SwitchComponent v-model="checked"></SwitchComponent>
    </Header>
    <TopCardList></TopCardList>
    <Overview></Overview>
  </div>
</template>

<script>
  import './assets/css/globals.css'
  import TopCardList from "@/components/TopCardList"
  import Overview from "@/components/Overview"
  import Header from "@/components/Header"
  import SwitchComponent from "@/components/Switch"

  export default {
    name: 'App',
    components: {
      SwitchComponent,
      Header,
      Overview,
      TopCardList,
    },
    data() {
      return {
        checked: false,
      }
    },
    created() {
      let mq = window.matchMedia('(prefers-color-scheme: dark)')

      this.checked = mq.matches

      mq.addListener(() => {
        this.changeDarkMode(mq.matches)
      })
    },
    methods: {
      changeDarkMode(val) {
        this.checked = val
      }
    },
    computed: {
      isDarkMode() {
        return {
          'is-dark-mode': this.checked,
          'is-light-mode': !this.checked
        }
      },
    },
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
</style>

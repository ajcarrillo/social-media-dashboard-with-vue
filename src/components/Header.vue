<template>
  <header class="header">
    <div class="wrapper">
      <div class="header-grid">
        <div>
          <h1>Social Media Dashboard</h1>
          <p class="header-total">Total Followers: 23, 004</p>
        </div>
        <SwitchComponent v-model="checked"></SwitchComponent>
      </div>
    </div>
  </header>
</template>

<script>
  import '../assets/css/header.css'
  import SwitchComponent from "@/components/Switch"

  export default {
    name: "Header",
    components: {
      SwitchComponent
    },
    data() {
      return {
        checked: false
      }
    },
    watch: {
      checked(val) {
        if (val) {
          document.getElementById('app').classList.remove('is-light-mode')
          document.getElementById('app').classList.add('is-dark-mode')
        } else {
          document.getElementById('app').classList.remove('is-dark-mode')
          document.getElementById('app').classList.add('is-light-mode')
        }
      }
    }
  }
</script>

<style scoped>

</style>
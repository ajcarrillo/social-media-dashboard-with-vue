<template>
  <header class="header">
    <div class="wrapper">
      <div class="header-grid">
        <div>
          <h1>Social Media Dashboard</h1>
          <p class="header-total">Total Followers: 23, 004</p>
        </div>
        <slot></slot>
      </div>
    </div>
  </header>
</template>

<script>
  import '../assets/css/header.css'

  export default {
    name: "Header",
    data() {
      return {
        checked: false
      }
    }
  }
</script>

<style scoped>

</style>
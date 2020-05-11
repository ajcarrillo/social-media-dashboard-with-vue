<template>
  <div class="dark-mode">
    <p class="dark-mode-title">Dark Mode</p>
    <input :checked="value"
           class="checkbox"
           id="checkbox"
           type="checkbox"
           v-on:change="updateValue($event)"
    />
    <label class="switch" for="checkbox">
    
    </label>
  </div>
</template>

<script>
  import '../assets/css/switch.css'

  export default {
    name: "SwitchComponent",
    props: ['value'],
    methods: {
      updateValue($event) {
        this.$emit('input', $event.target.checked)
      }
    }
  }
</script>

<style scoped>

</style>
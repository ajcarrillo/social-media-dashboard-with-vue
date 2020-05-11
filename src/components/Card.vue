<template>
  <article :class="cardClass">
    <p class="card-title">
      <img :src="socialNetworkImg" alt=""/>
      {{draft.username}}
    </p>
    <p class="card-followers">
      <span class="card-followers-number">{{draft.followers}}</span>
      <span class="card-followers-title">Followers</span>
    </p>
    <p class="card-today">
      <img alt="" src="../assets/images/icon-up.svg"/>
      {{draft.todayFollowers}} Today
    </p>
  </article>
</template>

<script>
  import '../assets/css/card.css'

  export default {
    name: "Card",
    props: {
      socialNetwork: {
        type: Object,
        required: true
      }
    },
    data() {
      return {
        draft: {}
      }
    },
    created() {
      this.draft = Object.assign({}, this.socialNetwork)
    },
    computed: {
      cardClass() {
        return `card ${this.draft.name}`
      },
      socialNetworkImg() {
        return require(`../assets/images/${this.draft.icon}.svg`)
      }
    }
  }
</script>

<style scoped>

</style>
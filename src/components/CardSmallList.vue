<template>
  <div class="card-small">
    <p class="card-small-views">Page Views</p>
    <p class="card-small-icon">
      <img :src="socialNetworkImg" alt=""/>
    </p>
    <p class="card-small-number">{{draft.pageViews}}</p>
    <p class="card-small-percentage">
        <span>
          <img alt="" src="../assets/images/icon-up.svg"/>
          {{draft.growth}}%
      </span>
    </p>
  </div>
</template>

<script>
  import '../assets/css/card-small.css'

  export default {
    name: "CardSmallList",
    props: {
      card: {
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
      this.draft = Object.assign({}, this.card)
    },
    computed: {
      socialNetworkImg() {
        return require(`../assets/images/${this.draft.icon}.svg`)
      }
    }
  }
</script>

<style scoped>

</style>
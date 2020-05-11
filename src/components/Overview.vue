<template>
  <div class="wrapper">
    <h2>Overview - Today</h2>
    <div class="grid">
      <CardSmallList :card="card"
                     :key="card.key"
                     v-for="card in cardSmallList"
      ></CardSmallList>
    </div>
  </div>
</template>

<script>
  import '../assets/css/overview.css'
  import CardSmallList from "@/components/CardSmallList"

  export default {
    name: "Overview",
    components: {CardSmallList},
    data() {
      return {
        cardSmallList: [
          {
            icon: 'icon-facebook',
            pageViews: '87',
            growth: 3,
            key: 1,
          },
          {
            icon: 'icon-twitter',
            pageViews: '52',
            growth: 2257,
            key: 2,
          },
          {
            icon: 'icon-instagram',
            pageViews: '5462',
            growth: 1375,
            key: 3,
          },
          {
            icon: 'icon-youtube',
            pageViews: '117',
            growth: 303,
            key: 4,
          },

        ]
      }
    }
  }
</script>

<style scoped>

</style>
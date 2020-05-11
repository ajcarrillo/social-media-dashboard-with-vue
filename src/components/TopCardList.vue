<template>
  <section class="top-cards">
    <div class="wrapper">
      <div class="grid">
        <Card :key="socialNetwork.id"
              :social-network="socialNetwork"
              v-for="socialNetwork in socialNetworks">
        </Card>
      </div>
    </div>
  </section>
</template>

<script>
  import '../assets/css/top-card-list.css'
  import Card from "@/components/Card"

  export default {
    name: "TopCardList",
    components: {Card},
    data() {
      return {
        socialNetworks: [
          {
            username: '@LeonidasEsteban',
            id: 1,
            followers: '1596',
            todayFollowers: 12,
            icon: 'icon-facebook',
            name: 'facebook',
          },
          {
            username: '@LeonidasEsteban',
            id: 2,
            followers: '28k',
            todayFollowers: 20,
            icon: 'icon-twitter',
            name: 'twitter',

          },
          {
            username: '@LeonidasEsteban',
            id: 3,
            followers: '6k',
            todayFollowers: 30,
            icon: 'icon-instagram',
            name: 'instagram',


          },
          {
            username: '@LeonidasEsteban',
            id: 4,
            followers: '12k',
            todayFollowers: -50,
            icon: 'icon-youtube',
            name: 'youtube',

          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
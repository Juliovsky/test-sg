<template>
<div class="container">
  <ul class="casino-games-list">
     <CasinoGame :casinoGames="casinoGames"/>
  </ul>
</div>
</template>

<script>

import CasinoGame from './CasinoGame.vue'
import casinoGamesData from '../../casino_games.json'

export default {
  components: {
    CasinoGame
  },
  data () {
    return {
      casinoGames: casinoGamesData
    }
  }
}
</script>

<style scoped>
.casino-games-list {
  background-color: white;
  border: 1px solid #D1D1D1;
  border-radius: 12px;
  margin: 30px auto;
}

</style>

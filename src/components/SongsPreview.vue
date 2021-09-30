<template>
  <div class="Songs-wrapper container">
    <div class="row g-2">
      <div v-for="(song, index) in songsList" :key="index" class="col-2 mx-auto">
        <Song :songItem="song"/>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Song from './SongCard.vue'

export default {
  name: 'SongsPreview',
  props: {
  },
  components:{
    Song,
  },
  data(){
    return {
      songsList: []
    }
  },
  mounted(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((response) => {
      this.songsList = response.data.response.slice();
      console.log(this.songsList)
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

</style>

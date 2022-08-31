<template>
  <div id="app">
    <playing-song></playing-song>
    <h2 @click="play_this_song">
      <div v-for="song in current_song" :key="song[`song_id`]">
        <p>{{song}}</p>
        <img src = "song.image_url">
      </div>

    </h2>
  </div>
</template>

<script>
import playingSong from '@/components/playingSong.vue';

export default {
  data() {
    return {
      current_song: [{
        title: '',
        artist: '',
        song_id: '',
        image_url: ''
    }]
    }
  },
  methods: {
    play_this_song(i) {
      console.log(i)
      console.log(`check here`)
      this.current_song = i
    }
  },
  components: {
    playingSong
  
  },
  name: 'app'
};

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

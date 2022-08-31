<template>
  <div id="app">
    <playing-song
    v-for="(song, index) in current_song" :key="index" @play_this_song="play_current_song" :song="song"
    >
     <p>{{song.artist}}</p>
        <img src = "song.image_url">
    </playing-song>
    
      

    
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
    play_current_song(i) {
     console.log(i)
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

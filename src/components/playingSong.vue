<template>
    <div>
        <h1>Choice of songs:</h1>
        
        <section v-for="(song, index) in songlists" :key="index">
            <article  @click="clicked_song(index)">
            
            <h1>Title: {{song.title}}</h1>
            
            </article>
         
        </section>
        
    </div>
</template>

<script>
    export default {
        methods: {
            clicked_song(index) {
                
                this.$emit('play_this_song', this.songlists[index])
                
            }
        },
        data() {
            return {
                songlists: [{
                    title: 'Bar Bar Bar',
                    artist: 'Crayon Pop',
                    song_id: 5576117192,
                    image_url: 'https://kpopping.com/documents/7c/5/Crayon-Pop-Bar-Bar-Bar-Concept-Teasers-3-Versions-documents-25.jpeg?v=b8fd6'
                },
                {
                    title: "I Can't Stop Me ",
                    artist: 'TWICE',
                    song_id: 5882688897,
                    image_url: 'http://images6.fanpop.com/image/photos/43600000/I-Can-t-Stop-Me-twice-jyp-ent-43612482-1500-1000.jpg'
                },
                {
                    title: 'Lion Heart',
                    artist: 'SNSD',
                    song_id: 4186615445,
                    image_url: 'https://seoulbeats.com/wp-content/uploads/2015/08/20150825_seoulbeats_snsd_girlsgeneration5-e1440413361127.jpg'
                },
                {
                    title: "As If It's Your Last",
                    artist: 'BLACKPINK',
                    song_id: 2235591632,
                    image_url: 'https://c-fa.cdn.smule.com/rs-s77/arr/5b/9d/cc4bed5a-55e9-46d6-965f-dcec4506b7ae_1024.jpg'
                },
                {
                    title: 'Never Gonna Give You Up',
                    artist: 'Rick Astley',
                    song_id: 6061798175,
                    image_url: 'https://i.ytimg.com/vi/dQw4w9WgXcQ/maxresdefault.jpg'
                }]
            }
        },
        name: 'playing-song'
        
    }
</script>

<style scoped>

</style>
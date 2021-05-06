<template>
  <v-content>
    <Hero></Hero>
    <Gallery></Gallery>
    <LatestPost></LatestPost>
  </v-content>
</template>

<script>
import Hero from '@/components/Hero.vue';
import LatestPost from '@/components/LatestPost.vue';
import Gallery from '@/components/Gallery';
  export default {
    name: 'Home',
    
    components: { Hero, LatestPost, Gallery },
  data() {
     return {
       items: [   
      ]
    };
  }
};
</script>

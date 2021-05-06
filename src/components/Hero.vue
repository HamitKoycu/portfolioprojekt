<template>
   <div class="heroBlock">
     <v-carousel hide-delimiters cycle>
        <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
        >
         <v-row
            class="fill-height title hidden-xs-only"
            align="center"
            justify="center"
          >
            <div>{{item.title}}</div>
          </v-row>
        </v-carousel-item>
  </v-carousel>
   </div>
</template>

<script>
  export default {
    name: 'Hero',

   data () {
      return {
        items: [
          {
            src: require("../assets/images/img.baggrund.jpg"),
          },
          {
            src: require("../assets/images/img.baggrund1.png"),         
          },
        ],
      }
    },
  }
</script>
